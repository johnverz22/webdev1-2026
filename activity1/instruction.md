# Activity 1: Blueprinting Your 4-Page Developer Portfolio

Welcome to your first web development project! Today, you are stepping into the shoes of a junior frontend developer to build the raw foundation of your professional portfolio.

Right now, we are entirely ignoring colors, fonts, and styling. Your only goal today is to master **Semantic HTML5**—using the correct tags so browsers, search engines, and screen readers know exactly what your content means.

Think of semantic tags as labeled boxes. By using the correct box, you create a well-organized map of your content.

---

## Phase 1: Workspace Setup

Before building, we need a clean workspace. This includes preparing our files and our images.

1. Open your code editor (like VS Code).
2. Create a brand new folder named `activity1`.
3. Inside that folder, create **four** blank text files. Name them exactly like this:
* `index.html` *(Your Profile Home)*
* `projects.html` *(Your Work Hub)*
* `contact.html` *(Your Message Hub)*
* `blog.html` *(Your Learning Journal)*


4. **Prepare your images:** * Find a picture of yourself (or a placeholder avatar) and save it directly inside your `activity1` folder. Name it exactly `profile.jpg`.
* Take a quick screenshot of your code editor, and save it in the same folder. Name it exactly `screenshot.png`.



---

## Phase 2: The Master Template (The Frame of the House)

Every page on your website will share the exact same top menu and bottom footer. You will build this "frame" once, and then copy it to all four files.

1. Open `index.html`. Type out the standard HTML5 boilerplate (the `<!DOCTYPE html>`, `<html>`, `<head>`, and `<body>` tags).
2. Inside the `<head>`, add a `<title>` tag with your name (e.g., "Alex Rivera | Portfolio").
3. Inside the `<body>`, we will build our shared frame. Follow these steps in order:
* Open a `<header>` tag. Inside it, put an `<h1>` heading with your name and title. Close the header.
* Open a `<nav>` tag. Inside it, create an unordered list (`<ul>`).
* Inside the list, create four list items (`<li>`). Inside each list item, put an anchor tag (`<a>`) linking to your four files (`href="index.html"`, `href="projects.html"`, etc.). Close the list and the nav.
* Open a `<main>` tag. Leave it completely empty for now. Close the main tag.
* Open a `<footer>` tag. Add a paragraph (`<p>`) with a copyright notice. Close the footer.


4. **The Golden Rule:** Highlight all the code you just wrote, copy it, and paste it into `projects.html`, `contact.html`, and `blog.html`.

*Checkpoint: You now have four identical pages linked together. The rest of this activity is just filling in the empty `<main>` tags on each page!*

---

## Phase 3: Filling the Rooms (Page by Page)

### Room 1: The Home Page (`index.html`)

Open your `index.html` file and place your cursor *inside* the empty `<main>` tags.

1. **The About Section:** * Create a `<section>` tag. Give it an `id` attribute of "about".
* Inside the section, add an `<h2>` heading that says "About Me".
* Below the heading, add an image using the `<img>` tag. Point the `src` attribute to the image you saved in Phase 1 (`src="profile.jpg"`) and add an `alt` attribute describing the picture (e.g., `alt="Headshot of Alex Rivera"`).
* Below the image, add a paragraph (`<p>`) introducing yourself as an IT student.


2. **The Skills Section:**
* Below your "about" section, create a new `<section>` tag with an `id` of "skills".
* Add an `<h2>` heading for "Technical Skills".
* Use an unordered list (`<ul>`) and list items (`<li>`) to list three technologies you are learning (like Semantic HTML, Git, etc.).


3. **The Quick Stats Sidebar:**
* Below your "skills" section, open an `<aside>` tag. We use aside for tangentially related information.
* Add an `<h3>` heading that says "Quick Stats".
* Add two paragraphs (`<p>`) listing your current year level and your location.



---

### Room 2: The Projects Page (`projects.html`)

Open `projects.html` and go inside its `<main>` tag.

1. Add a main `<h1>` heading at the top saying "My Development Showcases".
2. Open a `<section>` tag with an `id` of "gallery".
3. Inside the gallery, we will use the `<article>` tag. We use this because a project card is a standalone piece of content that makes sense on its own.
* Open an `<article>` tag.
* Inside it, add an `<h3>` heading with the name of a project (e.g., "Project 1: Semantic Portfolio").
* Add a paragraph (`<p>`) describing the project.
* Add an anchor tag (`<a>`) that links out to `https://github.com`. Add the attribute `target="_blank"` to the anchor tag so it opens safely in a new tab.


4. Repeat Step 3 to create a second `<article>` for a second project.

---

### Room 3: The Contact Page (`contact.html`)

Open `contact.html` and go inside its `<main>` tag. Here, we build an interactive form.

1. Add an `<h2>` heading saying "Connect With Me".
2. Open a `<form>` tag.
3. Inside the form, you will build three input areas. *Every input must have a matching label for accessibility.*
* **Name Field:** Create a `<label>` tag that says "Your Full Name:". Below it, create an `<input>` tag with the attribute `type="text"`.
* **Email Field:** Create a `<label>` tag that says "Email Address:". Below it, create an `<input>` tag with the attribute `type="email"` (this forces the browser to check for an @ symbol).
* **Message Box:** Create a `<label>` that says "Your Message:". Below it, use the `<textarea>` tag (note: this is not an input tag, it is its own tag and requires a closing `</textarea>`!).


4. At the bottom of the form, add a `<button>` tag with the attribute `type="submit"`. Put the text "Send Message" inside the button.

---

### Room 4: The Learning Journal (`blog.html`)

Open `blog.html` and go inside its `<main>` tag. This page uses special tags meant for reading materials.

1. Add an `<h1>` heading saying "My Web Dev Journey".
2. Open an `<article>` tag to house your first blog post.
3. **Post Details:** * Add an `<h2>` heading for the post title (e.g., "Week 1: Surviving HTML").
* Below the title, type "Published on: " and wrap today's date in a `<time>` tag. This tells search engines exactly when this was written.


4. **Post Content:**
* Write two paragraphs (`<p>`) explaining what you learned today and what was difficult.
* Let's add a quote! Open a `<blockquote>` tag. Inside it, type a piece of advice you want to remember (e.g., "Semantics provide meaning, not style").


5. **Adding a Screenshot Code:**
* Open a `<figure>` tag. This is used for images that have captions.
* Inside the figure, add an `<img>` tag. Point the `src` attribute to the screenshot you saved in Phase 1 (`src="screenshot.png"`) and add an `alt` description (e.g., `alt="Screenshot of HTML boilerplate"`).
* Directly below the image (but still inside the `<figure>`), add a `<figcaption>` tag. Type a caption like "My first HTML layout."

---
## Activity 1 Grading Rubric (50 Points Total)

| Evaluation Criteria | Excellent | Proficient | Needs Work | Score |
| :--- | :--- | :--- | :--- | :--- |
| **1. Semantic Architecture (15 pts)**<br>*Did you use the correct HTML "boxes"?* | **(13–15 pts)** Flawless use of tags (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`). Tags are properly nested and closed. Only one `<main>` is used per page. | **(7–12 pts)** Mostly correct, but contains minor structural errors (e.g., mixing up `<section>` and `<article>`, or forgetting a closing tag). | **(0–6 pts)** Missing core structural tags. Everything is just loosely thrown onto the page without semantic meaning, or layout is broken. | **/15** |
| **2. Content Substantiality & Effort (15 pts)**<br>*Did you write meaningful, personalized content?* | **(13–15 pts)** Exceptional effort. The "About Me" is descriptive, project descriptions are clear, and the blog post shows genuine thought and reflection on the learning process. | **(7–12 pts)** Content is present but brief or slightly generic. The blog post might be only one short sentence, or project descriptions lack detail. | **(0–6 pts)** Bare minimum effort. Uses 1-word answers, excessive "Lorem Ipsum" dummy text, or leaves sections completely blank. | **/15** |
| **3. Navigation & File Structure (10 pts)**<br>*Does the website actually work?* | **(9–10 pts)** All 4 files are named correctly. The navigation menu is identical on all pages, and every link works flawlessly without "File Not Found" errors. | **(5–8 pts)** Files exist, but 1 or 2 links are broken, or a page is missing the updated navigation menu. | **(0–4 pts)** Missing files, broken relative file paths, or severe inconsistencies across the master templates. | **/10** |
| **4. Media & Accessibility (10 pts)**<br>*Is the site inclusive and media-ready?* | **(9–10 pts)** Images load perfectly with descriptive `alt` text. The contact form correctly pairs every `<label>` with its matching `<input>`. | **(5–8 pts)** Images load but are missing `alt` text, or form labels exist but are not logically connected to the input fields. | **(0–4 pts)** Broken image links (`src` errors), completely missing `alt` text, and form inputs are placed without labels. | **/10** |
| **Total Score** | | | | **__/50** |

---

### 💡 Tips for Maxing Out Your Score:

* **Write like a professional:** Treat this like a real portfolio you are sending to a hiring manager. Double-check your spelling and grammar in your paragraphs.
* **Click every single link:** Before you type `git push`, open your files in the browser one last time. If clicking "Learning Journal" from your Contact page gives you an error, fix it before submitting!
* **Check your image paths:** If your image shows up as a broken icon, your `src="..."` text does not match the exact name of your image file. Remember, `Profile.jpg` is different from `profile.jpg`!
