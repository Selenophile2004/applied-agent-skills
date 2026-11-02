# Module 2 — Solution and Phase Approval

## 1. Role and Boundary

The root `SKILL.md` supplies shared evidence, framework, status, topology, approval, and canonical-source rules. This file defines how Codex turns an approved problem basis into a consultant-reviewable solution architecture and justified high-level phases.

Module 2 answers two questions:

1. **What intervention direction should be approved?**
2. **How should that direction be divided into phases, workstreams, waves, and gates?**

Module 2 does not create the detailed service table, task-level workplan, Gantt chart, pricing model, phase deep dives, or PowerPoint slides. Those belong to later modules or skills.

## 2. Supported Request Modes

Select only the requested mode.

| Mode | Use when | Output |
|---|---|---|
| `Full M2` | Both solution direction and phase architecture need approval | M2A solution architecture followed by M2B phase architecture |
| `M2A solution only` | The consultant wants to agree on the intervention before phasing | Solution logic, alternatives when real, recommendation, and assumptions |
| `M2B phases only` | A solution direction is already approved | Delivery topology and high-level phase definitions |
| `Validate proposed solution` | The user already has a solution or phases | Traceability, gaps, tradeoffs, and corrected structure without unnecessary reinvention |
| `Alternative comparison` | Management faces genuine strategic choices | Options, criteria, tradeoffs, and recommendation; phases only if requested |
| `Multi-entity architecture` | Scope spans a group, subsidiaries, functions, or sites | Delivery-unit matrix, service depth, parallel tracks, waves, and program-level gates |
| `Partial revision` | Only one solution component, phase, gate, or topology element must change | Only the requested revision, with dependency impacts identified |

Do not generate phases when the user requests only a solution decision. Do not redesign an approved solution when the user requests only phasing.

## 3. Entry Conditions

Preferred input is the compact approved M1A handoff:

```text
organization/scope
decision question
desired outcome
enablers
constraints and gap
consequences
critical assumptions and unresolved evidence
```

M2 may also begin from a user-supplied diagnosis, existing proposal, approved strategy, or named solution. Record whether the input is `Approved`, `Provisional`, or `User supplied`.

Before drafting, confirm that the available input is sufficient to distinguish:

- the decision to be made;
- current-to-desired-state gap;
- material causes, design constraints, or unresolved uncertainties;
- intended outcomes and success evidence;
- scope boundary and affected delivery units;
- non-negotiable constraints;
- existing decisions that must remain unchanged.

If these are incomplete, do not silently rerun Module 1. Ask only the smallest questions needed for M2, or issue a provisional M2 that names the dependency.

## 4. Default Interaction Pattern

For a high-uncertainty or politically sensitive project, use two internal approval passes:

```text
M2A — solution architecture
  -> consultant approval or revision
M2B — phase and delivery topology
  -> consultant approval or revision
```

For a straightforward engagement, M2A and M2B may be presented together, but the approval request must still distinguish solution direction from phase structure. Approval of one does not imply approval of the other.

## 5. Solution-Design Workflow

### 5.1 Restate the decision, not the narrative

Begin with one governing decision question and the desired outcome. Reference approved M1A rather than repeating its full narrative.

Create a short design brief:

```text
Decision:
Desired outcome:
Scope:
Non-negotiable constraints:
Critical uncertainty:
```

### 5.2 Diagnose what the solution must change

Translate the approved gap into solution requirements. Keep symptoms, causes, constraints, and required changes separate.

Use this traceability chain:

```text
Issue or gap -> cause / constraint / uncertainty
  -> required intervention or capability
  -> intended outcome -> success evidence
```

If a cause is not sufficiently established, do not design a permanent intervention around it. Either mark the intervention as a hypothesis or create an early diagnostic/validation gate.

### 5.3 Define solution design principles

Use three to seven project-specific principles to guide option design and later phase decisions. A principle must constrain a real choice.

Useful forms include:

- preserve or leverage a verified organizational strength;
- resolve a named governance or operating ambiguity;
- reduce irreversible investment until uncertainty is resolved;
- design for a defined client capability or resource constraint;
- enable measurable adoption or benefits;
- protect regulatory, continuity, or stakeholder requirements.

Avoid generic principles such as `be agile`, `use best practices`, or `focus on customers` unless translated into a concrete design implication.

### 5.4 Generate alternatives only when a real choice exists

Create alternatives when management could legitimately choose different scopes, operating models, entry modes, sequencing approaches, or service depths. Do not create cosmetic options to make a predetermined answer appear analytical.

When alternatives are useful:

1. include the current path or minimum-change baseline when decision-relevant;
2. make each option internally coherent;
3. compare options against criteria tied to the decision;
4. expose tradeoffs rather than optimizing every criterion simultaneously;
5. avoid numeric scoring unless weights and scores have a verified basis.

Candidate criteria may include strategic fit, expected impact, feasibility, capability requirements, investment, time to value, risk, reversibility, stakeholder acceptance, regulatory fit, and scalability. Use only relevant criteria.

### 5.5 Select and challenge the recommendation

Recommend one direction or a conditional path. State:

- why it best addresses the approved gap;
- what it deliberately excludes;
- critical tradeoffs;
- required client capabilities or decisions;
- material risks and assumptions;
- evidence that would disconfirm or change the recommendation.

Run a compact pre-mortem:

```text
If this solution failed, what would most likely have caused the failure?
```

Use the answer to strengthen conditions, gates, governance, or adoption logic—not to add generic risk language.

### 5.6 Choose frameworks as working tools

Use the shared framework-selection rule in `SKILL.md`. Select the lightest method that resolves a material uncertainty.

Create an internal framework record:

| Field | Content |
|---|---|
| Decision need | What uncertainty or design question must be resolved? |
| Primary framework | One main lens or method |
| Supporting method | Optional; use only if it closes a separate gap |
| Adaptation | How the method is tailored to this organization |
| Evidence required | Inputs needed for responsible use |
| Limitation | What the framework cannot establish |

Prefer one primary framework and no more than two supporting methods in a given decision step. Remove any framework that changes neither the decision nor the completeness of the solution.

Do not automatically expose framework names in client-facing output. Explain the logic in plain language unless method visibility helps establish credibility or scope.

## 6. Solution Architecture

Express the recommended solution as a small set of coherent components. Each component must map to an approved gap or desired capability.

For each component, define:

- purpose;
- gap or outcome addressed;
- scope boundary;
- required capability or change;
- relationship to other components;
- principal success evidence;
- material assumption or dependency.

Separate core intervention components from cross-cutting enablers. Governance, change management, data, technology, benefits tracking, communication, capability building, and knowledge transfer may enable several components without becoming standalone phases.

Use the minimum number of components needed to explain the solution. Do not reproduce a detailed service catalog.

## 7. Delivery Topology

### 7.1 Classify each delivery element

Before naming phases, classify proposed elements using the shared taxonomy: phase, workstream, wave, delivery unit, and service depth.

If an element can occur concurrently and does not depend on the completion of another element, it is probably a workstream or parallel track rather than a phase.

### 7.2 Select the topology

Choose one of these patterns or a justified hybrid:

- sequential phases;
- parallel workstreams within shared phases;
- prioritized entity waves;
- gated pilot-to-scale;
- program-level phases with entity-specific tracks;
- another dependency-driven arrangement.

Represent complex scope using separate dimensions:

```text
delivery unit x service subject x service depth x time
```

Do not flatten this matrix into a single numbered list if doing so hides parallel delivery or different service depths.

## 8. Phase Architecture

### 8.1 Create phase boundaries

Apply the shared phase tests. For every proposed phase, write one sentence titled `Why separate`. If that sentence cannot name a material boundary, keep the work inside an existing phase as a workstream or activity.

### 8.2 Use Phase 0 responsibly

Apply the shared Phase 0 rule. The proposal must name both its reviewable output and the decision it unlocks; otherwise treat the work as mobilization.

### 8.3 Define each phase

Use the shared minimum phase definition. Add two M2-specific fields:

- `Why separate` — the boundary, uncertainty, dependency, or gate that justifies a distinct phase;
- `Conditionality` — mandatory, optional, gated, pilot, or later-to-be-scoped.

Keep phase names short and outcome-oriented, workstreams at theme level, and outputs limited to what the phase gate needs.

Do not add pricing, detailed actions, staffing, or weekly schedules in M2.

### 8.4 Handle conditional implementation

When implementation cannot be scoped responsibly before diagnosis or design:

- define its intended purpose and dependency;
- mark it `Conditional — scope after [named gate]`;
- state which approved outputs will determine scope, duration, service depth, and commercials;
- avoid invented estimates.

## 9. Output Schemas

### 9.1 Full M2 approval package

```markdown
Artifact: M2 — Solution and Phase Architecture — vX
State: Draft | Provisional

Decision and scope
[Governing question, desired outcome, boundary, constraints]

Solution architecture
[Recommended direction, design principles, and solution components]

Traceability
| Issue/gap | Intervention logic | Intended outcome | Success evidence | Assumption |

Alternatives and recommendation
[Include only when a genuine choice exists]

Delivery topology
[Sequential phases, parallel workstreams, waves, delivery units, service depths]

High-level phases
| Phase | Objective | Why separate | Major workstreams | Principal outputs | Entry condition | Exit/gate | Conditionality |

Material risks and assumptions
[Only decision-relevant items]

Approval requested
[Approve/amend solution direction separately from phase architecture]
```

### 9.2 M2A solution-only output

```markdown
Artifact: M2A — Solution Architecture — vX
State: Draft | Provisional

Decision and design requirements
Solution principles
Solution components
Traceability
Alternatives and tradeoffs, if applicable
Recommendation and disconfirming evidence
Approval requested: approve or amend the solution direction before phasing.
```

### 9.3 M2B phase-only output

```markdown
Artifact: M2B — Phase Architecture — vX
State: Draft | Provisional
Canonical solution source: [approved artifact/version]

Delivery topology
Phase definitions
Cross-phase enablers
Dependencies and conditional elements
Approval requested: approve or amend phase names, boundaries, sequence, outputs, and gates.
```

### 9.4 Validation output

When validating an existing user solution, return:

```markdown
What is coherent and supportable
Traceability or topology gaps
Elements misclassified as phases/workstreams/waves
Material tradeoffs or assumptions not yet visible
Recommended corrections
Approval decision required
```

Do not rewrite sound content merely to impose this module's wording.

## 10. Archetype Adaptation Rules

### 10.1 Gated decision study

Use when management must first decide whether to proceed. The first phase should reduce the uncertainty that controls the Go/No-Go decision. Any later strategy, design, or implementation phase is conditional on that gate.

### 10.2 Transformation lifecycle

Diagnosis, target-state design, and implementation may be appropriate, but they are not automatic. Split internal and external diagnosis only when they require different evidence, produce independently useful outputs, or support separate decisions.

### 10.3 Strategy-to-operating-model

Keep strategic analysis, strategic choices, and operating-model design distinct when each produces a separate decision. Do not begin detailed operating design before strategic choices and design principles are stable.

### 10.4 Multi-entity program

Separate group-level topics from entity-specific topics. Use parallel tracks or waves where entities receive similar services at different priorities or depths. Define program-level governance and gates without pretending every entity is in the same condition.

## 11. Review Protocol

### 11.1 Traceability review

- Every solution component addresses an approved gap, constraint, or outcome.
- No material gap is left without a response or explicit exclusion.
- No component exists only because a framework contains it.
- Intended outcomes have plausible success evidence.

### 11.2 Recommendation review

- Alternatives are genuinely different when included.
- Criteria reflect the decision rather than favoring a predetermined answer.
- Tradeoffs, exclusions, and disconfirming evidence are visible.
- Client capability, sponsorship, politics, and resource constraints are considered.

### 11.3 Topology review

- Phases, workstreams, waves, delivery units, and service depth are not conflated.
- Parallel work is not presented as false sequence.
- Entity-specific conditions are not generalized to the group.
- Cross-cutting enablers are not forced into standalone phases without a gate.

### 11.4 Phase review

- Each phase has one primary objective and a justified boundary.
- Entry conditions and dependencies support the proposed order.
- Principal outputs enable the exit gate.
- Conditional phases visibly state their condition.
- Phase definitions remain high-level enough for M3 to add service detail.
- No unsupported duration, price, staffing, or benefit claim appears.

### 11.5 Redundancy review

Keep one canonical home:

- approved problem basis -> M1A;
- solution direction and phase boundaries -> M2;
- activities, deliverables, timing, and commercials -> M3;
- detailed phase methods and actions -> M4.

Reference upstream artifacts instead of copying their full narrative.

## 12. Approval and Handoff

Request explicit approval of two decision objects:

1. **Solution direction:** components, logic, tradeoffs, exclusions, and assumptions.
2. **Phase architecture:** topology, phase names, boundaries, sequence, major outputs, dependencies, and gates.

If only one object is approved, keep the other open. Do not proceed to M3 until phase architecture is explicitly approved.

Present a concrete review choice rather than asking a vague “What do you think?”:

- approve both objects;
- approve the solution direction and revise the phase architecture;
- revise the solution direction before phasing;
- mark specific inputs as required before approval.

The approved M2 handoff to M3 contains:

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

Send only a concise approved M2 summary back to M1B. Do not send the detailed approval package into the executive summary.

## 13. Acceptance Tests

Module 2 passes only if it can:

1. develop a solution from an approved M1A without rewriting the diagnosis;
2. compare genuine options without inventing quantitative scores;
3. recommend a direction while exposing tradeoffs and disconfirming evidence;
4. choose a fitting framework without creating framework salad;
5. separate a sequential phase from a parallel workstream and an entity wave;
6. create a justified Go/No-Go gate for a decision study;
7. use Phase 0 only for a real validation or scoping output;
8. keep implementation conditional when responsible scoping depends on earlier outputs;
9. validate a user-supplied phase model without rewriting sound content;
10. stop after solution/phase approval and avoid producing M3 or M4 detail.
