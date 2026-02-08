# Typography

Learn a system of logical guidelines to make text beautiful and easy to read.

## Typeface Classifications

**Serif** - Decorative tails/feet at ends of letters. Traditional, classic, formal mood. Some legible at small sizes, others better for large.

**Sans Serif** - No decorative tails. Modern, simple. Highly legible at all sizes. Safe, neutral option for most interfaces.

**Script** - Based on handwriting. Low legibility - not suitable for small sizes. Can convey formal or casual mood at large sizes.

**Display** - Wide range of decorative styles. Designed for large sizes only. Strong character, good for conveying different moods.

**Monospaced** - Every character takes same horizontal space. Good for code and numbers (easier to compare).

## Use a Single Sans Serif Typeface

Safest for most interface designs.

### Reasons

**1. Legibility**
- Sans serif most legible
- Main purpose of interface text: clearly communicate information
- If not legible = harder to read, understand, use

**2. Neutrality**
- Don't convey strong mood/personality
- Fits most brand personalities
- Content is focal point, not typeface
- Less chance of unsuitable choice

**3. Simplicity**
- Less character and detail
- Complicated typefaces = distracting, increased cognitive load
- Less is more with typography

## Evoke Emotion Using a Second Typeface for Headings

As you get more confident, try second typeface for HEADINGS ONLY.

**Typeface Moods:**
- **Sans serif** - neutral, minimal, modern
- **Serif** - traditional, established, classic
- **Rounded sans serif** - fun, soft, playful
- **Casual script** - personal, handmade
- **Formal script** - formal, feminine, elegant
- **Light sans serif** - chic, modern, luxurious

## Tips for Choosing a Sans Serif Typeface

- Choose popular, tried and tested typefaces
- Look for variety of weights (light, regular, medium, semibold, bold)
- Look for taller lowercase letters (x-height) and greater letter spacing = more legible at small sizes
- Get inspiration from companies known for good design
- Ensure multi-language support if needed
- Look for OpenType features
- When in doubt, use default system typeface

## Normalize Font Sizes with font-size-adjust

Different fonts at the same `font-size` can appear vastly different in visual size due to varying x-heights (the height of lowercase letters). `font-size-adjust` normalizes this.

**Use cases:**
- **Fallback fonts:** Prevent layout shift when web fonts load
- **Mixing fonts:** Make a serif heading font and sans-serif body font work together with one type scale

```css
/* The value is the x-height ratio (x-height / font-size) */
body {
  font-family: "Custom Font", Arial, sans-serif;
  font-size-adjust: 0.5;  /* Normalize based on x-height */
}
```

**How to find the value:**
1. Measure your primary font's x-height ratio
2. Apply it - fallback fonts will scale to match visually

**Browser support:** 83%+ (Chrome 127+, Firefox 118+, Safari 17+)

## Limit Font Weights and Ensure Clear Distinction

Don't use all available weights - adds noise and clutter. More importantly: avoid weights that are too similar to distinguish.

**Problematic combinations (too close together):**
- Light vs Thin
- Book vs Regular
- Medium vs Regular
- Semibold vs Bold

**Guidelines:**
- Pick 2-4 weights with clear visual distinction
- Common useful set: Regular (400), Medium (500), Bold (700)
- Very thin or thick weights - headings/large text only (difficult at small sizes)
- Each weight should serve a clear purpose in your hierarchy

## Use a Type Scale to Set Font Sizes

Logical way to create balanced font sizes that work together.

### How to Create

1. Start with base font size (body text)
2. Multiply by scale factor for larger sizes

### Popular Type Scales (smallest to largest)
- 1.067 – Minor Second
- 1.125 – Major Second
- 1.200 – Minor Third
- 1.250 – Major Third
- 1.333 – Perfect Fourth
- 1.414 – Augmented Fourth
- 1.500 – Perfect Fifth
- 1.618 – Golden Ratio

### Example (1.200 Minor Third, base 16px)
```
Heading 1: 40px / 48px line-height / bold
Heading 2: 32px / 40px line-height / bold
Heading 3: 24px / 32px line-height / bold
Heading 4: 20px / 28px line-height / bold
Body:      16px / 24px line-height / regular
Small:     14px / 20px line-height / regular
```

**Tips:**
- Round to nearest whole number
- Try to make line-heights divisible by 4 (aligns to 4pt grid)
- Adjust as needed once confident

### Small vs Large Type Scales

**Small scales (e.g., Major Second):**
- Less difference between sizes
- Better for complex apps, tools, dashboards

**Large scales (e.g., Perfect Fifth):**
- Larger differences between sizes
- Better for simpler interfaces, marketing sites

### Responsive Type Scales

Instead of just scaling individual font sizes, scale the **type scale ratio itself** based on viewport width:

| Viewport | Scale Ratio | H1 | H2 | H3 | Body |
|----------|-------------|----|----|-----|------|
| 320px | 1.2 (Minor Third) | 35px | 29px | 24px | 17px |
| 1024px | (interpolated) | 50px | 39px | 31px | 19px |
| 1500px | 1.33 (Perfect Fourth) | 63px | 47px | 36px | 20px |

**Why this works:**
- Headings can be dramatically larger on desktop (63px H1) without being too big on mobile (35px)
- The hierarchy stays proportional at all sizes
- Smooth fluid interpolation - no breakpoint jumps

### Fluid Typography with clamp()

Use `clamp()` for font sizes that scale smoothly:

```css
/* clamp(minimum, preferred, maximum) */
h1 {
  font-size: clamp(35px, 5vw + 1rem, 63px);
}

h2 {
  font-size: clamp(29px, 4vw + 0.5rem, 47px);
}

.prose {
  font-size: clamp(17px, 1.5vw + 0.5rem, 20px);
}
```

**Benefits:**
- No hard jumps at breakpoints
- Smooth scaling between screen sizes
- Headings get proportionally bigger with more space

**Note:** For UI elements like buttons and labels, fixed sizes (14px) often work better for consistency.

## Distinguish UI Text from Body Text

**UI text** (buttons, labels, navigation, table cells) and **body text** (articles, descriptions, long-form content) have different requirements.

### UI Text: 14px is Fine

For compact UI components, 14px works well and is common practice (Tailwind's base size):

- Buttons, labels, navigation items
- Table cells, form labels, badges
- Sidebar content, metadata

14px keeps UI components compact - important when combined with padding.

### Body Text: Scale Responsively

For long-form reading content, don't leave text hard at 16px - scale it:

- **Mobile:** 16-17px is appropriate due to limited space
- **Tablet/Desktop:** 18-20px when there's room to breathe

```css
.prose {
  font-size: clamp(16px, 2.5vw, 19px);
}
```

### Input Fields: 16px Minimum on Mobile

iOS Safari auto-zooms inputs below 16px. See Forms chapter for details.

The key insight: avoid *both* tiny text that strains eyes *and* oversized text that wastes mobile screen space.

## Use at Least 1.5 Line Height for Long Body Text

**Line height** = vertical distance between two lines of text.

**For accessibility and readability:**
- Minimum 1.5 (150%) for body text
- Keep between 1.5 and 2

**Benefits:**
- Prevents rereading same line
- More comfortable to read

**Tips:**
- Longer lines = taller line height
- Darker/heavier typefaces = taller line height
- Typefaces that look larger = taller line height

## Set Paragraph Spacing to 1.5x Line Height

The gap between paragraphs should be noticeably larger than the gap between lines within a paragraph. A reliable rule: set paragraph spacing (margin) to 1.5 times the line spacing.

```css
p {
  line-height: 1.5;          /* 24px at 16px font-size */
  margin-block-start: 0;
  margin-block-end: 1.5em;   /* ~36px = 1.5 × 24px */
}
```

This creates a clear visual break between paragraphs while keeping the text block cohesive. Keep paragraphs to roughly 5 lines max for comfortable reading.

## Decrease Line Height as Font Size Increases

Large text doesn't need 1.5 line height.

**Reason:** Line height is relative to font size - same percentage creates larger actual gap on bigger text.

**Example:**
- Heading at 24px with 1.6 line height = large gap
- Change to 1.3 line height for consistent gap

## Ensure Ideal Line Length

**Optimal:** 40-80 characters per line (including spaces)

**Too long:**
- Hard to gauge where line starts/ends
- Eyes get lost tracking back

**Too short:**
- Eyes stressed from frequent travel back

**Guidelines:**
- Don't use full page width for text
- Align text block to left or centre of page
- Especially important for long body text

### Use ch Units for Line Length

The `ch` unit equals the width of the "0" character in the current font. This makes the 40-80 character guideline directly implementable:

```css
.prose {
  max-width: 65ch;  /* ~65 characters per line */
}
```

This automatically adapts to different font sizes and typefaces.

## Left Align Text

English read left to right, downwards in F-pattern.

**Left-aligned = easiest to read:**
- Each line starts at same left edge
- Consistent anchor for eyes

### Don't Centre Align Long Body Text
- Starting point changes each line
- Eyes work harder to find start
- OK for headings and short text

### Don't Justify Long Body Text
- Variations in letter/word spacing
- Harder to distinguish text and follow lines
- Especially hard for dyslexia
- Creates distracting "rivers" of white space

### Avoid Multiple Text Alignments
Harder to follow, looks messy.

## Decrease Letter Spacing for Large Text

**Letter spacing** = space between letters

**Guidelines:**
- Decrease letter spacing more as text gets bigger
- "Text type" typefaces designed for small sizes have wide letter spacing
- "Display type" typefaces designed for large sizes - may not need adjustment

## Use OpenType Features for Polished Typography

Modern fonts contain advanced features that improve readability and professional appearance. Use CSS `font-variant` and `font-feature-settings` to activate them.

### Small Caps

Use for abbreviations and words set in uppercase inside body text so they blend in better. Always use real small caps - never fake them by scaling down capitals.

```css
/* Real small caps */
.abbreviation {
  font-variant-caps: all-small-caps;
  font-feature-settings: "c2sc", "smcp";
}
```

Fake small caps (scaled-down capitals) have thinner strokes and look out of place next to regular text.

### Figure Styles

Figure styles split into two groups:

**Old-style vs Lining figures:**
- **Old-style figures** have varying heights (some descend below baseline) - better for body text as they blend in
- **Lining figures** are all the same height - better for headings and UI elements

```css
.body-text { font-variant-numeric: oldstyle-nums; }
.ui-numbers { font-variant-numeric: lining-nums; }
```

**Proportional vs Tabular figures:**
- **Proportional figures** have varying widths (natural spacing) - good for running text
- **Tabular figures** all take the same horizontal space - essential for tables, prices, and anywhere numbers need to align vertically

```css
.price-table { font-variant-numeric: tabular-nums; }
.prose       { font-variant-numeric: proportional-nums; }
```

### Ligatures

**Common ligatures** (fi, fl, ff, ffl, ffi) improve legibility in body text. Enabled by default in most browsers - don't disable them.

**Discretionary ligatures** are more ornamental. Use sparingly and only for decorative headings:
```css
.decorative-heading {
  font-variant-ligatures: discretionary-ligatures;
  font-feature-settings: "dlig";
}
```

### Proper Punctuation

Use the correct typographic marks:
- **Hyphen** (-) connects words: "five-dollar"
- **En dash** (\u2013) replaces "to": "6\u20135 p.m."
- **Em dash** (\u2014) indicates a break in thought: "Why is typography important?\u200A\u2014\u200AIt can also be used as an indicator of a break."
- **Curly quotation marks** (\u201c \u201d \u2018 \u2019) for prose - straight marks (' ") are for code only

## Ensure Text on Photos is Legible

Common mistake: placing text directly on photos.

**Contrast requirements:**
- Small text (≤18px): 4.5:1 minimum
- Large text (>18px bold OR >24px regular): 3:1 minimum

### Solutions

**Linear gradient overlay:**
- Dark grey, 90% opacity at bottom, 0% halfway up
- Add text shadow

**Semi-transparent overlay:**
- Dark grey, 50% opacity over entire photo
- Add text shadow

**Blurred semi-transparent overlay:**
- Add blur effect for easier reading

**Solid text background:**
- Popular for video captions
- White text on dark grey background

## Avoid Light Grey and Pure Black Text

**Light grey text:**
- Accessibility issue - many can't read or find difficult
- Always aim for 4.5:1 contrast minimum

**Pure black text:**
- Too high contrast causes eye strain and fatigue
- Black: 0% brightness, White: 100%
- Large difference makes eyes work harder
- Use accessible dark grey instead

## Chapter Summary

1. Limit to regular and bold weights in single sans serif typeface for legibility, neutrality, simplicity
2. Use type scale to create predefined font sizes that work together
3. Use 1.5+ line height for long body text; decrease line height as font size increases
4. Ensure 40-80 characters per line for readability
5. Left align text for optimal readability (F-pattern)
6. Use OpenType features: real small caps, tabular figures for data, common ligatures, proper punctuation marks
