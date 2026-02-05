# Layout and Spacing

Create a consistent spacing system and learn about alignment and layout.

## Group Related Elements

Breaking up information into smaller groups helps structure and organise an interface.

### 4 Grouping Methods

**1. Place related elements in the same container**
- Strongest visual cue for grouping
- Create containers using borders, shadows, background colours
- Use for main structure (headers, sidebars, content areas)
- Cards and dialog boxes group smaller related content
- Avoid containers for EVERY group - causes clutter

**2. Space related elements close together (Proximity)**
- Related elements closer together
- Unrelated elements further apart
- Can help declutter vs containers

**3. Make related elements look similar (Similarity)**
- Similar visual characteristics: size, shape, colour
- Highlight certain elements by making them slightly different
- If elements look similar, they should FUNCTION similarly
- Don't make non-interactive elements look like buttons

**4. Align related elements in a continuous line (Continuity)**
- Eyes naturally follow elements aligned in lines
- Lists group related elements
- Disrupt continuity to indicate end of group or highlight element

### Combining Methods
Use multiple methods together for clearer groupings. If elements are grouped multiple ways, you can often remove containers to simplify.

## Create a Clear Visual Hierarchy

Present information in order of importance.

### Methods to Control Prominence

**Size** - Make important elements larger

**Colour** - Use brighter, richer, warmer, higher contrast colours for important elements

**Contrast** - Style important elements differently to stand out

**Spacing** - Surround important elements with more space

**Position** - Place important elements toward top or first in row

**Depth** - Elevate important elements (appear closer)

### Practical Steps to Improve Visual Hierarchy

1. Group related information into separate sections
2. Order information in each section by importance
3. Order sections by importance (most important = top)
4. Change element styles based on importance:
   - Important: large, bold, "Text strong" colour
   - Secondary: smaller, regular weight, "Text weak" colour
   - Use icons for common patterns (star ratings)
   - Important CTAs: primary button with brand colour
   - Less important details: remove unnecessary labels

## Test Visual Hierarchy - The Squint Test

Quick test: Squint at your design (or blur/step back).

**Should be able to:**
- Tell what most important elements are
- Recognise what interface is for

## Use Depth to Create Visual Hierarchy

**Elevation:**
- Higher elevation = closer, more prominent
- Lower elevation = further away, less prominent
- Elevate important elements higher
- Elevation can make elements feel interactive

## Understand the Box Model

Interfaces = rectangles within rectangles.

**Each rectangle has:**
- **Margin** - space between box and neighbouring boxes
- **Border** - stroke around edge
- **Padding** - space between border and contents

**Key observation:** Spacing starts small in innermost rectangles and increases moving outwards.

## Design @1x Using Points

**Points vs Pixels:**
- @1x: 1pt = 1px
- @2x: 1pt = 4px (2x2)
- @3x: 1pt = 9px (3x3)

Always work in points (@1x).

## Create a Set of Predefined Spacing Options

**8pt Grid (T-shirt sizes):**
```
XS:  8pt   - Closely related elements
S:   16pt  - Related elements
M:   24pt  - Component padding
L:   32pt  - Grid gutters, section gaps
XL:  48pt  - Large section gaps
XXL: 80pt  - Page section padding
```

**Why 8pt?**
- Many screen sizes divisible by 8
- More flexibility than 10pt
- For detailed interfaces, use 4pt increments

**Benefits:**
- Simplified designs (less variation)
- Improved consistency
- Design faster (fewer options)

## Space Elements Based on How Closely Related They Are

**Key principle:** More closely related = closer together

### Application Method
1. Break interface into rectangles within rectangles
2. Start with XS (8pt) for innermost rectangles
3. Gradually increase spacing moving outwards

**Example spacing progression:**
- XS (8pt): Card text (closely related)
- M (24pt): Card padding, section content
- L (32pt): Between navigation links, between cards (grid gutters)
- XXL (80pt): Page section vertical padding

### Create Spacing Rules
Example rules for consistency:
- M (24pt) internal padding for components
- L (32pt) gaps between columns
- XXL (80pt) vertical padding for sections

## Be Generous with White Space

White space = empty space between/around elements (can be any colour/pattern).

**Benefits:**
- Easier to see groupings and hierarchy
- Easier to understand information
- Looks simpler, cleaner, more sophisticated

**Tip:** Instead of XS spacing option, consider using next one up.

**Test:** Use Squint Test - if you can't distinguish elements, increase spacing.

## Align the Main Layout to a 12 Column Grid

**Components:**
- **Columns (12)** - vertical columns for aligning main elements
- **Gutters** - empty spaces between columns (separate/align content)
- **Margins** - empty space on left/right edges

### Columns
- Align main containers to one or more columns
- Smaller elements inside don't need to align to grid
- Generally flexible width (percentages)
- 12 columns for large screens, fewer for mobile

**Example:** 3 cards spanning 4 columns each on desktop, stack on 4 columns on mobile.

### Gutters
- Remain empty
- Narrower than columns
- Fixed width, wider on larger screens
- Example: L (32pt) on desktop, S (16pt) on mobile

### Margins
- Prevent content hitting edges
- Fixed or flexible width
- Wider on larger screens
- Example: XXL (80pt) on desktop, S (16pt) on mobile

**Why 12?** Most common, sufficient flexibility, aligns with frontend frameworks.

## Align Text to Improve Readability

**Left-aligned text is easiest to read:**
- Consistent left edge = anchor for eyes
- Maintain straight left edge with other elements (icons)

### Align Horizontal Text to Baseline
- Baseline = invisible line text sits on
- Different sized text in same line: align to baseline (not vertical centre)
- Creates easier reading, neater design

## Try to Avoid Using Multiple Alignments

Fewer alignments = simpler, neater.

**Issues with multiple alignments:**
- Eyes work harder moving around
- Looks messy
- Increases cognitive load

**Tip:** If you must use centre alignment, full-width buttons help both left/right handed users reach easily.

## Keep Related Actions Close (Fitts's Law)

**Fitts's Law:** Closer and larger target = faster to select.

**Application:**
- Keep actions close to related elements
- Ensure sufficient target area (48pt x 48pt minimum)
- Move close buttons to start position (near menu icon)
- Increase size of menu items for faster/easier tapping
- Add visible borders to indicate target area

## Ensure an Interface is Unbreakable

Don't just design for short text and small numbers.

**Guidelines:**
- Accommodate long data and edge cases
- Avoid hiding essential overflowing data
- Keep components flexible for content reflow
- Or decrease font sizes for long data

**If hiding is necessary:**
- Don't hide essential information
- Consider cropping in middle (not end) to help differentiate items

## Use the Rule of Thirds for Photos

Divide photo into 3x3 grid = 4 focal points at intersections.

**Application:**
- Align key elements to grid
- Place main subject on focal point
- Don't centre subjects - creates rigid, still appearance
- Asymmetry introduces natural motion and flow
- Align horizon with horizontal grid

**Especially effective for:**
- Action shots (increases sense of motion)
- Landscapes (align horizon to grid)

## Chapter Summary

1. Group related elements using containers, proximity, similarity, or continuity
2. Create clear visual hierarchy using size, colour, contrast, spacing, position, depth
3. Interfaces = rectangles within rectangles with margin, padding, border (box model)
4. Create predefined spacing options in 8pt increments; space based on relationship
5. Align to 12-column grid; avoid multiple different alignments
