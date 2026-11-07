\# Plant Management - Claude Code Instructions



\## 1. Project Overview



You are working on the Flutter client application for Plant Management.



The application manages plants, propagation processes, production batches, stages, records, and related greenhouse operations.



The project has an existing Backend API.



The MVP targets Android only.



Future iOS and Desktop support should remain possible without rewriting business logic.



\## 2. Mandatory Documentation



Before making changes, read the relevant project documentation:



\- `docs/product/PRODUCT\_BRIEF.md`

\- `docs/architecture/ARCHITECTURE.md`

\- `docs/api/API\_GUIDELINES.md`

\- `docs/design/DESIGN\_SYSTEM.md`

\- `docs/development/AI\_WORKFLOW.md`



These documents define the approved product scope, architecture, API integration rules, design standards, and development workflow.



If documentation conflicts with existing code or API behavior, do not silently assume which is correct. Report the conflict.



\## 3. Core Rules



\- Follow the approved architecture.

\- Follow the Design System.

\- Respect the existing Backend API.

\- Do not invent API contracts.

\- Do not modify Backend code without explicit permission.

\- Do not add packages without approval.

\- Do not expand product scope without approval.

\- Do not introduce unnecessary abstractions.

\- Write maintainable and testable code.

\- Preserve existing functionality unless a change is explicitly requested.



\## 4. Development Process



For every meaningful task:



1\. Understand the request.

2\. Inspect relevant files and existing implementation.

3\. Identify dependencies and potential risks.

4\. Prepare a concise implementation plan.

5\. Request approval if the task requires a decision outside your authority.

6\. Implement the approved plan.

7\. Run relevant checks and tests.

8\. Review the final changes.

9\. Provide a completion report.



For routine tasks within an already approved scope, do not request unnecessary approval.



\## 5. Code Standards



\- Use Dart and Flutter conventions.

\- Follow the architecture defined in `ARCHITECTURE.md`.

\- Keep widgets focused and reusable.

\- Keep business logic outside UI widgets.

\- Use Riverpod for state management.

\- Use GoRouter for navigation.

\- Use Dio through the centralized network layer.

\- Handle asynchronous states explicitly.

\- Handle errors properly.

\- Avoid duplicated logic.

\- Write tests for important business logic.



\## 6. UI Standards



\- Follow `DESIGN\_SYSTEM.md`.

\- Support Persian and RTL layouts.

\- Use shared components where appropriate.

\- Handle loading, empty, success, and error states.

\- Avoid hardcoded screen dimensions.

\- Do not introduce unapproved colors or typography.



\## 7. Git Safety



\- Never commit or push directly to `main`.

\- Work on the assigned feature branch.

\- Do not switch branches without permission.

\- Do not overwrite unrelated user changes.

\- Do not discard uncommitted work.

\- Review Git status and diffs before making commits.

\- Do not commit unless the task or user explicitly authorizes it.



\## 8. Backend Safety



The Backend is an existing and independent system.



Do not:



\- Modify Backend files.

\- Change API contracts.

\- Change database schemas.

\- Change Backend validation rules.

\- Perform destructive operations against production.



If Backend changes are required, stop and request approval.



\## 9. Dependency Policy



Do not add, remove, or upgrade packages without approval.



First inspect existing dependencies and determine whether they are sufficient.



\## 10. Testing and Validation



Before reporting a task as complete, run applicable checks:



\- `dart format`

\- `flutter analyze`

\- Relevant unit tests

\- Relevant widget tests

\- Relevant integration tests, when appropriate



Report the actual results. Never claim that a command or test was executed if it was not.



\## 11. Task Boundaries



Only implement the requested task and its necessary dependencies.



Do not perform unrelated refactoring, redesign existing screens, or modify unrelated files.



If you discover unrelated issues, report them separately.



\## 12. Completion Report



Every completed task must include:



\- What was implemented.

\- Files changed.

\- Important decisions.

\- Tests and validation results.

\- Known limitations.

\- Remaining work.



\## 13. Priority of Instructions



When making decisions, follow this order:



1\. Explicit instructions from the Product Owner.

2\. Approved project decisions.

3\. Project documentation.

4\. Existing code conventions.

5\. Your own implementation judgment.



When uncertain about a product or architectural decision, ask rather than assume.

