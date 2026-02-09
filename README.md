# Effective UI Design

You've seen it happen: Claude Code generates a form with thin gray text, buttons that all look the same, and spacing that feels random. You fix it, move on, and next time it happens again.

This [Claude Code](https://docs.anthropic.com/en/docs/claude-code) skill stops that cycle. Install it once, and every UI task follows professional design guidelines automatically. No reminding, no repeating yourself.

## The problem

Claude Code has no design opinion. Without guidance it defaults to:

- Text that fails WCAG contrast requirements
- Buttons with no visual hierarchy (everything looks equally important)
- Forms with no validation feedback or sensible field sizing
- Arbitrary spacing with no system behind it
- No consideration for dark mode, reduced motion, or screen readers

You can fix this per-prompt, but that gets old after the third time.

## What this changes

The skill loads 10 reference files covering the decisions you'd otherwise make by hand:

| Topic | What it handles |
|-------|----------------|
| [Fundamentals](references/01-fundamentals.md) | Interaction cost, cognitive load, affordance, animation, reduced motion, semantic HTML |
| [Less is more](references/02-less-is-more.md) | Progressive disclosure, mobile-first, when to remove rather than add |
| [Colour](references/03-colour.md) | OKLCH palettes, contrast ratios (WCAG 2.1 AA), dark mode, `light-dark()`, relative color syntax |
| [Layout & spacing](references/04-layout-spacing.md) | 8pt grid, container queries, subgrid, responsive images, safe areas, intrinsic layouts |
| [Typography](references/05-typography.md) | Type scale, fluid sizing with `clamp()`, OpenType features, vertical rhythm |
| [Web fonts](references/05b-webfonts.md) | `font-display`, preloading, variable fonts, fallback matching |
| [Copywriting](references/06-copywriting.md) | Concise text, sentence case, error messages, empty states |
| [Buttons](references/07-buttons.md) | Primary/secondary/tertiary weights, destructive actions, undo over confirmation |
| [Forms](references/08-forms.md) | Single column layout, validation with `:user-valid`/`:user-invalid`, dropdowns vs alternatives |
| [SEO](references/09-seo.md) | Meta tags, structured data (JSON-LD), Core Web Vitals, internal linking |

Built on 20+ years of shipping web interfaces. Updated for modern CSS (Baseline 2023-2025) and current accessibility standards.

## What it doesn't do

This isn't a component library or a CSS framework. It doesn't generate design tokens or output Figma files. It's a set of rules that shape how Claude Code thinks about UI, so the code it writes starts closer to where you'd end up anyway.

## Install

```bash
git clone git@github.com:sebastian-software/effective-ui-design-skill.git ~/.claude/skills/effective-ui-design
```

Or via HTTPS:

```bash
git clone https://github.com/sebastian-software/effective-ui-design-skill.git ~/.claude/skills/effective-ui-design
```

One command. The skill activates automatically whenever Claude Code works on frontend tasks. Nothing to configure.

## License

MIT — see [LICENSE](LICENSE) for details.

Copyright (c) 2026 [Sebastian Software GmbH](https://sebastian-software.de), Mainz, Germany.
