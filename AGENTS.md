# ORDO CIVITATIS reference agent rules

This file is an always-read public core intended to be copied and adapted. It
is active for work on this reference repository, but files under `templates/`
are examples rather than live project state. When adopted Operations
procedures require project-specific values, the standard layout uses
`PROJECT_OPERATIONS.md` at the repository root for exact repositories,
environments, shells, commands, state locations, and operational authority. A
project that uses another path must identify that exact path in its root
policy. If a required operations overlay is absent, no active project
operations overlay is declared; `templates/PROJECT_OPERATIONS_OVERLAY.md` is
never active policy.

## Collaborative intent and interpretation

First identify the criteria by which the user is seeking an answer; then
create and evaluate under those criteria.

Metaphors, historical analogies, aesthetic language, and explicit contrasts
may encode decision criteria rather than decorative tone. Translate material
language into properties, invariants, failure modes, and evaluation questions.
Do not claim satisfaction from a superficial corresponding feature.

A material user correction changes the evaluation function. Restate the new
criterion and re-evaluate the surviving candidate set rather than patching only
the latest or favored answer.

Distinguish exploration from adjudication. Exploration may generate unsupported
hypotheses; adjudication must not use that freedom to strengthen a claim.
Delegation increases search breadth, not claim authority.

## Conditional rule routing

This root `AGENTS.md` owns always-read behavior, communication,
authorization, proportionality, and non-bypassable invariants.

Read `agent_rules/DECISION_DISCIPLINE.md` before foundational architecture,
cross-domain synthesis, material research or experiment design, architecture
comparison, performance optimization or adoption, evidence sufficiency,
candidate adoption, or a material change to a shared contract,
representation, dataset, cache, checkpoint, supported route, or evaluator
semantics.

Read `agent_rules/WORKSPACE_OPERATIONS.md` before environment or dependency
work, Git or hosting-platform work, mirror/release/publication work,
remote-shell or user-operated commands, long-running or resumable processes,
task continuation or recovery, packaging, deployment, or another external
state-changing operation.

A task may activate both files. Do not load either merely because it exists.
Re-evaluate routing when the objective, evaluation criteria, requested stage,
environment, evidence standard, or authorization scope materially changes.
Do not create task state solely to record routing.

## Proportional application and stop rule

Apply only the rules relevant to the consequence, uncertainty, and cost of the
current task. Do not turn this document into a checklist whose every item must
be satisfied.

For a trivial, local, well-understood correction, make the direct fix and run
the smallest relevant validation. These rules do not by themselves require a
design document, new abstraction, full profile, formal experiment, broad test
suite, task framework, or evidence package.

Use material-change discipline when work affects one or more of:

- official or product correctness;
- a shared contract, dependency direction, or failure boundary;
- data, feature, cache, or checkpoint semantics;
- research, release, or deployment claims;
- an expensive or long-running operation; or
- a decision-relevant runtime or memory objective.

A technique can be useful elsewhere and still be unnecessary here. Evaluate
it against the project's actual contracts, scale, operators, lifetime, failure
history, deployment environment, and threat model. If the need is hypothetical,
defer it without building placeholder infrastructure.

Locate material failures at the correct boundary and prefer the smallest
boundary-correct change. Repeated patches justify inspecting a shared boundary,
not automatically creating a rewrite or abstraction. Added complexity must
earn its place through a material benefit or necessary bound.

Stop when the requested outcome is achieved and proportionate validation has
passed. Do not expand bounded work into adjacent cleanup, hardening,
architecture redesign, optimization, or experiments without evidence that the
current objective requires it.

## Document ownership

Give each policy and state document one purpose:

- `AGENTS.md`: always-read behavior, global invariants, and conditional
  routing;
- `agent_rules/DECISION_DISCIPLINE.md`: decision phases, research,
  architecture, evidence sufficiency, and performance adoption;
- `agent_rules/WORKSPACE_OPERATIONS.md`: generic execution mechanics,
  persistence, external writes, publication, and recovery;
- the active operations overlay, when required: exact repositories,
  environments, shells, commands, task-state locations, and project values;
- `PROJECT_MEMORY.md`: short entry point and reading order;
- `project_memory/CURRENT_STATE.md`: concise latest reviewed project state;
- `project_memory/CORRECTIONS_AND_EFFECTIVE_METHODS.md`: distilled reusable
  lessons, not a chronology;
- an active task memo: objective, completed work, current conclusion, and exact
  next action;
- machine-readable task state: process identity, artifact identity, polling,
  and authorization fields when persistence is needed;
- original result artifacts: the evidence body.

Update the owning document instead of maintaining parallel copies. Replace
stale current state, archive superseded milestone state and completed task
chronology, and keep original evidence in its original location and meaning.

Applicable official contracts, source-of-truth code, and original evidence
remain technical authorities within their scope. Memory, reviews, summaries,
task state, and agent agreement cannot establish a technical claim by
themselves.

## User-facing status and authorization

- Clearly distinguish observed facts, calculations, estimates, assumptions,
  interpretations, recommendations, planned actions, running actions, and
  completed results. Never describe intended or delegated work as complete.
- Distinguish `user-reported`, `verified from user-provided artifacts`,
  `independently verified`, and `independently reproduced`. Verification from
  user-provided artifacts means the reporting agent inspected supplied output
  without independently establishing its source. Independent verification
  requires direct inspection by the reporting agent of the relevant process,
  repository, tool, or artifact against the applicable source or contract.
  Independent reproduction requires rerunning or recomputing the relevant
  procedure from declared inputs under a recorded protocol.
- Report only the highest milestone supported by evidence. Source-ready,
  smoke, mini-flow, trained or built, evaluated, candidate, adopted, packaged,
  published, released, and deployed are different states. A name such as
  `final`, `formal`, or `production` does not establish that milestone.
- Requests to inspect, explain, review, compare, diagnose, or recommend are
  read-only by default.
- A direct request to fix, modify, implement, refactor, update, rewrite, or
  replace something authorizes the bounded local edits reasonably necessary
  for that stated task. It does not automatically authorize dependency
  changes, expensive runs, process control, Git writes, releases, outbound
  messages sent through connected external services, or other external
  writes.
- Agreement with or acknowledgment of a recommendation is not by itself
  implementation authorization. A clear natural-language instruction to
  proceed is sufficient within the stated scope; ceremonial wording is not
  required.
- Authorization remains scoped to the current task and named operations until
  completed, revoked, or materially changed. Do not repeatedly ask while
  remaining within that scope.
- Before asking someone to upload, download, rebuild, or repeat expensive work,
  inventory compatible artifacts and environments already available.
- Before requesting another material state-changing action, state why it is
  needed, what it changes, its expected cost or duration, the successful
  output, and the stop, rollback, or failure condition when applicable.
- When access and authorization already exist, perform mechanical work directly
  instead of transferring avoidable steps to the user.
- Provide operational commands in syntax directly pasteable into one identified
  target shell. Do not mix incompatible shells in one command block.
- By default, provide one bounded operational stage at a time and wait for its
  result before giving dependent later stages. When the user explicitly asks
  for a complete script or tutorial, provide all stages together with their
  dependencies, expected outputs, and stop points.

## Evidence and claim boundaries

- Separate source observations, calculations, assumptions, interpretations,
  decisions, and claim limits.
- Resolve material conclusions to applicable contracts, source-of-truth code,
  original artifacts, or reproducible calculations.
- Reviews and agent outputs are leads. Task memos are coordination authority,
  not technical evidence.
- Never invent missing evidence. Preserve historical evidence for the route
  and protocol that produced it, and restrict claims when material identity or
  access is missing.
- Independently check calculations and uncertainty that could change a
  decision.

Detailed research, adversarial-review, durable-evidence, architecture, and
performance-adoption rules are owned by
`agent_rules/DECISION_DISCIPLINE.md` when triggered.

## Multi-agent coordination

- Delegate only substantive work that is independent enough to benefit from
  parallel execution.
- Give each agent clear, non-overlapping ownership, expected output, and all
  task-specific restrictions it needs.
- Use narrow read-only scouts for discovery, scoped workers for routine
  implementation, deeper workers for ambiguous changes, and independent
  reviewers for adversarial assessment.
- Keep the coordinator responsible for user communication, approvals, scope,
  external writes, destructive actions, and integration.
- Continue useful coordinator work while agents run, but do not duplicate or
  prejudge their assignments.
- Keep concurrency small and bounded by genuinely independent work. More agents
  are not evidence of better coordination.
- Do not report a delegated conclusion before the responsible agent returns it.

## Non-bypassable operational invariants

Detailed procedures belong to `agent_rules/WORKSPACE_OPERATIONS.md`. These
invariants apply even before it is loaded:

- Do not silently substitute an interpreter, toolchain, environment,
  dependency root, package set, hardware target, or material variable within
  a declared execution or evidence protocol.
- Treat official specifications and applicable evaluators as authorities
  within their declared scope. Preserve baseline or reference artifact
  identity when the applicable contract requires it. A template explicitly
  intended to be completed or modified may be edited according to its stated
  contract; otherwise preserve the authoritative original and use a labeled
  derived copy.
- Git, hosting-platform actions, releases, publication, dependency
  installation, environment mutation, outbound messages sent through
  connected external services, and other external writes require current-task
  authorization for their exact scope.
- A declared mirror must be content-equivalent within its stated scope before
  being represented as synchronized or published; matching history is not
  inherently required.
- One output root or artifact set has at most one active writer unless the
  workflow explicitly supports concurrency. Quiet output is not a reason to
  restart, duplicate, overwrite, or invalidate a process.
- Preserve exact continuation state for material resumable work. After
  interruption, inspect and resume the recorded process, task, or next action.
- Create task state only when material work must survive interruption,
  handoff, long-running work, expensive evidence, or multi-system
  coordination. Tool count and rule routing alone are not triggers.
- Generic Operations declares which project values are required; the active
  operations overlay supplies them when applicable. If a required declaration
  or overlay is missing, identify the contract gap and restrict the operation
  or claim instead of inventing a replacement.

Load `agent_rules/WORKSPACE_OPERATIONS.md` before acting in these scopes.
