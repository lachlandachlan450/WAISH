# WAISH — Warwick AI Safety Hub website

A static, dependency-free site: four HTML pages sharing one stylesheet. No build step.

## Hosting on GitHub Pages

1. Create a repository (e.g. `waish-site`) and push these files to the root of the `main` branch.
2. In the repo, go to Settings → Pages.
3. Under "Build and deployment", set Source to "Deploy from a branch", pick `main` and `/ (root)`, then save.
4. The site appears at `https://<username>.github.io/waish-site/` within a couple of minutes.

To use a custom domain, add it under Settings → Pages and point your DNS at GitHub per their docs.

## Customising

- **Colours, fonts, spacing** — everything lives in the `:root` block at the top of `style.css`. Change a variable once and it applies site-wide.
- **People** — edit `people.html`; each profile is a self-contained `<div class="person">` block you can copy. Put photos in an `images/` folder and swap the placeholder `<div>` for an `<img>` (a comment in the file shows how).
- **Application link** — in `apply.html`, replace the `href="#"` on the "Open the application form" button with your Google Form URL, and fill in the `[DATE]` deadline.
- **Contact details** — placeholders are marked in `contact.html`.
- **Blog link** — the "Blog" nav item on every page (header and footer) currently points to the dummy URL `https://waish.substack.com`. Find-and-replace that URL across the HTML files once your Substack (or other blog) exists.
- **Hero pattern** — the tick-mark field on the home page is drawn by the small script at the bottom of `index.html`; adjust `gap`, `len`, or the stray probability to taste, or delete the `<svg>` and script to remove it.

## Adding a page

Copy any existing page, update the `<title>`, move the `aria-current="page"` attribute in the nav to the new link, and add the link to the nav in every page (header and footer).
