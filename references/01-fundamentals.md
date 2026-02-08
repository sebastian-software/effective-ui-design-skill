# Fundamentals

Overarching UI design principles that form the foundation of all guidelines.

## Minimise Usability Risks

Base design decisions on risk - the risk that someone could have difficulty using an interface.

**Common usability risks:**
- Thin, light grey text - some may find it difficult to read
- Icons without labels - some might not understand what icons mean (especially those with cognitive/vision impairments)
- Coloured headings - could be mistaken for links
- Navigation with only arrows/dots (e.g. carousels) - use descriptive labels instead that tell users what content awaits them

**Guidelines:**
- Consider people with poor eyesight, low computer literacy, reduced dexterity and cognitive ability
- Meet WCAG 2.1 level AA requirements as minimum
- Keep an eye out for potential usability risks
- If anything is slightly vague, confusing or unclear - simplify it

## Have a Logical Reason for Every Design Detail

Every element must have a purpose that improves usability.

- Design using objective logic, rather than subjective opinion
- Be able to articulate the rationale behind each decision
- "That looks nice" or "I don't like it" are NOT logical or constructive feedback
- Focus on HOW it works and WHY it works that way

## Minimise Interaction Cost

Interaction cost = sum of physical and mental effort required to achieve a task.

**Actions that add to interaction cost:**
- Looking, scrolling, searching, reading
- Clicking, waiting, typing
- Thinking, remembering

### How to Minimise Interaction Cost

**1. Keep related actions close (Fitts's Law)**
- The closer and larger a target, the faster it is to click
- Keep actions close to the element they relate to
- Ensure sufficient target area: minimum 48pt x 48pt

**2. Reduce distractions**
- Avoid animated banners, pop-ups, unnecessary visuals
- Remove attention-grabbing elements that pull focus from tasks

**3. Minimise choice (Hick's Law)**
- Time to make a decision increases with number and complexity of choices
- Reduce choices to speed up decisions
- Highlight recommended or popular items

## Minimise Cognitive Load

Cognitive load = amount of brain power required to use an interface.

**Quick ways to reduce cognitive load:**
- Remove unnecessary styles, information, and decisions
- Break up information into smaller groups
- Use conventional design patterns (Jakob's Law)
- Maintain consistency - similar elements look and work similarly
- Create clear visual hierarchy

## Create a Design System

A system of predefined options and guidelines for efficient design decisions.

### 1. Set Predefined Style Options

**Colour Options (Colour Palette):**
```
Brand       - Interactive elements (buttons, links)
Text strong - Headings, primary text
Text weak   - Secondary text
Stroke strong - Form borders, icons
Stroke weak - Decorative borders
Fill        - Secondary backgrounds
Background  - White or near-white
```

**Typography Options (Type Scale 1.200):**
```
Heading 1: 40px / 48px line-height / bold
Heading 2: 32px / 40px line-height / bold
Heading 3: 24px / 32px line-height / bold
Heading 4: 20px / 28px line-height / bold
Body:      16px / 24px line-height / regular
Small:     14px / 20px line-height / regular
```

**Spacing Options (8pt Grid):**
```
XS:  8pt   - Closely related elements
S:   16pt  - Related elements
M:   24pt  - Component padding
L:   32pt  - Grid gutters, section gaps
XL:  48pt  - Large section gaps
XXL: 80pt  - Page section padding
```

**Shadow Options:**
- Raised - small, sharp shadow for interactive elements like cards
- Overlay - larger, softer shadow for dropdowns, floating dialogs

**Border Radius Options:**
- Small: 8pt
- Medium: 16pt
- Large: 32pt

### 2. Create Reusable Modules

- Start with smallest components (buttons, avatars, form inputs)
- Combine small components to create larger ones
- Arrange components in specific layouts for reusable page templates
- Create a component library / UI kit

### 3. Define Usage Guidelines

- How to use components and visual styles
- How to write interface text (copywriting)
- Examples from the book:
  - Indicate interactive elements using brand colour
  - Use sentence case
  - Left align buttons and text
  - Avoid disabled buttons
  - Front-load text
  - Be concise, use plain language

## Ensure an Interface is Accessible

Design interfaces that can be used by everyone, regardless of disability.

**Consider:**
- Blindness, low vision, colour blindness
- Motor impairment
- Mental disabilities

**Key principles:**
- Provide comparable experience for all
- Meet WCAG 2.1 level AA as minimum
- Include people with disabilities in usability testing

### Use Semantic HTML

Use meaningful HTML elements instead of generic `<div>` everywhere:

```html
<!-- Don't: ambiguous structure -->
<div>
  <div>Logo + Nav</div>
  <div>
    <div>Main content</div>
    <div>Sidebar</div>
  </div>
  <div>Footer</div>
</div>

<!-- Do: clear structure -->
<header>Logo + Nav</header>
<nav>Navigation</nav>
<main>
  <section>Main content</section>
  <aside>Sidebar</aside>
</main>
<footer>Footer</footer>
```

**Why it matters:**
- Screen readers use semantic elements to navigate (jump to `<nav>`, skip to `<main>`)
- Improves SEO and machine readability
- Makes code self-documenting

**Key elements:** `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`, `<figure>`, `<figcaption>`

### Assistive Technology

**Screen Readers:**
- Software that describes interface using speech or braille
- Users use keyboard to step through elements
- Mobile users swipe or drag finger across screen

**Screen Magnifiers:**
- Enlarges part of interface for people with low vision
- Users have limited view - can only see small part at a time
- Important: Keep this in mind when designing

### Good Accessibility Benefits Everyone

- Anyone could get temporary disability (eye/arm injury)
- Situational disabilities (bright sunny day affecting screen visibility)
- Good accessibility = great usability

## Design for Affordance

Affordance is an object's ability to convey its function through its appearance. A raised button suggests pressing; a handle suggests pulling; text that flows off the edge suggests scrolling.

**In digital design:**
- Buttons should look tappable (depth, fill colour, hover states)
- Scrollable areas should show partial content at the edges to hint at more
- Draggable items should have grab handles or visual weight
- Input fields should look like containers that accept text

**The risk of flat design:** Removing all depth cues can make interfaces ambiguous. Ensure interactive elements are still distinguishable from static content through colour, weight, or shape.

## Use Common Design Patterns (Jakob's Law)

Stick with conventional design patterns that people are already familiar with.

- Building on existing mental models means less learning time
- Reduces usability issues, cognitive load, and interaction cost
- Example: Accordion components for expandable content

**Play it safe:**
- Use conventional form field styles
- Save time on usability testing
- Focus creativity on unique selling points

## Use the 80/20 Rule (Pareto Principle)

Roughly 80% of effects come from 20% of causes.

**In product design:**
- ~80% of users use 20% of features
- ~80% of complaints come from 20% of issues
- ~80% of attention is spent on 20% of a page

**Application:**
- Prioritise the small number of things with largest impact
- Optimise for tasks most people will be doing
- Don't over-invest in edge cases

## Keep Costs in Mind

Every minute spent costs money.

**Ways to improve efficiency:**
- Use existing design systems, templates, icon sets
- Outsource time-intensive tasks
- Stick with familiar UI patterns
- Learn technical constraints of implementation
- Talk to developers early and often
- Simple approach is usually cheaper and easier

## Be Consistent

Similar elements look and work in a similar way.

### Within Your Product
- Create design system with guidelines for components, templates, visual styles, language
- Predictable functionality improves usability and reduces errors

### With Other Products
- Maintain consistency with well-established products
- Follow platform guidelines (iOS, Android) unless they test poorly
- Follow well-established, accessible UI patterns

**Conventional patterns:**
- Text links are underlined
- Checkboxes are small squares with tick icon
- Input fields are rectangles with label on top

## Clearly Indicate Interaction States

Interactive elements must change appearance when interacted with.

**8 Interaction States Checklist:**

| State | When | Design Treatment |
|-------|------|------------------|
| **Default** | At rest | Base styling |
| **Hover** | Pointer over (not touch) | Subtle lift, colour shift |
| **Focus** | Keyboard/programmatic focus | Visible focus ring |
| **Active/Press** | Being clicked/tapped | Pressed in, darker |
| **Disabled** | Not interactive | Reduced opacity, no pointer |
| **Loading** | Processing | Spinner, skeleton |
| **Error** | Invalid state | Red border, icon, message |
| **Success** | Completed | Green check, confirmation |

**Common miss:** Designing hover without focus. Keyboard users never see hover states - they need visible focus indicators.

### Focus Rings with :focus-visible

Never remove focus indicators without replacement - it's an accessibility violation.

```css
/* Show focus ring only for keyboard navigation (~96% support) */
:focus-visible {
  outline: 2px solid var(--brand);
  outline-offset: 2px;
}
```

Browsers that support `:focus-visible` automatically suppress focus rings on mouse/touch clicks. No need for a separate `:focus { outline: none }` rule.

**Focus ring requirements:**
- High contrast (3:1 minimum against adjacent colours)
- 2-3px thick
- Offset from element (not inside it)
- Consistent across all interactive elements

## Animation and Motion

Animation adds context that static interfaces can't provide. It offloads spatial reasoning to the brain's visual cortex, reducing cognitive load and increasing perceived speed. But animation is a powerful tool that must be used purposefully — decorative animation wears on users after the fiftieth viewing.

**The test for good animation:** If users notice your animation, it may be doing too much. Good microinteraction animations are seamless — users don't consciously register them, they just feel the interface is responsive and clear.

### Animation Patterns

Use these categories to identify and communicate the purpose of an animation:

| Pattern | Purpose | Example |
|---------|---------|---------|
| **Transition** | Move users between places/tasks in the information space | Page-to-page slide, tab switching |
| **Supplement** | Bring info on/off page without changing location or task | Tooltip appearing, dropdown opening |
| **Feedback** | Connect user action to interface reaction | Button press ripple, form validation |
| **Demonstration** | Show how something works instead of telling | Onboarding walkthrough, feature tour |
| **Decoration** | Purely aesthetic, no new information | Background particle effects |

**Prioritisation:** Transitions and feedback provide the most cognitive benefit. Decorations provide the least and risk annoying users. When resources are limited, prioritise animations that answer "What just happened?" for the user.

**Questions to justify an animation:**
- Does it show the user where information came from or went to?
- Does it indicate progress?
- Does it move the user through an information space?
- Does it explain something faster than words could?

### The Cone of Vision

The eye is most sensitive to colour and detail at the centre (foveal region). Peripheral vision is blurry but highly sensitive to motion.

**Practical implications:**
- **Centre of vision:** Colour fades and small movements are sufficient to draw attention
- **Peripheral vision:** Use motion to attract attention — colour changes alone may go unnoticed
- Two independently moving objects on opposite sides of the screen cannot both be tracked
- Overusing motion causes "banner blindness" — the brain learns to ignore excessive animacy

### Easing (Timing Functions)

Easing describes the rate of change over time. Different easings suit different situations:

| Easing | CSS | Best For |
|--------|-----|----------|
| **Ease-out** (deceleration) | `ease-out` | User-initiated actions (clicks, taps). Feels snappy and responsive |
| **Ease-in** (acceleration) | `ease-in` | System-initiated animations (alerts, pop-ups). Starts slowly, less startling |
| **Ease-in-out** | `ease-in-out` | Moving elements toward each other |
| **Linear** | `linear` | Fades and colour changes only. Motion with linear easing looks mechanical |

For unique brand feel, use custom `cubic-bezier()` curves. Keep a chart of your project's easings to maintain consistency.

### Duration (Timing Scale)

Use a predefined set of durations for consistency, similar to a typographic scale:

```
Immediate:  100ms  — Fades, colour changes under cursor/finger
Fast:       300ms  — Button presses, toggles, responsive interactions
Slower:     400ms  — Elements moving on page, dropdowns, tooltips
Deliberate: 700ms  — Large movements across screen, demonstrations
```

These values follow a Fibonacci-like relationship (100 + 300 = 400, 300 + 400 = 700) creating natural harmony.

**Guidelines:**
- Colour/opacity changes under the cursor feel slow above 100ms
- Moving elements across the page needs 300ms+ to track
- Centre-of-vision animations need shorter durations (70-200ms)
- Peripheral animations benefit from longer durations (300-700ms)
- When in doubt, halve your duration — developers consistently overestimate how long animations should run

### Only Animate Transform and Opacity

For smooth 60fps animations, only animate `transform` and `opacity`. Other properties (width, height, margin, padding) trigger expensive layout recalculations.

```css
/* Good - GPU accelerated */
.card:hover {
  transform: translateY(-2px);
  opacity: 0.9;
}

/* Avoid - triggers layout */
.card:hover {
  margin-top: -2px;
  height: 102%;
}
```

A consistent frame rate matters more than a high one — a steady 30fps looks smoother than 60fps with dips.

### Every Entrance Needs an Exit

When something animates onto the screen, it must also animate as it leaves. Alerts that beautifully slide in but instantly vanish on dismissal make the interface feel unfinished. Invest in a system that waits for exit animations to complete before removing elements.

### Avoid Flashes of Unloaded States (FOULS)

When loading content dynamically, ensure users never see empty/unloaded pages:

1. Start in a **loading state** (skeleton screens, shimmer placeholders)
2. **Transition** loaded content in smoothly
3. Never show the unloaded state — build with an "always be loading" mentality

### Signal Oncoming Animations

Anticipatory animation helps users mentally prepare. For example, hovering over a collapsible sidebar can cause it to slightly shift in the direction it will expand if clicked.

### Respect Reduced Motion Preferences

Vestibular disorders affect ~35% of adults over 40. Seizure-triggering animations can be dangerous — never flash elements more than twice per second.

```css
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    transition-duration: 0.01ms !important;
  }
}
```

Replace motion-based animations with fades for users who prefer reduced motion — fades do not trigger vestibular disorders.

## Chapter Summary

1. Minimise usability risk by keeping interfaces simple and familiar
2. Every interface detail needs a logical reason behind it
3. Minimise interaction cost and cognitive load as much as possible
4. Create a design system of predefined styles, modular components, and usage guidelines
5. Good accessibility means great usability - design for everyone
6. Use animation purposefully to add context — prioritise transitions and feedback over decoration
