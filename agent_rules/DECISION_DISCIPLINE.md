# Decision discipline

## Authority and activation

This file is a conditionally mandatory extension of the repository root
`AGENTS.md`. Read it before work involving one or more of:

- foundational or unconventional architecture or cross-domain synthesis;
- a material research hypothesis or experiment design;
- architecture comparison or a decision-bearing technical claim;
- performance adjudication, optimization, or adoption;
- evidence sufficiency, claim boundaries, or candidate adoption; or
- a material change to a shared contract, dependency boundary,
  representation, dataset, cache, checkpoint, supported route, or evaluator
  semantics.

Do not load this file merely because it exists. A trivial, local,
well-understood correction normally needs only the core rules and the smallest
relevant validation.

`AGENTS.md` owns global behavior, communication, authorization,
proportionality, and non-bypassable invariants. This file owns decision
necessity, protocol, acceptance, claim, architecture, and adoption.
`WORKSPACE_OPERATIONS.md` separately owns execution mechanics.

Apply only the sections relevant to the active task and phase. Re-evaluate
routing when the user materially changes the objective, criteria, evidence
standard, requested stage, environment, or authorization scope.

## Decision phases

These phases guide reasoning. They are not a persisted state machine and do
not require schemas, transition artifacts, or task infrastructure.

### Exploration

Generate and clarify materially different mechanisms. Radical assumptions,
cross-domain transfer, and deliberately unconstrained candidates are allowed.
Label unsupported mechanisms as hypotheses, but do not reject an idea merely
because implementation, evidence, or performance validation does not yet
exist.

Exploration freedom does not strengthen a decision claim. A name, analogy, or
plausible story is not evidence that a mechanism works.

### Architecture adjudication

Once candidates are sufficiently specified, compare their identity,
expressiveness, composition rules, dependencies, failure boundaries,
representation ceiling, counterexamples, optional components, multiplicity,
and supported claim level.

Do not apply full implementation, runtime, or experiment gates prematurely
while only generating candidates. Apply them when they can distinguish a
decision or expose a required constraint.

### Evidence and execution adjudication

When selecting an implementation, experiment, optimization, authoritative
route, or decision-bearing claim, apply the relevant contract, source and
original evidence, matched controls, uncertainty, runtime and memory,
engineering cost, deployment constraints, falsifiers, and adoption gate.

Moving to a later phase does not convert an exploratory hypothesis into
evidence. The user request and task stage determine which phase is active.

### Material user corrections

A material user correction changes the evaluation function. After it:

1. restate the revised criterion in plain language;
2. identify which earlier interpretations or conclusions it invalidates;
3. re-evaluate and re-rank all surviving candidates; and
4. do not preserve a favored candidate through incremental exceptions.

## Metaphor and cross-domain mechanism translation

When a metaphor, historical analogy, aesthetic phrase, or explicit contrast
materially guides a decision:

- translate it into properties, invariants, failure modes, and evaluation
  questions;
- preserve aspects that cannot be removed without changing the request;
- do not claim satisfaction from a superficial corresponding feature; and
- distinguish the mnemonic from the operational criterion that governs the
  decision.

A cross-domain analogy counts as a transferred mechanism only if it changes at
least one of:

- constructive state;
- invariant or conservation law;
- admissible operation;
- governing equation;
- decomposition or composition rule;
- runtime or failure behavior; or
- falsifiable prediction.

Renamed standard components, historical parallels, or collected terminology
alone do not constitute cross-domain synthesis.

## Optional foundational architecture lens

When the user explicitly seeks a foundational, distinctive, irreducible, or
enduring architecture, the following mnemonic lens may be used. It is not a
universal acceptance gate, and the generic definitions own the meaning.

1. **Irreducible identity (Venus).** After removing components claimed to be
   auxiliary or replaceable, does a recognizable and materially useful core
   remain?
2. **Generative expansion (Caesar).** Does the core only solve the current
   instance class, or does it establish primitives that successors can extend
   under changing conditions?
3. **Institutional closure and transmission (Napoleon).** Can accumulated
   capabilities become a coherent, composable, governable, and transmissible
   order that unfamiliar users can extend without relying on the original
   designer's case-by-case judgment?

A proposal satisfying only one or two dimensions must be described that way.
Do not promote a theorem, primitive, negative control, or restricted
constructor into a full architecture merely because it strongly satisfies one
dimension.

## Claim levels and architectural multiplicity

Separate claim levels when applicable:

- core theorem or invariant;
- restricted-domain constructor;
- full-contract architecture; and
- supported end-to-end operational route.

A restricted theorem does not establish full-contract correctness or
end-to-end performance. Optional guides, compound representations, fallbacks,
repair, abstention, and specialist routes are part of the architecture
identity when required by the supported contract. Charge them to quality,
runtime, dependency, and failure behavior.

When a proposal contains a core, guide, fallback, repairer, or specialist:

- state whether components share one representation and invariant;
- state whether deleting one leaves the same architecture or invokes a
  different algorithm;
- state who selects among them and from which inputs; and
- when selection is input-dependent and semantics differ, evaluate the design
  explicitly as an ensemble, portfolio, routing system, or mixture rather
  than denying the multiplicity.

## Adversarial adjudication

After a material, decision-bearing architecture is sufficiently specified and
before it drives implementation, an expensive experiment, or adoption, give
it one bounded adversarial pass:

- locate the original source or reproducible calculation behind agent- or
  delegate-produced observations;
- construct the strongest plausible alternative explanation;
- identify a concrete counterexample, representation ceiling, or failure
  boundary;
- state what evidence would reverse the conclusion; and
- report unresolved reviewer disagreement rather than silently averaging it.

This does not require a formal proof, review framework, or adversarial pass
over every exploratory idea. Delegation increases breadth, not authority.

## Research and evidence

- Separate observed source facts, recomputed calculations, assumptions,
  interpretations, decisions, and claim limits.

- Resolve material conclusions to the applicable authoritative basis:
  official or product contracts, source-of-truth code at an exact identity,
  original result artifacts, or explicit reproducible calculations. Targets,
  plans, consensus, and sunk work are inputs, not reasons for a conclusion.

- Reviews, summaries, generated reports, and prior-agent conclusions are
  leads. Verify actionable findings against source, applicable semantics, or
  original evidence before changing code, repeating work, or strengthening a
  claim.

- Task memos and handoffs are authoritative only for recorded coordination
  state. They are not experiment evidence.

- For a material research hypothesis or experiment decision, identify when
  applicable:

  - the proposed mechanism;
  - a matched baseline or control;
  - relevant prevalence across cases, cohorts, or repetitions;
  - compute, runtime, memory, and engineering opportunity cost; and
  - a concrete falsifier or explicitly inconclusive outcome.

- First-principles reasoning exposes assumptions. It does not replace reading
  source, contracts, literature, base rates, or original results, or running
  proportionate tests.

- Treat official specifications and applicable evaluators as authorities
  within their defined scope. Preserve the original identity of baseline or
  reference artifacts when the applicable contract requires it. A template
  explicitly intended to be completed or modified may be edited according to
  its stated contract; otherwise preserve the authoritative original and use a
  labeled derived copy.

- For durable decision-bearing evidence, record the applicable source
  identity, artifact identities, environment and hardware identity, workload
  or cohort, units, date, protocol, and material exclusions.

- Never invent missing evidence. Restrict the claim. Missing external access
  is not automatically a local coding blocker or a reason to repeat existing
  evidence.

- Independently validate important calculations and report uncertainty when
  it could change the decision.

## Architecture and change discipline

- Locate a material failure at the correct boundary: input data, state or
  cache, training or build, domain transformation, feasibility enforcement,
  core algorithm or optimizer, validation, wrapper, package, or environment.
  Prefer the smallest boundary-correct change.

- Give shared components cohesive ownership, explicit inputs and outputs,
  intended dependency direction, and clear failure behavior. A stable
  documented interface may be sufficient; a new abstraction is not required
  by default.

- Keep research and supported operational surfaces explicit. A bounded
  research helper need not become product architecture and must not silently
  enter the supported runtime closure.

- Assign each material correctness invariant one authoritative owner.
  Orchestration may coordinate owners but must not duplicate their policy or
  depend on private implementation details without an explicit bounded reason.

- Added complexity must produce a material measured benefit, improve decision
  quality, increase necessary reliability or reproducibility, or enforce an
  applicable correctness, feasibility, or safety bound under the actual
  failure and threat model.

- Do not add a second validator that merely re-encodes an existing
  authoritative policy without owning a distinct trust, correctness, or
  acceptance boundary. Independent validation is justified when a producer
  must not self-certify or a distinct boundary owns it.

- Do not add generalized abstractions, frameworks, fallback systems,
  provenance or security mechanisms, transaction systems, registries, or
  broad harnesses for hypothetical future use without an observed recurring
  failure, an applicable requirement, a measured bottleneck, or an explicitly
  authorized product need.

- Before a substantial refactor, state:

  - the recurring failure or hypothesis;
  - why the current boundary causes it;
  - the semantics and invariants to preserve;
  - intended dependency direction and failure behavior;
  - what will be removed or deliberately omitted; and
  - the real mini-flow or artifact check that reaches the affected boundary.

- Repeated local patches justify inspecting a shared boundary, not
  automatically creating an abstraction or rewrite.

## Performance optimization

- Establish a representative baseline at the decision-relevant scope,
  including end-to-end behavior when the claim or affected path is
  end-to-end. Declare the primary metric and correctness, quality, memory, and
  reliability guardrails. Do not substitute throughput, latency, quality,
  correctness, memory, startup cost, or recovery behavior for one another.

- Measure only enough to identify the decision-relevant bottleneck and normal
  variance. Separate only applicable stages, such as input or cache wait, data
  movement, algorithm components, validation, serialization, startup, and
  packaging.

- Deconstruct the measured bottleneck from first principles:

  1. which invariant the work enforces;
  2. which algorithm and data structures implement it;
  3. how often the path runs;
  4. its observed and asymptotic time and space cost;
  5. necessary versus avoidable reconstruction, dense materialization, data
     movement, synchronization, allocation, serialization, or repeated work;
     and
  6. what can be removed, reused, incremental, sparse, batched, vectorized,
     fused, prefetched, overlapped, or safely parallelized.

- Estimate the maximum possible benefit in the declared primary metric before
  implementation. For an end-to-end speed claim, use the measured time share
  to bound the best possible overall speedup. Do not optimize below
  measurement variance or the required material improvement unless it unlocks
  a necessary change.

- Prefer eliminating unnecessary work over making it faster. The sequence
  `remove or reuse -> lower complexity -> incremental or sparse -> batch,
  vectorize, or fuse -> overlap or prefetch -> parallelize` is a heuristic,
  not a mandatory order.

- Prefer one attributable material optimization at a time unless changes are
  semantically inseparable.

- Retain an optimization only when applicable conditions hold:

  - semantic equivalence or explicitly bounded numerical equivalence;
  - completion of the relevant operational mini-flow;
  - preserved correctness, feasibility, project-defined acceptance, recovery,
    and reliability requirements;
  - no unacceptable peak-memory or operational regression; and
  - material measured improvement in the declared primary metric at the
    decision-relevant scope, or satisfaction of a necessary runtime, memory,
    reliability, recovery, or deployment bound without unacceptable
    regression in the declared guardrails.

- Unit tests prove encoded behavior, not operational completion or policy
  necessity. When integration is the main risk, a real mini-flow is usually
  stronger than many isolated tests.

- Before an expensive full run, exercise the same relevant source, data,
  environment, state, wrapper, evaluator, and stage transitions at small
  scale. Require only elements that can affect the changed path.

- Hardware-specific performance claims require representative uncontended
  measurement when suitable hardware is available. Otherwise record the
  limitation and restrict the claim rather than blocking unrelated work.

- Reliability and speed are simultaneous requirements. Revise a guardrail
  only through an explicit evidence-backed change to its authoritative
  definition and corresponding validation and claim updates.

- Do not discard completed state or evidence merely because code was
  refactored.

- Reuse completed state or evidence for a changed route, experiment,
  comparison, or claim only after verifying the relevant source,
  configuration, schema, environment, state, and semantic compatibility.

- Historical evidence remains valid for the route and protocol that produced
  it even when it cannot support the changed route.

- Do not retry an unchanged rejected optimization unless the condition that
  caused rejection materially changed.
