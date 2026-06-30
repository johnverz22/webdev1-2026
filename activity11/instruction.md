# 🎨 Activity 11: Building "BuildWeb" — A Responsive Landing Page

You're going to recreate a dark-themed, modern landing page using a **Mobile-First** approach: HTML structure first, then mobile CSS, then a desktop "pivot" media query, then JavaScript interactivity. Let's break it down.

---

## 0. The HTML Skeleton (Build This First!)

Before any CSS works, the browser needs the actual content and structure in place. Build these elements top-to-bottom, in this order. Don't worry about classes for styling logic yet — just get the right *tag* and *content* on the page.

👉 **Page Wrapper / Sticky Nav**
* **Tag to use:** `<nav>`
* **What goes inside:**
  * A `<div class="container nav-inner">` holding your logo link, an unordered list (`<ul class="nav-links">`) of 3 `<li><a>` nav links, a `<div class="nav-cta">` with two `<a class="btn">` buttons, and a `<button class="hamburger">` with three empty `<span>` tags inside (these become the 3 bars via CSS).
  * Directly below the `nav-inner` div (but still inside `<nav>`), add a separate `<div class="mobile-menu">` containing duplicate links + one CTA button — this is the dropdown that JavaScript will show/hide.

👉 **Hero Section**
* **Tag to use:** `<section class="hero">`
* **What goes inside:**
  * A `<div class="container">` containing: a `<span class="tag">` eyebrow label, an `<h1>` headline (wrap the colored word in `<em>`), a `<p>` description, a `<div class="hero-actions">` with two `<a class="btn">` buttons, and a `<div class="bp-viz">` (the breakpoint visualizer card) containing a header bar, a `<div class="bp-track">` with a `<div class="bp-fill">` inside, four `<div class="bp-marker">` labels, and a `<div class="bp-code">` block.

👉 **Social Proof Strip**
* **Tag to use:** `<div class="proof">`
* **What goes inside:**
  * A `<p>` ("Trusted by...") and a flex row containing 5 small `<div class="avatar">` circles with 2-letter initials, plus a `<div class="proof-text">` with a student count.

👉 **Features Section**
* **Tag to use:** `<section class="features" id="features">`
* **What goes inside:**
  * A `.section-heading` block (tag + h2 + p), then a `<div class="features-grid">` holding 6 repeated `<div class="feature-card">` blocks — each with an icon div, an `<h3>` title, and a `<p>` description.

👉 **Curriculum Section**
* **Tag to use:** `<section class="curriculum" id="curriculum">`
* **What goes inside:**
  * A `<div class="curriculum-layout">` with two halves: (1) `.curriculum-info` containing a tag, h2, p, and a `.stat-row` of 3 stat blocks; (2) `.accordion` containing 6 `.acc-item` blocks, each with a `<button class="acc-header">` (number + title + chevron span) and a `<div class="acc-body"><div class="acc-body-inner">` for the hidden content.

👉 **CTA Strip**
* **Tag to use:** `<div class="cta-strip">`
* **What goes inside:**
  * An `<h2>`, a `<p>`, and a `<div class="cta-actions">` with two `<a class="btn">` buttons.

👉 **Footer**
* **Tag to use:** `<footer>`
* **What goes inside:**
  * A `<div class="footer-inner">` with a copyright `<p>` and a `<ul class="footer-links">` of 3 links.

---

## 1. The Global Design Tokens

Before touching any layout, we set up our "design system" variables. In Figma, you'd call this your Style Guide.

👉 **Root Variables (Color & Font Tokens)**
* **Selector to use:** `:root`
* **CSS Properties & Values:**
  * `--bg: #0A0F1E;` /* Our main dark navy background color */
  * `--bg-card: #111827;` /* A slightly lighter dark shade used for cards */
  * `--text: #F5F0E8;` /* The main off-white text color */
  * `--muted: #8892A4;` /* Grayish-blue color for secondary/subtitle text */
  * `--accent: #4AFFA4;` /* The bright mint-green color used for highlights and buttons */
  * `--border: rgba(255,255,255,0.08);` /* A nearly invisible white used for subtle dividing lines */
  * `--radius: 12px;` /* A reusable rounded-corner value for cards */

👉 **Page Defaults**
* **Selector to use:** `body`
* **CSS Properties & Values:**
  * `background: var(--bg);` /* Applies our dark navy token as the page background */
  * `color: var(--text);` /* Applies our off-white token as the default text color */
  * `font-family: var(--font-body);` /* Sets Inter as the default body font */
  * `line-height: 1.6;` /* Adds breathing room between lines of text for readability */

---

## 2. Phase 1: The Mobile Base (Layout & Styling)

Build everything top-to-bottom as if you only have a phone screen. Don't worry about side-by-side columns yet!

👉 **Page Wrapper**
* **Selector to use:** `.container`
* **CSS Properties & Values:**
  * `width: 90%;` /* Keeps content from touching the screen edges */
  * `max-width: 1120px;` /* Stops the content from getting too wide on bigger screens later */
  * `margin-inline: auto;` /* Centers the container horizontally on the page */

👉 **Navigation Bar**
* **Selector to use:** `.nav-inner`
* **CSS Properties & Values:**
  * `display: flex;` /* Turns on Flexbox so the logo and hamburger sit in a row, not stacked */
  * `align-items: center;` /* Vertically centers the logo and hamburger icon */
  * `justify-content: space-between;` /* Pushes the logo to the left and hamburger to the far right */

👉 **Desktop Nav Links (Hidden on Mobile)**
* **Selector to use:** `.nav-links`
* **CSS Properties & Values:**
  * `display: none;` /* Hides the text links since there's no room for them on a phone */

👉 **Hamburger Button**
* **Selector to use:** `.hamburger`
* **CSS Properties & Values:**
  * `display: flex;` /* Turns on Flexbox so the 3 small bars stack correctly */
  * `flex-direction: column;` /* Stacks the 3 bars vertically instead of side-by-side */
  * `gap: 5px;` /* Adds equal spacing between each of the 3 bars */

👉 **Mobile Dropdown Menu**
* **Selector to use:** `.mobile-menu`
* **CSS Properties & Values:**
  * `max-height: 0;` /* Starts the menu fully collapsed (closed) by default */
  * `overflow: hidden;` /* Hides any content that's "inside" the collapsed menu */
  * `transition: max-height 0.35s ease;` /* Makes the menu slide open smoothly instead of snapping instantly */

👉 **Hero Section**
* **Selector to use:** `.hero`
* **CSS Properties & Values:**
  * `padding: 100px 0 80px;` /* Adds tall empty space above/below to let the headline breathe */
  * `text-align: center;` /* Centers the headline and paragraph text on mobile */

👉 **Hero Heading**
* **Selector to use:** `.hero h1`
* **CSS Properties & Values:**
  * `font-size: clamp(2.5rem, 6vw, 5rem);` /* Makes the giant headline scale fluidly with screen width, with min/max limits */
  * `line-height: 1.08;` /* Tightens the spacing between headline lines so it looks bold, not loose */

👉 **Hero Button Group**
* **Selector to use:** `.hero-actions`
* **CSS Properties & Values:**
  * `display: flex;` /* Lines the two buttons up next to each other */
  * `justify-content: center;` /* Centers the button group horizontally */
  * `gap: 14px;` /* Adds even spacing between the two buttons without using margins */
  * `flex-wrap: wrap;` /* Lets buttons drop to a new line if the screen is too narrow to fit both */

👉 **Generic Button Style**
* **Selector to use:** `.btn`
* **CSS Properties & Values:**
  * `display: inline-flex;` /* Lets the button hug its text content while still using Flexbox internally */
  * `align-items: center;` /* Vertically centers text inside the button */
  * `padding: 10px 22px;` /* Adds inner spacing so text isn't cramped against the button edges */
  * `border-radius: 8px;` /* Rounds the button corners */

👉 **Features Grid (Cards)**
* **Selector to use:** `.features-grid`
* **CSS Properties & Values:**
  * `display: grid;` /* Turns on CSS Grid for the feature cards */
  * `grid-template-columns: 1fr;` /* Forces exactly ONE column, so cards stack vertically on mobile */
  * `gap: 24px;` /* Adds even spacing between stacked cards */

👉 **Individual Feature Card**
* **Selector to use:** `.feature-card`
* **CSS Properties & Values:**
  * `background: var(--bg-card);` /* Gives the card a slightly lighter background than the page */
  * `border: 1px solid var(--border);` /* Adds a subtle outline so the card separates from the background */
  * `padding: 32px 28px;` /* Adds inner breathing room around the icon, title, and text */

👉 **Curriculum Layout Wrapper**
* **Selector to use:** `.curriculum-layout`
* **CSS Properties & Values:**
  * `display: grid;` /* Turns on Grid to control the info text vs. the accordion */
  * `grid-template-columns: 1fr;` /* Single column on mobile, so info stacks above the accordion */
  * `gap: 40px;` /* Adds spacing between the stacked info block and accordion */

👉 **Accordion Item Header**
* **Selector to use:** `.acc-header`
* **CSS Properties & Values:**
  * `display: flex;` /* Lines up the number, title, and arrow icon in a row */
  * `justify-content: space-between;` /* Pushes the arrow icon to the far right of the header */
  * `padding: 18px 20px;` /* Gives the clickable header comfortable tap-target spacing */

👉 **Accordion Body (Collapsible Content)**
* **Selector to use:** `.acc-body`
* **CSS Properties & Values:**
  * `max-height: 0;` /* Default state is fully collapsed/hidden */
  * `overflow: hidden;` /* Prevents hidden text from peeking out before it's opened */
  * `transition: max-height 0.3s ease;` /* Animates the smooth "accordion" expand/collapse effect */

👉 **Call-To-Action Strip**
* **Selector to use:** `.cta-strip`
* **CSS Properties & Values:**
  * `border-radius: 20px;` /* Rounds the corners of the highlighted CTA box */
  * `padding: 40px 24px;` /* Adds inner spacing around the CTA heading and buttons */
  * `text-align: center;` /* Centers all text and buttons inside the strip */

👉 **Footer**
* **Selector to use:** `.footer-inner`
* **CSS Properties & Values:**
  * `display: flex;` /* Aligns copyright text and footer links */
  * `flex-wrap: wrap;` /* Allows the links to drop below the copyright text if needed on narrow screens */
  * `gap: 16px;` /* Adds spacing if items wrap onto a new line */

---

## 3. Phase 2: The Large Screen Pivot (Media Query)

Now we "pivot" for bigger screens. Wrap all of this inside ONE media query.

👉 **Media Query Wrapper**
* **Selector to use:** `@media (min-width: 1024px)`
* **CSS Properties & Values:**
  * *(This is the container — place all the rules below INSIDE these curly braces)* /* Tells the browser "only apply these styles when the screen is 1024px wide or larger" */

```css
@media (min-width: 1024px) {

  /* Rules go here */

}
```

👉 **Desktop Nav Links**
* **Selector to use:** `.nav-links`
* **CSS Properties & Values:**
  * `display: flex;` /* Reveals the text links since there's now enough horizontal room */

👉 **Hamburger Button**
* **Selector to use:** `.hamburger`
* **CSS Properties & Values:**
  * `display: none;` /* Hides the hamburger icon since the full menu is now visible */

👉 **Mobile Dropdown Menu**
* **Selector to use:** `.mobile-menu`
* **CSS Properties & Values:**
  * `display: none !important;` /* Forcefully removes the mobile dropdown from the layout entirely on desktop */

👉 **Features Grid (Cards)**
* **Selector to use:** `.features-grid`
* **CSS Properties & Values:**
  * `grid-template-columns: repeat(3, 1fr);` /* Switches from 1 stacked column to 3 equal-width columns side-by-side */

👉 **Curriculum Layout Wrapper**
* **Selector to use:** `.curriculum-layout`
* **CSS Properties & Values:**
  * `grid-template-columns: 1fr 1fr;` /* Splits the section into two equal side-by-side columns: text on the left, accordion on the right */
  * `gap: 56px;` /* Increases the spacing between the two columns now that there's more room */

👉 **CTA Strip**
* **Selector to use:** `.cta-strip`
* **CSS Properties & Values:**
  * `padding: 64px 48px;` /* Increases the inner spacing now that the box has more room to breathe */

---

## 4. Phase 3: Bringing It to Life with JavaScript

Your HTML and CSS are done, but nothing actually *clicks* yet. JavaScript handles the three interactive behaviors on this page. Build these inside a single `<script>` tag, wrapped in a `DOMContentLoaded` listener.

👉 **Hamburger Menu Toggle**
* **What it does:** Listens for a click on the hamburger button and shows/hides the mobile dropdown.
* **Logic to write:**
  * Select the `.hamburger` button and the `.mobile-menu` div using `document.querySelector()`.
  * Add a `'click'` event listener to the hamburger.
  * Inside the listener, call `.classList.toggle('open')` on the `.mobile-menu` — this is what triggers the CSS `max-height` transition you wrote in Phase 1.
  * Also toggle the `aria-expanded` attribute between `'true'`/`'false'` so screen readers know the menu state — good accessibility practice!

👉 **Auto-Close Menu on Window Resize**
* **What it does:** If a user has the mobile menu open and then resizes/rotates their screen past the desktop breakpoint, the menu should snap closed automatically instead of floating awkwardly over the desktop layout.
* **Logic to write:**
  * Add a `'resize'` event listener on the `window` object.
  * Inside it, check `if (window.innerWidth >= 1024)`.
  * If true, remove the `'open'` class from `.mobile-menu` (this matches the `min-width: 1024px` breakpoint you used in your CSS media query — keep these numbers in sync!).

👉 **Accordion Expand/Collapse**
* **What it does:** Clicking a curriculum lesson header opens its description and closes any other open lesson (an "only one open at a time" accordion).
* **Logic to write:**
  * Select all `.acc-header` buttons with `document.querySelectorAll()`.
  * Loop through them and add a `'click'` listener to each.
  * On click: first loop through *every* `.acc-item` and remove the `'open'` class + set that item's `.acc-body.style.maxHeight = '0px'` (this closes everything).
  * Then, add the `'open'` class to the clicked item only, and set its `.acc-body.style.maxHeight` equal to `scrollHeight + 'px'` — this is the trick that lets a `max-height` transition animate to "auto" height smoothly.

---

## 5. "Designer-to-Developer" Cheat Sheet

A few quick translations to connect what you already know in Figma to what you're typing in code.

> **Figma "Auto-Layout" → CSS `display: flex;`**
> When you set a frame to Auto-Layout in Figma to make items line up and resize together, that's the exact same concept as turning on Flexbox in CSS.

> **Figma "Gap" (Auto-Layout spacing) → CSS `gap: [value];`**
> The "Gap" field you set inside an Auto-Layout frame in Figma maps directly to the `gap` property in Flexbox or Grid — no more guessing with margins!

> **Figma "Corner Radius" → CSS `border-radius: [value];`**
> The rounded-corner slider you drag in Figma's right-hand panel is just the `border-radius` property in disguise.