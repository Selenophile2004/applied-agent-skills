---
name: semantic-analytics-agent
description: "Build governed analytical agents over semantic models, SQL, BI and spreadsheets, with verified metrics, access scope and reproducible answers."
---

# Semantic Analytics Agent

1. Translate the question into metric, grain, dimensions, period/calendar, filters, units and comparison. Resolve ambiguous definitions against the current metric catalog and ask only when the answer materially changes.
2. Select the authoritative semantic model or source. Enforce actual caller permissions through approved query surfaces. Verify effective identity and access behavior for the chosen BI host. Keep query actions read-only unless mutation is explicitly requested.
3. Use the correct query dialect and execute over the complete relevant data. Return aggregates, control totals, diagnostics and a recoverable query/source handle. Preserve date boundaries, units, null semantics and the distinction between zero and missing.
4. Reconcile totals or representative slices against a reference. Separate descriptive changes, candidate drivers and causal claims. In a margin-drop question, verify numerator and denominator under identical filters before attributing a driver.
5. Deliver answer, definitions, filters, units, sources, verification and limitations. For implementation, include fixture cases for ambiguous KPI, wrong date scope, missing data, denominator edge case and unauthorized rows. Power BI, SQL and Excel are supported design contexts subject to the available tools.

## Query contract

Record the metric formula or catalog identifier, aggregation behavior, model and data version, effective access scope, calendar and timezone, filters, units and query handle. Resolve additive, weighted, distinct-count and snapshot metrics according to their definitions before comparing periods or totaling slices.

Validate grain and join cardinality before aggregation. Identify fan-out, incomplete periods, stale refreshes, null and denominator behavior. Report the effective date range and whether comparisons use like-for-like coverage. Use the approved execution environment's permission model rather than assuming a generic BI role grants safe access.

For metric reconciliation and evaluation cases, read [governed analytics cases](references/applied-workflow.md).
