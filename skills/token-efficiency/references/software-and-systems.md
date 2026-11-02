# Software, debugging and system work

- Inspect relevant entry points, interfaces, dependencies and existing commands. Use filenames, symbol searches, diffs and focused logs before broad file reads. Read enough context to preserve invariants.
- Reproduce or characterize the issue with the smallest informative check. Retain exact failures and changed inputs; diagnose repeated failures rather than rerunning an unchanged approach.
- Patch the affected implementation and its dependents. Reuse existing utilities, environments and dependencies when appropriate; avoid unrelated refactors and full-file rewrites.
- Validate the changed behavior with meaningful targeted checks and required project checks. Broaden testing for shared or unresolved effects, not by habit after relevant checks already pass.
- For file/system operations, inspect only the necessary scope and metadata. Use native platform commands, verify target paths and permissions, and preserve recoverable evidence. Efficiency does not expand authorization for destructive or external actions.
- Keep command output compact while preserving error details and exit status. Use asynchronous completion where supported and avoid tight status loops.
- Deliver the working change, script or requested findings with concise validation evidence and any actual unresolved limitation.
