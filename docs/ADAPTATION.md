# Adapting ORDO CIVITATIS

## Four policy layers

The public framework separates rules by authority and activation:

| Layer | Owner | Responsibility |
|---|---|---|
| Always-on core | `AGENTS.md` | interpretation, status, authorization, proportionality, stop rule, and non-bypassable invariants |
| Conditional decisions | `agent_rules/DECISION_DISCIPLINE.md` | exploration, architecture and research adjudication, evidence sufficiency, and performance adoption |
| Conditional operations | `agent_rules/WORKSPACE_OPERATIONS.md` | generic environment, command, process, task-state, Git, packaging, publication, and recovery procedure |
| Project values | `PROJECT_OPERATIONS.md` or another declared overlay path, when required by Operations | exact repositories, environments, shells, commands, paths, cadence, and organizational authority |

Generic Operations says which values must be declared when the relevant
procedures apply. The standard location is `PROJECT_OPERATIONS.md` at the
project root. A project that uses another location must declare that exact path
in its root policy. If a required operations overlay is absent, no active
project operations overlay is declared, and the template must not be treated
as policy. The overlay should specialize rather than copy the generic rules.
If a project must depart from one, record the concrete need, replacement
boundary, validation, and claim limit.

Project Memory is not a fifth policy layer. It manages durable state,
coordination routes, and reusable lessons; it must point to policy owners
rather than duplicate them.

## Adoption levels

### Core-only adoption

Use only `AGENTS.md` when a project needs the always-on collaboration,
authorization, evidence, proportionality, and stop rules but not the
specialized Decision or Operations procedures. Remove routing references to
files that are not adopted.

### Partial layered adoption

Combine the core with Decision when material research, architecture, evidence,
or performance decisions need specialized guidance but operational procedures
do not. Combine the core with Operations when environment, Git, process,
recovery, packaging, deployment, or publication procedures apply but the
specialized Decision rules do not.

In either case, the root routing must reference only the files actually
adopted. Supply any project-specific declarations required by Operations in
root `PROJECT_OPERATIONS.md` or another exact path declared by the root policy.
If a task later triggers the other specialized rule set, adopt and route that
file before continuing the affected work.

### Full layered adoption

Use the core, both specialized rule files, and the applicable project-specific
operations overlay when a project needs both Decision and Operations rules.
Adopt Project Memory separately only when its persistence conditions apply.

## Decide what is material in your project

Before adopting a rule, ask:

1. Which real failure or decision does this rule address?
2. Is the relevant state local, shared, external, expensive, or irreversible?
3. Which authoritative contract or invariant is involved?
4. What is the smallest validation that reaches the actual boundary?
5. What operator or maintenance cost does the rule add?
6. What evidence would show that the rule can be removed or simplified?

Rules whose need is only hypothetical should remain proposals, not mandatory
infrastructure.

## Suggested adaptation sequence

### 1. Establish project authorities

Identify:

- source-of-truth repositories and any mirrors;
- official or product contracts;
- invariant owners and dependency direction;
- original evidence locations;
- external writes and who may authorize them; and
- target environments and deployment boundaries.

Keep changing identities and paths in the project-specific overlay or
current-state record, not in the generic core.

For a full layered adoption, copy
`templates/PROJECT_OPERATIONS_OVERLAY.md` to `PROJECT_OPERATIONS.md` at the
repository root. Replace every applicable placeholder and remove sections that
do not apply. A template full of placeholders is not an active operational
contract. A project that deliberately uses another location must identify the
exact path in its root policy.

### 2. Define material-change triggers

Choose the events that require more than a local fix. Typical triggers include
correctness, shared schema, release behavior, expensive work, environment
changes, and decision-relevant performance objectives. Remove triggers that do
not exist in your project.

### 3. Define status vocabulary

Name the milestones that matter, and state the evidence required for each.
Avoid names that imply completion merely because a directory or script uses a
word such as `final` or `production`.

### 4. Define authorization scope

List operations that change materially different state: local edits,
dependencies, processes, Git history, remote branches, releases, outbound
messages sent through connected external services, or production systems.
Decide which can be covered by one task-scoped approval and which require
separate authority.

### 5. Adopt only the needed memory tiers

A short project may need only an `AGENTS.md`. A long-lived project with handoff
and expensive work may also need current state, task continuation, corrections,
and archived milestone snapshots. Do not create empty tiers in anticipation of
future use.

### 6. Validate an operational mini-flow

First check representative routing scenarios:

- trivial explanation or local fix uses the core only;
- material architecture or experiment work loads Decision;
- environment, Git, process, packaging, or publication work loads Operations;
- a performance change with a real run loads both; and
- a task that changes phase re-evaluates routing.

Then run one real small task through the adopted instructions. Verify that a
new agent can locate authority, understand authorization, complete the
workflow, report the right milestone, and resume without duplicate work.
Static routing review does not establish runtime behavior.

## What belongs in the project-specific overlay

Put exact repositories, paths, hosts, shells, toolchains, environments,
commands, polling policy, deployment procedures, and organizational authority
in the project-specific overlay rather than the generic rules.

The overlay may be public or non-public according to the adopting project's
publication boundary. It may also own project-specific artifact-retention,
evaluation, packaging, deployment, incident, security, and review procedures
when those procedures actually apply.

## What must be excluded from a public extraction unless intentionally public

Exclude internal repository identities, credentials and access details,
proprietary architecture, private datasets or customer information,
unpublished results, internal artifact identities, incident details, and other
non-public operational values.

Do not publish a non-public overlay by replacing names with generic labels.
Create a separate public extraction that preserves only the reusable
semantics.

## Avoid competing authority

- Keep routing in the root `AGENTS.md`; do not restate the full specialized
  files there.
- Keep decision necessity and acceptance in Decision, and execution mechanics
  in Operations. A rule that says both whether and how to run should be split
  at that boundary when practical.
- Keep exact mutable values in the project overlay. Do not copy generic
  procedure into it merely for convenience.
- Let Project Memory point to active policy and record durable state; it must
  not become another policy owner.

When a repository uses nested `AGENTS.md` files, state each file's subtree
scope and follow the agent platform's documented precedence. Use nested files
to add or specialize genuinely local rules. Do not duplicate the root policy
across subtrees, and do not silently weaken root authorization or evidence
boundaries.

## Avoiding over-adaptation

Do not add all of the following by default:

- a plugin architecture;
- a policy service;
- a universal schema registry;
- an evidence database;
- a cryptographic provenance layer;
- a transaction coordinator; or
- a general workflow engine.

Each may be appropriate for a real requirement. None is implied by the generic
framework.

## Synthetic adaptation examples

These examples are fictional and illustrate scope, not preferred technology.

### Small documentation repository

Adopt status clarity, local-versus-external authorization, and the stop rule.
Skip task state and long-running process rules unless work actually becomes
resumable or automated.

### Internal data export service

Add a project-specific overlay for data-retention policy, destination
authorization, schema ownership, and process recovery. Keep generated
summaries separate from the exported records used as evidence.

### Latency-sensitive API

Define end-to-end latency as the primary metric, error rate and memory as
guardrails, and production traffic shape as the workload. Reject component
optimizations whose best possible system contribution is immaterial.

## Publication checklist for an adapted framework

- The generic core and specialized files contain no private identities or
  changing project values.
- Examples are clearly synthetic.
- Templates contain placeholders rather than real state.
- Public claims do not imply evidence that has not been published.
- Any non-public overlay or non-public project-specific values are excluded.
- Root routing reaches each specialized file for its representative scenarios.
- Public source archives are generated from the intended tracked content rather
  than a complete working-directory copy. They exclude VCS metadata,
  non-public overlays, export audits, task-state directories, editor and
  temporary files, and unrelated generated archives.
- Local links resolve and no document competes for the same policy ownership.
