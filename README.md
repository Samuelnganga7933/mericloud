# MeriCloud website

Marketing site for MeriCloud, a software and systems engineering company.

## Structure

| Path | Purpose |
|---|---|
| `index.html` | Site entry point and page shell. |
| `404.html` | Not-found page. |
| `error.html` | Legacy error URL that redirects to `404.html`. |
| `assets/css/site.css` | Site styles, including light and dark themes. |
| `assets/js/site.js` | Page content, navigation and form handling. |
| `assets/images/` | Photography used throughout the site. |
| `assets/favicons/` | Favicons and the Apple touch icon. |
| `favicon.ico`, `favicon.svg` | Root copies browsers request by convention. |

The site is plain static HTML, CSS and JavaScript. There is no build step.

## Deployment

The site is hosted on Vercel from this repository root. Pushing to `main` deploys the files above. `index.html`, `404.html` and `assets/` must stay at the root.

## Forms

The contact and newsletter forms submit directly to Formspree with AJAX; no email app is opened. The endpoint is defined once in `assets/js/site.js`:

```js
const FORMSPREE_ENDPOINT="https://formspree.io/f/mkjrgpya";
```

To use a different Formspree project, replace that value. Contact submissions include the fields `name`, `email`, `phone`, `organisation`, `topic`, `message`, `budget`, `timeline` and `contact_preference`. Newsletter submissions include `email` and the hidden `form=newsletter` field. Both include a `_subject` value so the two form types are easy to tell apart in Formspree.

The company email address is `hello@mericloud.tech`. Keep it consistent anywhere it appears. It is only used for direct contact links; form submissions do not use `mailto:`.

## Notes

- Colours follow the visitor browser setting (light or dark). There is no theme toggle.
- The cookie banner stores the visitor choice in local storage. It does not set analytics cookies yet.
- Legal technology and the two prototype products use a generic office photo. Replace it with real screenshots when available.
- Service lists, process stages and FAQ answers are drafted wording. Check them against what the company actually offers before launch.
