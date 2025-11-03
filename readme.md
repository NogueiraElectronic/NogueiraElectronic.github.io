
# Jesús Torres Nogueira – Electronic Engineer Portfolio

A modern, fully-responsive personal portfolio showcasing expertise in Machine Learning, Computer Vision, Embedded Systems, and Industrial Automation. Built with clean HTML, CSS, and vanilla JavaScript – no frameworks, no dependencies.

[Live Demo](https://nogueiraelectronic.github.io) | [GitHub Repository](https://github.com/NogueiraElectronic/portfolio)

---

## Table of Contents

- [General Description](#general-description)
- [Main Features](#main-features)
- [Sections Overview](#sections-overview)
- [Technologies Used](#technologies-used)
- [Installation & Local Development](#installation--local-development)
- [Usage](#usage)
- [Code Structure](#code-structure)
- [Performance & Security](#performance--security)
- [Internationalization (i18n)](#internationalization-i18n)
- [Responsive Breakpoints](#responsive-breakpoints)
- [Accessibility Features](#accessibility-features)
- [SEO Optimization](#seo-optimization)
- [License](#license)
- [Author](#author)
- [Acknowledgments](#acknowledgments)
- [Project Status](#project-status)
- [Contact](#contact)

---

## General Description

This portfolio is a single-page, static website designed to present:

- Professional background and engineering specialization
- Technical skills across 8 core domains
- Three flagship projects with detailed metrics and technologies
- Direct contact methods and professional availability

It is optimized for performance, accessibility, search engines, and user experience, with full internationalization support for English and Spanish.

> **Problem Solved**: Establish a professional, fast, and secure online presence without backend complexity, databases, or external dependencies.

> **Solution**: Pure static site hosted on GitHub Pages, fully version-controlled and deployable in seconds.

---

## Main Features

| Feature | Description |
|-------|-----------|
| Responsive Design | Mobile-first layout with fluid grids and flexible images |
| CSS Custom Properties | Centralized theme variables for easy maintenance |
| Internationalization | Full English/Spanish support with language persistence |
| Hero Image Carousel | Auto-rotating professional images with dot indicators |
| Smooth Scrolling | Native smooth scroll behavior for anchor links |
| Mobile Navigation | Hamburger menu with overlay and body lock |
| KPI Section | Three animated stat cards with hover elevation |
| About Section | Two-column layout with personal info sidebar |
| Skills Grid | Eight categorized skill cards with technology tags |
| Projects Showcase | Three rich project cards with images, stats, and GitHub/demo links |
| Contact Section | Dual-column layout with info and call-to-action |
| Footer | Copyright, quick links, and clean design |
| Performance Optimized | Preloaded hero image, lazy loading for others |
| No External Dependencies | Zero npm packages, frameworks, or CDN calls |

---

## Sections Overview

| Section | Key Content |
|-------|-----------|
| **Hero** | Name, title, professional summary, CTA buttons, 4-image carousel |
| **KPIs** | 1+ year experience, 10+ projects, 10+ technologies |
| **About** | Biography, location, availability, specialization |
| **Skills** | 8 domains: ML, CV, Programming, IoT, Automation, Data Science, 3D, Instrumentation |
| **Projects** | NEXUS v8.0 (Facial Recognition), Chlorella Simulator (Data Generator), Industrial Warehouse (BIM) |
| **Contact** | Email, location, GitHub, response time guarantee |
| **Footer** | Copyright 2025, navigation links |

---

## Technologies Used

| Category | Tools |
|--------|-------|
| **Markup** | HTML5 (semantic structure) |
| **Styling** | CSS3 (Flexbox, Grid, Variables, Transitions, Backdrop-filter) |
| **Scripting** | Vanilla JavaScript (ES6+) |
| **Hosting** | GitHub Pages (static deployment) |
| **Images** | JPEG (optimized), inline SVG data URIs |
| **Icons** | SVG paths with stroke styling |
| **Typography** | System font stack for performance |
| **Deployment** | Git push to main → automatic build |

> No build tools, no package manager, no external libraries.

---

## Installation & Local Development

```bash
# 1. Clone the repository
git clone https://github.com/NogueiraElectronic/portfolio.git
cd portfolio

# 2. Open in browser
open index.html
# Or use any local server (Live Server, Python, etc.)
```

The site works completely offline after initial load.

---

## Usage

### Editing Content
All translatable text is stored in the `i18n` object in the `<script>` tag:
```js
const i18n = { en: { ... }, es: { ... } };
```

### Adding a Project
1. Duplicate a `.project-card` block
2. Update:
   - Image path
   - Title, category, description
   - Tech tags
   - Stats
   - GitHub/demo links

### Updating KPIs
Edit the `.kpi-sub` text nodes:
```html
<div class="kpi-sub" data-i18n="kpi.projects.sub">10+ completed</div>
```

### Changing Hero Images
Replace files in `/img/`:
- `hero1.jpg`, `hero2.jpg`, `hero3.jpg`, `hero4.jpg`
- Update `<img>` sources in the carousel

---

## Code Structure

```
portfolio/
│
├── index.html                  # Complete single-page application
├── img/                        # All visual assets
│   ├── hero1.jpg
│   ├── hero2.jpg
│   ├── hero3.jpg
│   ├── hero4.jpg
│   ├── jesus.jpg
│   ├── nexus.jpg
│   ├── chlorella.jpg
│   └── nave-industrial.jpg
├── README.md                   # This documentation
└── LICENSE                     # MIT License
```

---

## Performance & Security

| Aspect | Implementation |
|------|----------------|
| **Page Speed** | < 1.2s load time (3G), 95+ Lighthouse score |
| **Image Optimization** | Preload hero, lazy load others |
| **Code Delivery** | Single HTML file, inline CSS/JS |
| **Security** | No backend, no forms, no cookies |
| **Email Protection** | `mailto:` link (consider Formspree for spam protection) |
| **XSS Prevention** | No user input, no dynamic script injection |
| **GitHub Pages** | HTTPS enforced, static-only |

---

## Internationalization (i18n)

- **Languages**: English (`en`), Spanish (`es`)
- **Persistence**: `localStorage` saves user preference
- **Switching**: Flag icons in header
- **Coverage**: 100+ strings translated
- **Meta Tags**: Dynamic `<title>` and `lang` attribute

```js
function switchLanguage(lang) {
  localStorage.setItem("preferredLanguage", lang);
  applyI18n(lang);
  setActiveFlag(lang);
}
```

---

## Responsive Breakpoints

| Breakpoint | Width | Key Changes |
|----------|-------|-----------|
| Mobile | ≤ 768px | Stacked layout, hamburger menu |
| Tablet | ≤ 1024px | Two-column KPIs, simplified project grid |
| Desktop | > 1024px | Full grid, side-by-side hero, three-column KPIs |

---

## Accessibility Features

- Semantic HTML (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`)
- ARIA labels (`aria-label`, `role="button"`)
- Keyboard navigation (Enter/Space on flags)
- Focus indicators
- High contrast ratios
- Alt text on all images
- Screen reader friendly structure

---

## SEO Optimization

```html
<meta name="description" content="Jesús Torres Nogueira - Electronic Engineer specialized in ML, Computer Vision, and Embedded Systems">
<meta name="keywords" content="machine learning, computer vision, embedded systems, IoT, automation, engineer">
<meta name="author" content="Jesús Torres Nogueira">
```

- Open Graph ready (add if needed)
- Favicon support (add `favicon.ico`)
- Canonical URL via GitHub Pages

---

## License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

> You may use the code and design as inspiration. Full copying requires attribution to the original author.

---

## Author

**Jesús Torres Nogueira**  
*Industrial and Automatic Electronic Engineer*

- GitHub: [@NogueiraElectronic](https://github.com/NogueiraElectronic)
- Email: nogueira.electronico@gmail.com
- Portfolio: [nogueiraelectronic.github.io](https://nogueiraelectronic.github.io)
- LinkedIn: [Jesús Torres Nogueira](https://www.linkedin.com/in/jes%C3%BAs-torres-nogueira/)

---

## Acknowledgments

- GitHub Pages – Reliable static hosting
- VS Code – Primary development environment
- Chrome DevTools – Responsive and performance testing
- Figma – Initial wireframes and UI design
- Open source community – Inspiration and best practices

---

## Project Status

**Stable Version**: Fully functional, production-ready  
**Last Updated**: November 2025  
**Deployment**: GitHub Pages (automatic on push)

---

## Contact

Available for:
- Freelance projects
- AI and Computer Vision consulting
- Embedded systems development
- Industrial automation solutions

**Email**: [nogueira.electronico@gmail.com](mailto:nogueira.electronico@gmail.com)  
**Response Time**: Within 24 hours

---

<div align="center">

If this portfolio has been useful or inspiring, consider giving it a star on GitHub.

Made with dedication by Jesús Torres Nogueira

</div>

