# Project Copilot Instructions & Architecture

## Project History

- The website originated in early 2025 when my Carrd.co single-page business card site was no longer sufficient (I needed a public website and a portfolio hidden behind a password).
- The project was used to refresh coding skills and update the tech stack:
  - Switched from Atom IDE to Visual Studio Code.
  - Chose to stay with traditional Apache hosting for low cost and footprint.
  - Kept the stack minimal: HTML5 + CSS and minimal JS, no Node.js or React.
  - Used GitHub for backups and learned about modern CSS flex layouting via Copilot, solving many past coding issues.
- In 2026, started using Cursor for research/analysis, Claude Code for skill repository, and returned to VS Code to update the website:
  - Refactored HTML to reduce the gap between portfolio and webpage naming/style files.
  - Made content edits, added video, and experimented with About and FAQ sections.

---

## Project Structure

```
/assets/                # Images, icons, and other static assets
.github/                # GitHub-specific files and Copilot instructions
index.html              # Main HTML file, entry point of the website
index_layout.css        # Layout-related CSS (structure, containers, grid)
index_typography.css    # Typography and font styles
index_buttons.css       # Button and interactive element styles
index_image.css         # Image and video container styles
faq_section.css         # Styles for the FAQ section (experimental)
copilot-instructions.md # This file
```
- `index_style.css` and `about_section.css` are **deprecated** and should not be used for new code.

---

## HTML Structure

- **index.html** is the main entry point.
- Content is organized into semantic sections:
  - Header and navigation (if present)
  - Main content with project showcases (using `.container`, `.columns`, `.image`, `.frame`)
  - About/Transition section (deprecated)
  - FAQ section (experimental, before footer)
  - Footer

---

## Styling

- **index_layout.css**: Handles overall page layout, containers, and responsive breakpoints.
- **index_typography.css**: Manages font families, sizes, weights, and text utilities.
- **index_buttons.css**: Styles for buttons, including play buttons for videos.
- **index_image.css**: Ensures consistent sizing and aspect ratios for images and video frames.
- **faq_section.css**: Dedicated styles for the FAQ section (experimental; may be merged into other CSS files if successful).
- **index_style.css** and **about_section.css**: Deprecated.

---

## JavaScript

- Inline scripts in `index.html` handle video playback (YouTube embeds), restoring cover images, and play button interactions.

---

## Assets

- All images and icons are stored in the `/assets/` directory, referenced with cache-busting query strings.

---

## Best Practices

- Semantic HTML5 structure for accessibility and SEO.
- Separation of concerns: layout, typography, buttons, and section-specific styles are in their own CSS files.
- Responsive design with media queries in CSS files.
- Modular and maintainable code organization.
- No backend or build tools are used.

---

## Known Bugs

- In mid-size view, the images representing projects are not scaling properly.

---

## Diagrammatic Schema

```
project-root/
│
├── index.html
├── index_layout.css
├── index_typography.css
├── index_buttons.css
├── index_image.css
├── faq_section.css
├── index_style.css   (deprecated)
├── about_section.css (deprecated)
├── /assets/
│    └── images, icons, etc.
└── .github/
     └── copilot-instructions.md (this file)
```

**Section Flow in index.html:**
```
[Header/Meta]
    ↓
[Main Content: Project Showcases]
    ↓
[About/Transition Section] (deprecated)
    ↓
[FAQ Section] (experimental)
    ↓
[Footer]
```

---

## FAQ Section Notes

- The FAQ section is experimental. If it works with readers, its styles will be merged into the main typography, buttons, and other CSS files.

---

# Section Structure & Layout Pattern (for new sections)

## General Pattern:
- Each major section starts with a heading (`<h2 class="section-header">`).
- The main content is wrapped in a `<div class="container columns" id="section-id">`.
- Inside the container, use `<div class="wrapper"><div class="inner"> ... </div></div>` for layout consistency.
- Each content block/item is inside a `<div>`, using heading and paragraph classes for typography (e.g., `<h3 class="text-block text-block--large">`, `<p class="text-block text-block--normal">`).
- Use `<hr class="divider">` for visual separation between items, except after the last item.

## Example (FAQ Section):

```
<h2 class="section-header">Frequently Asked Questions</h2>
<div id="faq" class="container columns">
  <div class="wrapper">
    <div class="inner">
      <div>
        <h3 class="text-block text-block--large">What is your design process?</h3>
        <p class="text-block text-block--normal">My design process is iterative and user-centered, starting with research, ideation, prototyping, and continuous feedback.</p>
        <hr class="divider">
      </div>
      <div>
        <h3 class="text-block text-block--large">Do you work remotely?</h3>
        <p class="text-block text-block--normal">Yes, I am fully equipped for remote collaboration and have experience working with distributed teams.</p>
        <hr class="divider">
      </div>
      <div>
        <h3 class="text-block text-block--large">What tools do you use?</h3>
        <p class="text-block text-block--normal">Primarily Figma for design, but I'm also proficient in prototyping tools and have experience with design systems, code, and various collaboration platforms.</p>
        <hr class="divider">
      </div>
      <div>
        <h3 class="text-block text-block--large">Are you available for consulting?</h3>
        <p class="text-block text-block--normal">Yes, I am available for select consulting engagements. Please use the contact options above to get in touch.</p>
      </div>
    </div>
  </div>
</div>
```

## Key Points:
- Use `<h2 class="section-header">` for section titles.
- Use `<div class="container columns" id="...">` for section containers.
- Use `<div class="wrapper"><div class="inner">...</div></div>` for content grouping.
- Use `<div>` blocks with `<h3>` and `<p>` for each item.
- Use `<hr class="divider">` between items.
- This ensures new sections visually and structurally match the rest of the site.