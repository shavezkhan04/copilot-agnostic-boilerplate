# Auto-Orchestration Prompt Template

Use this macro-prompt when a broad feature request arrives and the AI should automatically sequence through the project personas.

## Template

```text
Project context:
- Repository root: /home/shavez/my-git-repos/copilot-agnostic-boilerplate
- Working structure: src/, tests/, docs/, .copilot/
- Project conventions: kebab-case for files/directories, PascalCase for system components, uppercase snake_case for env vars

Task:
<Describe the broad feature, change request, or bug fix here>

Execution protocol:
1. Start as the Project Architect Agent.
2. Analyze the request for system boundaries, architecture constraints, and regression risk.
3. Produce a concise design summary with assumptions, key interfaces, and risks.
4. Hand off to the Project Developer Agent.
5. Implement the required code and maintain the project structure and naming conventions.
6. Hand off to the Project QA Agent.
7. Define edge-case scenarios, write or update assertions/tests, and validate against acceptance criteria.
8. After completion, update /docs/memory_bank.md with:
   - Current Focus
   - Active Tasks
   - Architectural Decisions made
   - Technical Debt log

Deliverables:
- Architecture notes
- Implementation summary
- Test or validation results
- Memory bank update

Constraints:
- Keep changes aligned with project conventions
- Prefer clarity, maintainability, and explicit boundaries
- Avoid hidden coupling or framework-specific assumptions
- If a decision requires trade-offs, document them clearly in the memory bank
```

## Example

```text
Project context:
- Repository root: /home/shavez/my-git-repos/copilot-agnostic-boilerplate
- Working structure: src/, tests/, docs/, .copilot/
- Project conventions: kebab-case for files/directories, PascalCase for system components, uppercase snake_case for env vars

Task:
Add a lightweight notification workflow that accepts a user event, validates input, emits an event to an integration boundary, and records the action in the application state.

Execution protocol:
1. Start as the Project Architect Agent.
2. Analyze the request for system boundaries, architecture constraints, and regression risk.
3. Produce a concise design summary with assumptions, key interfaces, and risks.
4. Hand off to the Project Developer Agent.
5. Implement the required code and maintain the project structure and naming conventions.
6. Hand off to the Project QA Agent.
7. Define edge-case scenarios, write or update assertions/tests, and validate against acceptance criteria.
8. After completion, update /docs/memory_bank.md with:
   - Current Focus
   - Active Tasks
   - Architectural Decisions made
   - Technical Debt log

Deliverables:
- Architecture notes
- Implementation summary
- Test or validation results
- Memory bank update

Constraints:
- Keep changes aligned with project conventions
- Prefer clarity, maintainability, and explicit boundaries
- Avoid hidden coupling or framework-specific assumptions
- If a decision requires trade-offs, document them clearly in the memory bank
```
