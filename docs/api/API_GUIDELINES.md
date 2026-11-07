# API Integration Guidelines

## 1. General Rules

The Flutter application integrates with an existing Backend API.

The Backend is the source of truth for:

- Data models
- Business rules
- Validation rules
- Relationships
- API contracts

Never assume an API contract without verifying it.

## 2. API Discovery

Before implementing an API integration:

1. Inspect the available API documentation.
2. Identify the relevant endpoint.
3. Review HTTP methods and URL parameters.
4. Review request and response structures.
5. Identify required and optional fields.
6. Review pagination and filtering behavior.
7. Review error responses.
8. Confirm the expected data types.

If documentation is missing, inspect the Backend implementation or request clarification.

## 3. Base URL and Environments

Use environment-specific configuration.

Expected environments:

- Development
- Production

The actual URLs must be determined from the existing project configuration.

Do not hardcode environment-specific URLs inside feature code.

Never commit secrets, private credentials, or sensitive configuration.

## 4. HTTP Client

Use a centralized Dio instance.

Responsibilities:

- Base URL
- Connection and receive timeouts
- Request headers
- Response handling
- Error handling
- Development logging

Feature repositories must not create independent HTTP clients.

## 5. Data Models

Use DTOs for API serialization.

Rules:

- Match JSON field names and types exactly.
- Handle nullable fields explicitly.
- Do not assume fields are always present.
- Do not silently convert invalid data.
- Keep API DTOs separate from domain entities when separation provides value.
- Use generated serialization code where appropriate.

## 6. Repository Pattern

Screens and state providers must not directly call Dio.

Use the following flow:

    Presentation
        ↓
    Provider / State Controller
        ↓
    Repository
        ↓
    API Service
        ↓
    Backend API

Repositories are responsible for abstracting data access and mapping API responses.

## 7. Error Handling

Handle at least these cases:

- Network unavailable
- Request timeout
- Unauthorized response
- Forbidden response
- Not found
- Validation error
- Server error
- Unexpected response
- Invalid JSON or serialization error

Do not expose raw technical exceptions directly to users.

Preserve useful error details for debugging.

## 8. Pagination and Filtering

Follow the actual API contract.

Do not assume:

- Page-based pagination
- Offset-based pagination
- Cursor-based pagination
- Default page sizes
- Filter parameter names

Inspect the endpoint before implementation.

## 9. API Changes

Claude must never:

- Modify Backend endpoints.
- Change request or response contracts.
- Rename API fields.
- Change Backend validation rules.
- Add or remove database fields.

Any Backend change requires explicit approval.

## 10. API Documentation Gaps

If an endpoint or its behavior is unclear:

- Do not invent a contract.
- Document the missing information.
- Ask for clarification when implementation depends on it.
- Continue with unrelated tasks where possible.

## 11. API Testing

Use mocked responses for repository and state tests.

For integration testing, use the appropriate development environment.

Never run destructive operations against production data.