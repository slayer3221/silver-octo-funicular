# vahanalabs.ai — static site

Flat folder. Every file sits at the top level — **no subfolders**. Upload all of them together, side by side.

## Files

| Path | Page |
|---|---|
| `index.html` | Healthcare operating leverage (home) |
| `about.html` | Arvita Tripati — about (redirect target for arvitatripati.com) |
| `market-entry.html` | Vahana Labs market entry / PACE |
| `speaking.html` | Speaking |
| `book.html` | Built to Survive |
| `cell-therapy-operating-journey.html` | Cell therapy operating journey |
| `map-*.html` | Seven specialty operating-leverage one-pagers |
| `support.js` | Page runtime — required, do not rename |
| `*.jpg`, `*.png` | Photography, book cover, favicons |

Fonts (Lora, Open Sans) load from Google Fonts. Colors, spacing, and type are baked into the pages — there is no external stylesheet to lose.

## Deploy

- **GitHub Pages** — commit every file to the repo root (or `/docs`), enable Pages on that branch. When uploading through the GitHub web UI, select all the files at once; do not upload only the HTML.
- **Netlify / Vercel / Cloudflare Pages** — drag the folder in. No build command.
- **Any web host** — upload all files to the same directory.

## DNS

- `vahanalabs.ai` → this site.
- `arvitatripati.com` → 301 redirect to `https://vahanalabs.ai/about.html`.

Canonical URLs are declared per page against the `vahanalabs.ai` paths, so the redirect will not create duplicate-content ambiguity.

## Before going live

- `mailto:` CTAs on `book.html` (launch announcement, book list) stand in for a real signup form.
- "Follow the authors" on `book.html` points to Arvita's LinkedIn only.
- The seven `map-*.html` one-pagers are snapshots — re-export if the sources change.
