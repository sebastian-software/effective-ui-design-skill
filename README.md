# Effective UI Design Skill

A comprehensive UI design skill for [Claude Code](https://docs.anthropic.com/en/docs/claude-code) that enforces professional design guidelines for creating intuitive, accessible, and beautiful interfaces.

## Features

- **Accessibility First**: WCAG 2.1 Level AA compliance built-in
- **Complete Design System**: Color, typography, spacing, layout guidelines
- **Component Guidelines**: Buttons, forms, and interactive elements
- **Copywriting Rules**: Clear, concise interface text

## Installation

Clone this repository into your Claude Code skills directory:

```bash
git clone git@github.com:sebastian-software/effective-ui-design-skill.git ~/.claude/skills/effective-ui-design
```

Or using HTTPS:

```bash
git clone https://github.com/sebastian-software/effective-ui-design-skill.git ~/.claude/skills/effective-ui-design
```

## What's Included

| Topic | Description |
|-------|-------------|
| Fundamentals | Usability, interaction cost, cognitive load, accessibility |
| Less is More | Progressive disclosure, minimalism, mobile-first |
| Colour | Contrast ratios, WCAG 2.1, color palettes, dark mode |
| Layout & Spacing | 8pt grid, 12-column layout, visual hierarchy |
| Typography | Type scale, line height, font weights |
| Copywriting | Concise text, sentence case, error messages |
| Buttons | Primary/secondary/tertiary weights, target sizes |
| Forms | Single column, validation, field styling |

## Key Guidelines

### Accessibility
- Text contrast: minimum 4.5:1 ratio (small text ≤18px)
- Large text/UI elements: minimum 3:1 ratio
- Target areas: minimum 48pt × 48pt

### Typography
- Body text: minimum 18px for long text
- Line height: minimum 1.5 for body text
- Line length: 40-80 characters

### Spacing (8pt Grid)
```
XS:  8pt   - Closely related elements
S:   16pt  - Related elements
M:   24pt  - Component padding
L:   32pt  - Grid gutters
XL:  48pt  - Large section gaps
XXL: 80pt  - Page section padding
```

## Usage

Once installed, the skill automatically activates when you work on UI/frontend tasks in Claude Code. It ensures all created UI content follows professional design guidelines.

## License

MIT License - see [LICENSE](LICENSE) for details.
