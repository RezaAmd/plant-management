# AI Development Workflow

## 1. Purpose

This document defines how Claude Code contributes to the Plant Management Flutter application.

The goal is to enable efficient implementation while maintaining product, architectural, and code quality.

## 2. Roles

### Product Owner

Responsible for:

- Product direction.
- Feature priorities.
- MVP scope.
- Final product decisions.
- Approval of major UI/UX changes.

### Technical Supervisor

Responsible for:

- Architecture decisions.
- Technical standards.
- Design System.
- Code review.
- Task definition and technical approval.

### Claude Code

Responsible for:

- Code implementation.
- UI development.
- Business logic implementation.
- API integration.
- Tests.
- Bug fixing.
- Refactoring within approved boundaries.
- Reporting implementation results.

## 3. Development Workflow

Each meaningful feature follows this process:

1. Understand the requirements.
2. Inspect relevant existing code and documentation.
3. Identify dependencies and risks.
4. Prepare an implementation plan.
5. Present the plan for approval when required.
6. Implement the approved plan.
7. Run relevant tests and static analysis.
8. Review the changes.
9. Report completed work and remaining issues.

Do not begin implementation when a critical requirement is unclear.

## 4. Autonomy Levels

### Independent Decisions

Claude may independently:

- Choose internal implementation details.
- Organize code within the approved architecture.
- Implement routine layouts using the Design System.
- Choose spacing and component composition within approved rules.
- Write and improve tests.
- Fix bugs.
- Refactor without changing product behavior.
- Improve code readability and maintainability.

### Requires Approval

Claude must request approval before:

- Adding a new package or dependency.
- Changing the architecture.
- Changing the primary color palette.
- Introducing major UI/UX patterns.
- Adding a new product feature.
- Changing business rules.
- Changing data models or API contracts.
- Expanding MVP scope.

### Prohibited Without Explicit Permission

Claude must not:

- Modify the Backend.
- Change database schemas.
- Change existing API contracts.
- Remove approved functionality.
- Commit or push directly to main.
- Publish or release the application.
- Introduce unapproved architectural changes.
- Perform destructive operations against production data.

## 5. Approval Rules

Approval is required for decisions that affect product behavior, architecture, dependencies, or scope.

Approval is not required for every file, function, widget, or routine implementation detail.

Once an implementation plan is approved, Claude may complete all tasks within that plan without repeatedly asking for permission.

If new scope or an unexpected architectural decision becomes necessary, stop and request approval.

## 6. Git Workflow

Use feature branches.

Examples:

- feature/flutter-bootstrap
- feature/api-integration
- feature/dashboard
- feature/plant-management
- feature/propagation-management

Rules:

- main is the stable branch.
- Never push directly to main.
- Do not commit unfinished or broken work.
- Use meaningful commit messages.
- Keep changes focused.
- Review the diff before committing.
- Use Pull Requests for merging.
- Do not rewrite shared Git history without permission.

## 7. Code Quality

Before completing a task:

- Run dart format.
- Run flutter analyze.
- Run relevant tests.
- Fix introduced warnings and errors.
- Review changed files.
- Ensure no unrelated changes were introduced.

Do not claim tests passed unless they were actually executed.

## 8. Package Management

Before adding a dependency:

1. Explain why it is needed.
2. Check whether existing packages can solve the problem.
3. Describe relevant trade-offs.
4. Request approval.

Do not add packages independently.

## 9. Backend Protection

The existing Backend is outside the scope of Flutter implementation.

If an API limitation blocks a feature:

- Describe the limitation.
- Identify the affected endpoint or contract.
- Propose possible solutions.
- Wait for approval before changing Backend code.

## 10. Completion Report

At the end of each task, provide:

- Summary of implemented functionality.
- Important files changed.
- Architecture or design decisions.
- Tests executed and their results.
- Known issues or limitations.
- Required follow-up tasks.

## 11. Documentation

Keep documentation updated when an approved architectural or development decision changes.

Do not silently modify product requirements or approved documentation.