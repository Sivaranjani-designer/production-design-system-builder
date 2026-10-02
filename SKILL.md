---
name: production-design-system-builder
description: Build, extend, audit, and document a production-ready native Figma Design System using foundations, primitive and semantic variables, modes, typography, reusable components, variants, properties, patterns, accessibility, documentation, and governance. Use when a user asks to create or improve a Figma Design System, component library, token architecture, or reusable design-system workflow.
---

# Production Design System Builder

## Purpose

Create a professional, reusable, production-ready **native Figma Design System** in the current Figma Design file.

The system must be more than a visual UI kit. It should provide:

- Foundations
- Primitive tokens
- Semantic tokens
- Native Variables and Variable Collections
- Light/Dark modes where appropriate
- Native Text Styles
- Grid and responsive foundations
- Borders and Effects
- Iconography guidance
- Native Components
- Component Sets and Variants
- Component Properties
- Auto Layout
- Token bindings
- Reusable UX patterns
- Accessibility guidance
- Documentation
- Naming conventions
- Contribution/governance guidance
- Changelog and audit

## Core Principles

Always:

1. Prefer native Figma features over visual simulations.
2. Reuse existing foundations, variables, styles, components, and tokens.
3. Never duplicate an existing asset just because a task is being continued.
4. Avoid hardcoded values when an appropriate token exists.
5. Keep everything editable and reusable.
6. Use scalable, predictable naming.
7. Prioritize accessibility, consistency, responsiveness, and developer handoff.
8. Keep the system visually clean and professionally organized.
9. Do not create unnecessary product screens or decorative mockups.
10. Do not claim a native feature was created unless it can be verified in the Figma UI.

## Inputs

Before creating a new system, identify if available:

- Design system name
- Version
- Brand colors
- Typography preference
- Existing Figma file architecture
- Existing variables/styles/components
- Light/Dark requirements
- Target platforms
- Accessibility requirements

If these are not supplied, use sensible professional defaults without inventing product-specific requirements.

Use placeholders when documenting configurable information:

- `[DESIGN SYSTEM NAME]`
- `[VERSION]`
- `[BRAND PRIMARY]`
- `[BRAND SECONDARY]`

---

# PHASE 0 — Inspect Before Building

Before creating anything:

- Inspect the current Figma Design file.
- Determine whether a design system already exists.
- Identify existing pages, collections, variables, modes, styles, components, and component sets.
- Reuse existing assets whenever possible.
- Do not recreate existing foundations.
- If the user is asking to extend an existing system, continue from the current state.

If the file already contains a partial design system, work incrementally rather than starting over.

---

# PHASE 1 — Design System Architecture

Create or use a dedicated page named:

`DESIGN SYSTEM`

Organize the page into clearly separated sections:

1. Overview
2. Foundations
3. Design Tokens
4. Colors
5. Typography
6. Spacing
7. Grid & Layout
8. Radius
9. Borders
10. Elevation
11. Icons
12. Components
13. Patterns
14. Accessibility
15. Governance

Create concise documentation containing:

- Purpose
- Design principles
- System structure
- Accessibility principles
- Naming conventions

Recommended design principles:

- Consistency
- Clarity
- Accessibility
- Scalability
- Reusability
- Simplicity
- Responsive design

---

# PHASE 2 — Primitive Variables

Create a **native Figma Variable Collection** named:

`Primitives`

Do not simulate Variables with frames, text, color swatches, or documentation cards.

## Color primitives

Create scalable color families such as:

### Neutral
`neutral/50` through `neutral/950`

### Primary
`primary/50` through `primary/900`

### Secondary
`secondary/50` through `secondary/900`

### Status
- `success/50` through `success/900`
- `warning/50` through `warning/900`
- `error/50` through `error/900`
- `info/50` through `info/900`

Use a coherent accessible palette. Reuse an existing brand palette if one already exists.

## Spacing

Create native Number variables using a consistent scale, for example:

- `space/0`
- `space/1`
- `space/2`
- `space/4`
- `space/6`
- `space/8`
- `space/12`
- `space/16`
- `space/20`
- `space/24`
- `space/32`
- `space/40`
- `space/48`
- `space/64`
- `space/80`
- `space/96`
- `space/120`

Avoid unnecessary values.

## Radius

Create Number variables:

- `radius/none`
- `radius/xs`
- `radius/sm`
- `radius/md`
- `radius/lg`
- `radius/xl`
- `radius/2xl`
- `radius/full`

## Sizing

Create reusable Number variables where useful:

- `size/4`
- `size/8`
- `size/12`
- `size/16`
- `size/20`
- `size/24`
- `size/32`
- `size/40`
- `size/48`
- `size/56`
- `size/64`
- `size/80`

Only create values that have a meaningful use.

---

# PHASE 3 — Semantic Variables

Create a second native Variable Collection:

`Semantic`

Semantic variables describe **purpose**, not raw visual values.

Create semantic color roles such as:

## Background

- `color/background/default`
- `color/background/subtle`
- `color/background/brand`
- `color/background/inverse`
- `color/background/disabled`

## Text

- `color/text/default`
- `color/text/secondary`
- `color/text/muted`
- `color/text/disabled`
- `color/text/inverse`
- `color/text/brand`
- `color/text/link`

## Border

- `color/border/default`
- `color/border/subtle`
- `color/border/strong`
- `color/border/focus`
- `color/border/error`

## Icon

- `color/icon/default`
- `color/icon/secondary`
- `color/icon/muted`
- `color/icon/disabled`
- `color/icon/brand`
- `color/icon/inverse`

## Actions

- `color/action/primary`
- `color/action/primary-hover`
- `color/action/primary-pressed`
- `color/action/secondary`
- `color/action/secondary-hover`
- `color/action/secondary-pressed`
- `color/action/disabled`

## Status

- `color/status/success`
- `color/status/warning`
- `color/status/error`
- `color/status/info`

## Aliasing rule

Semantic variables should reference primitive variables wherever possible.

Preferred architecture:

`Primitive → Semantic → Component`

Do not unnecessarily hardcode the same raw color value into multiple semantic variables.

---

# PHASE 4 — Modes

Where appropriate, create:

- `Light`
- `Dark`

Use modes primarily on semantic color variables.

Do not blindly invert colors.

Map roles intentionally so that:

- Text remains readable
- Backgrounds remain appropriate
- Borders remain visible
- Interactive states remain distinguishable
- Status colors remain meaningful
- Contrast remains accessible

---

# PHASE 5 — Typography

Create native Figma Text Styles.

Use a professional sans-serif typeface available in the environment.

Create a hierarchy such as:

### Display
- `Display/Large`
- `Display/Medium`
- `Display/Small`

### Heading
- `Heading/H1`
- `Heading/H2`
- `Heading/H3`
- `Heading/H4`
- `Heading/H5`
- `Heading/H6`

### Body
- `Body/Large`
- `Body/Medium`
- `Body/Small`

### Label
- `Label/Large`
- `Label/Medium`
- `Label/Small`

### Caption
- `Caption/Large`
- `Caption/Medium`
- `Caption/Small`

Define:

- Font family
- Font size
- Weight
- Line height
- Letter spacing
- Intended usage

Preserve existing Text Styles when extending an existing system.

Do not create fake typography variables where native Text Styles are the appropriate Figma feature.

---

# PHASE 6 — Grid & Responsive Foundations

Document responsive foundations for:

- Desktop
- Tablet
- Mobile

Define:

- Container widths
- Grid columns
- Gutters
- Breakpoints
- Responsive spacing principles

Use sensible professional values.

Document component behavior such as:

- Stacking
- Resizing
- Wrapping
- Navigation transformation
- Table responsiveness
- Form responsiveness

---

# PHASE 7 — Borders, Elevation & Icons

## Borders

Document and/or create reusable styles for:

- Subtle border
- Default border
- Strong border
- Focus border

## Elevation

Create reusable native Figma Effects where supported:

- `Elevation/None`
- `Elevation/Low`
- `Elevation/Medium`
- `Elevation/High`
- `Elevation/Overlay`

Do not simulate Effects using unrelated objects.

## Iconography

Document:

- Icon style
- Stroke consistency
- Alignment
- Sizing
- Spacing
- Accessibility

Show examples for:

- 16px
- 20px
- 24px
- 32px

Use editable placeholders only when actual icons are unavailable.

---

# PHASE 8 — Component Library

Create a clearly separated:

`COMPONENTS`

section.

Build **native Figma Components**, Component Sets, Variants, Component Properties, and Auto Layout.

Never rebuild the foundation layer.

## Buttons

Create a Button component set.

Types:

- Primary
- Secondary
- Tertiary
- Ghost
- Destructive
- Link

Sizes:

- Small
- Medium
- Large

States:

- Default
- Hover
- Pressed
- Focus
- Disabled
- Loading

Properties where appropriate:

- Label
- Leading Icon
- Trailing Icon
- Icon Only

Use existing:

- Semantic color tokens
- Spacing tokens
- Radius tokens
- Typography
- Auto Layout

## Inputs

Create:

- Text Input
- Textarea
- Search Field

States:

- Default
- Hover
- Focus
- Filled
- Disabled
- Error
- Success
- Read Only

Properties may include:

- Label
- Placeholder
- Helper text
- Error message
- Leading icon
- Trailing icon

## Selection Controls

Create:

- Checkbox
- Radio
- Switch
- Select
- Multi Select

Include appropriate states:

- Default
- Hover
- Focus
- Selected
- Disabled
- Error

## Forms

Create:

- Form Field
- Form Label
- Helper Text
- Error Message
- Required Indicator
- File Upload
- Date Input

Make them compatible with the input components.

## Navigation

Create:

- Navigation Item
- Tabs
- Breadcrumb
- Pagination
- Stepper
- Sidebar Navigation
- Top Navigation
- Bottom Navigation

Include active/inactive and other meaningful states.

## Data Display

Create:

- Card
- Badge
- Tag
- Chip
- Avatar
- Avatar Group
- List Item
- Stat Card
- Table
- Table Row
- Data Cell
- Timeline

Semantic types for Badge/Tag:

- Neutral
- Brand
- Success
- Warning
- Error
- Info

## Feedback

Create:

- Alert
- Toast
- Banner
- Inline Message
- Progress Bar
- Progress Indicator
- Spinner
- Skeleton
- Empty State

## Overlays

Create:

- Modal
- Dialog
- Drawer
- Popover
- Tooltip
- Dropdown Menu
- Context Menu

Document:

- Trigger
- Placement
- Close behavior
- Focus behavior
- Accessibility
- Responsive behavior

## Table System

Create reusable:

- Table
- Table Header
- Table Row
- Table Cell
- Table Action
- Pagination

States:

- Default
- Hover
- Selected
- Disabled
- Loading
- Empty

Use Auto Layout and nested reusable components.

---

# PHASE 9 — Component Naming & Properties

Use predictable names.

Examples:

- `Button`
- `Form/Input`
- `Form/Checkbox`
- `Navigation/Tabs`
- `Feedback/Alert`
- `Data/Table`
- `Overlay/Modal`

Use variant properties such as:

- `Type=Primary`
- `Size=Medium`
- `State=Default`

Avoid:

- `Variant 1`
- `Copy`
- `New Component`
- `Frame 123`
- `Component 1`

Use Component Properties appropriately:

- Boolean
- Text
- Instance Swap
- Variant properties

Do not create properties that duplicate existing variants unnecessarily.

---

# PHASE 10 — Token Binding

Audit components and replace hardcoded values where appropriate.

Prioritize binding:

- Colors
- Spacing
- Radius
- Typography
- Borders
- Elevation

Components should inherit system-level changes.

Preferred architecture:

`Primitive → Semantic → Component`

Do not break an existing component merely to force a token binding where the current Figma environment does not support it safely.

---

# PHASE 11 — Component Documentation

Place concise documentation beside major components.

Document:

- Purpose
- Anatomy
- Variants
- Properties
- States
- Usage
- Do
- Don't
- Accessibility
- Responsive behavior

Avoid overly long documentation.

---

# PHASE 12 — UX Patterns

Create a `PATTERNS` section using existing components.

Document reusable patterns for:

- Authentication
- Form submission
- Search and filtering
- CRUD workflow
- Confirmation
- Error handling
- Empty state
- Loading state
- Dashboard summary
- Data table
- Notifications
- File upload

Do not create complete product screens.

Use only reusable pattern examples.

---

# PHASE 13 — Accessibility

Create a dedicated Accessibility section.

Document:

- Color contrast
- Keyboard navigation
- Focus states
- Touch target sizing
- Form labels
- Error messaging
- Icon accessibility
- Disabled states
- Screen reader considerations
- Motion considerations

Ensure interactive components have visible focus states where applicable.

---

# PHASE 14 — Documentation & Governance

Create a documentation structure:

1. Overview
2. Foundations
3. Tokens
4. Components
5. Patterns
6. Responsive
7. Accessibility
8. Naming
9. Contribution
10. Changelog

Create a clear navigation/index.

## Token documentation

Document:

- Color
- Typography
- Spacing
- Sizing
- Radius
- Borders
- Elevation

For colors include:

- Token name
- Role
- Example
- Usage

For spacing include:

- Token
- Value
- Usage

For typography include:

- Style
- Size
- Weight
- Line height
- Usage

## Contribution process

Document:

1. Identify the need
2. Check existing components
3. Reuse existing tokens
4. Propose a new component
5. Define variants and states
6. Check accessibility
7. Document usage
8. Review before publishing

## Changelog

Create:

`Version 1.0`

Include:

- Version
- Date
- Change
- Author

Provide a structure for future versions.

---

# PHASE 15 — Optional Prototype Interactions

Prototype interactions are optional and should not block completion of the Design System.

When native component prototyping is supported, component variants may be connected using appropriate Figma Prototype interactions.

Examples:

- Toggle Off → On
- Toggle On → Off
- Checkbox Unchecked → Checked
- Tabs Inactive → Active
- Accordion Collapsed → Expanded
- Select Closed → Open
- Modal Closed → Open

Prefer `Change to` for transitions between variants of the same component set.

Do not create product navigation flows.

If the current environment cannot create native Prototype interactions, skip this phase and report it. Never simulate or claim prototype interactions were created.

---

# PHASE 16 — Verification Gates

This is mandatory.

Never claim completion based only on an internal task summary.

## Variables verification

Native Variables must actually appear in Figma's native Variables interface.

Verify:

- Variable Collections exist
- Variables exist
- Correct variable types are used
- Modes exist where required
- Semantic variables alias primitives where appropriate

If native Variables cannot be created, do not create fake replacements and do not claim success.

## Components verification

Verify:

- Components are native Figma Components
- Component Sets exist
- Variants exist
- Properties are real Component Properties
- Auto Layout is actually applied

## Styles verification

Verify:

- Text Styles are native
- Effects are native where applicable

## Integrity verification

Verify:

- No duplicate components
- No duplicate variable names
- No broken variants
- No detached main components
- No unnecessary hardcoded values
- No random frame/component names
- Existing system was not unintentionally altered

---

# PHASE 17 — Final Audit

Perform a full audit.

## Foundations

- Colors
- Typography
- Spacing
- Grid
- Radius
- Borders
- Elevation
- Icons

## Tokens

- Primitive variables
- Semantic variables
- Light mode
- Dark mode
- Naming
- Aliasing

## Components

- Native components
- Component Sets
- Variants
- Properties
- Auto Layout
- States
- Token bindings

## Documentation

- Purpose
- Usage
- Anatomy
- Do/Don't
- Accessibility
- Responsive behavior

## Quality

- No unnecessary duplicates
- No broken variants
- No inconsistent naming
- No detached main components
- No fake native features
- No random placeholder names
- No missing important states

---

# PHASE 18 — Final Cleanup

Organize the DESIGN SYSTEM page professionally.

Use:

- Clear section hierarchy
- Consistent spacing
- Consistent typography
- Clear labels
- Logical grouping
- Clean component presentation
- Documentation beside relevant components

The final result should look and function like a professional design system maintained by a senior product design team.

## Final success criteria

A successful system contains, as applicable:

**FOUNDATIONS**
+
**TOKENS**
+
**NATIVE VARIABLES**
+
**MODES**
+
**TYPOGRAPHY**
+
**GRID**
+
**RADIUS**
+
**BORDERS**
+
**ELEVATION**
+
**ICONOGRAPHY**
+
**COMPONENTS**
+
**VARIANTS**
+
**PROPERTIES**
+
**TOKEN BINDINGS**
+
**PATTERNS**
+
**DOCUMENTATION**
+
**ACCESSIBILITY**
+
**GOVERNANCE**

It must function as a real production design system, not merely look like a UI kit.
