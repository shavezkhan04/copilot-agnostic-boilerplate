# Memory Synchronization Prompt Template

Use this template after closing a feature, resolving a critical bug, or handing off work to ensure the project memory reflects the latest state.

## Template

```text
Run a workspace audit across the repository and update /docs/memory_bank.md with the current project state.

Review:
- current feature or bug-fix status
- changed files and impacted areas
- architecture decisions made or revised
- active tasks and any blockers
- technical debt introduced or resolved

Required output:
1. Summarize the current focus
2. Update the Active Tasks section with verified status
3. Record any Architectural Decisions made
4. Add or revise items in the Technical Debt log
5. Note any remaining risks or follow-up tasks

Scope:
- confirm whether the feature or bug fix is complete
- identify any missing validations
- call out untested edge cases or assumptions
- ensure the memory bank is the single source of truth for delivery state

Final instruction:
Write the result directly into /docs/memory_bank.md in a concise, structured format.
```

## Example: Critical Bug Fix

```text
Run a workspace audit across the repository and update /docs/memory_bank.md with the current project state.

Review:
- current bug-fix status for the failing path in <component_or_module>
- changed files and impacted areas
- architecture decisions made or revised due to the fix
- active tasks and any blockers
- technical debt introduced or resolved

Required output:
1. Summarize the current focus
2. Update the Active Tasks section with verified status
3. Record any Architectural Decisions made
4. Add or revise items in the Technical Debt log
5. Note any remaining risks or follow-up tasks

Scope:
- confirm whether the bug fix is complete
- identify any missing validations
- call out untested edge cases or assumptions
- ensure the memory bank is the single source of truth for delivery state

Final instruction:
Write the result directly into /docs/memory_bank.md in a concise, structured format.
```
