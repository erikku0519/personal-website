# Eric Jung — Personal Website

A static personal/speaker site for Eric Jung (Product Manager at Amazon Japan). Built from the Figma mock with a bilingual **EN / KR** toggle.

## Stack
Plain HTML + CSS + vanilla JS — no build step, no dependencies.

- `index.html` — markup, all translatable strings tagged with `data-i18n`
- `styles.css` — light theme, indigo (`#6366f1`) accent, responsive
- `script.js` — `I18N` dictionary (English + Korean) + language toggle (persists to `localStorage`)
- `assets/logos/` — "Featured At" logos
- `assets/img/` — hero / about talk photos

## Run locally
No build needed — just serve the folder:

```bash
cd PersonalWebsite
python3 -m http.server 8000
# open http://localhost:8000
```

(Opening `index.html` directly works too, but a server avoids any font/asset quirks.)

## Language toggle
Click **EN / KR** in the top-right of the nav. The choice is saved to `localStorage` and re-applied on the next visit. To add or edit copy, update the matching key in both `en` and `kr` blocks of the `I18N` object in `script.js`.

## Deploy
Any static host works — GitHub Pages, Netlify, Cloudflare Pages, S3. Upload the folder as-is.

## Notes / TODO
- Replace placeholder links (social, article URLs, `mailto:`) with real ones.
- Article titles in KR/JP are intentionally kept in their original language.
- Hero/about images are Eric's talk thumbnails; swap for higher-res headshots if desired.
