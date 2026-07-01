# [Iamlucie.com](http://Iamlucie.com)

### Product Designer Profile

A personal lean tech stack project serving 3 purposes:

1. **Stay in touch with modern front-end development** workflows and tooling.
2. **Demonstrate ability to ship and evolve over time** to complement NDA-work and sandbox projects.
3. **A public-facing website** for general visibility.

---

## 🚀 Project Overview

This version of my website originated in early **2025** when Behance + Carrd.co + LinkedIn was no longer sufficient for my professional needs. The goal was to create a dual-purpose platform:

1. **A public-facing website** for general visibility.
2. **A private portfolio** secured behind a password for sensitive case studies.

## 🛠 Tech Stack


| Category       | Tools                                                                                                    |
| -------------- | -------------------------------------------------------------------------------------------------------- |
| **Language**   | HTML5, CSS3, Vanilla JavaScript                                                                          |
| **Editor**     | Visual Studio Code (Migrated from Atom)                                                                  |
| **Hosting**    | Apache (Traditional / Low-footprint)                                                                     |
| **AI Support** | GitHub Copilot (code), Claude Code (brand, skill docs, CSS/layout refactor), Cursor (research, analysis) |
| **VCS**        | GitHub                                                                                                   |


---

## 📅 Project History & Evolution

### Phase 1: The Refresh (2025)

This phase focused on migrating from "no-code" to a custom-built environment to refresh coding skills and modernize the stack.

- **IDE Migration:** Switched from **Atom** to **Visual Studio Code**.
- **Refactoring:** Generated > structured HTML and CSS.
- **Minimalist Philosophy:** Intentionally avoided heavy frameworks (no Node.js or React) to keep the site simple, fast and cost-effective.
- **Layout Mastery:** Used **GitHub Copilot** to refresh on how web layouting gets done in 2025. #flex
- **Backups:** Revived GitHub and started to use it as the primary backup system.
- **Portfolio:** Derived a private portfolio from the public website.

### Phase 2: AI-Assisted Optimization (2026)

Incorporated advanced AI tools to analyze market, define positioning, and to experiment in code with new sections and video content.

- **Workflow Integration:** Started using **Cursor** (job market trends spotting) and continued using **VS Code** for code updates.
- **Refactoring:** Cleaned up the HTML structure to bring closer portfolio and webpage CSS classes. Resolved undesired project image cropping — switched from fixed height with `object-fit: cover` to natural aspect ratio across all breakpoints.
- **New Features:**
  - Integrated video content with **watch intro pills** indicating playable videos on project cards.
  - Shipped the **FAQ section** as an accordion with real content covering role, process, AI approach, location, and availability.
  - Optimized profile picture: reworked it as a **round grayscale portrait** (matching the portfolio) to mitigate the low-quality photo and reduce visual prominence, shifting content focus to work and expertise instead. A compact 56px avatar variant remains available in the CSS as an alternative.
  - Analyzed the codebase with Copilot in VS Code and saved the public website architecture documentation in `.github/copilot-instructions.md`

### Phase 3: Alignment with New Personal Brand Definition (2026)

Aligned the public site's visual style with the private portfolio so both share one design language, following a refreshed personal brand definition.

- **Typography & components:** Switched typography to **IBM Plex Mono / Sans**, adopted **Boxicons** for the profile links, and restyled the profile buttons as outlined pills.
- **Layout:** Migrated the layout onto the shared width contract documented in the portfolio's `PAGE_WIDTH.md` (1000px max content width, 44px / 22px gutters, 600px mobile breakpoint) and switched project cards to image-first stacking on mobile.
- **Design tuning:** Rescaled the FAQ headings and tightened accordion spacing for the smaller type, and shrank the watch-intro badge to stay proportional to the smaller project images while preserving legibility.
- Kept the site-specific content, FAQ, and video interactivity untouched.

---

## 💡 Key Learnings

- Taking the longer path and learning AI-coding tools sequentially from VS Code over Cursor to Claude Code has the benefit of being able to see the differences and legacy DNA of the older tools.
- Since the project is not built from scratch, it is best to try Claude Code on non-code problems first. Trying to refactor and overhaul the coding workflow simmultaneously would make me slower initially while I want to ship an update in a predictable time and quality.
- AI pair-programming (Copilot) significantly reduces time spent on CSS layout debugging.
- Keeping naming conventions consistent between public and private sections is vital for long-term scalability and future design system experiments.

---

## 🐛 Known Issues

The following bugs are documented and scheduled for fixes:

1. **Video Pill Border Radius Animation** — The watch intro pills on project cards exhibit unwanted border-radius animation on hover. The default and hover states should have identical rounded corners without transitioning between them.
2. **Play/Pause Icon Styling Mismatch** — The play icon (default state) and pause icon (hover state) have different rounded corners, creating a visual inconsistency when hovering over video pills. 
3. **Play/Pause Duplication** — There likely are two sets of play/pause buttons over each other, one from website, one from YouTube. Most obvious when pause button is hit and disappears on mouse moving away while the Youtube one stays present for longer.

---

## 📋 Credits & Attributions

This project utilizes a few external assets and tools to build the optimal lightweight experience:

- **UI Icons:** Adapted from the asset ecosystem provided by Boxicons.
- **Font:** IBM Plex
- **Development Assistance:** Layout optimization and modern CSS techniques assisted by GitHub Copilot, later Cloude LLM models.
- **Photography:** Profile imagery is the intellectual property of the author and using it for AI training is prohibited (All Rights Reserved).

---

*Created by Lucie*