# Activity 4: The CSS Masterclass — From Structure to Style

In Activities 1, 2 and 3, you mastered the "bones" of the web: Semantic HTML. Now, you will breathe life into those structures. This 3-part progressive challenge will take you from linking your first stylesheet to mastering the precise physics of the CSS Box Model.

You will be working on the **Product Showcase** you built in Activity 2 (or a fresh copy of it).

---

## Milestone 1: The Global Glow-Up (Syntax & Branding)
**Goal:** Establish the foundation. You will move from plain-text browser defaults to a professional, branded environment using external CSS.

1. **Workspace Setup:**
   - Inside your `activity4` folder, create a file named `style.css`.
   - Link this file in your `index.html` inside the `<head>` tag using `<link rel="stylesheet" href="style.css">`.
2. **Global Rules:**
   - Use the `body` selector to set a background color (e.g., `#f8f9fa`) and a primary font-family (e.g., `'Segoe UI', Tahoma, sans-serif`).
   - Use the `h1` and `h2` selectors to set a consistent brand color and increase the `line-height` for better readability.
3. **Typography Cleanup:**
   - Remove the default underlines from all `<a>` tags globally and set them to a color that contrasts well with your background.

---

## Milestone 2: The Component Architect (Classes & Interactivity)
**Goal:** Move beyond "styling every tag." You will learn to target specific elements and add interactive feedback.

1. **Class-Based Cards:**
   - In your HTML, add `class="feature-card"` to your product feature items.
   - In CSS, use the `.feature-card` selector to give them a white background and a subtle border.
2. **Visual Hierarchy:**
   - Create a class `.text-highlight` and apply it to key technical specs or prices. Set this class to have a bold `font-weight` and a distinct color.
3. **User Feedback:**
   - Select your navigation links and add a `:hover` state. Change the background color or text color when the user hovers over them to provide visual confirmation.

---

## Milestone 3: The Box Model Sandbox (Layout Precision)
**Goal:** Master the "physics" of web layout. You will ensure your elements have the perfect amount of internal breathing room and external separation.

1. **The Universal Reset:**
   - At the very top of your `style.css`, add the universal selector `*` and set `box-sizing: border-box;`. This ensures padding and borders don't break your layout math.
2. **The Hero Spacing:**
   - Target your "Hero" section. Use `padding` to give the content space from the edges and `margin-bottom` to push the next section away.
3. **Form Refinement:**
   - Style your newsletter `<input>` and `<button>`. Use `padding` inside the input so text isn't touching the borders.
   - Add a `border-radius` to the button and the input to give them a modern, rounded appearance.

---

# Grading Rubric
- CSS Syntax and Linking (10 points)
  - Stylesheet is correctly linked via the `<head>` using a relative path
  - CSS rules follow the standard Syntax (Selector { property: value; }) with no missing semicolons
- Global and Class Selectors (15 points)
  - Uses global element selectors for base typography and background colors
  - Implements reusable `.class` selectors for components like feature cards
  - Correctly utilizes the `:hover` pseudo-class for interactive navigation elements
- Box Model Implementation (15 points)
  - Successfully applies `box-sizing: border-box` to prevent layout calculation errors
  - Uses `padding` effectively to create internal breathing room within containers
  - Employs `margin` to maintain consistent vertical rhythm and separation between sections
- Code Organization and Semantics (10 points)
  - CSS is kept entirely separate from HTML (no inline `style` attributes)
  - Selectors are named logically and follow a clear, readable structure
  - Maintains the semantic integrity of the underlying HTML while applying styles
