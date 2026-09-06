# ORDO CIVITATIS

[![Latest release](https://img.shields.io/github/v/release/Kaz9487/ordo-civitatis?label=release&color=blue)](https://github.com/Kaz9487/ordo-civitatis/releases/latest)
[![License: MIT](https://img.shields.io/github/license/Kaz9487/ordo-civitatis?color=blue)](LICENSE)

## Coding Agent Engineering Reference

Framework revision: **0.2.0**. See the [changelog](CHANGELOG.md) for release
status, versioning conventions, and adoption notes.

ORDO CIVITATIS is a practical reference for teams that use coding agents in
software projects. It helps teams define what agents may change, what evidence
supports a claim, how much process a task needs, how interrupted work can be
resumed, and when the agent should stop. Its goal is to avoid both careless
shortcuts and unnecessary complexity.

## Why this project exists

Coding agents can fail even when they have the right tools and enough technical
ability. For example, an agent may:

- treat a recommendation as permission to make a change;
- treat a task summary as evidence that a result is correct;
- report a local build as released or deployed;
- restart expensive work without checking whether it is still running;
- optimize a component that has little effect on the full workflow;
- turn a small correction into a framework for hypothetical future needs.

ORDO CIVITATIS addresses these problems through project-level rules. One idea
guides the framework: the amount of process should match the impact of the
task. A small, well-understood correction should remain small. Work that can
affect correctness, shared interfaces, important evidence, deployment,
expensive operations, or measured performance needs more careful design and
validation.

## How the rules are organized

The framework separates rules that apply to every task from rules needed only
for specialized work.

| Layer | File | Purpose |
|---|---|---|
| Core rules | [`AGENTS.md`](AGENTS.md) | Collaboration, authorization, status reporting, proportionality, and stop rules |
| Decision rules | [`agent_rules/DECISION_DISCIPLINE.md`](agent_rules/DECISION_DISCIPLINE.md) | Research, architecture, evidence-based decisions, and performance changes |
| Operations rules | [`agent_rules/WORKSPACE_OPERATIONS.md`](agent_rules/WORKSPACE_OPERATIONS.md) | Environments, Git and other external changes, long-running work, recovery, packaging, and publication |
| Project settings | `PROJECT_OPERATIONS.md` or a declared operations-overlay path, when required | The actual repositories, environments, commands, paths, and authority for one project |

For agents that support this layout, the root `AGENTS.md` is the always-read
policy. It tells the agent when a task also requires the Decision or Operations
rules. The agent decides which additional rule files apply to the current task.
ORDO CIVITATIS does not include an automatic policy loader.

The generic Operations rules identify which project settings must be declared
when the relevant procedures apply. The standard location is
`PROJECT_OPERATIONS.md` at the project root. A project that uses another
location must declare that exact path in its root policy. This keeps changing
paths, commands, environments, and organizational procedures out of the
reusable rules.

## Optional Project Memory

Long-running or expensive work sometimes needs to survive a summarized
conversation, a handoff, or an interrupted session. The optional Project
Memory templates help agents record:

- the latest reviewed project state;
- where an active task stopped;
- the exact next action;
- lessons that should prevent repeated mistakes;
- where the original evidence can be found.

These records help agents resume work safely. They do not prove that source
code is correct, an experiment is reproducible, or a result supports a claim.
Those conclusions must still be checked against source code, project
specifications, calculations, or original result artifacts.

See [`docs/MEMORY_SYSTEM.md`](docs/MEMORY_SYSTEM.md) for the full design.

## Repository map

```text
.
├─ .gitattributes
├─ .gitignore
├─ .github/
│  └─ pull_request_template.md
├─ README.md
├─ CHANGELOG.md
├─ LICENSE
├─ AGENTS.md
├─ agent_rules/
│  ├─ DECISION_DISCIPLINE.md
│  └─ WORKSPACE_OPERATIONS.md
├─ docs/
│  ├─ RATIONALE.md
│  ├─ ADAPTATION.md
│  └─ MEMORY_SYSTEM.md
└─ templates/
   ├─ PROJECT_OPERATIONS_OVERLAY.md
   ├─ PROJECT_MEMORY.md
   ├─ HANDOFF.md
   ├─ task-memo.md
   ├─ task-state.example.json
   └─ project_memory/
      ├─ README.md
      ├─ CURRENT_STATE.md
      └─ CORRECTIONS_AND_EFFECTIVE_METHODS.md
```

- [`docs/RATIONALE.md`](docs/RATIONALE.md) explains why the main boundaries
  exist.
- [`docs/ADAPTATION.md`](docs/ADAPTATION.md) explains how to choose, adapt, and
  test the rules for a real project.
- [`docs/MEMORY_SYSTEM.md`](docs/MEMORY_SYSTEM.md) explains how project state,
  task checkpoints, reusable lessons, archives, and original evidence differ.
- [`templates/`](templates/) contains examples and placeholders. These files
  are not active project policy or real project state.

## Adoption options

Start with [`docs/ADAPTATION.md`](docs/ADAPTATION.md). Keep only the rules that
address real risks in your project.

### Core-only adoption

This is usually enough for a small project that needs clear rules for
collaboration, authorization, evidence, and stopping work at the right point.

1. Copy [`AGENTS.md`](AGENTS.md).
2. Remove or rewrite references to specialized files you are not adopting.
3. Remove rules that do not correspond to a real risk in your project.

### Partial layered adoption

Projects may combine the core with one specialized rule file when only one
category applies. Update the root routing to reference only the files actually
adopted, and supply any project-specific declarations required by those rules.

### Full layered adoption

Use the full structure when a project involves research, performance work,
multiple environments, deployment, expensive processes, or tasks that must be
resumed later.

1. Copy [`AGENTS.md`](AGENTS.md).
2. Copy both files under [`agent_rules/`](agent_rules/).
3. Copy
   [`templates/PROJECT_OPERATIONS_OVERLAY.md`](templates/PROJECT_OPERATIONS_OVERLAY.md)
   to `PROJECT_OPERATIONS.md` at the root of the adopting project.
4. Replace every applicable placeholder with the project's actual settings.
5. Remove sections and rules that do not apply.
6. Add the Project Memory templates only when work must survive a summarized
   conversation or handoff, track a long-running process, or preserve expensive
   or decision-bearing state that should not be repeated casually.

In the standard full layered layout, the operations template becomes active
only after it has been completed and copied to `PROJECT_OPERATIONS.md` at the
project root. A project that uses another location must declare that exact path
in its root policy. The template under `templates/` is never active policy.

## Test the adopted rules

Choose realistic test cases that match the layers you adopted, such as:

- a simple explanation or local correction;
- an architecture or research decision;
- an environment, Git, packaging, or publication task;
- a performance change that requires a real run;
- a task that begins as analysis and later becomes implementation.

Then run one small representative task through the adopted instructions from
start to finish. Confirm that a new agent can:

- find the applicable rules;
- understand what it is authorized to change;
- complete the task without unnecessary process;
- report only the milestone it actually reached;
- when continuation rules are adopted, resume the task without repeating
  completed work.

A written policy and static review do not prove that an operational path
works.

## Core principles

- Use only as much process as the task actually needs, based on its impact,
  uncertainty, and cost.
- Separate observations, assumptions, recommendations, running work, and
  completed results.
- Do not treat permission for local edits as permission to commit, push,
  publish, deploy, or send messages through external services.
- Trace important claims back to source code, project specifications, original
  artifacts, or reproducible calculations.
- Give each correctness rule one clear source of truth.
- Measure the bottleneck that matters before optimizing it.
- Prefer a real mini-flow through affected execution and integration boundaries,
  checking the expected result. Add tests for important uncovered risks and
  applicable required checks.
- Save enough context to resume important work without treating the saved
  summary as technical evidence.
- Stop when the requested result is complete and the necessary validation has
  passed.

## Agent compatibility

This structure assumes that the coding agent reads a root `AGENTS.md` file and
can open the repository files referenced by it. Because the agent decides when
specialized rules apply, test this behavior with realistic tasks on every agent
you intend to support. If an agent does not support `AGENTS.md` or cannot read
repository files, provide the relevant rules through that agent's supported
instruction system.

## Evidence limits

This repository does not include a controlled study comparing agent teams,
rule sets, or project outcomes. Treat ORDO CIVITATIS as an inspectable
engineering framework. Adapt it to real needs, test it on real workflows, and
limit claims to the evidence available in the adopting project.

## Current scope

ORDO CIVITATIS is currently designed as a reference framework for building and
maintaining `AGENTS.md`-based coding-agent governance. It does not currently
provide a runtime, plugin system, policy server, orchestration service, or
other execution tooling.

The project may evolve gradually as concrete needs emerge from real-world
adoption, implementation experience, and user or contributor feedback.
Additional capabilities will not be added solely because they might be useful
in the future.

## License

Licensed under the [MIT License](LICENSE).
