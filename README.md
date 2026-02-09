# Effective UI Design

A [Claude Code](https://docs.anthropic.com/en/docs/claude-code) skill that applies UI design guidelines whenever you work on frontend code. Distilled from 20+ years of building web interfaces, updated for modern CSS (Baseline 2023-2025) and current accessibility standards.

Claude Code tends to produce generic, unstyled interfaces unless you tell it otherwise. This skill fixes that. It enforces consistent spacing, contrast ratios, typography, and layout patterns across everything it generates — without you having to repeat yourself.

## What it covers

| Topic | What's in there |
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

## Install

```bash
git clone git@github.com:sebastian-software/effective-ui-design-skill.git ~/.claude/skills/effective-ui-design
```

Or via HTTPS:

```bash
git clone https://github.com/sebastian-software/effective-ui-design-skill.git ~/.claude/skills/effective-ui-design
```

The skill activates automatically when Claude Code works on UI or frontend tasks.

## License

MIT — see [LICENSE](LICENSE) for details.

Copyright (c) 2026 [Sebastian Software GmbH](https://sebastian-software.de), Mainz, Germany.
