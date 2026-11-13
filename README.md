# woolf.accountants website

Static website for woolf.accountants. Plain HTML and one CSS file. No framework, no build step, no JavaScript, no tracking. Fonts and images are served from this site; no outside services are called.

## Structure

| File | What it is |
| --- | --- |
| `index.html` | Home page |
| `services.html` | Services & Packages |
| `about.html` | About |
| `contact.html` | Contact |
| `thanks.html` | Shown after someone sends the contact form |
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
4. After changing `style.css`, raise the number in `style.css?v=2` (to `?v=3` and so on) in every HTML file, so browsers load the new styles instead of an old saved copy.
5. If you change what a page is about, update its `<title>`, `<meta name="description">`, and the matching `og:title` / `og:description` tags in the `<head>`.
6. Email buttons link to `mailto:wolfgang@woolf.accountants?subject=...`. Spaces in the subject are written `%20` and an apostrophe is `%27`.
7. If you add a page, add it to the nav in every page and to `sitemap.xml`.

To preview locally, open `index.html` in a browser, or run `python3 -m http.server` in this folder and visit http://localhost:8000.

## Contact form

The form on `contact.html` is sent by Web3Forms (web3forms.com), which emails each message to wolfgang@woolf.accountants and then sends the visitor to `thanks.html`. The Web3Forms access key is the `access_key` hidden field in `contact.html`. It is meant to be public; it only lets the form send to the address it was created for. To change where messages go, create a new key at web3forms.com and replace that value.

## Deploying

The site is served by GitHub Pages from the root of the `main` branch. It deploys automatically when changes are pushed to `main`; there is nothing to build.
