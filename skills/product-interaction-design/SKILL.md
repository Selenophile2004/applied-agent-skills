---
name: product-interaction-design
description: "Design user flows and interaction states for web products, dashboards, agents and workflow tools."
---

# Product Interaction Design

Design how people complete tasks in products, dashboards, agents and workflow tools. Use the actual data, permission and execution model where available. Label assumptions when the implementation is unknown.

## Flow and state model

1. Identify actor, goal, entry condition, permissions, decision points and successful exit. Map the primary flow and the highest-impact recovery path. Check which choices need context before commitment.
2. Specify a state matrix with surface, state, trigger, visible status, available actions, next state and recovery. Include applicable loading, empty, partial, stale, denied, approval, failure and cancellation states. Distinguish a first-use empty state, filtered no-results and a load failure when they require different actions.
3. For async work, separate queued, running, waiting, succeeded and failed. Map the displayed state to the actual case or run ID and step. Define retry, resume, cancellation and confirmation according to the product's real capabilities. Show what was saved, what may run again and where the user can find the result. Handle duplicate submission and stale responses where relevant.
4. Specify concise copy, focus transitions, keyboard behavior and status announcements for critical actions. Check narrow layouts, text expansion, locale and RTL. Use existing component patterns where they meet the interaction need.
5. Prototype and inspect the primary flow and one important recovery path when the deliverable calls for a prototype. Verify the expected visible state, action availability and navigation or focus destination. Identify states that are only specified or simulated.

## Deliver

Provide the flow, state matrix, critical copy and acceptance cases. For each acceptance case state the starting state, event, expected visible change and resulting action or state. Example: a failed export shows its run reference and saved configuration, offers the permitted recovery action and returns focus to the result once completion is announced. Use the example only where the backend supports that recovery.
