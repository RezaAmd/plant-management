# Design System

## 1. Design Goals

The application UI should be:

- Clean and functional.
- Easy to use during daily greenhouse operations.
- Consistent across all features.
- Information-dense without being visually crowded.
- Responsive to different Android screen sizes.
- Suitable for both short interactions and detailed data entry.

## 2. Design Principles

1. Clarity over decoration.
2. Consistency over one-off designs.
3. Reuse shared components.
4. Keep important actions easy to find.
5. Use visual hierarchy to organize complex information.
6. Provide clear feedback for every user action.
7. Avoid unnecessary animations and visual effects.

## 3. Color System

The final color palette must be approved before implementation.

Use semantic color tokens rather than hardcoded colors throughout the application.

Required tokens:

- Primary
- On Primary
- Secondary
- Background
- Surface
- Surface Variant
- Primary Text
- Secondary Text
- Border
- Success
- Warning
- Error
- Info

The palette should be appropriate for a plant and greenhouse management application.

Do not introduce arbitrary colors in individual screens.

## 4. Typography

The application must use a consistent typography scale.

The font family will be selected by the product owner.

Proposed typography scale:

| Style | Size (sp) | Usage |
|---|---:|---|
| Display | 28 | Major page headings |
| H1 | 24 | Main screen headings |
| H2 | 20 | Section headings |
| H3 | 18 | Card and subsection headings |
| Body Large | 16 | Important content |
| Body | 14 | Standard text |
| Caption | 12 | Supporting information |

Use appropriate font weights to establish hierarchy.

Typography must support Persian text and right-to-left layouts.

Do not use font sizes outside the design scale without a good reason.

## 5. Spacing

Use a consistent spacing scale.

| Token | Size (dp) |
|---|---:|
| XS | 4 |
| SM | 8 |
| MD | 12 |
| LG | 16 |
| XL | 24 |
| XXL | 32 |

Avoid arbitrary spacing values unless required by a specific component.

## 6. Components

Build reusable components for common UI patterns:

- Primary and secondary buttons
- Text fields
- Dropdowns
- Date pickers
- Cards
- Section headers
- Status indicators
- Empty states
- Loading indicators
- Error states
- Confirmation dialogs
- Quantity indicators
- Timeline items

Shared components should be placed in the appropriate shared location.

Do not duplicate the same component implementation across features.

## 7. Forms

Forms should:

- Clearly identify required fields.
- Display validation errors near the relevant field.
- Preserve user input when possible.
- Disable submission when appropriate.
- Show loading feedback during submission.
- Provide success or failure feedback.

Avoid unnecessarily long forms. Group related fields logically.

## 8. Lists and Data Presentation

Use appropriate presentation patterns depending on the data:

- Lists for repeated records.
- Cards for grouped information.
- Tables only when comparing multiple structured values.
- Timelines for chronological processes.
- Badges for meaningful statuses.

Avoid displaying every available field at once.

## 9. RTL and Localization

The application must support Persian and right-to-left layouts.

Rules:

- Use directional layout properties.
- Avoid hardcoded left/right assumptions.
- Verify icon direction where applicable.
- Handle Persian and English text correctly.
- Ensure dates and numbers are displayed consistently.

Localization implementation details must be finalized during project setup.

## 10. Responsive Layout

Although MVP targets Android, layouts must adapt to different screen widths.

Avoid fixed screen dimensions.

Use flexible constraints and appropriate scrolling behavior.

## 11. UI States

Every data-driven screen should account for:

- Initial state
- Loading state
- Loaded state
- Empty state
- Error state

Do not leave users with blank screens during loading or failure.

## 12. Component Approval

Claude may make routine layout and spacing decisions within this system.

Changes to the main color palette, typography family, or major UI patterns require approval.