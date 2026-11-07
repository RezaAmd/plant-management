# Application Architecture

## 1. Overview

The client application is developed using Flutter and Dart.

The architecture must support maintainability, testability, separation of concerns, and future platform expansion.

The initial target platform is Android.

## 2. Architectural Principles

- Feature-first organization.
- Separation of UI, business logic, and data access.
- Dependency inversion.
- Reusable shared components.
- Explicit state management.
- Testable business logic.
- No direct API calls from UI widgets.
- Avoid unnecessary abstractions and premature complexity.

## 3. Proposed Technology Stack

The following technologies are proposed and require confirmation during project setup:

| Concern | Proposed Technology |
|---|---|
| Framework | Flutter |
| Language | Dart |
| State Management | Riverpod |
| Navigation | GoRouter |
| HTTP Client | Dio |
| JSON Serialization | json_serializable |
| Testing | Flutter Test |

Do not introduce additional packages without approval.

## 4. Project Structure

Use a feature-first structure with shared core infrastructure.

Proposed structure:

    lib/
    ├── app/
    │   ├── app.dart
    │   ├── router/
    │   └── theme/
    │
    ├── core/
    │   ├── network/
    │   ├── error/
    │   ├── constants/
    │   ├── utils/
    │   └── widgets/
    │
    ├── features/
    │   ├── plants/
    │   │   ├── data/
    │   │   ├── domain/
    │   │   └── presentation/
    │   │
    │   ├── propagation/
    │   │   ├── data/
    │   │   ├── domain/
    │   │   └── presentation/
    │   │
    │   └── ...
    │
    └── main.dart

Each feature should contain only the layers it actually needs.

## 5. Layer Responsibilities

### Presentation

Responsible for:

- Screens and widgets.
- User interactions.
- UI state.
- Form validation presentation.
- Navigation.

Must not contain direct HTTP requests or complex business logic.

### Domain

Responsible for:

- Business entities.
- Repository contracts.
- Use cases when they provide meaningful value.
- Business rules that should not depend on Flutter or external packages.

### Data

Responsible for:

- API communication.
- DTOs and serialization.
- Repository implementations.
- Mapping API responses to domain models.

## 6. State Management

Use Riverpod for application and feature state management.

Rules:

- Keep state close to the feature that owns it.
- Avoid unnecessary global state.
- Separate loading, data, empty, and error states.
- Do not put business logic inside widgets.
- Prefer immutable state.
- Handle asynchronous operations explicitly.

## 7. Navigation

Use GoRouter.

Rules:

- Routes must be centrally organized.
- Navigation should be declarative.
- Route parameters and extra data must be handled safely.
- Navigation structure should support future deep linking.

## 8. Networking

Use a centralized Dio client.

Responsibilities:

- Base URL configuration.
- Request and response handling.
- Error mapping.
- Timeouts.
- Logging in development.
- Environment-specific configuration.

API contracts must follow the existing Backend implementation.

## 9. Dependency Injection

Use Riverpod providers for dependency management.

Repositories and services should be injected rather than instantiated directly inside screens.

## 10. Platform Strategy

MVP target: Android.

However:

- Keep business logic platform-independent.
- Avoid Android-specific dependencies in domain code.
- Isolate platform-specific integrations.
- Do not implement or test iOS/Desktop builds unless requested.

## 11. Testing Strategy

### Unit Tests
For business logic, mapping, validation, and utilities.

### Widget Tests
For important UI components and screen behavior.

### Integration Tests
For critical end-to-end application workflows.

Prioritize tests around business-critical functionality.

## 12. Architecture Change Policy

Changes to the approved architecture require prior approval.

Claude may suggest improvements, but must not independently replace core architectural decisions or introduce major architectural patterns.