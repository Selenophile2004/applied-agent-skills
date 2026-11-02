# Data, spreadsheets and BI

- Inspect schemas, sheet/table names, dimensions, headers, types, keys and relevant relationships first. Use representative records for discovery; compute final results over the complete relevant dataset unless sampling is intentional, appropriate and disclosed.
- Resolve columns by verified names rather than old positions. Preserve joins, identifiers, locale/calendar meaning, filters, signs, currencies and unit scales. Distinguish missing values, zeroes, estimates and actuals.
- Run joins, aggregations, reconciliation and error scans in the runtime or data engine. Return control totals, coverage, affected-record counts, mismatches and source locations. Keep detailed diagnostics in a reusable file when useful.
- Patch affected formulas/ranges and recalculate their dependencies with a supported engine. Check formula errors and control totals; retain unaffected data and structure. Do not rebuild an entire workbook for a local repair without a concrete need.
- For BI work, inspect relevant measures, visuals, relationships, interactions, bookmarks and access/filter semantics. Reuse the established model and design; batch supported metadata operations rather than repeatedly enumerating everything.
- Reuse unchanged exports and previews. Verify data, structure and affected visual behavior as required by the task and authoring skill; broaden checks when shared dependencies change.
- Distinguish offline/package checks from live application or query-engine verification. Token economy does not justify trusting sampled control totals, weakening access checks or skipping necessary recalculation.
