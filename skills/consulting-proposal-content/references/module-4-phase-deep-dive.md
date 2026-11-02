# Module 4 — Phase Deep Dive

## 1. Role and Boundary

The root `SKILL.md` supplies shared evidence, framework, approval, taxonomy, and slide-separation rules. This file defines how Codex expands selected approved M3 rows into consultant-reviewable phase detail.

M4 is optional and selective. It explains how a chosen phase, workstream, method, or deliverable will work without regenerating the full proposal.

M4 does not:

- redesign the approved solution or phase architecture;
- silently expand M3 scope;
- create a task-level project plan unless explicitly requested;
- change approved duration or commercials;
- decide slide layouts or edit PowerPoint.

## 2. Supported Request Modes

| Mode | Use when | Output |
|---|---|---|
| `Full phase deep dive` | One selected phase needs complete delivery detail | Phase overview, sub-stages, service hierarchy, roles, deliverables, risks, and gates |
| `Selected workstream` | Only named M3 rows need expansion | Detail for those row IDs only |
| `Delivery detail` | The reader needs to understand what will be done and produced | Activities, executable actions, roles, inputs, deliverables, outcomes, and acceptance |
| `Method detail` | The reader needs to evaluate how an analytical question will be answered | Method rationale, inputs, steps, evidence, outputs, limitations, and quality checks |
| `Deliverable specification` | A key output is ambiguous or commercially important | Purpose, components, format, owner, review, acceptance, and exclusions |
| `Roles and governance detail` | Client participation or decision rights drive feasibility | Responsibility, decisions, forums, cadence, and escalation points |
| `Risk and readiness detail` | A phase is conditional, adoption-sensitive, or high risk | Readiness conditions, risks, mitigations, and go/no-go criteria |
| `Validation / revision` | The user supplies detailed phase content | Integrity findings and changed blocks only |

Produce only the requested phase, rows, or detail mode. Do not add method cards for every activity.

## 3. Entry Conditions

Preferred input is the selective approved M3 handoff:

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

M4 requires approved M3 rows. If the user supplies detailed content without an approved M3, Codex may validate or organize it, but any resulting deep dive must be labeled `Provisional — pending M3 approval` and cannot become final proposal scope.

If detail development reveals:

- a new activity, deliverable, duration, role, dependency, or commercial implication that materially changes a row, reopen M3;
- a new solution component, phase boundary, phase sequence, or delivery topology, reopen M2.

Do not hide an upstream change inside a detailed action list.

## 4. Select the Required Depth

Use the shallowest level that resolves the consultant's or client's decision.

| Level | Content | Use when |
|---|---|---|
| `D0 — M3 reference` | Existing approved row only | The master table is already sufficient |
| `D1 — Phase overview` | Purpose, scope, workstreams, outputs, gate | The phase needs a concise explanatory page or section |
| `D2 — Delivery detail` | Activities, actions, roles, inputs, deliverables, acceptance | Scope or responsibilities need evaluation |
| `D3 — Method / deliverable detail` | Analytical method, evidence, output specification, limitations | Method credibility or output quality is decision-critical |
| `D4 — Execution plan` | Task sequence, owners, milestones, control cadence | Explicitly requested after delivery detail is approved |

Do not default to D4. A proposal usually needs D1–D3; detailed execution planning may require a separate project-management artifact.

Select M4 for a row when at least one of these is material: high value, high risk, unfamiliar method, client-intensive participation, complex dependency, conditional scope, critical deliverable, adoption challenge, or commercial ambiguity. Otherwise retain the M3 row without expansion.

## 5. Preserve the Approved Hierarchy

Start from the M3 row ID and extend it rather than creating a new parallel structure.

Example internal identifiers:

```text
P2-W1            approved M3 row
P2-W1-S1         sub-stage
P2-W1-A1         activity/action block
P2-W1-D1         deliverable specification
P2-W1-G1         decision or acceptance gate
```

Use the shared service hierarchy only to the depth required:

```text
phase or wave -> delivery unit -> workstream/service category
  -> main activity -> executable action -> deliverable
  -> expected outcome -> acceptance
```

Preserve approved terminology. Do not rename phases, workstreams, or deliverables merely to make the deep dive sound more sophisticated.

## 6. Phase Overview

Create a compact overview before detailed tables when the full phase is requested:

```markdown
Phase and M3 source:
Decision or change enabled:
Scope and exclusions:
Entry conditions:
Selected workstreams / row IDs:
Principal outputs and intended outcome:
Exit / approval gate:
Detail depth selected and why:
```

Reference M3 rather than copying its full text. The overview should explain why the detailed blocks belong together.

## 7. Delivery Detail

### 7.1 Structure the service logic

For each selected M3 row, define only the additional detail needed below M3 level:

- genuine sub-stages, if applicable;
- main service activities;
- executable actions;
- consultant contribution;
- client inputs, participation, decisions, or ownership;
- methods or tools when decision-relevant;
- deliverables and expected outcomes;
- dependencies, decision points, and acceptance conditions;
- phase-specific risks, assumptions, and mitigations.

Apply the shared distinctness test. If a proposed sub-stage lacks a distinct purpose, method, output, owner, dependency, or gate, keep it as an activity.

### 7.2 Activity and action depth

Use `main activity` for a coherent body of work and `executable action` for the material steps needed to produce the approved deliverable.

An executable action should state:

```text
verb + object + method or participation qualifier + intended use
```

Example form:

```text
Validate the target decision-rights model through workshops with named role groups so that governance exceptions can be resolved before approval.
```

Do not list routine administration, every meeting, or internal consulting tasks that add no scope clarity.

### 7.3 Roles and collaboration

Make client participation explicit where it affects feasibility or quality. Distinguish:

- input provider;
- participant or co-designer;
- reviewer;
- decision maker;
- deliverable owner after handoff.

Use RACI or RAPID only when the work and decisions are stable enough for those frameworks and the user requests or benefits from a formal responsibility model. Do not create a large responsibility matrix for a simple phase.

### 7.4 Delivery-detail table

Use one linked table or split tables if width harms readability:

```markdown
| Detail ID | M3 row | Sub-stage | Service category | Main activity | Executable actions | Consultant contribution | Client input / decision | Deliverable | Expected outcome | Dependency / risk | Milestone / acceptance |
```

Omit columns that do not add decision value. Keep approved M3 fields by reference when they are unchanged.

## 8. Method Detail

Create method detail only for a material analytical or design question. A branded framework name is not sufficient.

### 8.1 Method-selection test

Use the shared framework-selection rule and answer:

1. What question must this method answer?
2. Why is this method appropriate to the evidence and context?
3. What inputs are required?
4. What analytical or design steps will be performed?
5. What evidence or output will result?
6. What decision will that output support?
7. What limitation or uncertainty remains?

If the method cannot answer a named question or change a decision, omit it.

### 8.2 Method card

```markdown
Method ID and linked M3/M4 row:
Analytical or design question:
Selected method / framework:
Why it fits:
Required inputs and client access:
Steps at proposal level:
Expected evidence / output:
Decision supported:
Limitations and fallback:
Quality check / validation:
```

Adapt methods to the organization. Do not copy a textbook sequence when data availability, regulatory context, organizational maturity, or project scope requires modification.

### 8.3 Fallback logic

If a method depends on data or access that may be unavailable, specify:

- minimum viable input;
- preferred input;
- fallback method;
- resulting reduction in confidence, depth, or deliverable quality;
- decision required from the consultant or client.

Do not promise the same output quality under materially weaker evidence.

## 9. Deliverable Specification

Specify a deliverable when its content, usability, acceptance, or boundary is not obvious from M3.

```markdown
Deliverable ID and linked row:
Name:
Purpose and decision supported:
Required components:
Format or level of editability, if relevant:
Inputs and dependencies:
Primary users and owner:
Review and approval forum:
Acceptance criteria:
Explicit exclusions:
Version or handoff requirements:
```

Differentiate:

- **working artifact** — supports the project team but is not necessarily handed over;
- **formal deliverable** — reviewed and transferred to the client;
- **decision package** — enables a governance decision;
- **operational asset** — intended for ongoing use after handoff.

Do not promise implementation-ready detail when the approved service depth is strategic guidance or high-level design.

## 10. Risks, Readiness, and Gates

Include only phase-specific risks that can change scope, method, sequence, quality, adoption, or acceptance.

Use this structure:

```markdown
| Risk / readiness condition | Trigger or evidence | Effect on phase | Mitigation / decision | Owner | Gate affected |
```

For adoption-sensitive phases, assess sponsorship, stakeholder alignment, capability, capacity, communication, incentives, and reinforcement only to the degree supported by scope. Use change frameworks as diagnostic or planning tools, not as mandatory lists.

For pilots or conditional phases, define the evidence required to proceed, revise, scale, or stop. Do not convert a vague milestone into a Go/No-Go gate without explicit criteria.

## 11. Duration, Resources, and Commercial Effects

Approved M3 duration and service depth remain canonical. M4 may explain their drivers but may not change them silently.

If detailed work reveals a material change:

- state the affected M3 row;
- explain the new evidence;
- estimate only when authorized and supported;
- return the duration, staffing, scope, or commercial change to M3 for approval.

Do not add named team members, effort estimates, fees, or payment terms unless explicitly requested and verified.

## 12. Content Blocks for Later Slide Development

M4 remains content-first. When later slide development is expected, mark candidate content blocks without choosing layouts:

```markdown
Content block ID:
Single message or decision supported:
Required evidence / table / process logic:
Must remain together:
May be separated if:
Source M3/M4 IDs:
```

Create a separate content block only when it has a distinct message, method, deliverable, comparison, or gate. Do not create one block per task. The downstream proposal-writing skill decides storyline and slide boundaries; the PowerPoint skill decides layout.

## 13. Partial and Revision Rules

### 13.1 Selected row or workstream

Return only the requested M3 row IDs and the minimum shared phase context needed to understand them. Do not repeat other workstreams.

### 13.2 Method-only request

Return method cards only. Reference approved activities and deliverables by ID instead of regenerating delivery detail.

### 13.3 Deliverable-only request

Return deliverable specifications only. Do not expand unrelated actions, methods, or roles.

### 13.4 Existing deep-dive revision

Preserve approved IDs and classify changes as:

- `Editorial` — no scope change;
- `M4 detail change` — method, actions, roles, specification, or phase-specific risk within approved M3 scope;
- `M3 scope/control change` — approved activity, deliverable, outcome, role, dependency, duration, acceptance, or commercial field changes;
- `M2 architecture change` — solution, topology, or phase changes.

Apply only authorized changes at the correct level. For a mature artifact, return changed blocks and a short change log rather than reproducing all phase detail.

## 14. Output Packages

### 14.1 Full phase deep dive

```markdown
Artifact: M4 — [Phase name] Deep Dive — vX
State: Draft | Provisional
Canonical M3 source: [artifact/version and selected row IDs]

Phase overview
[Compact overview]

Delivery detail
[Linked table]

Method cards
[Only for material methods]

Deliverable specifications
[Only for critical or ambiguous deliverables]

Risks, readiness, and gates
[Only decision-relevant items]

Content blocks for later slide development
[Optional; no layout decisions]

Approval requested
[Approve/amend named blocks, roles, methods, deliverable specifications, risks, and gates]
```

### 14.2 Validation output

```markdown
Detail that can remain unchanged
Missing or excessive depth
Scope changes requiring M3 or M2 reopening
Corrected blocks
Unresolved inputs or method limitations
Approval decision required
```

## 15. Review Protocol

### 15.1 Scope integrity

- Every detail block maps to selected approved M3 IDs.
- No new deliverable, role, duration, or commitment is hidden in prose.
- Changes are escalated to M3 or M2 at the correct level.
- Unselected phases and rows remain untouched.

### 15.2 Hierarchy and depth

- Sub-stages pass the shared distinctness test.
- Activities and actions are not mislabeled as phases or sub-stages.
- Detail level is proportionate to risk and decision need.
- Routine project administration is omitted.
- M4 does not become a task-level plan without explicit authorization.

### 15.3 Method integrity

- Every method answers a named question.
- Inputs and evidence requirements are visible.
- Method steps are adapted to context.
- Limitations and fallbacks are explicit.
- Framework branding does not substitute for analytical logic.

### 15.4 Deliverable and acceptance integrity

- Activities produce the specified deliverables.
- Deliverable components support their stated purpose.
- Outcomes are not renamed documents.
- Acceptance criteria are observable and authorized.
- Handoff ownership and editability are explicit when relevant.

### 15.5 Content and token efficiency

- Unchanged M3 content is referenced by ID rather than copied.
- Shared context is stated once at phase level.
- Method cards and deliverable specifications exist only where needed.
- Repeated risks, roles, or inputs are consolidated.
- Later slide blocks represent distinct messages, not individual tasks.

## 16. Approval and Handoff

Request the consultant to choose one:

- approve all named M4 blocks;
- approve specified blocks and revise named blocks;
- provide missing inputs for a method, deliverable, role, or gate;
- return a change to M3 or M2 because approved scope or architecture must change.

Approval applies only to the selected phase, row IDs, and block versions. Do not treat approval of one method card as approval of the full phase.

The approved M4 handoff to `consulting-proposal-writing` contains only:

```text
canonical M3 and M4 artifact versions
approved phase and detail IDs
single messages or decisions supported
approved service hierarchy and action logic
approved methods and evidence requirements
approved deliverable specifications and outcomes
roles, dependencies, risks, and gates that must remain visible
candidate content blocks, if requested
```

Do not begin slide implementation. The storyline and slide manifest must be approved before `persian-landscape-proposals` is used.

## 17. Acceptance Tests

Module 4 passes only if it can:

1. deep-dive one selected phase without reproducing the full M3 table;
2. expand only named workstream IDs when requested;
3. select D1, D2, D3, or D4 depth proportionately;
4. distinguish sub-stage, main activity, executable action, method, deliverable, outcome, and gate;
5. create a method card that explains question, inputs, steps, evidence, decision, limitations, and fallback;
6. specify a critical deliverable without inventing scope or implementation depth;
7. make client and consultant participation explicit without forcing a large RACI;
8. escalate M3 scope changes and M2 architecture changes correctly;
9. create candidate content blocks without deciding slide layout;
10. revise only named detail blocks while preserving approved IDs;
11. avoid unsupported duration, staffing, pricing, and impact claims;
12. stop at the M4 approval gate before storyline or PowerPoint production.
