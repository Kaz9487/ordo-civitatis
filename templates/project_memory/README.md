# Project Memory maintenance

Last reviewed: `<last-reviewed>`

## Purpose

This directory owns durable current state, reusable corrections, and milestone
state archives. It is not a transcript, policy duplicate, or evidence database.

- `CURRENT_STATE.md`: latest reviewed durable state.
- `CORRECTIONS_AND_EFFECTIVE_METHODS.md`: distilled reusable lessons.
- `archive/`: superseded milestone state when durable facts materially change.

`AGENTS.md` owns always-read behavior and conditional routing. The specialized
files under `agent_rules/` own conditional Decision and Operations policy.
The active operations overlay, when required, owns exact mutable operational
values.
`PROJECT_MEMORY.md` owns durable-state reading routes. This file owns retention
and maintenance.

## Authority boundaries

Resolve technical claims to the applicable source, official contract, original
artifact, or explicit calculation. Current state is a reviewed handoff.
Corrections are reusable guidance. Task checkpoints are authoritative for
recorded coordination state only.

## State lifecycle

Keep `CURRENT_STATE.md` concise and replace stale facts. Before replacing it
for a completed milestone that materially changes durable project state,
archive the prior version as:

```text
archive/CURRENT_STATE_<date>_<milestone>.md
```

Do not create a milestone snapshot for wording, formatting, or locator-only
maintenance that leaves durable facts unchanged.

## Correction lifecycle

Update an existing correction when it covers the same failure class. Add a new
entry only for a genuinely different reusable lesson. Keep task-specific
chronology in archived task records rather than copying it into this file.

When a correction becomes agent policy, keep only enough rationale to explain
why it exists and point to its authoritative core, Decision, Operations, or
project-overlay owner.

## Task lifecycle

Create task checkpoints only when persistence is needed. On completion:

1. archive the task memo and state;
2. distill changed durable facts into `CURRENT_STATE.md`;
3. update corrections only for a reusable lesson; and
4. leave original evidence in its original location.

## Proportional maintenance

- Verify only the source, state, and artifacts relevant to the current action.
- Do not load all history for a trivial task.
- Do not relabel historical evidence after semantic changes.
- Do not create empty memory tiers in anticipation of future use.
