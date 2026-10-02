# Production Design System Builder

A reusable Figma Agent Skill for building, extending, auditing, and documenting production-ready native Figma Design Systems.

## Overview

Production Design System Builder is a structured workflow designed for Product Designers and Design System Designers who want to create scalable, reusable, and maintainable design systems in Figma.

The skill guides Figma Agent through the complete design-system lifecycle — from foundations and token architecture to components, accessibility, documentation, and governance.

## What It Covers

- Native Figma Variables and Variable Collections
- Primitive and Semantic Design Tokens
- Light and Dark Modes
- Typography and Text Styles
- Spacing, Sizing, Radius, Borders, and Elevation
- Responsive Grid and Layout Foundations
- Reusable Components and Component Sets
- Variants and Component Properties
- Auto Layout
- Instance Swap and Boolean Properties
- Token Binding
- Accessibility
- Responsive Component Guidelines
- UX Patterns
- Design System Documentation
- Governance and Contribution Guidelines
- Design System Audits and Verification

## Token Architecture

The recommended token architecture is:

**Primitive → Semantic → Component**

### Primitive Tokens

Define foundational values such as:

- Colors
- Spacing
- Radius
- Sizing

### Semantic Tokens

Translate foundational values into meaningful UI roles:

- Background
- Text
- Border
- Icon
- Action
- Status

### Components

Reusable components consume semantic tokens rather than directly depending on raw primitive values.

This architecture makes the system easier to scale, theme, maintain, and update.

## Design System Principles

The skill follows these principles:

- Consistency
- Clarity
- Accessibility
- Scalability
- Reusability
- Simplicity
- Responsive Design
- Maintainability

## Verification First

The skill is designed to avoid claiming that a Figma feature was created when it cannot be verified.

It prioritizes:

1. Inspecting the existing file
2. Reusing existing architecture
3. Avoiding unnecessary duplication
4. Verifying native Figma implementation
5. Auditing the final result

The skill does not treat visual documentation or simulated structures as a replacement for native Figma Variables, Components, Styles, or Properties.

## Usage

Download `SKILL.md` from this repository.

In Figma Agent, upload the Markdown file as a custom Skill and use it to build, extend, or audit a Design System.

### Example

> Use the Production Design System Builder skill to audit the existing design system. Do not make changes. Identify missing tokens, components, accessibility requirements, documentation gaps, and governance issues.

## Recommended Workflow

```text
Inspect
   ↓
Foundations
   ↓
Primitive Tokens
   ↓
Semantic Tokens
   ↓
Modes
   ↓
Typography
   ↓
Components
   ↓
Variants & Properties
   ↓
Token Binding
   ↓
Accessibility
   ↓
Patterns
   ↓
Documentation
   ↓
Governance
   ↓
Final Audit
