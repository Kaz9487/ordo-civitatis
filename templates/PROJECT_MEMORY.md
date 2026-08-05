# Project Memory

Last reviewed: `<last-reviewed>`

This is the single entry point for durable project memory. It contains reading
routes, not project status or experiment detail.

In short:

- always-read behavior and specialized-rule routing live in `AGENTS.md`;
- conditional decision and operations policy live in `agent_rules/`;
- exact operational values live in the active operations overlay when required;
- latest reviewed project state lives in
  `project_memory/CURRENT_STATE.md`;
- reusable lessons live in
  `project_memory/CORRECTIONS_AND_EFFECTIVE_METHODS.md`;
- a recorded resumable task lives in its active memo and sibling state file;
- original artifacts remain the evidence body.

If no active memo/state pair exists, there is no recorded resumable material
task. This does not mean that every short current request needs a memo.

## Reading routes

### New material task

1. Follow the conditional routing in `AGENTS.md`.
2. Read `project_memory/CURRENT_STATE.md`.
3. Read correction entries relevant to the task boundary.
4. Read the applicable source, official contracts, and original evidence.

### Resumed task

1. Follow the conditional routing in `AGENTS.md`.
2. Read current project state.
3. Read the active task memo and sibling state file.
4. Consult indexed or original evidence only when the next action or claim
   requires it.

The task checkpoint is authoritative for recorded coordination state. It is not
experiment evidence.

### Memory maintenance or historical reconstruction

- Read `project_memory/README.md` before changing retention rules.
- Consult milestone archives, completed task archives, source history, and
  original artifacts only when historical reconstruction is necessary.

A trivial local task does not require loading unrelated history.

## Retention summary

```text
latest durable project facts  -> project_memory/CURRENT_STATE.md
superseded milestone state    -> project_memory/archive/
active task coordination      -> task-state root declared by the operations overlay
completed task chronology     -> task archive declared by the operations overlay
reusable lessons              -> project_memory/CORRECTIONS_AND_EFFECTIVE_METHODS.md
original evidence             -> original artifact location
source evolution              -> source history
```

The detailed maintenance procedure belongs in `project_memory/README.md`.
