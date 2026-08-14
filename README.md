# vahanalabs.ai — static site

Flat folder. Every file sits at the top level — **no subfolders**. Upload all of them together, side by side.

## Files

| Path | Page |
|---|---|
| `index.html` | Master home page — technology capability vs. realized value |
| `healthtech-companies.html` | For healthtech companies (was the home page) |
| `healthcare-operators.html` | For healthcare organizations & investors |
| `about.html` | Arvita Tripati — about (redirect target for arvitatripati.com) |
| `market-entry.html` | 301/refresh redirect → `healthtech-companies.html` |
| `speaking.html` | Speaking |
| `press-speaking.html` | Media — press, podcasts, speaking history |
| `book.html` | Built to Survive |
| `cell-therapy-operating-journey.html` | Cell therapy operating journey |
| `map-*.html` | Seven specialty operating-leverage one-pagers |
| `support.js` | Page runtime — required, do not rename |
| `sitemap.xml`, `robots.txt` | Search |
| `*.jpg`, `*.png`, `favicon.svg` | Photography, book cover, favicons |

Fonts (Lora, Open Sans) load from Google Fonts. Colors, spacing, and type are baked into the pages — there is no external stylesheet to lose. The `map-*.html` one-pagers carry the design tokens inlined in their own `<style>` block.

## Deploy

- **GitHub Pages** — commit every file to the repo root (or `/docs`), enable Pages on that branch. When uploading through the GitHub web UI, select all the files at once; do not upload only the HTML.
- **Netlify / Vercel / Cloudflare Pages** — drag the folder in. No build command.
- **Any web host** — upload all files to the same directory.

## DNS

- `vahanalabs.ai` → this site.
- `arvitatripati.com` → 301 redirect to `https://vahanalabs.ai/about.html`.

Canonical URLs are declared per page against the `vahanalabs.ai` paths, so the redirect will not create duplicate-content ambiguity.

## Search

`sitemap.xml` lists all fifteen pages; `robots.txt` points to it. The commercialization content that previously sat at `/` now lives at `/healthtech-companies.html`, and `/` carries the new master positioning. After deploy submit the sitemap in Google Search Console and request reindexing of `/`, `/healthtech-companies.html` and `/healthcare-operators.html`. Point a server-side 301 from `/market-entry.html` to `/healthtech-companies.html` if the host allows it; the file itself carries a canonical plus meta refresh as a fallback.

## Navigation

Header and footer are identical on every page: **For healthtech companies · For healthcare organizations · Speaking · Insights · About**, plus the booking CTA. The wordmark links to `index.html`; Insights points at the Substack. `Built to Survive` and the Substack sit in the footer only. The specialty maps are reached from the homepage, not the nav.

## Before going live

- `mailto:` CTAs on `book.html` (launch announcement) stand in for a real signup form.
- "Follow the authors" on `book.html` points to Arvita's LinkedIn only.
- Claims worth a last read: the `$81M` attribution wording, `27× scale with 20% lower unit cost`, `2.5 months to four weeks`, and the "Work involving Gilead and Moderna programs" line in the `market-entry.html` credibility strip.
