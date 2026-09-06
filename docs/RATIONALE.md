# Rationale

## Why a discipline rather than a tool

Many agent failures are not caused by an incapable model or a missing tool.
They come from unclear boundaries:

- a recommendation is mistaken for authorization;
- a coordination note is mistaken for evidence;
- a local test is mistaken for operational completion;
- a source edit is mistaken for a release;
- a nearby optimization is mistaken for an end-to-end improvement;
- or a hypothetical future concern is allowed to reshape today's system.

ORDO CIVITATIS addresses these failures as engineering-discipline problems. It does
not provide a runtime, scheduler, evidence database, or security service.

## Why the policy is conditionally layered

An always-read policy can become counterproductive when rarely applicable
operational detail and decision procedure compete with the few rules every
task needs. ORDO CIVITATIS therefore separates:

- an always-read core for interpretation, authority, authorization,
  proportionality, and non-bypassable invariants;
- conditional Decision rules for exploration, research, architecture,
  evidence sufficiency, and performance adoption;
- conditional Operations rules for environments, commands, task persistence,
  external writes, processes, packaging, and publication; and
- a project operations overlay when adopted Operations procedures require
  exact project values.

This reduces always-on instruction density without making specialized rules
optional after their trigger occurs. It also keeps mutable repositories,
paths, versions, shells, and procedures out of generic policy.

The split does not create a plugin loader, deterministic router, or persisted
phase machine. Conditional routing remains a model-executed instruction in
ordinary Markdown. It should be checked with representative tasks, including
tasks that change from exploration to implementation or from local work to an
external write.

## Proportionality is the first boundary

A rule that is sensible for a high-consequence release can be wasteful for a
one-line local correction. Applying every control to every task creates its own
failure mode: slow work, excessive ceremony, duplicated policy, and validation
that does not affect a decision.

The framework therefore begins with materiality:

- What can this task change?
- Which claim or invariant could be affected?
- How expensive or irreversible is the action?
- What uncertainty could change the decision?

If the answer is small and local, the response should remain small and local.
If the task crosses a material boundary, the design and evidence should expand
only enough to cover that boundary.

## Authority and coordination are different

Agents need durable coordination records: authorization, process identity,
artifact identity, completed steps, and an exact next action. Those records can
be authoritative for resuming work safely.

They are not automatically evidence that a program is correct, a result is
reproducible, or a hypothesis is supported. Technical claims resolve instead
to the applicable source, official contract, original artifact, or explicit
calculation.

This distinction prevents two common errors:

1. repeating expensive work because a coordination record is ignored; and
2. overstating a result because a summary is treated as the result itself.

## Authorization is an engineering boundary

Local edits, process control, dependency changes, Git writes, releases, and
outbound messages sent through connected external services affect different
state and may involve different people. Treating one as implicit permission
for all the others creates surprise external changes.

At the same time, repeatedly asking for approval inside an already clear scope
creates friction and transfers mechanical work back to the user. The useful
boundary is a named task and operation set whose authorization persists until
completion, revocation, or material change.

## Boundary-correct change

The shortest patch is not always the smallest system change. A local shortcut
can duplicate policy, leak storage details across layers, or move a failure into
another component.

Boundary-correct work asks:

- Who owns the invariant?
- What are the inputs and outputs?
- Which dependency direction is intended?
- What happens on failure?
- Can an existing stable interface express the requirement?

This does not imply that every change needs a new abstraction. A documented
contract or direct local fix may be sufficient.

## Why a real mini-flow comes first

A collection of passing tests can leave the changed operational boundary
untouched. For execution and integration changes, a small real workflow can
connect the input, affected components, and resulting artifact in one check.
Its value comes from exposing a plausible failure and checking the expected
result against the contract, not from being called a mini-flow.

Reducing the workload keeps this check affordable while preserving the parts
that determine the result. Separate property, edge-case, failure, or recovery
tests remain useful where they cover important risks the workflow misses.
Required checks still apply. A small run cannot establish full-scale behavior.
Decision owns these validation choices and claim limits.

## Performance work needs a decision-relevant upper bound

Optimizing a component without bounding its possible effect can produce
impressive local numbers and negligible decision value. Declare the primary
metric and estimate the possible improvement before substantial implementation
or an expensive run. A bounded prototype can first establish an unfamiliar
mechanism or cost structure. Estimates should retain their uncertainty. For an
end-to-end speed claim, use the component's share of end-to-end time to bound
the best possible overall speedup. For a
memory, startup, recovery, reliability, deadline, or deployment objective, use
the corresponding decision-relevant bound instead.

Measurement should also preserve distinct guardrails. Throughput, latency,
quality, correctness, memory, startup cost, and recovery behavior cannot be
substituted for one another.

The framework prefers removing unnecessary work over accelerating it.

## Why durable memory is replace-and-archive

An append-only project summary eventually contains mutually incompatible
states. A chronological task log is useful for resumption but too detailed for
project orientation. A correction log is useful for recurring lessons but
should not become an incident transcript.

ORDO CIVITATIS separates them:

- current state is replaced when the durable picture changes;
- superseded milestone state is archived;
- task chronology is archived after completion;
- reusable lessons are distilled;
- original evidence remains in its original location and meaning.

This supports fast orientation without erasing history.

## Empirical limits

This public framework does not contain a controlled study comparing agent
teams, policy sets, or project outcomes. It should therefore be evaluated as a
set of inspectable engineering hypotheses and templates. Adopters should remove
irrelevant rules, test the remaining ones against real workflows, and preserve
their own claim limits.
