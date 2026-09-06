# Project operations overlay

This template supplies project-specific operational values required by the
generic `agent_rules/WORKSPACE_OPERATIONS.md`.

When adopted Operations procedures require project-specific values, copy this
file to `PROJECT_OPERATIONS.md` at the repository root. That is the standard
active-overlay path; a project using another location must declare the exact
path in its root policy. This template is never active policy. Remove sections
that do not apply and replace every placeholder that remains. Do not keep
fictional placeholders in active policy. Keep sensitive values private unless
their publication is intentional and reviewed.

## Execution environments

- Canonical local environment: `<path-or-identifier>`
- Approved remote or evaluator environments: `<identities-or-none>`
- Approved build, deployment, or publication environments:
  `<identities-or-none>`
- Required framework or tool versions: `<versions-or-not-constrained>`
- Dependency roots: `<paths-or-none>`
- Dependency installation policy: `<policy>`
- Evidence environment identity requirements: `<requirements>`

## Local validation workflow

- Applicable existing validation environment: `<identity>`
- Routine local validation commands covered by an implementation task:
  `<commands>`
- Fixture and output scope, including what may be replaced: `<paths-and-policy>`
- Production access restrictions: `<restrictions>`
- Cost or duration limits requiring separate authorization: `<limits-or-none>`

Declare actual conditions. Do not assume local tests use disposable data or
have no production access. Remove this section if no such declarations are
needed for the adopted workflow.

## Repository and external-write boundaries

- Source-of-truth repository: `<repository>`
- Mechanical mirror, when applicable: `<repository-or-none>`
- Mirror scope: `<paths-or-none>`
- Approved remote transport: `<transport>`
- Change-review procedure: `<procedure>`
- Publication or release authority: `<policy>`
- Other external-write boundaries: `<operations-and-authority-or-none>`

## Task continuation

- Active task-state root: `<path>`
- Completed task archive: `<path-or-none>`
- Default polling cadence: `<duration-or-task-specific>`
- Long-running process identity fields: `<fields>`
- Single-writer scope: `<run-root-or-artifact-policy>`

## Shell and remote operations

- Local shell: `<shell>`
- Remote shell or shells: `<shells-or-none>`
- Required command wrappers: `<commands-or-none>`
- Destructive-operation policy: `<policy>`

## Packaging, deployment, and publication

- Package command: `<command-or-none>`
- Package validation command: `<command-or-none>`
- Deployment procedure: `<procedure-or-none>`
- Publication procedure: `<procedure-or-none>`
- Artifact identity and retention requirements: `<requirements-or-none>`

## Project-specific operational exceptions

List only exceptions justified by an actual project requirement. State the
affected generic rule, concrete reason, replacement boundary, validation, and
claim limit. Do not silently weaken authorization, evidence, or environment
identity rules.

- `<none, or documented exception>`
