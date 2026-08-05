# Project Memory System

## Purpose

Project Memory gives a new or resumed agent the minimum durable context needed
to act without replaying the entire history. It is not a transcript and not an
evidence database.

The system separates four questions:

1. What is currently true about the project?
2. Where did the active task stop?
3. Which reusable lesson should prevent a repeated mistake?
4. Where is the original evidence?

Each question has a different owner.

## Document roles

| Document or artifact | Responsibility |
|---|---|
| `AGENTS.md` | Always-read behavior, routing, authorization, and global invariants |
| `agent_rules/DECISION_DISCIPLINE.md` | Conditional research, architecture, evidence, and performance decision policy |
| `agent_rules/WORKSPACE_OPERATIONS.md` | Conditional generic execution, persistence, external-write, and recovery policy |
| Active operations overlay, when required | Exact mutable operational values for the adopted project |
| `PROJECT_MEMORY.md` | Short entry point and proportional reading routes |
| `project_memory/CURRENT_STATE.md` | Latest reviewed durable project state |
| `project_memory/CORRECTIONS_AND_EFFECTIVE_METHODS.md` | Distilled reusable lessons |
| Active task memo | Human-readable task coordination and exact next action |
| Task state file | Machine-readable process, artifact, polling, and authorization state |
| Original artifacts | Evidence body |
| State and task archives | Historical reconstruction when needed |

No document should maintain a second copy of another owner's policy or state.
Project Memory manages durable state and navigation; it does not own agent
policy.

## Lifecycle

```text
work begins
  -> create task checkpoint only if persistence is needed
  -> perform bounded work and update material coordination state
  -> complete and validate the task
  -> archive task chronology
  -> replace current project state if durable facts changed
  -> archive the superseded milestone state when appropriate
  -> distill a reusable correction only if a new lesson was established
  -> leave original evidence in place
```

## Current state: replace, do not append

`CURRENT_STATE.md` should orient a new agent quickly. It may include:

- an at-a-glance status;
- repository and environment roles;
- current supported routes or services;
- evidence and artifact locators;
- explicit claim limits;
- current decisions; and
- whether a required next action exists.

When a completed milestone changes durable facts, preserve the previous state
in a dated, labeled archive and replace stale statements in the active file.
Do not keep contradictory timelines in the current-state document.

Formatting, wording, or locator maintenance that does not change durable facts
does not require another milestone snapshot.

## Task checkpoint: coordination authority

Create a task checkpoint when at least one of these applies:

- the task may survive context compaction, resume, or handoff;
- it starts or monitors a long-running process;
- it produced expensive or decision-bearing work that must not be repeated
  casually;
- it coordinates material work across agents, systems, repositories, or
  environments; or
- exact authorization, process, artifact, or next-action state must persist.

Do not create one merely because several tools were called.

The task memo is authoritative for the coordination state it records. It is
not evidence that an implementation is correct or a hypothesis is supported.
Machine fields belong in a sibling state file rather than prose.

After resume, continue from the exact next action. Repeat completed work only
when a relevant source, environment, protocol, artifact, or semantic change
invalidates it.

## Correction log: distill, do not chronicle

A correction entry should explain a recurring failure class, the corrected
reasoning, its scope, and the effective method. It should not preserve every
command or event.

Update an existing entry before adding a new one. If a lesson becomes agent
policy, keep the rationale and point to its authoritative core, Decision,
Operations, or project-overlay owner instead of maintaining a competing copy.

Detailed incidents belong in archived task chronology, source history, or the
original artifact set.

## Evidence remains external to memory

Memory may record a concise locator, identity, and claim scope for an original
artifact. It must not:

- copy per-item results into a summary and call the summary evidence;
- treat a task memo or generated report as the evidence body;
- change the meaning of a historical result after source semantics change; or
- trigger a rerun merely because a memory locator is unavailable.

When an artifact is missing, inspect compatible retained artifacts and restrict
the claim. Repeat work only when the missing evidence is necessary for the
current decision and cannot be recovered.

## Reading routes

The root `AGENTS.md` and any specialized rules it activates apply before these
durable-state routes. Memory does not decide whether Decision or Operations is
required.

### New material task

1. Read current state.
2. Read corrections relevant to the task boundary.
3. Read the applicable source, contracts, and original evidence.

### Resumed task

1. Read durable current state.
2. Read the active memo and state file.
3. Read only the original evidence needed for the next action or claim.

### Historical reconstruction

Read milestone state archives, completed task archives, source history, and
original artifacts only as needed. Do not load all history for a trivial task.

## Common anti-patterns

- A handoff file duplicates current state and becomes stale.
- Current state grows as an append-only diary.
- A correction log becomes a list of dated incidents.
- An empty task framework is created for a trivial edit.
- A summary is cited instead of the original result.
- A missing locator causes an automatic expensive rerun.
- Two documents define competing reading orders.

The templates in this repository demonstrate the intended separation without
containing live project state.
