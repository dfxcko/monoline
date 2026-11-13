# Monoline

**[monoline.si](https://monoline.si)** — design 3D-printed lamps, vases and bowls that print as one continuous line.

Sculpt the form, add textures, transitions and holes, check printability live, and export spiral-vase G-code or STL for Bambu Lab printers (0.4 / 0.6 / 0.8 mm nozzles).

## The site
A static site with no build step. `index.html` is the whole app; it loads Three.js from jsDelivr and fonts from Google Fonts.

| File | Purpose |
|---|---|
| `index.html` | The app |
| `favicon.svg`, `favicon.png`, `apple-touch-icon.png`, `icon-512.png` | Icons |
| `og.png` | Link-preview image |
| `site.webmanifest`, `robots.txt`, `sitemap.xml`, `_headers` | Site metadata (Cloudflare Pages reads `_headers`) |

## Hosting on Cloudflare Pages
1. Cloudflare dashboard → **Workers & Pages** → **Create** → **Pages** → **Connect to Git** → pick this repository.
2. Build settings: framework preset **None**, build command empty, output directory `/`.
3. After the first deploy: the project → **Custom domains** → add `monoline.si` (and `www.monoline.si`).
4. At the domain registrar, set the nameservers Cloudflare shows you (or add the CNAME record it gives).

Every push to `main` then goes live automatically.

## Run locally
```bash
python3 -m http.server 8000   # then open http://localhost:8000
```

Made by [David Ficko](https://davidficko.com).
