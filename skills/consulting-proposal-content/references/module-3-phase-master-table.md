# Module 3 — Execution-Phase Master Table

## 1. Role and Boundary

The root `SKILL.md` supplies shared taxonomy, evidence, conditionality, and approval rules. This file defines how Codex converts an approved M2 phase architecture into an executive-level delivery table.

Module 3 is the canonical source for high-level execution scope:

- service categories or workstreams;
- principal activities;
- deliverables and expected outcomes;
- client inputs and dependencies;
- indicative duration and commercials when verified;
- phase exit and acceptance conditions.

Present the table first. Do not create detailed methods, task instructions, slide layouts, or PowerPoint content. Selected phase detail belongs to M4.

## 2. Supported Request Modes

| Mode | Use when | Output |
|---|---|---|
| `Full master table` | All approved phases need execution-level definition | One complete M3 table or a linked pair of tables |
| `Selected phase table` | Only one or more named phases are requested | Rows for those phases only |
| `Scope matrix` | Delivery spans several entities, topics, or service depths | Delivery-unit × subject × depth × phase/wave matrix |
| `Table revision` | An existing table needs correction or refinement | Changed rows only plus impact note, preserving approved content |
| `Column completion` | The user needs only deliverables, outcomes, client inputs, duration, or another field | Requested columns keyed to stable row IDs |
| `Schedule view` | Approved scope must be sequenced | Dependency-based schedule after table approval |
| `Commercial view` | Verified pricing or payment data must be organized | Commercial table linked to approved scope IDs |
| `Validation` | The user supplies a draft phase/service table | Integrity findings and corrected rows without unnecessary rewriting |

Produce only the requested mode. Do not add schedule or commercial views merely because the source examples contain them.

## 3. Entry Conditions

Preferred input is the approved M2 handoff:

```text
canonical M2 artifact/version
solution components
delivery topology
approved phase names and sequence
phase objectives and scope boundaries
major workstreams
principal outputs
entry conditions, dependencies, and gates
conditional elements
material assumptions requiring visibility
```

M3 must not proceed from an approved solution with unapproved phase architecture. If the user explicitly supplies an already approved phase model, record that artifact as the canonical M2-equivalent input.

If the user explicitly requests an M3-style table without an approved phase architecture, either recommend M2 first or produce `Provisional scope table — pending M2 approval`. A provisional table cannot unlock M4, schedule finalization, commercial commitment, or slide production.

If table development reveals a new phase, changed phase boundary, new solution component, or material scope expansion, stop and propose an M2 change. Do not hide architecture changes inside table rows.

## 4. Table-Design Workflow

### 4.1 Lock the approved architecture

Create an internal scope header:

```text
M2 source and version:
Included phases:
Included delivery units:
Conditional elements:
Protected exclusions:
Requested optional fields:
```

Use approved phase names and sequence exactly. Refining a workstream label is allowed; changing the solution architecture is not.

### 4.2 Choose the table grain

Choose the smallest row unit that remains unambiguous:

- **One row per phase** — use only for a compact executive view with tightly related work and few outputs.
- **One row per phase–workstream combination** — default when workstreams have distinct activities, deliverables, owners, dependencies, or acceptance conditions.
- **One row per delivery unit–phase–workstream combination** — use when entities receive materially different scope or service depth.
- **Cross-phase enabler row** — use for governance, change, benefits, reporting, risk, capability, or knowledge-transfer work that genuinely spans phases.

Split a row when a cell contains unrelated objectives, different owners, separate gates, or several deliverables that cannot share one outcome. Do not split rows merely to create a visually larger table.

### 4.3 Assign stable IDs

Assign each row a stable internal ID, such as `P1-W1`, `P2-W3`, or `X-GOV`. Preserve IDs across revisions so later modules can reference changed rows without repeating the whole table.

If an approved row is removed, mark it `Superseded` rather than silently reusing its ID for different work. Client-facing output may hide IDs when they do not improve readability, but the approved handoff must retain them.

### 4.4 Expand only approved workstreams

For each approved M2 phase and major workstream:

1. restate the phase objective without copying the full M2 narrative;
2. define principal activities at proposal scope level;
3. identify reviewable deliverables;
4. state the expected operational or decision outcome;
5. identify essential client inputs, decisions, or participation;
6. record dependencies and assumptions;
7. define the observable phase or row acceptance condition;
8. add duration or commercials only when authorized and supported.

Use a traceability check:

```text
M2 component/phase -> M3 row -> activities -> deliverables
  -> expected outcome -> exit/acceptance condition
```

### 4.5 Check coverage and overlap

Create an internal coverage map from every approved M2 component and workstream to at least one M3 row. Document deliberate cross-phase coverage once; do not duplicate the same activity in several rows to make the table look complete.

Use MECE where scope categories need clean ownership. Do not force an artificial partition when collaboration or shared responsibility is real; make the interface explicit instead.

## 5. Field Grammar

Use only columns that add decision value. The following grammar controls the fields most often confused:

| Field | Write as | Avoid |
|---|---|---|
| Objective | Decision or change the row must enable | A list of tasks |
| Main activity | Verb + object + material qualifier | Vague nouns such as `analysis` without scope |
| Deliverable | Tangible or reviewable artifact, design, decision package, model, map, or approved specification | Meetings, effort, or outcomes stated as documents |
| Expected outcome | Changed operational, strategic, organizational, or decision state enabled by deliverables | A renamed deliverable |
| Client input / role | Specific data, access, workshop participation, decision, validation, or ownership | Generic `client cooperation` |
| Dependency / assumption | Condition that changes feasibility, order, effort, or confidence | Routine project hygiene presented as a major dependency |
| Exit / acceptance | Observable condition for accepting the row or closing the phase | `High quality`, `completed successfully`, or other subjective labels |

### 5.1 Activity rules

Activities should be specific enough to define scope but not so detailed that they become a task plan. Use parallel verbs for comparable rows, such as `assess`, `analyze`, `design`, `validate`, `prioritize`, `pilot`, or `establish`.

Do not treat a framework name as an activity. State what will be done with the framework and why.

### 5.2 Deliverable rules

Every deliverable must result from a named activity and support an outcome or gate. Distinguish:

- working analyses used by the project team;
- formal client deliverables;
- decisions or approvals required from governance bodies.

Do not promise a deliverable whose required data, authority, or capability is absent without making the dependency visible.

### 5.3 Outcome rules

Use outcomes to state what becomes clearer, decided, designed, enabled, adopted, controlled, or measurable. Do not claim business impact that depends on later implementation unless it is labeled as an intended or enabled outcome.

### 5.4 Acceptance rules

An acceptance criterion should be observable and linked to the purpose of the deliverable. Appropriate forms include:

- named decision approved by the authorized forum;
- required scope covered and validated by named stakeholders;
- model reconciled to agreed inputs;
- target design meets approved principles and constraints;
- pilot evidence meets a defined threshold;
- owner accepts handoff and required capability is in place.

Use quantitative thresholds only when supplied or explicitly developed within scope.

## 6. Table Architecture

### 6.1 Default phase–workstream table

Use this structure unless another mode is more decision-useful:

```markdown
| ID | Phase | Service category / workstream | Objective | Main activities | Deliverables | Expected outcome | Client input / decision | Dependencies / assumptions | Indicative duration | Exit / acceptance |
```

Omit optional columns that add no decision value. Add `Delivery unit`, `Service depth`, or `Conditional / option` when required by approved M2 topology.

### 6.2 Compact phase table

Use one row per phase only when activities and outputs remain coherent inside that row. Use short parallel bullets inside cells. If the row becomes a mini-document, switch to phase–workstream grain.

### 6.3 Multi-entity scope matrix

When scope spans several entities, first provide a scope matrix:

```markdown
| Delivery unit / entity | Service subject | Service depth | Applicable phase or wave | Conditionality / note |
```

Then provide the master table at the grain needed to describe activities and outputs. Do not repeat identical work for every entity; use a shared row plus explicit entity-specific variations when responsible.

### 6.4 Split-table option

If one table is too wide to review, split it using the same row IDs:

1. **Scope and content:** phase, unit, workstream, objective, activities, deliverables, outcome.
2. **Delivery controls:** client role, dependencies, duration, gate, conditionality, commercials.

Do not solve width by deleting decision-critical content or shrinking it into unreadable fragments.

## 7. Cross-Phase Enablers

Represent a cross-phase enabler once and show where it applies. Typical candidates include governance, risk, benefits tracking, reporting, change, communication, capacity, capability building, and knowledge transfer.

Do not make an enabler a standalone phase unless it has a distinct objective, boundary, output, and gate under the shared phase tests. Do not copy the same governance or change activity into every phase row.

## 8. Duration and Schedule

### 8.1 Indicative duration

Include duration only when the user supplies it, an approved source contains it, or the consultant explicitly authorizes an estimate. State the basis and material assumptions. Prefer defensible ranges over false precision.

Do not add phase durations to calculate total elapsed time when work runs in parallel. Distinguish effort from calendar duration.

### 8.2 Schedule view

Create a schedule only after the relevant M3 rows, dependencies, and durations are approved. Use stable row IDs:

```markdown
| ID | Start condition | Duration | Predecessor | May run in parallel with | Milestone / gate |
```

The schedule may visualize approved scope; it may not introduce new activities. If sequencing exposes a missing dependency or phase boundary, reopen the affected M2/M3 decision before finalizing the schedule.

## 9. Commercial View

Commercial fields are optional. Include them only when explicitly requested and supported by verified project inputs.

Use a separate linked table when commercials would overcrowd the scope table:

```markdown
| Phase / ID | Base or option | Pricing basis | Verified fee | Currency / tax treatment | Payment milestone | Commercial assumption / exclusion |
```

Before presenting commercials, verify:

- exact currency and unit;
- whether tax/VAT is included;
- price validity and payment terms, if provided;
- which rows or phases the fee covers;
- treatment of optional or later-to-be-scoped work;
- consistency between phase totals and any stated engagement total.

Never infer fees, discounts, payment terms, or price ranges from reference proposals. Do not price conditional implementation before its scope is approved.

## 10. Partial and Revision Rules

### 10.1 Selected phases

Return only rows for the requested phases. Include the canonical M2 source and any cross-phase dependency required to understand those rows; do not regenerate the other phases.

### 10.2 Column completion

When asked to add or improve one field, preserve row IDs and all unrequested approved cells. Flag a conflict rather than rewriting the rest of the row silently.

### 10.3 Existing table revision

Classify proposed changes as:

- `Editorial` — clarity or parallel grammar; no scope change;
- `M3 content change` — activities, deliverables, outcome, role, dependency, duration, or acceptance;
- `M2 architecture change` — solution component, phase boundary, topology, or major scope change.

Apply editorial and authorized M3 changes directly. Stop and reopen M2 for architecture changes.

### 10.4 Delta output

For a mature table, return changed rows and a concise change log rather than reproducing the whole artifact unless the user asks for a consolidated version.

## 11. Output Package

### 11.1 Full M3

```markdown
Artifact: M3 — Execution-Phase Master Table — vX
State: Draft | Provisional
Canonical M2 source: [artifact/version]

[Scope matrix, only if needed]

[Master table — presented first]

Material notes
[Only ambiguities, conditional elements, or assumptions that cannot fit cleanly in the table]

Approval requested
[Approve/amend table grain, rows, activities, deliverables, outcomes, client inputs, dependencies, duration/commercial fields, and gates]
```

### 11.2 Validation output

```markdown
Integrity findings
Rows that can remain unchanged
Corrected or split rows
Missing traceability or dependencies
Items requiring M2 reopening
Approval decision required
```

Do not preface the table with a long narrative. A one-sentence scope note is sufficient when context is necessary.

## 12. Review Protocol

### 12.1 Architecture integrity

- Every row maps to an approved M2 component, phase, or cross-phase enabler.
- Phase names, order, and boundaries remain unchanged.
- No row introduces an unapproved solution or service.
- Table grain is consistent or intentionally varied with a clear reason.

### 12.2 Row integrity

- Each row has one coherent objective.
- Activities create the stated deliverables.
- Deliverables enable the expected outcome.
- Acceptance criteria test the row or phase purpose.
- Client inputs and decisions are specific.
- Dependencies affect execution rather than repeat generic project hygiene.

### 12.3 Coverage and readability

- Approved workstreams are covered without avoidable overlap.
- Similar rows use parallel wording and comparable depth.
- Repeated content is replaced by row IDs or shared enabler references.
- Cells remain concise enough for executive review.
- Wide content is split into linked tables rather than compressed into ambiguity.

### 12.4 Time and commercial integrity

- Duration basis and parallelism are explicit.
- Schedule contains no new scope.
- Currency, tax, coverage, and option status are unambiguous.
- Totals reconcile to verified inputs.
- Conditional work is not presented as committed scope or price.

## 13. Approval and Handoff

Request the consultant to choose one:

- approve the table and unlock M4;
- approve specified rows and revise named rows;
- provide missing inputs for named fields;
- reopen M2 because a solution or phase architecture change is required.

Do not treat approval of a schedule or commercial view as approval of unapproved scope rows.

The approved M3 handoff to M4 contains only the selected phase and row IDs plus:

```text
canonical M3 artifact/version
selected phase/rows
objective
approved activities
approved deliverables and outcomes
client role/input
dependencies and assumptions
exit/acceptance condition
approved duration or service depth, when relevant
```

Do not pass the whole master table when M4 is requested for one phase.

## 14. Acceptance Tests

Module 3 passes only if it can:

1. generate a table first from an approved M2 without rewriting M1 or M2;
2. choose phase, phase–workstream, or unit–phase–workstream grain appropriately;
3. return only one selected phase or requested field when asked;
4. distinguish activities, deliverables, outcomes, and acceptance criteria;
5. represent multi-entity scope without duplicating identical work;
6. represent governance or change once as a cross-phase enabler;
7. preserve stable row IDs across revisions;
8. create a schedule only from approved rows, dependencies, and durations;
9. include commercials only from verified inputs and reconcile totals;
10. detect an M2 architecture change and stop instead of hiding it in the table;
11. hand off only selected rows to M4;
12. stop at the M3 approval gate before creating detailed phase content.
