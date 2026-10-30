# Studio Wobido – Development Guidelines

## 1. Project Overview

We are building the online shop for Studio Wobido, an independent design studio based in Germany.

The storefront is based on Shopify's official Horizon theme.

The goal is to create a playful, distinctive and minimal shopping experience that reflects the Studio Wobido brand.

Figma designs are the primary visual reference.

## 2. Technical Foundation

- Shopify Horizon theme
- Shopify Liquid
- HTML
- CSS
- Vanilla JavaScript

### General Rules

- Preserve Shopify's native architecture and functionality.
- Do not introduce React, Vue or other JavaScript frameworks.
- Avoid additional dependencies and npm packages unless absolutely necessary.
- Keep the theme compatible with Shopify's native Theme Editor.
- Prefer reusable Shopify sections and blocks.
- Use Shopify's native product, cart and checkout functionality.
- Never implement a custom checkout system.
- Keep code clean, modular and maintainable.

## 3. Design System

### Brand Colors

Primary Blue: #1463E7
Primary Yellow: #FCFFA8
Primary Cream: #F8F7EE

Secondary Pink: #FF99D5
Secondary Green: #00B380

Default Background: #F8F7EE

### Typography

Font Family: Spline Sans
Preferred Weight: Medium (500)

Spline Sans is not available in Shopify's font picker. It is self-hosted from `assets/` and loaded via `@font-face` in our own stylesheet.

Typography sizes:

- H1: 48px
- H2: 32px
- Body: 20px
- Body line height: 27px

Use CSS variables for typography and colors wherever possible.

### Design Principles

- Playful and contemporary
- Minimal but expressive
- Strong use of color
- Generous whitespace
- Clear visual hierarchy
- Image-driven layouts

Do not introduce additional colors, fonts or design styles without approval.

Important:
The grey areas in Figma screenshots are placeholders, not actual design colors.

## 4. Responsive Design

The existing Figma designs primarily represent desktop layouts.

Create responsive implementations for:

- Desktop
- Tablet
- Mobile

When no mobile reference exists, derive the responsive layout from the desktop design.

Do not simply scale down the desktop layout.
Prioritize usability, readability and a consistent brand experience.

## 5. Shopify Architecture

- Use Shopify sections wherever appropriate.
- Make relevant content editable through the Theme Editor.
- Use Shopify's native product and collection objects.
- Avoid hardcoded product information.
- Keep navigation, cart and product functionality compatible with Shopify.
- Do not break existing theme functionality.

### Keeping Horizon Updatable

This repository receives official Horizon updates from Shopify as merges. Every edit to an original Horizon file can cause a merge conflict later.

- Prefer Theme Editor settings over code changes.
- Put brand styles in our own files (e.g. `assets/studio-wobido.css`), not in `base.css` or Horizon's section stylesheets.
- Create new sections, blocks or snippets instead of rewriting existing ones.
- If an original Horizon file must be edited, keep the change minimal and mark it with a comment containing `Studio Wobido`, so it is easy to find during updates.

## 6. Development Workflow

Before changing files:

1. Inspect the existing implementation.
2. Identify the relevant files.
3. Explain the planned changes.
4. Avoid unnecessary modifications.

When implementing changes:

- Work incrementally.
- Keep changes focused.
- Reuse existing components where possible.
- Do not overwrite unrelated code.
- Explain important technical decisions.

After implementation:

- Check the local Shopify preview.
- Test responsive layouts.
- Check for console errors.
- Verify that Shopify Theme Editor functionality still works.

## 7. AI Development Rules

- Do not make assumptions about the design.
- Ask before making major design decisions.
- Do not redesign existing sections without approval.
- Do not install additional tools or dependencies without explaining why.
- Prefer simple solutions over unnecessary complexity.
- Explain changes in a way that is understandable to a developer with basic coding knowledge.

## 8. Priority

When making decisions, follow this priority:

1. Shopify functionality and compatibility
2. Figma design references
3. Studio Wobido design system
4. Clean and maintainable code
5. Performance and accessibility
