# Activity 6: Advanced UI Component Styling

In this activity, you will further practice your CSS design skills by implementing eight distinct UI components commonly found in modern web applications. Focus on precision, correct CSS selectors, and responsive component properties.

## Workspace Setup

1. Create a folder named `activity6`.
2. Inside, create two files:
   - `index.html` (for your HTML structures)
   - `style.css` (for your CSS rules)
3. Link the stylesheet in your HTML's `<head>`.
4. Render all eight components in order on your page, separating them clearly.

---

## Component Specifications

### 1. Modern Text Badge
A small, neat text tag to denote new items.
- **HTML Structure**: A inline tag (e.g. `<span class="ui-badge">New</span>`).
- **CSS Styling**:
  - Background color: `#E0F2FE` (soft light blue)
  - Text color: `#0369A1` (dark ocean blue)
  - Typography: Bold weight, font-size `11px`, letter-spacing `0.5px`, uppercase transformation, Arial or sans-serif font.
  - Spacing & Borders: Padding of `4px` top/bottom, `8px` left/right, and `4px` rounded corners.

### 2. Stadium Pill Tag
A fully rounded indicator pill tag.
- **HTML Structure**: An inline tag (e.g. `<span class="ui-pill">Active User</span>`).
- **CSS Styling**:
  - Background color: `#22C55E` (vibrant green)
  - Text color: `#FFFFFF`
  - Typography: Font-size `13px`, medium weight (`500`), Arial or sans-serif.
  - Spacing & Borders: Padding of `6px` top/bottom, `16px` left/right, and a very large border-radius (`9999px`) to create the stadium pill shape.

### 3. Circular Avatar
A circular visual placeholder for a user's initials.
- **HTML Structure**: A container tag (e.g. `<div class="ui-avatar">JD</div>`).
- **CSS Styling**:
  - Layout: `display: block`, width `64px`, height `64px`.
  - Spacing & Borders: Rounded corners set to `50%` (circle), background `#E2E8F0` (light gray).
  - Typography: Text color `#1E3A8A` (deep blue), font-size `20px`, bold, Arial or sans-serif, centered text.
  - Alignment: Line-height matches the height (`64px`) to center the text vertically.

### 4. Action Form Button
An interactive form submission button.
- **HTML Structure**: A `<button class="ui-btn">Create Account</button>` tag.
- **CSS Styling**:
  - Layout: `display: block`, pointer cursor on hover, no default borders.
  - Background color: `#4F46E5` (deep indigo).
  - Text color: `#FFFFFF`
  - Typography: Font-size `14px`, semi-bold weight (`600`), Arial or sans-serif.
  - Spacing & Borders: Padding of `12px` top/bottom, `24px` left/right, and `8px` rounded corners.
  - Hover State: Transitions the background color to `#4338CA` on hover.

### 5. Form Field Stack
A clean vertical stack displaying a form input and its label.
- **HTML Structure**: A container containing a `<label>` and an `<input type="email">` with placeholder text and a default value.
- **CSS Styling**:
  - Layout: Container max-width of `240px`.
  - Label: Display block, font-size `12px`, bold weight (`600`), color `#334155`, uppercase, and `4px` margin below.
  - Input: Display block, width `100%`, padding `10px 14px`, border `2px solid #CBD5E1`, border-radius `6px`, font-size `14px`, and color `#0F172A`.
  - Focus State: Changes border color to `#3B82F6` and background to `#F8FAFC` on focus with no outline.

### 6. Notification Alert Banner
A banner notification alert box.
- **HTML Structure**: A container card enclosing a message string.
- **CSS Styling**:
  - Layout: Display block, width `340px`, padding `14px` top/bottom, `18px` left/right.
  - Borders: Left border `5px solid #EF4444` (warning red), other corners rounded by `4px`.
  - Colors: Background `#FEE2E2` (light red warning tint).
  - Typography: Font-size `13px`, medium weight (`500`), text color `#991B1B`, Arial or sans-serif.

### 7. Feature Content Card
A content block to showcase specific features of a product.
- **HTML Structure**: A container card featuring an icon span, a title heading, and a descriptive paragraph.
- **CSS Styling**:
  - Card Container: Display block, width `280px`, background `#FFFFFF`, border `1px solid #E2E8F0`, border-radius `12px`, and padding `24px`.
  - Icon: Display block, size `24px`, and bottom margin of `12px`.
  - Heading: Font-size `16px`, bold weight (`700`), color `#0F172A`, margin-bottom `6px`, Arial or sans-serif.
  - Paragraph: Font-size `13px`, color `#64748B`, line-height `1.4`, Arial or sans-serif.

### 8. Stacked Application Sidebar Menu
A stacked sidebar navigation component.
- **HTML Structure**: A list element (`<ul class="nav-menu">`) containing links inside list items, including one active item.
- **CSS Styling**:
  - Menu Container: Display block, width `200px`, background `#1E293B` (slate dark), padding `8px`, rounded corners `8px`, and no default bullets/padding.
  - Links: Display block, padding `8px` top/bottom, `16px` left/right, font-size `14px`, medium weight (`500`), text-decoration none, and rounded corners of `4px`.
  - Inactive Link Colors: Text color `#94A3B8`.
  - Hover State: Text transitions to white (`#FFFFFF`) with background `#334155` on hover.
  - Active Link State: Text color `#38BDF8` (sky blue), background `#0F172A`, bold weight (`600`).
  - Spacing: Bottom margin of `4px` between links, except the last one.

---

## Grading Rubric

- Modern Text Badge (3 points)
  - Inline element styled with correct background, uppercase text, padding, and rounded corners
- Stadium Pill Tag (3 points)
  - Tag features correct green background, specific padding, and fully rounded border-radius pill shape
- Circular Avatar (3 points)
  - Avatar is block-aligned, perfectly square with `50%` border-radius, and text is centered horizontally and vertically
- Action Form Button (3 points)
  - Button uses correct base padding, rounded corners, cursor pointer, and hover transition
- Form Field Stack (3 points)
  - Field group elements stack vertically; input uses proper border, padding, and displays correct focus state styles
- Notification Alert Banner (3 points)
  - Alert has red left border, light red background, and correct inner text styling
- Feature Content Card (3 points)
  - Card container matches layout borders, padding, and shadow; card items spacing matches description
- Stacked Application Sidebar Menu (4 points)
  - Menu container removes default list-style and sets correct background
  - Active and inactive states display correct text and background color variations