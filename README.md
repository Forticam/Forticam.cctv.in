# Forticam CCTV – forticam.cctv.in

CCTV-focused website for **Forticam**: dome, bullet, PTZ and Wi-Fi cameras, DVR/NVR recorders and video door phones for homes, offices and companies in Faridabad and Gurgaon. Smart Surveillance, Smarter Protection For A Safer Spaces.

Plain HTML, CSS and JavaScript. No build step, no dependencies. It shares its brand, photos and styling with the main site, [forticam.in](https://forticam.in/) (repo `Forticam/forticam.in`).

## Files

| Path | What it is |
| --- | --- |
| `index.html` | The page: hero, cameras, which camera where, installation steps, gallery, FAQ, contact |
| `styles.css` | All styling |
| `script.js` | Photo lightbox and the consultation form (opens WhatsApp with the details filled in) |
| `images/`, `logo.png` | Photos and logo |
| `netlify.toml` | Hosting settings: security headers, caching, `www` redirect |
| `robots.txt`, `sitemap.xml`, `404.html` | SEO and error page |
| `Src, Public - View 1.tsv.csv` | Project board export (not part of the site) |

## Run it locally

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Publish

**Netlify (recommended)**

```bash
npm install -g netlify-cli
netlify login
netlify deploy --prod --dir=.
```

Or connect this GitHub repo in Netlify with the build command empty and the publish directory set to `.`, then add `forticam.cctv.in` under Domain management. Every push to `main` then deploys automatically.

**GitHub Pages**: Settings, Pages, deploy from `main` and `/ (root)`, then set the custom domain to `forticam.cctv.in`.

## Editing

- Phone and WhatsApp number: search `9217295528` in `index.html` and `script.js`.
- Add a support email: put a `mailto:` row in the contact `<dl class="details">` and an `email` field in the structured data block at the top of `index.html`.
- FAQ answers appear twice, in the visible FAQ section and in the FAQPage structured data. Change both together.
