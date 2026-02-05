# Colour

Learn how to use colour sparingly and purposefully to add meaning to an interface.

## Ensure Sufficient Contrast

Contrast = difference in perceived brightness between two colours (ratio 1:1 to 21:1).

### WCAG 2.1 Level AA Requirements

**3:1 Minimum - Large text and UI elements:**
- Text above 18px bold OR above 24px regular
- UI elements (form fields, buttons, checkboxes)
- Decorative elements don't need to meet this ratio

**4.5:1 Minimum - Small text:**
- Text 18px or less

### Common Contrast Issues
- Close icon contrast < 3:1
- Secondary text contrast < 4.5:1
- Search field border < 3:1
- Placeholder text < 4.5:1
- Button background against text < 4.5:1
- Link text contrast < 4.5:1

### APCA (Accessible Perceptual Contrast Algorithm)

Improved method in WCAG 3 draft - solves WCAG 2 limitations.

**APCA Contrast Values:**
- 90 - Preferred for body text (14px regular+)
- 75 - Minimum for body text (18px regular+)
- 60 - Minimum for other text (24px regular OR 16px bold+)
- 45 - Minimum for large text (36px regular OR 24px bold+) and UI elements
- 30 - Absolute minimum (placeholder text, disabled button text)
- 15 - Minimum for non-text elements

**Key differences from WCAG 2:**
- No ratios - uses contrast numbers (higher = more contrast)
- Value depends on text size AND weight
- Swapping text/background colours affects contrast
- Works better for dark interfaces

**Recommendation:** Use APCA for personal projects. For commercial projects requiring compliance, stick with WCAG 2 until WCAG 3 releases, but try to pass both.

## Don't Rely on Colour Alone to Convey Meaning

For accessibility to colour blind users:
- Use additional visual cues to differentiate elements
- Never use colour as the ONLY indicator

**Examples:**
- Form errors: Add icon + thicker border + background (not just red colour)
- Text links: Add underline (not just blue colour)

## Use System Colours to Indicate Status

**3 System Colours (Traffic light colours):**
- **Red (Error)** - negative message, error, urgent attention needed
- **Amber (Warning)** - caution, risky action
- **Green (Success)** - positive message, action completed

**Accessibility requirements:**
- Don't rely on system colours alone - use icons as additional cues
- System colours for text: minimum 4.5:1 contrast
- System colours for UI elements/icons: minimum 3:1 contrast

## Use Colour to Define Visual Hierarchy

Present information in order of importance.

### Saturation
- Higher saturation = more prominent
- Use saturated colours for important elements (links, buttons)

### Hue
- Certain hues are more prominent (red stands out most)
- Use prominent hues for important elements

### Contrast
- Higher contrast = more prominent
- Make headings darker than body text

## Use Black and White for Timeless Aesthetic

Benefits:
- Fewer distractions
- Highlights content
- Timeless look

**Design tip:** Design in black and white FIRST, regardless of brand colours. Focus on spacing, size, layout, contrast before adding colour.

**Proportion depends on brand:**
- Mostly white = simple, classic, minimal feel
- Mostly black = dramatic, powerful, luxurious feel

### Avoid Pure Black (#000000)
- High contrast against white causes eye strain
- Use dark grey instead
- Black: 0% brightness, White: 100% brightness - large difference strains eyes

## Add a Tinge of Colour to Black and White

Some brands add subtle colour tinge to differentiate.
- Get benefits of black/white interface
- Adjust mood with pinch of colour

## Use 1 Brand Colour

Single unique colour alongside black and white.

**Benefits:**
- Conveys brand mood/personality
- Can indicate interactive elements

**Colour Psychology Note:**
- Not universal - affected by culture, personal experience, colour blindness, surrounding elements
- Use as loose guideline only
- Test with users

**Tips for choosing brand colour:**
- Choose distinctive colour
- Remember system colours (red, amber, green) have strong meanings - using red for other elements causes confusion

## Apply Brand Colour to Interactive Elements

**Simple, effective approach:**
- Use brand colour for text links and buttons
- Teaches users what's interactive
- Don't add to ALL interactive elements (some already have visual cues)
- NEVER use brand colour on non-interactive elements

**CRITICAL:** Brand colour must have 4.5:1 contrast against background.

### What About Low Contrast Colours?

If brand colour is too light (e.g., yellow):
- Try darkening slightly (without losing brand recognition)
- Add text shadow to white button text
- Use text colour for button text/links
- Add border to buttons (3:1 contrast)

### If Brand Colour Has Meaning (Red/Green/Amber)
Avoid using for interactive elements to prevent conflicting meanings.

### Multiple Brand Colours
- Use highest contrast colour for interactive elements
- Use others sparingly for decorative elements
- NEVER use more than one colour for interactive elements

## Create a Colour Palette

Small set of predefined colours with rules governing usage.

### 5 Colour Variations (Solid Palette)

```
Brand:        HSB(hue, 65, 85)     - Interactive elements
              Must have 4.5:1 against fill

Text strong:  HSB(hue, 57, 24)     - Headings, primary text
              Very dark grey with brand tinge
              Must have 4.5:1 against fill

Text weak:    HSB(hue, 27, 48)     - Secondary text
              Dark grey with brand tinge
              Must have 4.5:1 against fill

Stroke strong: HSB(hue, 23, 65)    - Form borders, icons
              Medium grey with brand tinge
              Must have 3:1 against fill

Stroke weak:  HSB(hue, 5, 94)      - Decorative borders
              Light grey with brand tinge
              No contrast requirement (decorative only)

Fill:         HSB(hue, 2, 98)      - Secondary backgrounds
              Very light grey with brand tinge

Background:   HSB(0, 0, 100)       - White
```

### Interaction States

**Change opacity:**
- Default: 100%
- Hover: 80%
- Disabled: 20%
- Focus: outline

**Change fill colour:**
- Hover: Fill colour variation
- Press: Stroke weak colour variation

**Change elevation:**
- Hover: Add/increase shadow

**Toggle underline:**
- Text links: Remove underline on hover
- Navigation: Add underline on hover

**Use animation:**
- Move button up slightly on hover
- Keep subtle and quick

## Dark Colour Palette

```
Brand:        HSB(hue, 40, 99)
Text strong:  HSB(hue, 0, 100)     - White
Text weak:    HSB(hue, 5, 85)
Stroke strong: HSB(hue, 10, 65)
Stroke weak:  HSB(hue, 15, 25)
Fill:         HSB(hue, 20, 15)
Background:   HSB(hue, 30, 10)
```

**Tips:**
- Increase contrast above WCAG minimum (dark interfaces harder to see)
- Check with APCA for accuracy
- Start with white for Text strong
- Gradually increase saturation, decrease brightness
- Avoid pure black background

## Add Depth Using Colour and Shadows

Elements with higher elevation appear closer and more prominent.

### Define 2 Shadow Options
- **Raised** - small, sharp shadow for interactive elements (cards)
- **Overlay** - larger, softer shadow for floating elements (dropdowns, dialogs)

**Shadow tips:**
- Light comes from top (mimics real world)
- Use "Text strong" colour instead of black
- Small/sharp = slightly raised
- Large/soft = elevated higher

### Colour Indicates Depth
- Light colours look more elevated than dark
- Place lighter colours on top of darker colours

### Dark Interface Elevation
Shadows hard to see - rely on colour instead.

**3 Background Colours:**
- Base - darkest, main background
- Raised - slightly brighter
- Overlay - slightly brighter than raised

## Transparent Colours

Lower opacity makes colours see-through (alpha value 0-1).

### Problem with Solid Colours
Solid colours remain same regardless of background. Elements can have inconsistent prominence on different backgrounds.

### Transparent Colour Solution
Allows background to mix with foreground - maintains consistent prominence.

### Transparent Colour Palette (Dark Mode)

**5 variations of white:**
```
Text strong:   100% opacity (4.5:1 against overlay)
Text weak:     78% opacity (4.5:1 against overlay)
Stroke strong: 60% opacity (3:1 against overlay)
Stroke weak:   12% opacity (decorative)
Fill:          6% opacity
```

**5 variations of black (Light Mode):**
```
Text strong:   90% opacity (4.5:1 against fill)
Text weak:     60% opacity (4.5:1 against fill)
Stroke strong: 45% opacity (3:1 against fill)
Stroke weak:   10% opacity (decorative)
Fill:          4% opacity
```

**Brand colour variations (4 each for light/dark):**
- 100% - Brand
- 80% - Text
- 20% - Stroke strong
- 5% - Fill

**System colour variations (4 each for red/amber/green):**
- 100% - Text (4.5:1)
- 80% - Stroke strong (3:1)
- 20% - Stroke weak
- 5% - Fill

### Transparent Layers for Interaction States
- Hover: Fill colour variation overlay
- Press: Stroke weak colour variation overlay

## Naming Colours

### Primitive Colours
All available colours, named by appearance. Format: `[colour.mode.number]`
- Number 0-1000 indicates contrast level (1000 = highest)
- Example: `grey.light.1000`, `green.dark.800`

### Semantic Colours (Tokens)
Named based on how they should be used. Format: `[element.tone.emphasis.state]`

**Elements:** Text, Stroke, Icon, Fill, Background
**Tones:** Neutral, Brand, Error, Warning, Success
**Emphasis:** Strong, Weak
**States:** Hover, Press, Focus, Disabled

**Examples:**
- `text.error` - error messages
- `stroke.strong` - form field borders
- `fill.success.weak` - success alert backgrounds

## Adjust Photo Colour Temperature

Match photo colour temperature to palette for harmonious look:
- Cool palette (blue) = cooler photos
- Warm palette (orange) = warmer photos

Not for product photos where realistic colours matter.

## Chapter Summary

1. Ensure text/UI elements have sufficient contrast; don't rely on colour alone
2. Design in black and white first, then add colour purposefully (brand colour for interactive elements)
3. Create small predefined colour palette with usage rules
4. Consider transparent colours for consistent prominence across backgrounds
5. Name colours systematically based on usage
