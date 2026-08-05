# Corrections and effective methods

Last reviewed: `<last-reviewed>`

This file stores distilled reusable lessons, not a complete chronology.
Detailed incidents and task-specific evidence remain in task archives and
original artifacts. When a lesson becomes policy, point to its authoritative
core, Decision, Operations, or project-overlay owner rather than copying the
rule here.

For each correction, record:

- category and scope;
- failure class or faulty reasoning;
- corrected interpretation;
- effective method;
- current status or authoritative owner; and
- the condition that would make the lesson inapplicable.

Update an existing entry before adding another rule.

## Synthetic examples

The examples below are fictional.

### Example 1: Local output is not publication

- Category: status and authorization
- Scope: a customer-support report generator
- Failure: a locally generated CSV was reported as published before the upload
  step occurred.
- Correction: generated, reviewed, uploaded, and published are distinct
  milestones. Local generation does not authorize external publication.
- Effective method: report the highest completed milestone and name the exact
  pending external action.
- Status: reusable lesson; replace with project vocabulary when adopted.

### Example 2: Quiet work is not failed work

- Category: long-running process recovery
- Scope: a static-site image conversion job
- Failure: quiet output caused a second process to be launched against the same
  output directory.
- Correction: inspect recorded process and output state before restarting.
- Effective method: preserve process identity, phase, polling cadence, and a
  single-writer rule.
- Status: reusable only for workflows with resumable or expensive processes.

### Example 3: A future extension is not a current requirement

- Category: over-engineering
- Scope: a personal note-import utility
- Failure: a plugin registry and lifecycle framework were designed before a
  second importer existed.
- Correction: one possible future extension does not establish a reusable
  abstraction boundary.
- Effective method: implement the smallest current interface and revisit the
  boundary after a real second use case appears.
- Status: reusable lesson; not a ban on plugin systems with demonstrated need.
