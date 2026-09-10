# web-design-capstone

Student web design capstone. Build a complete, original multi-page site with semantic HTML and CSS. The author is a beginner and has not learned JavaScript yet.

## Stack

- **HTML5** — structure and content
- **CSS3** — layout, typography, and visual design
- No JavaScript unless the student explicitly asks for it
- No frameworks, build step, bundler, or package manager unless asked

Serve files locally (Live Server, or opening `index.html`) so relative paths work as they will on deploy.

## Layout

Keep the site multi-page and file-based:

```
index.html
pages/          # additional HTML pages (about, contact, etc.)
css/
  styles.css    # shared styles
assets/
  images/
  icons/
```

- One primary stylesheet unless a page truly needs its own.
- Link CSS with relative paths from each HTML file (`css/styles.css` from the home page; `../css/styles.css` from files in `pages/`).
- Name files in kebab-case (`about.html`, `hero-banner.jpg`).

## HTML

- Use semantic landmarks: `header`, `nav`, `main`, `section`, `article`, `aside`, `footer`.
- One `h1` per page. Headings must nest in order (`h2` then `h3`, never skip).
- Images need meaningful `alt` text; decorative images use `alt=""`.
- Forms need associated `<label>` elements. Use a real `action` if a form submits; otherwise keep fields usable without scripts.
- Prefer links for navigation. Do not use tables for layout.
- Do not rely on JavaScript for menus, tabs, or other core behavior. Use HTML and CSS (for example, links between pages, or a checkbox/`<details>` pattern if a mobile menu is needed).

## CSS

- Mobile-first. Start with a single-column layout; add breakpoints as needed (`min-width`).
- Prefer Flexbox and CSS Grid over floats or absolute positioning for page layout.
- Use custom properties for colors, fonts, and spacing on `:root`.
- Keep specificity low: classes over IDs for styling; avoid `!important`.
- Do not use inline styles except for one-off experiments that get moved into CSS.
- Respect reduced motion: wrap non-essential animation in `@media (prefers-reduced-motion: no-preference)`.

## Accessibility and quality

- Keyboard operable: visible focus, logical tab order, no keyboard traps.
- Color contrast should meet WCAG AA for text.
- Do not convey information by color alone.
- Validate HTML and check the site at desktop and phone widths before calling a page done.

## Working in this repo

- Match existing naming, indentation, and comment style.
- Change only what the task needs; do not add JavaScript, frameworks, CMS, or backend code unprompted.
- When adding a page, reuse shared header/nav/footer markup and link it from the site nav.
- Prefer real copy and images over lorem ipsum once the design direction is set.
- Explain new HTML or CSS in plain language when it helps a beginner understand the change.
