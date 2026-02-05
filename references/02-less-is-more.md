# Less is More

Practical techniques to simplify interfaces by removing unnecessary details.

## Remove Unnecessary Information

Every element competes with existing elements and can make things harder to understand.

**Guidelines:**
- Remove repeated elements to instantly simplify without losing information
- Avoid unneeded words and introductory phrases
- Reveal less important information gradually (progressive disclosure)
- Ensure every interface element has a logical reason behind it

**Example:** Course name repeated in each chapter title - make course name a subheading instead.

## Remove Unnecessary Styles

Unnecessary styles = those that don't convey information (purely decorative).

**Avoid:**
- Unnecessary lines, colours, backgrounds, animations
- Decorative colours without purpose (could confuse users who assume colours have meaning)
- Blue/underlined headings that aren't links
- Decorative icons that could be confused for buttons
- Very prominent icons that compete for attention

**Style Trends Fade:**
- Trendy effects age poorly
- Minimal styles highlighting quality content are better for longevity
- Some styles aren't practical (Glassmorphic, Neumorphic) - cause accessibility/hierarchy issues

**IMPORTANT:** Don't let aesthetics hinder usability or exclude people.

## Not All Links Need to Be Underlined

For accessibility, text links should be coloured and underlined. EXCEPT when elements already look interactive:

**Elements that can skip conventional link treatment:**
- Navigation menus
- Cards (image + text in raised container)
- Tabs

**When to remove colour from links:**
- When blue underlined text makes links too prominent
- When it confuses visual hierarchy
- Keep underline, remove colour to correct hierarchy

## Use Progressive Disclosure

Reveal information gradually as needed.

**Benefits:**
- Reduces cognitive load
- Speeds up decision making
- Shows only what's needed for current task

**Implementation:**
- Use descriptive labels for text links
- Show additional information via expandable sections
- Use opt-in checkboxes to reveal additional form fields

**Example:** Instead of optional mobile number field, use checkbox "Receive updates via text message" - when checked, reveal required mobile number field.

## Don't Confuse Minimalism with Simplicity

**Minimal ≠ Simple**

Minimal interfaces can be vague or confusing - lack crucial details for usability.

**Common issues in minimal interfaces:**
- Unlabelled pages, filters, navigation
- Very subtle selected states
- Hidden share/save actions
- Insufficient icon contrast

**Fix by ensuring:**
- Important actions are clearly visible
- Elements are properly labelled
- Sufficient contrast on all elements

## Make Sure Important Content is Visible

People don't use what they can't see.

**Guidelines:**
- Hiding behind menus is convenient but risky
- If there's space, ensure important content is visible when needed
- Make hidden content discoverable (expose edges of off-screen cards)

## Design for the Smallest Screen First

Mobile-first approach benefits:
- Restricted space forces prioritisation
- Removes unnecessary elements
- Results in simpler interfaces on larger screens too

**Why it works:**
- Large screens encourage filling space with unnecessary information
- More information = increased cognitive load
- More information = slower decision making
- You don't need to fill the screen

## Reduce Choice to Speed Up Decision Making

**Hick's Law:** Time to decide increases with number and complexity of choices.

### 4 Ways to Reduce Choice

**1. Remove choices**
- Ensure every option earns its place
- If not necessary, it's a potential distraction
- Example: Remove unnecessary form fields

**2. Group or categorise choices**
- Simpler to decide between categories than large lists
- Example: Break articles into categories (Interiors, Architecture, Gardens)

**3. Break up choices into multiple steps**
- Large complex tasks seem less overwhelming
- Decreases cognitive load
- Focus on one thing at a time
- Example: Multi-step forms, multi-level navigation menus

**4. Recommend choices**
- Suggest popular or common choices
- If many prefer certain choices, others likely will too
- Example: Video streaming recommending popular videos
- Example: Search boxes suggesting common terms

## Chapter Summary

1. Remove unnecessary information and styles to reduce cognitive load
2. Reveal information gradually (progressive disclosure) to avoid overwhelming users
3. Minimal ≠ Simple - don't remove critical information for aesthetics
4. Ensure important content is visible or discoverable
5. To help people decide faster: remove choices, group them, break into steps, or offer recommendations
