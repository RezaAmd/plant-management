# Product Brief

## 1. Product Overview

Plant Management is an application for managing plants, greenhouse operations, propagation processes, and related activities.

The application aims to provide a structured way to track plants throughout their lifecycle, manage propagation batches, record activities and observations, and maintain relevant operational data.

The product consists of an existing Backend API and a Flutter client application.

## 2. Product Goals

- Manage plant information and classifications.
- Manage propagation processes using Production Batches.
- Track propagation stages and their timelines.
- Record production activities, observations, measurements, and experimental results.
- Track quantity changes, losses, and production outcomes.
- Provide a clear and efficient user interface for daily greenhouse operations.
- Keep the architecture extensible for future features and platforms.

## 3. MVP Scope

### Platform
- Android only.
- Flutter is the client application framework.
- Architecture must allow future iOS and Desktop support without rewriting business logic.

### Users
- Single-user application for the MVP.
- Authentication is not currently required.
- The architecture should not prevent adding authentication and multi-user support later.

### Backend
- An existing Backend API is available.
- The Flutter application must integrate with the existing API.
- Backend changes are outside the scope of Flutter development unless explicitly approved.

### Initial Functional Scope
The exact feature priorities will be finalized after reviewing the existing API and product requirements.

Expected core areas:

- Plant Management
- Plant Classification
- Propagation Management
- Production Batches
- Production Stages
- Production Records and Activities
- Quantity Tracking
- Observations and Measurements

## 4. Non-Goals

The following are not MVP requirements:

- iOS release
- Desktop release
- Authentication implementation
- Multi-user permissions and roles
- Backend redesign
- Unapproved API changes
- Features not included in the approved MVP scope

## 5. Product Principles

- Data accuracy is more important than visual complexity.
- Daily operations should require as few steps as reasonably possible.
- Related information should be displayed in context.
- Production history and traceability should be preserved.
- The interface should remain consistent across features.
- Avoid unnecessary complexity in the MVP.
- Design decisions should support future expansion.

## 6. Important Domain Concepts

The application may contain concepts such as:

- Plant
- Plant Category
- Plant Variety
- Propagation Method
- Production Batch
- Production Stage
- Production Event
- Propagation Record
- Quantity Record
- Observation
- Experiment

These concepts must follow the existing Backend data model and approved domain specifications. Do not independently redefine their semantics.

## 7. MVP Acceptance Criteria

- The Android application can be built and run successfully.
- The application can communicate with the existing Backend API.
- Core approved workflows are functional.
- Loading, empty, success, and error states are handled.
- Forms validate user input.
- Navigation is consistent.
- No unapproved Backend or API changes are introduced.
- Critical business logic has appropriate tests.

## 8. Open Questions

The following items must be resolved during project discovery:

- Backend technology and API documentation.
- API base URL and environment configuration.
- Exact MVP feature priorities.
- Selected application font.
- Final color palette.
- Existing Backend validation and error conventions.