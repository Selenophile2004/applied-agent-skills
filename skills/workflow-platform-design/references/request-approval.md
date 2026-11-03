# Request and approval example

Use this example to check separation of business state, execution state and artifact version. Adapt states to the project.

## Model

- Request R belongs to workspace W. Its current content version is V.
- Decision D records R, V, reviewer, time, outcome and reason.
- Run J records R, V, execution state and a link to its retry or predecessor where applicable.
- Audit event records the actor, operation, state change and correlation ID. Store references to sensitive artifacts instead of copying their contents into audit logs.

## Example transitions

| Before | Trigger | Condition | After | Effect |
|---|---|---|---|---|
| Draft V1 | Submit | Owner can submit | In review V1 | Create review work item |
| In review V1 | Approve | Reviewer is authorized and submitted version is still V1 | Approved V1 | Record D for V1 |
| Approved V1 | Start delivery | Caller can execute V1 | Approved V1, run queued | Create a scoped run |
| Approved V1, run failed | Resume | Recovery allowed and completed effects verified | Approved V1, run recovering | Resume eligible steps |
| Approved V1 | Edit material content | Actor can revise | Draft V2 | Preserve V1 history and require review for V2 |

Use optimistic versions, transactional updates or an equivalent mechanism to enforce transition preconditions. A stale reviewer must receive a recoverable conflict. A run failure updates the run and surfaces recovery options while preserving the prior decision.

## Acceptance scenarios

- A reviewer sees and approves the submitted version. The next screen shows the decision and actor.
- An older approval request cannot approve newly edited content.
- A user from another workspace is denied at the backend even if they know the request ID.
- The operator can inspect failed step evidence and run recovery only for allowed states.
- Two conflicting transitions produce a consistent final state with enough audit evidence to explain the result.
