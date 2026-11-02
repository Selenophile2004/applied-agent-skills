# Consulting Proposal Content Development — Module Contract

## 1. Purpose

This contract defines how Codex develops management-consulting proposal content before slide production. It supports a complete proposal workflow and selective work on one section, one module, or any requested combination of modules.

The contract separates content development from presentation production:

- This skill develops, challenges, revises, and approves proposal content.
- `consulting-proposal-writing` turns approved content into an answer-first storyline and slide manifest.
- `persian-landscape-proposals` implements the approved manifest in the user-supplied PowerPoint template.

Do not begin PowerPoint production merely because proposal content exists. Use the presentation skill only when the user explicitly requests slide implementation.

## 2. Governing Principles

1. **Decision first.** Define the decision the proposal must support, the audience, desired outcome, scope, constraints, and success criteria before adding content.
2. **Consultant in the loop.** Codex proposes and challenges; the consultant approves or redirects at explicit gates.
3. **Evidence before certainty.** Separate verified facts, user-supplied claims, analysis, inference, assumptions, recommendations, and missing inputs.
4. **Frameworks serve the problem.** Select a framework only when it improves diagnosis, design, or delivery. Never force a fashionable framework onto every project.
5. **No framework salad.** Prefer one primary logic and only the minimum supporting lenses required to close material gaps.
6. **No arbitrary phase count.** The number and boundaries of phases must follow dependencies, risk, learning, ownership, capability, resources, and acceptance gates.
7. **One canonical source.** Each substantive idea has one authoritative module. Other modules may summarize it but must not independently recreate it.
8. **Selective generation.** Produce only the modules or subsections explicitly requested. Use other proposal material as context without rewriting it.
9. **No invented commitments.** Never fabricate dates, prices, staffing, client facts, quantified impact, credentials, methods, or deliverables.
10. **Approval controls progression.** Do not silently move from a draft solution to execution details or slide production.

## 3. Invocation Contract

The user may request:

- the complete workflow;
- one module only;
- selected modules in any sensible combination;
- one or more named subsections;
- revision of an existing proposal section;
- continuation from an already approved upstream artifact.

Interpret natural-language requests without requiring exact command syntax. When useful, the user may invoke the future skill as:

```text
Use $consulting-proposal-content.
Create Module 2 only for [project]. Use the attached proposal as context. Stop after the approval gate.
```

Or:

```text
Use $consulting-proposal-content.
Revise only the Current Situation and Consequences subsections of Module 1. Do not change the rest of the proposal.
```

Mandatory selective-generation rule:

> Produce only explicitly requested modules or subsections. Treat unrequested proposal content as context. Do not regenerate, rewrite, or expand it unless a dependency must be surfaced for approval.

If a requested module depends on an absent upstream decision, do not generate false certainty. Choose one of these responses:

1. use an approved input supplied by the user;
2. mark the dependent content `Provisional — pending consultant approval`;
3. request the smallest decision-critical input;
4. recommend running the missing upstream module.

Do not require the user to repeat information already available in the conversation or supplied files.

## 4. Shared Input Envelope

Before drafting, identify the minimum available context:

- organization and relevant history;
- project trigger and decision to be made;
- current situation, strengths, constraints, and evidence;
- affected stakeholders and organizational boundary;
- desired outcomes and success criteria;
- known scope, exclusions, timing, budget, and resource constraints;
- existing solution decisions or approved phases;
- relevant methods, standards, or mandated frameworks;
- output language, depth, and audience;
- existing proposal sections that must remain unchanged.

Do not turn this list into a long questionnaire. Ask only consolidated, high-impact questions whose answers could materially change the recommendation. Continue with explicitly labeled assumptions when reasonable.

## 5. Evidence and Status Model

### 5.1 Evidence labels

Use these internal labels while reasoning and make them visible when trust or approval requires it:

- `Verified project fact`
- `User-supplied evidence`
- `Authoritative external evidence`
- `Consultant/client analysis`
- `Inference`
- `Assumption`
- `Recommendation`
- `Missing input`

External research is not automatic. Use it when the user requests it or when current, source-sensitive facts are necessary. Cite sources close to the supported claim.

### 5.2 Artifact states

Every material module output has one state:

- `Draft` — prepared for review and still changeable.
- `Provisional` — usable for discussion but dependent on an unresolved input or approval.
- `Approved` — explicitly accepted by the consultant for downstream use.
- `Superseded` — replaced by a later named version.
- `Input Required` — responsible drafting cannot continue without a decision-critical input.

Approval applies only to the named artifact or version. A downstream revision does not retroactively alter the approved upstream artifact.

## 6. Core Taxonomy

Keep these concepts distinct:

- **Symptom:** an observable effect of a deeper problem.
- **Problem:** the decision-relevant gap between current and desired state.
- **Cause:** a factor that explains the problem; causal confidence must match evidence.
- **Consequence:** an effect of the current situation or of inaction.
- **Solution:** an intervention intended to close a defined gap.
- **Phase:** a bounded, usually sequential unit with an objective, entry conditions, outputs, dependencies, and an exit or approval gate.
- **Wave:** a time-bounded rollout or delivery grouping applied to different entities, locations, capabilities, or releases; waves may repeat similar work rather than represent different objectives.
- **Workstream:** a coherent theme of work that may run across multiple phases.
- **Delivery unit:** the organizational location receiving the service, such as a group, holding, subsidiary, business unit, function, or site.
- **Service depth:** the agreed level of involvement, such as strategic guidance, full design, implementation support, or hands-on delivery.
- **Activity:** work performed to produce an output.
- **Deliverable:** a tangible or reviewable artifact handed over or accepted.
- **Outcome:** the operational or business change enabled by deliverables.
- **Milestone:** a meaningful event or decision point; it is not automatically a deliverable.
- **Acceptance criterion:** the observable condition used to accept an output or close a phase.

Never present causes, symptoms, actions, owners, deliverables, and metrics as if they were peers at the same logical level.

### 6.1 Service hierarchy

Use the shallowest hierarchy that keeps scope unambiguous:

```text
Engagement -> phase or wave -> delivery unit -> workstream/service category
  -> main service activity -> executable action -> deliverable
  -> expected outcome -> acceptance criterion
```

Do not force every level into a simple engagement.

## 7. Dependency and Approval Flow

The default full workflow is:

```text
M1A: Organization context + current situation + consequences
  -> explicit situation/problem approval
M2: Solution direction + high-level phases
  -> explicit solution/phase approval
M1B: Insert a concise summary of approved M2 into the Executive Summary
M3: Execution-phase master table
  -> explicit table approval
M4: Selected phase deep dives, only where needed
  -> explicit phase-detail approval
Storyline/slide manifest
  -> PowerPoint implementation, only if requested
```

Module 1 is therefore assembled in two logical passes when no approved solution exists. This avoids independently inventing a solution summary in Module 1 and then producing a different solution in Module 2.

If the user provides an already approved solution and phases, M2 may be treated as satisfied. Record the supplied artifact as the canonical source and proceed only with requested downstream modules.

## 8. Module Registry

| Module | Primary decision | Required output | Canonical authority | Default gate |
|---|---|---|---|---|
| M1 — Executive/Management Summary | Do stakeholders agree on the situation, implications, and proposed direction? | Concise executive narrative | Situation and consequences; solution summary is inherited from M2 | Explicit approval of Sections 1–3; M2 approval controls final solution text |
| M2 — Solution and Phase Approval | What solution architecture and phase logic should be approved? | Recommended solution and high-level phases | Solution direction, phase boundaries, and rationale | Explicit solution/phase approval |
| M3 — Execution-Phase Master Table | What will be done, delivered, accepted, and when at a high level? | Table first, then only requested explanation | Execution scope and high-level delivery commitments | Explicit master-table approval |
| M4 — Phase Deep Dive | What exactly occurs inside selected phases? | Detailed content for selected phase(s) | Sub-stages, activities, methods, roles, detailed outputs, and gates | Explicit phase-detail approval |

### 8.1 Engagement archetype and delivery topology

Before drafting M2, identify the best-fitting engagement archetype:

- gated decision study;
- transformation lifecycle;
- strategy-to-operating-model design;
- multi-entity or multi-business program;
- another domain-specific archetype justified by the decision.

Then identify the delivery topology:

- sequential phases;
- parallel workstreams;
- entity or rollout waves;
- a hybrid of these.

Keep four scope dimensions separate when they exist: delivery unit, service subject, service depth, and time. Do not collapse a multi-entity matrix into an artificial phase sequence.

## 9. Module 1 — Executive/Management Summary

### 9.1 Purpose

Create a compact, decision-oriented summary that explains the organization context, current position, implications, and approved direction. It is not a table of contents and not a generic company profile.

### 9.2 Required sections

1. **Organization introduction and relevant history**
   - Describe only context relevant to the project decision.
   - Connect history to the current mandate, capability, market position, or transformation need.
   - Avoid promotional biography and unrelated chronology.

2. **Current situation and position**
   - Present both strengths/enablers and weaknesses/constraints.
   - Distinguish evidence from interpretation.
   - Explain the gap between current and desired state.

3. **Consequences and implications**
   - State operational, financial, strategic, organizational, customer, regulatory, or capability consequences only when supported.
   - Distinguish observed effects from future risks.
   - Explain the cost or risk of inaction without unsupported alarmism.

4. **Proposed solution and phases**
   - Summarize the approved M2 outcome at executive level.
   - Preserve M2 phase names, sequence, boundaries, and intended outcomes.
   - Do not add activities or promises not approved in M2.

### 9.2.1 Decision-brief variant

For market-entry, investment, feasibility, or other gated decisions, M1 may use this compact structure instead:

```text
Current situation -> management complexity or risk -> explicit decision questions -> gated approach
```

Use this variant only when the immediate objective is to decide whether or how to proceed. Do not force a full historical introduction when it does not affect the decision. Any “Why this consultant” or credentials content is optional and must remain separate from the situation diagnosis.

### 9.3 Dependency behavior

If M2 is not approved, either omit Section 4 or label it:

`Provisional solution direction — pending consultant approval`

Do not present provisional phase logic as final. If the user requests only Sections 1–3, produce only those sections.

Approve Sections 1–3 as the situation/problem basis before using them to design M2. Later insertion of the approved M2 summary into Section 4 does not reopen Sections 1–3 unless the solution work exposes a material contradiction or missing fact.

### 9.4 Quality test

The summary must let a senior reader answer: What organization and decision is this about? What is working? What is not? Why does it matter now? What direction has been approved?

## 10. Module 2 — Solution and Phase Approval

### 10.1 Purpose

Develop and obtain approval for the solution architecture and its high-level execution phases before detailed service design.

### 10.2 Required reasoning sequence

1. Restate the decision question and desired outcomes.
2. Confirm the critical problem, gap, causes or design constraints.
3. Create traceability:

```text
Issue or gap -> intervention logic -> expected outcome -> success evidence
```

4. Generate genuine alternatives only when a real choice exists.
5. Recommend a direction and state rationale, tradeoffs, risks, assumptions, and disconfirming evidence.
6. Convert the recommended direction into justified phases.
7. Stop for explicit consultant approval.

### 10.3 Phase-boundary tests

Create a distinct phase only when at least one material boundary exists:

- a prerequisite or irreversible dependency;
- a need to reduce uncertainty before committing further resources;
- a different primary objective, owner, capability, or resource profile;
- a pilot, validation, or design gate before rollout or scale;
- a risk-containment or regulatory gate;
- a separately acceptable output or decision;
- a meaningful transition from diagnosis to design, design to build, or build to adoption.

A `Phase 0` may be used for scoping, validation, baseline assessment, or risk reduction only when it produces a defined output and a real decision gate. Do not use Phase 0 as a label for ordinary project mobilization.

Do not create phases merely to fit a three-step template. Do not mislabel parallel workstreams as sequential phases.

Implementation may remain conditional, unpriced, or defined only at a high level when responsible scoping depends on approved diagnostic or design outputs. State the condition and later scoping decision explicitly.

### 10.4 Minimum phase definition

Each proposed phase must contain:

- phase name;
- objective;
- problem or dependency addressed;
- scope boundary;
- major workstreams or intervention themes;
- principal outputs;
- expected outcome;
- entry conditions;
- dependencies and assumptions;
- exit or approval gate;
- indicative duration only when supported.

### 10.5 Approval object

Ask the consultant to approve or amend the following as one named version:

- solution direction;
- phase names and sequence;
- phase objectives and boundaries;
- major dependencies;
- principal outputs and exit gates;
- unresolved assumptions.

Do not proceed to M3 merely because the consultant approved the general idea while disputing phase boundaries.

## 11. Module 3 — Execution-Phase Master Table

### 11.1 Purpose

Translate the approved M2 structure into an executive-level delivery table. Present the table first. Add narrative explanation only when the user requests it or when a material ambiguity cannot be resolved inside the table.

### 11.2 Default columns

Use only columns that add decision value. The default set is:

| Column | Required content |
|---|---|
| Phase | Approved M2 phase name and number |
| Delivery unit / entity | Group, subsidiary, business unit, function, site, or other recipient when scope spans several units |
| Service category / workstream | Coherent delivery theme, not a duplicate phase |
| Service depth | Optional involvement level when different units or topics receive different depths |
| Objective | Change or decision the phase must enable |
| Main activities / actions | Verbs describing material work |
| Deliverables | Tangible or reviewable outputs |
| Expected outcome | Operational or business change enabled |
| Client role / input | Required decisions, access, data, participation, or ownership |
| Dependencies / assumptions | Conditions that affect feasibility or sequence |
| Indicative duration | Range or estimate only when evidence supports it |
| Exit / acceptance criteria | Observable condition for phase closure |

Optional columns include consultant role, milestones, governance forum, owner, pricing, or payment terms. Add commercial columns only when explicitly requested and backed by verified inputs. Never infer a fee from examples.

Add a `Conditional / option` field when a downstream phase, price, or duration depends on a prior gate. A schedule or Gantt view may be produced only after activities, dependencies, and durations are approved; it must not introduce new scope.

### 11.3 Cross-phase enablers

Governance, benefits tracking, KPIs, reporting, risk management, capacity management, change management, communications, and knowledge transfer often span several phases. Represent them as cross-phase workstreams or enabling layers unless a true phase boundary exists.

The service-depth lens may use concepts such as `Strategic Guide`, `Full Design`, and `Hands-on Implementation` when useful, but it is optional and must reflect the actual engagement model.

### 11.4 Table quality tests

- Every activity supports a phase objective.
- Every deliverable results from named activities.
- Every outcome is enabled by deliverables and is not merely a renamed deliverable.
- Client inputs and decisions are visible.
- Dependencies are consistent with sequence.
- Exit criteria are observable.
- No row silently expands approved scope.
- Similar rows use parallel grammar and comparable depth.

## 12. Module 4 — Phase Deep Dive

### 12.1 Purpose

Develop detailed content only for selected phases whose delivery logic needs clarification. M4 is optional; not every proposal or phase needs a deep dive.

### 12.2 Selection rule

Prioritize a deep dive when a phase is high risk, high value, unfamiliar, method-sensitive, dependent on client participation, commercially material, or too complex for the master table.

### 12.3 Default content for each selected phase

- phase objective and decision supported;
- entry conditions and inputs;
- sub-stages, if genuine;
- service categories or workstreams;
- main activities and executable actions;
- methods, tools, or frameworks and why they fit;
- deliverables and expected outcomes;
- consultant and client roles;
- dependencies and decision points;
- milestones and acceptance criteria;
- risks, assumptions, and mitigations;
- indicative duration, if supported;
- exit gate and handoff to the next phase.

Create a sub-stage only when it has a distinct objective, method, output, dependency, owner, or approval gate. Do not turn every task into a sub-stage.

M4 supports two detail modes:

1. **Delivery detail:** service categories, activities, actions, roles, deliverables, outcomes, dependencies, and gates.
2. **Method detail:** analytical question, selected framework or method, required inputs, analytical steps, expected evidence, limitations, and example output type.

Use method detail only when it helps evaluate how the engagement will answer a material question. A framework name alone is not a method description.

### 12.4 Slide-readiness rule

Detailed content may later be distributed across several slides, but slide boundaries are determined by a distinct message or decision—not by the mere existence of a task list. M4 remains content-first; presentation layout belongs to the downstream slide workflow.

## 13. Framework Selection Engine

Framework selection is an internal design decision unless the user asks to show the method. Record the chosen framework, the reason for choosing it, and any limitations. Do not clutter client-facing output with framework names when the underlying logic is sufficient.

### 13.1 Selection sequence

1. Define the decision and problem type.
2. Identify what is unknown: causes, options, operating design, execution sequence, stakeholder adoption, governance, or benefits.
3. Choose the lightest framework that resolves that uncertainty.
4. Adapt it to organization context and available evidence.
5. Test whether it changes a decision or materially improves completeness.
6. Remove it if it adds labels but no insight.

### 13.2 Framework map

| Need | Candidate lenses | Use condition |
|---|---|---|
| Problem decomposition | Issue Tree, MECE | The problem mixes symptoms, causes, decisions, and actions |
| Organization diagnosis | McKinsey 7S, operating-model dimensions | Alignment across strategy, structure, systems, skills, staff, style, or shared values matters |
| Process improvement | SIPOC, value-stream/process mapping, Lean lenses | Handoffs, waste, controls, or process ownership drive the gap |
| Strategic choices | Scenario analysis, option matrix, portfolio logic | There are genuine alternatives and explicit tradeoffs |
| Decision rights | RACI, RAPID | Ambiguous roles or slow decisions threaten execution |
| Delivery sequencing | Stage-Gate, dependency roadmap, pilot-to-scale | Risk, learning, validation, or prerequisites justify gates |
| Change and adoption | ADKAR, Kotter, stakeholder/change-impact analysis | Behavior, sponsorship, capability, or adoption is critical |
| Benefits realization | KPI tree, benefits map, baseline-target-owner cadence | Value must be measured and sustained after delivery |
| Program governance | Workstreams, governance forums, RAID, milestone/decision cadence | Multiple teams, dependencies, risks, and decisions require coordination |

These are candidates, not a mandatory catalog. Other domain-specific or user-mandated frameworks may be used when they fit better.

### 13.3 Framework safeguards

- A framework never substitutes for evidence.
- A branded framework name never proves the recommendation.
- Use MECE where categories need completeness; do not suppress weak signals merely to force clean boxes.
- Use RACI/RAPID only after work and decisions are defined.
- Use change frameworks only when adoption is in scope.
- Use Stage-Gate only when gates represent real decisions or risk reduction.
- State causal claims cautiously when evidence is correlational or incomplete.

## 14. Partial-Request Scenarios

### Scenario A — Module 1 only, with approved solution

Use the approved solution artifact as the source for Section 4. Generate M1 only and leave all other proposal sections untouched.

### Scenario B — Module 1 only, without approved solution

Generate Sections 1–3. Omit Section 4 or make it explicitly provisional. Recommend M2 as the approval route; do not fabricate final phases.

### Scenario C — Module 2 only

Use the supplied diagnosis or existing proposal as context. Produce solution and phase logic only. Stop after the M2 approval request.

### Scenario D — Module 3 only

Confirm that an approved solution/phase structure exists. If it does, create the master table without rewriting M1 or M2. If it does not, mark the table provisional or recommend M2.

### Scenario E — One phase from Module 4

Deep-dive only the named phase. Preserve approved M2/M3 scope and terminology. Do not expand other phases.

### Scenario F — Two nonadjacent modules

Generate only the requested modules. Surface any dependency between them, but do not fill the intervening module unless the user approves that expansion.

### Scenario G — Existing user-authored proposal

Treat all unrequested sections as protected context. Identify contradictions that affect the requested section, but do not silently rewrite them.

## 15. Approval Protocol

At every gate, present:

1. the named artifact and version;
2. its current state;
3. the decision requested from the consultant;
4. material assumptions or unresolved items;
5. the next module that approval would unlock.

Accept clear natural-language approvals such as “approved,” “continue,” or an explicit instruction to proceed. If the user requests revisions, keep the gate open and issue a revised version. Do not repeatedly ask for approval after the user has already given it for the named version.

## 16. Handoff to Storyline and PowerPoint

Only approved content is eligible for final slide production. The handoff package should contain:

- approved module versions;
- audience and decision;
- core message and implications;
- evidence/assumption notes that must remain visible;
- canonical phase names and terminology;
- suggested slide purposes, not preselected layouts;
- tables or diagrams that must be preserved semantically;
- unresolved inputs that prohibit final claims.

Use `consulting-proposal-writing` to create the answer-first narrative and slide manifest. Then, if explicitly requested, use `persian-landscape-proposals` to select existing layouts, preserve slide-master elements, logos, fonts, RTL behavior, theme, and editable structure.

Content approval does not equal design approval, and slide implementation must not alter the approved meaning to fit a layout.

## 17. Quality Gates

### Logic gate

- The decision question is clear.
- The structure is collectively sufficient and minimally overlapping where MECE matters.
- Symptoms, causes, consequences, interventions, outputs, and outcomes remain distinct.
- Recommendation and phases follow from the diagnosis.
- Phase sequence follows real dependencies and gates.

### Evidence gate

- Material claims have a known evidence status.
- Facts, inferences, assumptions, and recommendations are distinguishable.
- Quantified impact, dates, prices, staffing, and credentials are not invented.
- Uncertainty is visible where it could change a decision.

### Execution gate

- Every phase has a purpose, boundary, output, dependency, and exit condition.
- Workstreams are not confused with phases.
- Activities, deliverables, outcomes, owners, and acceptance criteria are traceable.
- Client inputs and decision rights are explicit.
- Change, governance, and benefits are included only to the depth needed.

### Editorial gate

- Language is concise, parallel, and audience-appropriate.
- Each section has one primary purpose.
- Repeated content is replaced by a reference or short summary from the canonical module.
- Persian and English terminology is consistent when bilingual wording is required.

### Independent-reader gate

- A reader without the drafting conversation can understand the problem, implications, recommendation, and requested decision.
- The reader can distinguish what is known, proposed, pending, and approved.
- The output can be handed to the storyline and PowerPoint skills without reconstructing missing logic.

## 18. Acceptance Tests for the Future Skill

The implemented skill is acceptable only if it can pass all of these tests:

1. Generate only the current-situation subsection without rewriting the rest of M1.
2. Produce M1 Sections 1–3 when no solution is approved and avoid presenting invented final phases.
3. Develop M2, stop at the solution/phase gate, and resume after explicit approval.
4. Produce M3 from a supplied approved phase structure without regenerating M1 or M2.
5. Deep-dive only one named phase while preserving approved boundaries.
6. Support two requested modules without automatically generating the others.
7. Preserve an existing user-authored proposal outside the requested section.
8. Select and justify a fitting execution framework without defaulting to a fixed framework stack.
9. Refuse to invent commercials, timing, staffing, or evidence.
10. Hand off approved content to the separate storyline and PowerPoint skills without duplicating their responsibilities.

## 19. Token-Efficiency Rules

- Keep shared runtime rules compact in `SKILL.md`; use this contract for full multi-module orchestration, dependency disputes, audits, or skill maintenance.
- Store module-specific instructions only in the corresponding module file.
- For a normal single-module request, load only `SKILL.md` and the selected module reference; do not load this contract.
- For a full workflow, load this contract once and load each module reference only when its approval gate is reached.
- Summarize canonical upstream content instead of copying it in full.
- Do not repeat evidence, assumptions, terminology, or approval history in multiple sections; reference the source artifact and version.
- Prefer compact tables for repeated fields and prose for reasoning that would be obscured by a table.
