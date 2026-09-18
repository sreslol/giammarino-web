# Giammarino Paving & Sealcoating — Marketing Site

Draft static brochure site for **Giammarino Paving & Sealcoating**.

**Live (GitHub Pages):** https://sreslol.github.io/giammarino-web/

## Stack

- Single-page `index.html` at repo root (GitHub Pages from `main` / `/`)
- Tailwind CSS via CDN + custom `assets/css/site.css` (industrial contractor skin)
- Fonts: Barlow Condensed (display) + Source Sans 3 (body) via Google Fonts
- Font Awesome CDN; small vanilla JS for mobile nav
- No npm build, no framework, no backend

## Visual direction

Charcoal/asphalt backgrounds, amber CTAs and accent bars, sharp corners, numbered section labels (`01 / SERVICES`), photo-forward masonry gallery. Intentionally **not** the soft clinical therapy template used on [sreslol.github.io](https://github.com/sreslol/sreslol.github.io) (sophiarescinitilcsw.com) — no Playfair, no gray-50 page, no pill buttons.

## Local preview

```bash
python3 -m http.server 8080
```

Then visit http://localhost:8080

## Photos

Job-site JPGs live under `assets/photos/` with simple kebab-case names (Facebook export filenames removed). Old ~206×206 thumbs deleted. Highest-res asset: `equipment-giammarino-trailer.jpg` (branded trailer). Hero uses the wide `sealed-driveway-brick-garage.jpg`. Phone **(607) 242-8176** taken from trailer / promo lettering on photos.

`driveway-promo-estimate.jpg` still has baked-in Facebook promo text overlays.

## Custom domain (CNAME + Cloudflare) — not set yet

This repo has **no `CNAME` file yet**. Domain will be wired via Cloudflare later.

### 1. Add CNAME in this repo

At the repo root, create a file named `CNAME` with a single line (your final domain):

```
www.example.com
```

Commit and push to `main`.

### 2. Cloudflare DNS

1. Add a **CNAME** record: Name `www` (or `@` via CNAME flattening) → `sreslol.github.io`
2. In **GitHub → Settings → Pages → Custom domain**, enter the same hostname
3. Enable **Enforce HTTPS** after the certificate provisions

### 3. Update OG / canonical URLs

After the custom domain is live, update `og:url` and `og:image` in `index.html`.

## Demo content

Email and testimonials are still placeholders. Form does not submit. Equipment/process shots may show third-party machine brands (Ryno Worx, Wacker) — illustration only; site brand remains Giammarino.
