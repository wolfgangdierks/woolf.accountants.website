# woolf.accountants website

Static website for woolf.accountants. Plain HTML and one CSS file. No framework, no build step, no JavaScript, no tracking. Fonts and images are served from this site; no outside services are called.

## Structure

| File | What it is |
| --- | --- |
| `index.html` | Home page |
| `services.html` | Services & Packages |
| `about.html` | About |
| `contact.html` | Contact |
| `404.html` | Shown by GitHub Pages for any missing page |
| `style.css` | The only stylesheet, used by every page (colors are set at the top) |
| `assets/fonts/` | Public Sans typeface files, served from this site (license in `OFL.txt`) |
| `assets/img/` | Wolf logo badge, browser icons, link-preview image (`og-image.png`), and the illustrations (`.svg`) |
| `CNAME` | Custom domain for GitHub Pages (`woolf.accountants`) |
| `robots.txt`, `sitemap.xml` | For search engines |
| `.nojekyll` | Tells GitHub Pages to serve the files as-is |

Each page is a complete HTML file. The header (site name, navigation, "Talk about your margins" button) and the footer are repeated in every page, so a change to either must be made in all five HTML files.

## Editing the copy

1. Open the page's `.html` file and change the text between the tags. The page text is inside `<main>`.
2. Use typographic apostrophes and quotes (’ “ ”) in visible text. Write `&amp;` for an ampersand.
3. Keep the brand lowercase: woolf.accountants.
4. If you change what a page is about, update its `<title>`, `<meta name="description">`, and the matching `og:title` / `og:description` tags in the `<head>`.
5. Email buttons link to `mailto:wolfgang@woolf.accountants?subject=...`. Spaces in the subject are written `%20` and an apostrophe is `%27`.
6. If you add a page, add it to the nav in every page and to `sitemap.xml`.

To preview locally, open `index.html` in a browser, or run `python3 -m http.server` in this folder and visit http://localhost:8000.

## Deploying

The site is served by GitHub Pages from the root of the `main` branch. It deploys automatically when changes are pushed to `main`; there is nothing to build.
