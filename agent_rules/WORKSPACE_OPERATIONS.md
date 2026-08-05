# Workspace operations

## Authority and activation

This file is a conditionally mandatory extension of the repository root
`AGENTS.md`. Read it before work involving one or more of:

- environment, interpreter, toolchain, dependency, or hardware-target work;
- Git, hosting-platform, mirror, release, or publication work;
- remote-shell commands or user-operated multi-stage procedures;
- long-running, expensive, resumable, or monitored processes;
- task continuation, handoff, persistent state, or recovery;
- packaging or deployment; or
- another external state-changing operation.

Do not load this file merely because it exists. `AGENTS.md` owns global
behavior, authorization, proportionality, and non-bypassable invariants.
`DECISION_DISCIPLINE.md` owns whether a material experiment, architecture, or
optimization is justified and what claim it supports. This file owns how an
authorized operation is executed, persisted, recovered, and published.

Re-evaluate routing when the requested stage, environment, authorization
scope, process state, or external-write scope materially changes.

## Project operations overlay

This generic file declares which project-specific values may be required. It
does not know an adopter's actual repository, environment, shell, state path,
polling policy, package command, or publication authority.

When adopted Operations procedures require project-specific values, declare
them in `PROJECT_OPERATIONS.md` at the repository root. Start from
`templates/PROJECT_OPERATIONS_OVERLAY.md`, copy it to that standard path,
remove inapplicable sections, and replace every placeholder that remains.

A project that deliberately uses another path must identify that exact path in
its root policy. If a required operations overlay is absent, identify the
contract gap and restrict the operation or claim. The template is never active
policy.

Declare when applicable:

- canonical local interpreter or toolchain;
- approved remote, evaluator, build, deployment, and publication environments;
- dependency roots and installation policy;
- environment identity required for evidence-bearing runs;
- source-of-truth and mirror roles and scopes;
- allowed remote transport and publication authority;
- active task-state and archive locations;
- polling and single-writer policy;
- local and remote shells and required wrappers; and
- packaging, validation, deployment, and publication procedures.

Do not invent missing values. If an operation requires an undeclared value,
identify the contract gap and restrict the operation or claim. Do not keep
fictional placeholders in an active project policy.

## User-operated and shell procedures

- Provide commands in syntax directly pasteable into the named target shell.
  Do not mix incompatible shells in one command block.

- By default, give one bounded operational stage at a time and wait for its
  result before giving dependent later stages. When the user explicitly asks
  for a complete tutorial or script, provide all stages together with
  dependencies, expected outputs, and stop points.

- Before asking the user to perform a material action, follow the core
  requirement to explain why it is needed, what it changes, expected cost or
  duration, successful output, and stop, rollback, or failure condition.

- When the agent has access and authorization, perform avoidable mechanical
  work directly instead of transferring it to the user.

- Keep destructive commands scoped to exact, inspected targets. Do not use an
  unresolved variable, broad root, home directory, or ambiguous wildcard as a
  destructive target.

## Official and reference artifacts

- Treat official specifications and applicable evaluators as authorities
  within their declared scope. Preserve the original identity of baseline or
  reference artifacts when the applicable contract requires it.

- A template explicitly intended to be completed or modified may be edited
  according to its stated contract. Otherwise, create a labeled derived copy
  and preserve the authoritative original.

- Do not modify an authoritative external artifact in place. When
  transformation is necessary, create a labeled derived copy outside the
  official path and preserve the original bytes.

- Record or verify identity when an artifact participates in durable evidence,
  packaging, publication, or another content-binding claim.

## Execution environments and dependencies

- Use the environment declared by the applicable project overlay and task
  protocol. Do not silently substitute another interpreter, toolchain,
  dependency root, package set, hardware target, or material environment
  variable.

- Before a substantial or evidence-bearing run, record actual identity from
  the environment that will execute the task. Do not infer it from a directory
  name, another host, or historical documentation.

- Evidence is valid only for the environment and claim scope it records. Do
  not generalize it to another environment without an explicit equivalence
  argument or confirming run.

- Missing environment identity restricts environment-dependent claims; it does
  not automatically invalidate unrelated observations. If exact identity is
  an acceptance condition, the evidence cannot satisfy it until established.

- If an import or tool is missing, inspect the declared environment and
  overlay before changing anything. Do not switch runtimes, install packages,
  or add dependency roots without current-task authorization for that exact
  environment change.

- An undeclared or unauthorized environment substitution is invalid for the
  protocol it violates.

## Git, external writes, and mirrors

The authorization rules in `AGENTS.md` apply to every Git, hosting-platform,
release, publication, synchronization, outbound message sent through a
connected external service, and other external write.

- Local edits do not authorize commit, push, change-request creation, merge,
  release, publication, or synchronization. When no authorization exists,
  leave changes uncommitted and unpushed and report the exact pending action.

- Read repository and mirror roles from the active project overlay. Do not
  infer them from branch names, directory names, or commit history alone.

- A declared mirror must be content-equivalent within its stated scope before
  it is represented as synchronized, used as an authoritative review artifact,
  or published. Intermediate edits do not require immediate synchronization.

- After squash, rebase, or mechanical mirroring, compare tree or relevant
  content identity rather than requiring equal commit hashes. Do not
  manufacture matching history solely to create hash equality.

- Scratch files, active task state, caches, temporary dependencies, non-public
  overlays or project-specific values, credentials, and large raw evidence
  must not enter a mirror, package, or publication unless their inclusion is
  required, reviewed, and authorized.

- Use only the remote transport and credential procedure declared by the
  active overlay. A failed authentication probe in one environment does not by
  itself establish that credentials are invalid elsewhere.

## Active task continuation state

Create persistent task state when one or more of these applies:

- work may survive context compaction, conversation resumption, or handoff;
- it starts, resumes, or monitors a long-running process;
- it produces expensive or decision-bearing work that should not be repeated
  casually;
- it coordinates material work across agents, machines, repositories, shells,
  or environments; or
- exact authorization, process, artifact, or next-action state must persist.

Tool-call count and conditional-rule routing alone are not triggers. Do not
create empty placeholder memo, state, or evidence files.

Use the task-state root declared by the project overlay. Keep the human memo
compact and record when applicable:

- objective, scope, repository or branch, and prohibitions;
- authorization scope;
- active specialized rule sets;
- environment and validation policy;
- completed material work and results already reported;
- invalid or stale evidence;
- exact next action and remaining bounded work; and
- whether external writes, process control, dependency changes, or expensive
  runs are authorized.

Keep exact hashes, artifact identities, process status, polling interval, and
other machine fields in a sibling machine-readable state file only when they
need persistence. A flat evidence index is appropriate only when a real
cross-artifact index exists; original artifacts remain the evidence body.

Update task state after each material milestone and before a likely
long-running operation. After resume, continue from the recorded next action.
Do not repeat completed work unless a relevant source, environment, protocol,
artifact, or semantic change invalidated it.

On completion, archive task chronology according to the project overlay.
Distill only durable state and reusable lessons into their owning Project
Memory documents.

## Long-running process lifecycle

- A project-controlled long job should emit bounded progress: completed and
  total work, elapsed time, and an ETA or meaningful phase.

- For an official, external, or unmodifiable process without a reliable
  progress interface, record process identity, output root, phase, start time,
  last observable state, and completion or failure condition. Do not modify an
  authoritative external tool solely to add progress.

- Before starting or resuming expensive work, inspect recorded process, state,
  checkpoint, and output records. Do not launch a duplicate merely because
  output is quiet or the current conversation lacks context.

- Allow at most one active writer per output root or artifact set unless the
  workflow explicitly supports concurrent writers. Record process identity
  immediately after a successful launch.

- Use the polling cadence declared by the active overlay or task protocol. Do
  not poll more frequently without completion, failure, a changed operational
  need, or an explicit request.

- Quiet or buffered output does not justify restart, duplication, overwrite,
  or invalidation. After interruption, resume observing the recorded process
  instead of launching another copy.

## Packaging, deployment, and publication

- Read packaging, validation, deployment, and publication commands and
  authority from the project overlay. Do not invent a package layout or
  destination.

- Validate the artifact that will actually be distributed, not only its source
  directory. Record content identity when the release or evidence contract
  requires it.

- A source repository publication normally includes tracked project content,
  not the local VCS control directory as an ordinary file. A manually shared
  working-directory archive is different: exclude VCS metadata, credentials,
  non-public overlays or project-specific values, task state, caches, editor
  files, export audits, and unrelated generated artifacts unless explicitly
  intended.

- Generated, packaged, staged, uploaded, published, released, and deployed are
  distinct milestones. Report only the one established by current evidence.

- Before publication, resolve local links, identify remaining placeholders,
  scan for private values, confirm license and attribution, and verify that no
  public document claims unpublished evidence.

- Publication hygiene is not authorization. The exact external write still
  requires current-task approval.
