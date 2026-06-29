# Activity 10 - Responsive Redesign — Mobile First

**A step-by-step CSS activity — WEBDEV1 — Media Queries, Mobile-First Layout, and a first taste of Shadows, Transitions & JS**

## How this works

You already built Maya Cruz's portfolio page once, targeting a wide desktop screen. Now you're rebuilding the CSS **from nothing, in the opposite direction** — starting from the narrowest phone-width layout, and only adding complexity as the screen gets wider.

For Parts 1–3 of this activity (the layout and media query work), there is still no code given — same rule as last time. You derive the property names and values yourself, checking your work by resizing your actual browser window narrow and wide, rather than against a single screenshot. Part 4 is different: shadows, transitions, and a small bit of JavaScript are being introduced for the first time today, so that part gives you the code directly, with an explanation of what each line does. You're not expected to derive syntax you've never seen before.

---

## Part 0 — Why "mobile-first" changes the order you write CSS in

Before touching any code, understand the shift in thinking.

Last time, you wrote rules for the wide layout first (flex rows, grid columns), and at the bottom of the file you added `@media (max-width: ...)` blocks that *override* those rules to squeeze things down for small screens. That's called **desktop-first**.

**Mobile-first reverses this.** Your base CSS — the rules with no media query at all — should describe the simplest, narrowest, single-column version of the page. Then, as the screen gets *wider*, you use `@media (min-width: ...)` blocks to *add* row layouts, multi-column grids, and side-by-side arrangements on top of that simple base.

Why bother switching direction? A few real reasons:
- Most visits to most websites happen on phones. Writing the phone layout as your default means your most common visitor gets CSS written specifically for them, not CSS that was designed for something else and then forced to shrink.
- "Undoing" desktop layout for mobile (turning off flex, unsetting grid columns, fighting fixed widths) is often messier than just adding layout on top of a simple stacked base.
- It forces you to ask "does this even need to be side-by-side?" for every section, instead of assuming everything should be a row by default.

Keep this in mind as you go: **if something is already stacking correctly with zero CSS, leave it alone at the base level.** You only add a layout property when the *default* behavior doesn't match what you want at that screen size.

---

## Part 1 — Strip it down

Open your `styles.css` from the previous activity. Delete everything **except** your universal reset (the `*` selector with margin/padding/box-sizing) and any plain typography/color rules that don't involve flex, grid, or layout — things like font-family, font-size, color values, and text-align can stay, since those aren't layout decisions.

Resize your browser window as narrow as it'll go (or open DevTools and toggle device toolbar to something like a 375px-wide phone). Look at the page. Every section should now be a plain vertical stack: logo above nav links, hero text above the info cards (not beside them), all four skill cards full-width one after another, contact centered text, footer text above its links.

### Predict

For each of the four major sections (navbar, hero, skills, footer), write a one-word guess: at this narrow width, does this section's current stacked-by-default behavior already look correct, or does something still need to change even at this smallest size? You'll check yourself against this prediction as you go.

---

## Part 2 — Build the mobile (base) layout

Work through each section. Remember: only add a property if the default stacking genuinely isn't what you want yet, even on a narrow phone screen.

### Navbar

On a real phone, a row layout with a logo on the left and three links crammed on the right gets cramped fast. The common mobile pattern is to keep the logo and the link list **stacked**, centered, with some vertical spacing between them — which, notice, is extremely close to what already happens with zero layout CSS at all.

What you likely still want to add at the base level: center the text (logo and links) horizontally, and add a small consistent vertical gap between the logo and the nav list, plus padding around the whole header so it's not touching the screen edges. None of this requires flex yet — centering and spacing a vertical stack is a simpler tool than flexbox. Think about which single property centers inline/block text content, and whether margin or a gap-style property makes more sense for spacing two stacked block elements that aren't in a flex container.

For the three links inside `navbar__links` themselves — at this narrow width, do you want them stacked vertically too, or already in a small row? Look at typical mobile nav patterns (or decide based on how much room three short words like "About / Skills / Contact" would need) and make a call. If you decide they should be a small horizontal row even on mobile, that's a legitimate use of flex at the base level — mobile-first doesn't mean "no flex until desktop," it means "only add flex where the narrow layout genuinely benefits from it."

### Hero

At a narrow width, the two-column desktop layout (text beside info-cards) makes no sense — there isn't room. The base/mobile version should keep `hero__text` and `hero__panel` stacked, which is again already the default with zero CSS.

What you do still want at the base level: add `display: flex; flex-direction: column;` to `hero__panel` specifically (not to `.hero` itself), with a small gap, for the exact same reason as your previous activity — so the three info-cards have even spacing between them. Add reasonable padding around the whole `.hero` section so content has breathing room against the phone's screen edges (noticeably less than the ~100px you used on desktop — something more like 40–48px feels right for a phone). Reduce the heading's font size at this base level too — a headline sized for a 1140px-wide desktop column will likely wrap awkwardly or look oversized at 375px; bring it down to something that comfortably fits 2–3 lines on a narrow screen.

### Skills

At a narrow width, a 3-column grid with two wide cards spanning two columns doesn't have room to exist — there isn't space for even 2 columns to look right. The base/mobile layout should be a **single column**, one card per row, full width. Since that's exactly what happens with zero grid CSS at all, you may not need any grid property here at the base level — confirm by checking your browser. If your cards already stack full-width with just your padding/border styling and no grid declaration, leave it that way; you'll add the grid behavior later, only once the screen is wide enough to support it.

### Contact & Footer

Contact still doesn't need any layout property at this or any width — text-align handled it before and still does. For the footer, apply the same reasoning as the navbar: stacked and centered at this narrow width, likely without needing flex at the base level at all, unless you decide the two footer pieces should sit in a small row even on mobile.

### Checkpoint 1

Compare your actual choices to your Part 1 predictions. Which section most surprised you — where you assumed something would need new CSS at the narrow width, but it turned out the default stacking was already correct (or vice versa)? Write 2-3 sentences explaining why.

---

## Part 3 — Layer on wider layouts with min-width media queries

Now you'll widen your browser gradually and add layout back in stages, using `@media (min-width: ...)` blocks. The key habit: **don't jump straight to your old desktop values.** Widen the window slowly and add a breakpoint at the point where the mobile layout actually starts looking cramped or wasteful — not at an arbitrary round number you remember from before.

A `min-width` media query applies its rules only when the screen is *at least* that wide, layering on top of your base rules rather than replacing them outright (unless you specifically overwrite a property). This is the mirror image of the `max-width` queries you used last time.

### Tablet-ish breakpoint (around 600–700px wide — find your own exact number by testing)

Widen your browser until the navbar starts looking like it has obvious room to be a single row instead of stacked (if it isn't already). Add a `min-width` media query at that width and, inside it, give `.navbar` the row treatment: the same flex/justify-content/align-items combination you used in your very first activity, this time written inside the media query block instead of as a base rule.

Keep widening. At some point the skills grid has room for 2 columns instead of 1 — find that width, add another media query (or reuse the same one if the width matches), and give `.skills__grid` 2 equal columns at that breakpoint. Decide for yourself whether your two "wide" cards should span both columns at this in-between width (effectively becoming full-width again) or stay spanning just visually wider within 2 columns — look at what reads better and make a deliberate choice, not an accidental one.

### Desktop breakpoint (around 860–960px wide — again, find your own number)

Keep widening until the hero section has clear room for its two columns side by side. Add a `min-width` media query at that point and give `.hero` the row treatment from your very first activity (flex, gap, justify-content, align-items, the proportional `flex` values on the two children). Increase the heading's font size back up at this width too, since you shrunk it for mobile in Part 2.

At a similar or slightly wider breakpoint, bump the skills grid up to 3 columns and reapply the 2-column span to your wide cards.

Widen all the way to a large desktop width and confirm your page now matches the original desktop layout you built last time — but reached via the opposite direction (mobile base, scaled up), instead of desktop base, scaled down.

### Checkpoint 2

You picked your own breakpoint widths by testing, rather than using a fixed standard like exactly 768px. What's the risk of picking breakpoints based on common device widths (like "phones are 375px, tablets are 768px") instead of picking them based on when your specific content starts looking cramped or awkwardly spaced? Write 2-3 sentences.

---

## Part 4 — Soft introduction: shadows, transitions, and a touch of JavaScript

These three tools aren't this lesson's main objective, so unlike the sections above, you're given the code directly here. Read what each line does, then add it and see the effect — don't worry about deriving these from scratch.

### Box shadows — give cards depth

A box-shadow adds a soft drop-shadow behind an element, which is a quick way to make cards feel lifted off the page instead of flat. Add this to your `.skill-card` rule:

```css
box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
```

Reading this value left to right: `0` is horizontal offset (no left/right shift), `2px` is vertical offset (shadow falls slightly downward), `8px` is blur radius (how soft/spread-out the shadow edge is), and `rgba(0, 0, 0, 0.08)` is the shadow's color — black, but at only 8% opacity, which is what keeps it subtle instead of looking like a heavy dark blob.

### Transitions — make hover changes feel smooth instead of instant

Right now, if you add a `:hover` rule, any property change snaps instantly. A transition tells the browser to animate that change smoothly over a short duration instead. Add this to your `.skill-card` rule (alongside the box-shadow):

```css
transition: box-shadow 0.2s ease, transform 0.2s ease;
```

This says: whenever `box-shadow` or `transform` changes on this element, animate that specific change over 0.2 seconds, using an "ease" timing curve (starts and ends a little slower than the middle, which feels more natural than a perfectly linear speed).

Now add an actual hover effect that uses that transition:

```css
.skill-card:hover {
  box-shadow: 0 6px 16px rgba(0, 0, 0, 0.12);
  transform: translateY(-4px);
}
```

`transform: translateY(-4px)` shifts the element 4 pixels upward (negative Y moves up) without affecting any other element's layout position — that's what makes transform-based hover effects popular, they don't trigger any reflow of surrounding content. Combined with the slightly larger shadow on hover, the card reads as "lifting toward the cursor."

Try the same pattern on `.btn` — a transition on `background` or `transform`, with a `:hover` state that changes color slightly or lifts slightly. Experiment with your own values here; this part doesn't need to match anyone else's exactly.

### A small bit of JavaScript — toggle a mobile menu

Right now your navbar links are always visible, just rearranged by your media queries. A common real pattern is to **hide** the nav links by default on mobile, behind a hamburger icon/button, and only show them when tapped. This needs a little JavaScript, since CSS alone can't respond to a click by toggling visibility based on state.

First, add a button in your HTML, inside the navbar, right before your `nav` element:

```html
<button class="navbar__toggle" aria-label="Toggle menu">☰</button>
```

In your base (mobile) CSS, hide the link list by default and show the button:

```css
.navbar__links {
  display: none;
}

.navbar__toggle {
  display: block;
  font-size: 24px;
  background: none;
  border: none;
}
```

Inside your wider min-width media query (the one where the navbar becomes a row), reverse both of those — show the links, hide the toggle button, since at that width you don't need the hamburger menu at all:

```css
.navbar__links {
  display: flex;
}

.navbar__toggle {
  display: none;
}
```

Add a class for the "open" state that you'll toggle with JavaScript:

```css
.navbar__links.is-open {
  display: flex;
  flex-direction: column;
}
```

Now add a `script` tag at the bottom of your `body`, just before `</body>`:

```html
<script>
  const toggleBtn = document.querySelector('.navbar__toggle');
  const navLinks = document.querySelector('.navbar__links');

  toggleBtn.addEventListener('click', () => {
    navLinks.classList.toggle('is-open');
  });
</script>
```

Walking through this: `document.querySelector` finds the first element matching that CSS selector and stores a reference to it. `addEventListener('click', ...)` attaches a function that runs every time that element is clicked. `classList.toggle('is-open')` adds the `is-open` class if it's missing, or removes it if it's present — flipping it on and off with every click, which is exactly the behavior you want from a menu button.

Test it: narrow your browser until the hamburger button appears, click it, and confirm the links show up in a stacked list. Click again and confirm they disappear.

### Checkpoint 3

You hid `.navbar__links` using `display: none` by default on mobile, and used JavaScript to toggle a class that changes it back to `display: flex`. Why can't this particular behavior — showing/hiding content in response to a click — be done with CSS and media queries alone, the way your layout changes in Part 3 were? What's different about "screen got wider" versus "user clicked a button" as a trigger?

---

## Final check before you submit

1. Resize your browser through the full range — narrowest phone width up through a large desktop width — and confirm there's no point where the layout looks broken, overlapping, or oddly spaced in between your breakpoints.
2. Confirm the hamburger menu appears only at narrow widths and disappears once the navbar switches to its row layout.
3. Hover over a skill card and a button and confirm the shadow and lift transition feels smooth, not instant or jumpy.
4. Open DevTools, toggle to a few different device presets (a small phone, a tablet, a laptop), and check each one against what you'd expect from your media query breakpoints.

## Submit

1. `index.html` (with the toggle button and script tag added)
2. `styles.css` (fully rewritten mobile-first, with your min-width media queries)
3. Your three Checkpoint answers, as a comment block at the bottom of `styles.css`
