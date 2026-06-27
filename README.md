# Nexus — Digital Studio Single Page App

A premium, highly interactive single-page portfolio application built for **Nexus Digital Studio**. The project utilizes a component-driven React architecture compiled directly in the browser via Babel, featuring a rich dark aesthetic with gold accents, customized scrollbars, and fine-tuned micro-animations.

---

## File Directory

- [index.html](./index.html): Contains the single page container, embedded custom CSS stylesheets, React compiler links, and the complete application script.

---

## Features & Component Architecture

The app is broken down into structured React components and custom hooks, coordinated via a global state context:

1. **Global App State (`AppContext` & `AppProvider`)**:
   - Manages state variables for `currentPage` navigation routing, `isTransitioning` status, `menuOpen` mobile toggles, and shared contact form properties.
   - Triggers smooth client-side page transitions by applying entry/exit classes with timed delays.
2. **Dynamic Navigation Header (`Navbar`)**:
   - Toggles translucent blurred backgrounds and borders once scroll thresholds are met (`useScrollNav` hook).
   - Responsive mobile hamburger controller slide drawer.
3. **Scroll Reveal Hook (`useReveal`)**:
   - Uses the `IntersectionObserver` API to monitor elements containing `.reveal`.
   - Triggers slide-ups and fade-ins when elements enter the viewport.
4. **Pages**:
   - **Home Page**: Includes a hero section with animated metrics cards, a looping infinite text marquee track, a detailed grid of 6 services, and a call-to-action banner.
   - **About Page**: Visual timeline metric boxes, a principles grid, and detailed team profile cards (Arjun, Sofia, Kai) with distinct color gradients.
   - **Contact Page**: Complete client onboarding form featuring real-time input fields, field validations (validates name, valid email regex formats, phone structures, and a 20-character minimum message constraint), and a success banner upon submission.

---

##  Technology Stack

- **Framework**: React 18 (loaded via CDN)
- **Compiler**: Babel Standalone (translates JSX directly in the browser)
- **Styles**: Vanilla CSS3, custom typography fonts (Cormorant Garamond + Outfit) from Google Fonts, SVG noise overlay texture filters
- **APIs**: HTML5 IntersectionObserver, browser window Scroll APIs

---

##  How to Run

Because this project loads external script libraries and utilizes browser compilers, it runs best when served from a local server.

```bash
# Start serve from root directory
npx serve .
```
Then visit: `http://localhost:3000/LEVEL_2/TASK_1/`
