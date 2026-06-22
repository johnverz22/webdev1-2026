# Activity 2: The Semantic Challenge — Product Showcase

In Activity 1, you were given the specific "boxes" (tags) to use for your portfolio. Now, it's time to take off the training wheels. In this activity, you will build a **Single-Page Product Showcase** for a fictional gadget of your choice (e.g., a high-tech water bottle, a revolutionary keyboard, or a smart plant pot).

Your goal is to translate descriptive requirements into the most appropriate **Semantic HTML5** elements. You must decide which tags best describe the meaning of each piece of content.

---

## Phase 1: Setup

1. Create a folder named `activity2`.
2. Inside, create a single file named `index.html`.
3. Set up your standard HTML5 boilerplate (document type, language, head, and body).
4. Save an image of your fictional product (or a placeholder) as `product.jpg` in your `activity2` folder.

---

## Phase 2: Content Requirements

Instead of telling you which tags to use, I will describe what the content *is*. Your job is to select the correct HTML element for each requirement.

### 1. The Branding & Navigation
* Add the **main title** of your product website at the top.
* Create a **group of links** that would allow a user to jump to different parts of the page (e.g., Features, Specs, Reviews).

### 2. The Hero Introduction
* Define the **primary content area** of the page.
* Create a **thematic section** for the "Hero" area.
* Inside this section, include:
    * A **secondary heading** with a catchy tagline.
    * The **product image** you saved earlier (ensure you include descriptive text for those who cannot see the image).
    * A **short paragraph** explaining why this product is life-changing.

### 3. Core Features
* Create a new **thematic section** dedicated to product features.
* Include a **heading** for this section.
* List **three key features**. The order of these features does not matter, so choose the list type that reflects that.

### 4. Standalone User Review
* Create a section for a **customer testimonial**.
* The review should be treated as a **self-contained piece of content** that could be reused elsewhere (like on a social media feed).
* Inside the review, include:
    * The **reviewer's name** as a heading.
    * The **actual text of the review**.
    * A **direct quotation** from the reviewer highlighting their favorite part.

### 5. Technical Specifications
* Create a **thematic section** for technical details.
* Present the following data in a **structured grid of rows and columns**:
    * **Weight:** 500g
    * **Dimensions:** 10cm x 10cm x 20cm
    * **Battery Life:** 24 Hours
    * **Material:** Recycled Aerospace Aluminum

### 6. Side Information
* Add a small block of content that is **indirectly related** to the main product (e.g., a "Fun Fact" about the materials used or a "Related Products" link).

### 7. Stay Updated
* Create a **user input area** where people can sign up for a newsletter.
* You need a **field for their email address** and a **labeled prompt** explaining what the field is for.
* Add a **trigger** that the user clicks to submit their information.

### 8. Page Conclusion
* Add a **closing area** at the bottom of the page with a copyright notice and the current year.

---

## Phase 3: The Golden Rules

1. **No Divs or Spans:** For this activity, try to avoid using `<div>` or `<span>`. Challenge yourself to find a semantic tag that fits the purpose first.
2. **No Styling:** Focus entirely on the structure. Do not add CSS.
3. **Hierarchy Matters:** Ensure your headings (`h1` through `h6`) follow a logical order. Don't skip levels just for size!

---

## Grading Rubric

- Semantic Decision Making (20 points)
  - Every requirement matched with the most appropriate semantic tag (e.g., `<nav>` for links, `<article>` for reviews, `<table>` for specs)
  - Decisions show understanding of content meaning, not just generic container use
- Document Structure & Hierarchy (10 points)
  - Headings used in a logical progression without skipping levels
  - Page has a clear beginning, middle, and end using structural landmarks
- Technical Implementation (10 points)
  - Data grid (specs table) is correctly structured with proper HTML table elements
  - Form is fully accessible with correctly connected labels and inputs
  - Images have meaningful alternative text
- Content Quality & Logic (10 points)
  - Fictional product details are consistent and creative
  - Page reads like a real, professional product landing page
