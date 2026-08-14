# Explicit Agent Call Templates

Use these small, direct prompt patterns to summon a single agent with a clear mandate.

## Architect Agent

```text
Project Architect Agent: Review the current system structure and identify the design boundary for <feature_or_change>. Assess architecture risks, decoupling concerns, and regression impacts. Provide a concise recommendation and any schema or interface changes needed.
```

## Developer Agent

```text
Project Developer Agent: Implement <feature_or_fix> in the existing project structure using kebab-case file names, PascalCase system components, and clean self-documenting code. Keep the change aligned with the current architecture and document any assumptions.
```

## QA Agent

```text
Project QA Agent: Write focused unit tests for <interface_or_behavior>. Cover happy path, invalid input, and edge cases. Provide assertions, validation logic, and a brief acceptance criteria summary.
```

## QA Agent - Regression Validation

```text
Project QA Agent: Validate the regression risk around <change_area>. Identify likely edge cases, write exhaustive assertions, and summarize the acceptance criteria and gaps before final signoff.
```

## Developer Agent - Bug Fix

```text
Project Developer Agent: Fix the bug in <module_or_component> with the smallest safe change. Preserve project conventions, update relevant documentation if needed, and explain the root cause and fix in plain language.
```
