# Changelog

This file records changes to the reusable ORDO CIVITATIS framework. Version
numbers identify framework revisions, not measured agent performance.

During 0.x development, increment the patch number for wording clarifications,
link fixes, and narrow rule corrections. Increment the minor number for new
or materially changed decision, authorization, or validation principles.
Reset the patch number when incrementing the minor number. Compatibility is
not yet guaranteed. Consider 1.0.0 when the core contracts are stable enough
to support an explicit compatibility commitment.

Released revisions use Git tags in the form `vX.Y.Z` pointing to exact commits.
Do not move a published tag to different content. An unreleased entry does not
establish that a tag or GitHub release exists.

## 0.2.0 - 2026-09-06

### Changed

- Prefer real mini-flows through affected execution and integration boundaries,
  checking expected results. Use additional tests for important uncovered risks
  and applicable required checks, with explicit limits on small-run claims.
- Clarify that implementation requests include routine local validation, repair
  of failures caused by the change, and affected rechecks. Keep external writes,
  dependency changes, expensive runs, and unrelated process control within their
  separate authorization boundaries.
- Reduce unnecessary approval pauses, document loading, and persistent task
  state. Distinguish routine read-only Git inspection from operational writes,
  and assess materiality by impact, failure consequences, uncertainty, and cost.
- Expand exploration through first principles, mathematical structure, and
  cross-domain literature. Distinguish core method limitations from supporting
  gaps, and assess direct paths, abstraction, and bounded restructuring.
- Prioritize investigation by actual impact and scale effects. Allow bounded
  prototypes to establish mechanisms or cost structures before substantial
  optimization commitments.
- Add model-change evaluation examples and local validation declarations to
  adoption guidance and the operations overlay template.
- Introduce this changelog and the lightweight versioning convention.

### Adoption notes

Review the changed core, Decision, and Operations rules against local overrides.
Use the optional validation section of the operations overlay template only
where concrete environment, data, command, or cost declarations are needed.
These revisions have undergone document review and consistency checks, not a
controlled evaluation demonstrating improved model behavior.

## 0.1.0 - Retrospective baseline

This label identifies the framework before the 0.2.0 changes at commit
[`f6781e7`](https://github.com/Kaz9487/ordo-civitatis/commit/f6781e774a31ba3c801fbc3874738915bc7a34ee).
It was assigned retrospectively and does not imply an earlier tagged release.

- Layered core, Decision, and Operations rules.
- Adoption, rationale, and optional Project Memory documentation.
- Operations and continuation templates, with a pull request template.
