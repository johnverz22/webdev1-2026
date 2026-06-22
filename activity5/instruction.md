# Activity 5: Component Styling Challenge

Welcome to your CSS component sandbox! In this activity, you will move beyond styling entire page templates to craft specific, reusable UI components. Using CSS, you will design five distinct modern components from scratch.

## Workspace Setup

1. Create a folder named `activity5`.
2. Inside, create two files:
   - `index.html` (for your HTML structures)
   - `style.css` (for your CSS rules)
3. Link the stylesheet in your HTML's `<head>`.
4. Render all five components in order on your page, separating them clearly (e.g. with a border, margin, or heading in between).

---

## Component Specifications

### 1. The Blockquote Card
A quote card meant for articles or testimonials.
- **HTML Structure**: A parent container (e.g., `<div class="quote-card">`) containing a `<blockquote>` for the quote text, and a `<cite>` for the author/source.
- **CSS Styling**:
  - Background color: `#FFF8F0` (light cream/orange tint)
  - Left border: `6px solid #F97316` (vibrant orange)
  - Internal spacing: `24px` top/bottom, `28px` left/right
  - Maximum width: `300px`
  - Rounded corners: `8px` on the right side only (`border-radius: 0 8px 8px 0`)
  - Typography: Serif font (e.g., `Georgia, serif`), font-size `1rem`, color `#1C1917`, line-height `1.6`, and italicized style.
  - Cite block: Uppercase, non-italic, sans-serif font, small size, muted color `#78716C`, with `1px` letter-spacing.

### 2. Stat Counter Row
A row displaying key statistics, common on landing pages.
- **HTML Structure**: A parent container (e.g., `<div class="stats-row">`) housing three individual stat items, each with a number span/heading and a label span.
- **CSS Styling**:
  - Container: Use Flexbox (`display: flex`), gap `0`, background `#1E1B4B` (deep indigo), and rounded corners of `10px`.
  - Stat Items: Distribute space equally (`flex: 1`), center text, padding of `20px` top/bottom and `16px` left/right, and a thin border on the right (`1px solid #312E81`) except for the last item.
  - Stat Numbers: Block display, font-size `1.8rem`, bold, color `#A5B4FC`.
  - Stat Labels: Block display, font-size `0.7rem`, color `#818CF8`, uppercase with `1.5px` letter-spacing.

### 3. Input Field Label
A clean, accessible form input field component.
- **HTML Structure**: A wrapper element containing a `<label>`, an `<input type="text">` with a placeholder, and a helper text element.
- **CSS Styling**:
  - Layout: Stacks elements vertically (`display: flex` with `flex-direction: column` and gap `6px`), width `260px`.
  - Label: Font-size `0.8rem`, bold, color `#1E3A5F`, letter-spacing `0.5px`.
  - Input: Padding `10px 14px`, border `2px solid #CBD5E1`, border-radius `6px`, background `#F8FAFC`.
  - Focus State: Transition/state showing a blue border (`#3B82F6`) and a light blue background (`#EFF6FF`) with no outline when selected/clicked.
  - Helper Text: Small muted text (`0.72rem`, color `#64748B`) below the input.

### 4. Gradient Text Banner
A banner card featuring a modern gradient text heading.
- **HTML Structure**: A container containing an `<h2>` heading and a descriptive `<p>` paragraph.
- **CSS Styling**:
  - Container: Centered text, padding `28px 32px`, dark background `#0F0F23`, and rounded corners of `10px`.
  - Heading: Font-family `Georgia`, font-size `2rem`, bold weight, and a background gradient `linear-gradient(90deg, #F97316, #EC4899, #8B5CF6)` clipped to the text (`-webkit-background-clip: text` and `-webkit-text-fill-color: transparent`).
  - Paragraph: Font-size `0.82rem`, color `#6B7280`.

### 5. Price Tag with Strikethrough
A price showcase element for product pricing plans.
- **HTML Structure**: A card housing a plan label, an old original price, a new discounted price, and a discount/save badge.
- **CSS Styling**:
  - Card: White background, thin border `#E2E8F0`, rounded corners `10px`, padding `24px 28px`, text-align center, width `200px`, and a subtle shadow.
  - Plan Label: Small uppercase letter-spaced muted text at the top.
  - Old Price: Font-size `1rem`, color `#94A3B8` with a strikethrough line (`text-decoration: line-through`).
  - New Price: Large font-size `2rem`, bold weight, green color `#16A34A`.
  - Save Badge: Displayed below, background color `#DCFCE7`, text color `#16A34A`, small bold font, and fully rounded pill shape (`border-radius: 20px`).

---

## Grading Rubric

- Blockquote Card (4 points)
  - Correct HTML structure using blockquote and cite elements
  - Proper box model styles applied (background color, left border, specific padding, max-width, border-radius)
  - Matches requested serif typography, colors, and letter-spacing specifications
- Stat Counter Row (4 points)
  - Container uses Flexbox layout (`display: flex`) with correct items alignment and border dividers
  - Text styling applies proper block declarations, font sizes, colors, and uppercase transformations
- Input Field Label (4 points)
  - Uses accessible form tags: label correctly linked to input using 'for' and 'id'
  - Layout matches the vertical stack form layout
  - Focus state styling exists and displays distinct border and background color shifts
- Gradient Text Banner (4 points)
  - Banner container matches background, padding, and centered formatting
  - Heading implements background-clip gradient text styling correctly
- Price Tag with Strikethrough (4 points)
  - Plan card has shadow, border, and center-aligned layout
  - Old price shows line-through styling; new price is bold, green, and scaled up
  - Discount badge is styled as a green pill with rounded corners