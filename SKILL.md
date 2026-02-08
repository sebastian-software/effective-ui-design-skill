---
name: effective-ui-design
description: |
  Comprehensive UI design system with professional guidelines for creating intuitive, accessible, and beautiful interfaces. Use this skill when: (1) Creating any UI/frontend design or code, (2) Designing websites, apps, dashboards, or any digital interface, (3) Writing CSS, HTML, or frontend component code, (4) Reviewing or improving existing UI designs, (5) Making decisions about color, typography, layout, spacing, buttons, or forms, (6) Ensuring accessibility compliance (WCAG 2.1 AA), (7) Creating design systems or component libraries. This skill ensures ALL created UI content follows professional design guidelines without exception.
---

# Effective UI Design

This skill enforces comprehensive UI design guidelines for creating professional, accessible interfaces. Every UI design decision MUST follow these guidelines.

## Quick Reference

| Topic | Reference File |
|-------|---------------|
| Fundamentals | [references/01-fundamentals.md](references/01-fundamentals.md) |
| Less is More | [references/02-less-is-more.md](references/02-less-is-more.md) |
| Colour | [references/03-colour.md](references/03-colour.md) |
| Layout & Spacing | [references/04-layout-spacing.md](references/04-layout-spacing.md) |
| Typography | [references/05-typography.md](references/05-typography.md) |
| Web Fonts | [references/05b-webfonts.md](references/05b-webfonts.md) |
| Copywriting | [references/06-copywriting.md](references/06-copywriting.md) |
| Buttons | [references/07-buttons.md](references/07-buttons.md) |
| Forms | [references/08-forms.md](references/08-forms.md) |

## Core Principles (ALWAYS Apply)

### 1. Minimise Usability Risks
- Meet WCAG 2.1 level AA accessibility requirements
- Consider users with poor eyesight, low computer literacy, reduced dexterity
- Avoid thin/light grey text, icons without labels, colored headings that look like links

### 2. Have a Logical Reason for Every Design Detail
- Every element must have a purpose that improves usability
- Design using objective logic, not subjective opinion
- Be able to articulate the rationale behind each decision

### 3. Minimise Interaction Cost
- Keep related actions close (Fitts's Law)
- Reduce distractions
- Minimise choices (Hick's Law)
- Use minimum 48pt × 48pt target areas

### 4. Minimise Cognitive Load
- Remove unnecessary styles/information
- Break information into smaller groups
- Use familiar design patterns (Jakob's Law)
- Maintain consistency
- Create clear visual hierarchy

### 5. Create a Design System
- Define predefined colour palette
- Set typography scale
- Use 8pt spacing increments: 8pt, 16pt, 24pt, 32pt, 48pt, 80pt
- Create reusable components

## Critical Rules (NEVER Violate)

### Colour
- Text contrast: minimum 4.5:1 ratio (small text ≤18px)
- Large text/UI elements: minimum 3:1 ratio
- Never rely on colour alone to convey meaning
- Use brand colour ONLY for interactive elements
- Avoid pure black (#000000) on white - use dark grey instead

### Typography
- Use single sans-serif typeface for most interfaces
- Body text: minimum 18px for long text
- Line height: minimum 1.5 (150%) for body text
- Line length: 40-80 characters per line
- Left-align text (for English)
- Use only regular and bold font weights

### Layout
- Space elements based on relationship (closer = more related)
- Use 12-column grid for main layout
- Align elements to create neat edges
- Be generous with white space

### Buttons
- Define 3 button weights: Primary, Secondary, Tertiary
- Use single primary button per screen
- Left-align buttons (most important first)
- Button text: verb + noun (e.g., "Save post")
- Minimum size: 48pt × 48pt
- Avoid disabled buttons - validate on submit instead

### Forms
- Single column layout
- Stack labels above inputs
- Mark both required (*) and optional fields
- Match field width to expected input
- Use conventional form field styles
- Display hints above fields (not below)

## Design Checklist

Before finalizing any UI design:

1. **Accessibility**
   - [ ] All text has 4.5:1+ contrast ratio
   - [ ] UI elements have 3:1+ contrast ratio
   - [ ] Colour is not the only indicator
   - [ ] Target areas are 48pt+ minimum
   - [ ] Text links are underlined

2. **Visual Hierarchy**
   - [ ] Clear order of importance
   - [ ] Primary action is most prominent
   - [ ] Related elements are grouped
   - [ ] Consistent spacing applied

3. **Typography**
   - [ ] Single typeface (or 2 max with heading typeface)
   - [ ] Body text 18px+ for long content
   - [ ] Line height 1.5+ for body text
   - [ ] Left-aligned text
   - [ ] 40-80 characters per line

4. **Copywriting**
   - [ ] Concise text (no unnecessary words)
   - [ ] Sentence case used
   - [ ] Plain language (no jargon)
   - [ ] Front-loaded important info
   - [ ] Descriptive button text

5. **Forms**
   - [ ] Single column layout
   - [ ] Labels above inputs
   - [ ] Required/optional fields marked
   - [ ] Field widths match expected input
   - [ ] High contrast borders (3:1+)

## Implementation

When creating UI code:

1. Read the relevant reference files for detailed guidelines
2. Apply ALL rules without exception
3. Verify against the checklist above
4. Use the predefined spacing scale (8pt increments)
5. Use the colour palette structure from [references/03-colour.md](references/03-colour.md)

## Colour Palette Template

```
Brand:        HSB(hue, 65, 85)     - Interactive elements
Text strong:  HSB(hue, 57, 24)     - Headings, primary text (4.5:1+ contrast)
Text weak:    HSB(hue, 27, 48)     - Secondary text (4.5:1+ contrast)
Stroke strong: HSB(hue, 23, 65)    - Form borders, icons (3:1+ contrast)
Stroke weak:  HSB(hue, 5, 94)      - Decorative borders
Fill:         HSB(hue, 2, 98)      - Secondary backgrounds
Background:   HSB(0, 0, 100)       - White or near-white
```

## Typography Scale (1.200 Minor Third)

```
Heading 1: 40px / 48px line-height / bold
Heading 2: 32px / 40px line-height / bold
Heading 3: 24px / 32px line-height / bold
Heading 4: 20px / 28px line-height / bold
Body:      16px / 24px line-height / regular
Small:     14px / 20px line-height / regular
```

## Spacing Scale (8pt Grid)

```
XS:  8pt   - Closely related elements
S:   16pt  - Related elements
M:   24pt  - Component padding
L:   32pt  - Grid gutters, section gaps
XL:  48pt  - Large section gaps
XXL: 80pt  - Page section padding
```
