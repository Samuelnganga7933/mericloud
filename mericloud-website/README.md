# MeriCloud website

Marketing site for MeriCloud, a software and systems engineering company.

## What is here

| Path | Purpose |
|---|---|
| `site/index.template.html` | The whole interactive site as one readable HTML file. Images are inserted at build time. |
| `assets/` | Photography and screenshots used by the site. |
| `build.py` | Embeds the images and writes `dist/index.html`, a single file you can host anywhere. |
| `design-canvas/` | Claude Design artboards for every page (static layouts) and `canvas.json`. |
| `docs/brief.md` | Summary of the design and content brief. |

## Build and preview

```bash
python3 build.py
open dist/index.html   # or serve the dist/ folder with any static host
```

The site needs internet access only for Google Fonts.

## Notes

- Colours follow the visitor browser setting (light or dark). There is no theme toggle.
- The contact form and the newsletter button open an email to hello@meridian.tech in the visitor mail app. Connect a form or mailing service before launch. If the company email domain changes with the new name, update it in site/index.template.html.
- The cookie banner stores the visitor choice in local storage. It does not set analytics cookies yet.
- Legal technology and the two prototype products use a generic office photo. Replace it with real screenshots when available.
- Service lists, process stages and FAQ answers are drafted wording. Check them against what the company actually offers before launch.
