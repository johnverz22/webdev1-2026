**Activity 3**

**HTML5 STRUCTURE RECREATION ACTIVITY**

*Recreating the McDonald's Philippines Homepage Using Semantic HTML5 Only*

# **Part 1: Instructions**

In this activity, you will recreate the structure of the McDonald's Philippines homepage (mcdonalds.com.ph) using HTML5 only. A reference screenshot is provided. The goal is to practice organizing real-world web content into correct, semantic HTML — not to make it look pretty.

## Important Reminder

**This is an HTML-only activity. Do not write or link any CSS — no `<style>` tags, no style attributes, and no external stylesheets. Your page will look unstyled (plain black text, default spacing, images at full size). This is expected and correct. You will be graded on structure and correctness of tags, not on visual appearance.**

## What You Must Recreate

Using the provided screenshot as your reference, build a single HTML file containing the following sections of the page:

- Header — the logo and the main navigation menu (Home, About Us, Family Activities, McDelivery, Careers, Opportunities).

- Hero banner — the large "Easy Maging Best Me" headline, the banner image, and the "Apply Now!" button/link.

- Content grid — the six promotional cards: McDelivery, NXTGEN, Careers, Family Activities, Download the McDelivery PH App, and Charity. Each card has an image and a caption/title.

- Footer — the McDelivery logo, the two app store badges, the three link columns (Privacy Policy/Our Food/Terms and Conditions/Opportunities, and About Us/Careers/Menu/Family Activities), and the "Follow us on" social media links (Facebook, Instagram, Twitter).

## Technical Requirements

- Use proper HTML5 document structure: `<!DOCTYPE html>`, `<html>`, `<head>` with `<meta charset>` and `<title>`, and `<body>`.

- Use semantic tags where they apply: `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`. Do not build the entire page out of `<div>` tags.

- Use a heading tag (`<h1>`) for the main "Easy Maging Best Me" headline. Use lower-level headings (`<h2>`, `<h3>`) for section titles and card captions, following a logical order (do not skip from `<h1>` straight to `<h3>`, and do not use multiple `<h1>` tags).

- Use `<nav>` with a list (`<ul>`/`<li>`) of `<a>` links for both the header menu and the footer link columns.

- Use `<img>` tags for every image/logo/badge shown in the screenshot, each with a descriptive alt attribute. You may use placeholder filenames (e.g. "hero-banner.jpg") since real image files are not required.

- Use `<a>` tags for all clickable elements: nav links, the Apply Now! button, the app store badges, and the social media icons. A real destination URL is not required — you may use href="#".

- Each of the six promotional cards should be wrapped in its own `<article>` (or a consistent repeated structure), containing an image and a caption.

- Do not use any CSS. Do not use the `<style>` tag, the style="" attribute, or any `<link rel="stylesheet">` tag.

- Save your file as index.html.

## What You Will Submit

Submit a single file named index.html containing your complete recreation.

## Grading Rubric

- Document Structure (3 points)
  - Valid HTML5 skeleton: `<!DOCTYPE html>`, `<html lang>`, `<head>` with `<meta charset="UTF-8">` and a `<title>`
  - Single `<body>` element
- Semantic Sectioning (4 points)
  - Use of `<header>`, `<nav>`, `<main>`, `<section>`/`<article>`, and `<footer>` to organize the page instead of generic `<div>` tags for major regions
- Heading Hierarchy (2 points)
  - Exactly one `<h1>` for the main headline
  - `<h2>`/`<h3>` used logically for section titles and card captions with no skipped levels
- Navigation Menus (3 points)
  - Header nav and the two footer link columns each use `<nav>` containing a list (`<ul>`/`<li>`) of `<a>` links
- Images with Alt Text (3 points)
  - Every visual element from the screenshot (logo, hero banner, six card images, McDelivery logo, two app store badges) is represented with an `<img>` tag
  - Each image has a descriptive, non-empty alt attribute
- Promotional Card Structure (3 points)
  - All six cards are present
  - Each card follows the same repeated structure (e.g. `<article>` containing an `<img>` and a heading/caption)
- Footer Completeness (1 point)
  - Footer includes the McDelivery logo, both app store badges as links, both link columns, and the "Follow us on" social links inside a `<footer>` element
- No CSS Used (1 point)
  - No `<style>` tag, no style="" attributes, and no `<link rel="stylesheet">` anywhere in the file

## Notes for Grading

- Visual appearance, colors, layout/positioning, fonts, and spacing are NOT graded. The page will and should look unstyled.

- Placeholder content is acceptable for image filenames and href destinations (e.g. href="#"), since this is a structure-only exercise.

- Minor typos in visible text (e.g. "Best Me" vs "BEST ME") should not be penalized. Grade structure, not copy-editing.

- If a student uses additional semantic tags correctly beyond what is listed here (e.g. `<figure>`/`<figcaption>` for card images), this should be treated as a bonus indicator of understanding, not a deduction.


## Grading Walkthrough (How the Reference Solution Earns Each Point)

- Document Structure (3/3): DOCTYPE, html lang, head with meta charset and title, single body — all present.

- Semantic Sectioning (4/4): `<header>`, two `<nav>` instances plus a footer `<nav>` equivalent, `<main>`, `<section>`/`<article>` combination, and `<footer>` are all used for their intended purpose.

- Heading Hierarchy (2/2): One `<h1>` ("Easy Maging Best Me"), one `<h2>` ("Explore") for the card grid section, `<h3>` for each of the six card captions, `<h4>` for "Follow us on." No levels skipped, only one h1.

- Navigation Menus (3/3): Header menu and both footer link columns each use `<nav>` > `<ul>` > `<li>` > `<a>`.

- Images with Alt Text (3/3): Every image (logo, hero, six cards, McDelivery logo, two badges) has a specific, descriptive alt attribute — none are empty or generic.

- Promotional Card Structure (3/3): All six cards present, each as an `<article>` with one `<img>` and one heading, in a consistent repeated pattern.

- Footer Completeness (1/1): McDelivery logo, both badges as linked images, both nav columns, and the social links section are all inside `<footer>`.

- No CSS Used (1/1): No `<style>`, no style attributes, no stylesheet link anywhere in the document.

## Acceptable Variations (Should NOT Be Marked Wrong)

- Using `<section>` instead of `<article>` for the six cards, as long as it's used consistently.

- Wrapping the footer's three link groups in `<section>` instead of leaving them as bare `<nav>`/`<nav>`/`<section>` siblings.

- Using `<figure>` and `<figcaption>` for card images instead of `<img>` + heading — this is a more advanced correct pattern and should be credited fully.

- Different but still real and reachable-looking href values instead of "#".

- Different but still descriptive alt text wording, image filenames, or ordering of nav items, as long as all required items from the screenshot are present.