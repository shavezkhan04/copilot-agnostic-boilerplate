# Agent Orchestration

This document defines how the project personas collaborate and how they synchronize their work back into the project memory layer.

## Orchestration Principles

- Keep architecture decisions explicit before implementation begins.
- Keep development work scoped to the agreed structure and constraints.
- Use QA validation to confirm behavior against acceptance criteria.
- Maintain a single memory source of truth in [docs/memory_bank.md](../docs/memory_bank.md).
- Record status changes as soon as decisions, blockers, or outcomes emerge.

## Persona Interaction Flow

```text
Project Architect Agent
        |
        | 1. Defines constraints, boundaries, and interfaces
        v
Project Developer Agent
        |
        | 2. Implements features within the approved structure
        v
Project QA Agent
        |
        | 3. Validates edge cases and acceptance criteria
        v
Memory Synchronization
        |
        +--> Update Current Focus
        +--> Update Active Tasks
        +--> Update Architectural Decisions made
        +--> Update Technical Debt log
```

## Handoff Contract

Each agent handoff should include the following:

- Context summary
- Scope of work
- Key constraints or assumptions
- Decisions or blockers discovered
- Validation or verification status
- Next required action

## Execution Pattern

### Phase 1: Architecture

- Identify design constraints
- Clarify interfaces and system boundaries
- Review impact on decoupling and regression risk
- Record decisions in memory

### Phase 2: Development

- Implement within approved patterns
- Keep modules clear and self-documenting
- Respect naming conventions and project layout
- Record task progress in memory

### Phase 3: Quality Validation

- Identify edge cases and failure modes
- Validate behavior against acceptance criteria
- Capture regression evidence and risk notes
- Record QA findings in memory

## Memory Update Rules

After every significant milestone, the active agent must update the memory bank with:

- current focus and objective
- active tasks and their status
- architecture decisions or design changes
- technical debt or quality concerns

### Example sync message

```text
Agent: Project QA Agent
Scope: validation of login flow
Update:
- confirm success path and edge cases
- document failing scenario for retry path
- mark acceptance criteria as partially unmet
- next action: fix retry fallback and re-run assertions
```

## Completion Standard

The work is considered complete when:

- the architecture remains aligned with the intended system boundaries
- the implementation matches the approved structure and scope
- QA evidence confirms behavior against acceptance criteria
- the memory bank reflects the final state and any remaining risk
