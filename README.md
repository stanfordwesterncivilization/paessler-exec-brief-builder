# Paessler Executive Brief Builder

A single-page tool for Paessler sales reps. The rep fills in customer context, picks 3 PRTG pain points from a preset library, and downloads a customer-ready Word doc to package alongside a quote.

Branded to Paessler's official Brand Book (Corporate Blue `#050f34`, Corporate Cyan `#00AEEF`, Corporate Grey `#e5e6e9`, Roboto).

## Files

- `index.html` - the entire app (form, branding, pain library, .docx generator). No build step.

Built on top of [docx.js](https://docx.js.org/) and [FileSaver.js](https://github.com/eligrey/FileSaver.js/), loaded from CDN at runtime.

## Deploy to GitHub Pages

1. Create a new public repo (e.g. `paessler-brief-builder`) on GitHub.
2. Upload `index.html` and this `README.md` to the root of `main`.
3. **Settings -> Pages -> Branch: `main` / root -> Save.**
4. Wait ~30 seconds. Site will be live at:
   `https://<your-username>.github.io/paessler-brief-builder/`

## Local preview

Just open `index.html` in any browser. No server required.

## How to use it

1. Fill in customer info (Company, Industry, current setup, pain, impact, systems, outcomes, reporting needs).
2. Pick exactly 3 pain points from the PRTG pain library.
3. Add your rep details and the quote URL from `shop.paessler.com`.
4. Click **Create Executive Brief**. A `.docx` downloads.
5. Review and edit in Word. Print to PDF when ready and send alongside the quote.

## Editing the pain library

Open `index.html` and find the `PAIN_LIBRARY` array near the bottom. Each entry has:

- `key` - unique id
- `title` - the page heading
- `challenge` - "The Challenge" copy
- `solution` - "How PRTG Solves It" copy (1 sentence)
- `industryContext` - copy for the grey "Industry Context" block

Add, remove, or rewrite entries to match your messaging. The form auto-renders from array.

## Brand notes

The HTML uses an SVG approximation of the Paessler mark in the header. To use the official logo, drop the SVG/PNG into the repo and replace the `.brand-mark` block in `index.html`.
