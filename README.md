# Giammarino Paving & Sealcoating — Marketing Site

Static brochure site for **Giammarino Paving & Sealcoating** (asphalt paving, sealcoating, crack filling, line striping, patching).

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

## Logo slot

Sticky nav and footer include a dashed amber **LOGO** frame next to the GIAMMARINO wordmark. **Client logo drops in here** — replace the `.logo-frame` / wordmark block with an `<img>` (or SVG) when artwork is ready. Keep alt text like `Giammarino Paving & Sealcoating`.

## Photos

Job-site JPGs live under `assets/photos/` with simple kebab-case names. Highest-res asset: `equipment-giammarino-trailer.jpg` (branded trailer). Hero uses the wide `sealed-driveway-brick-garage.jpg`. Public phone **(607) 242-8176**.

Facebook promo overlay photo (`driveway-promo-estimate.jpg`) was removed from the gallery UI and deleted from the repo.

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

## Content notes

- Testimonials are real Facebook reviews (attributed lightly as “Facebook review”).
- Primary service area: Binghamton metro / Broome + nearby Southern Tier (not exclusive).
- Contact prefers call/text; email not published yet. Estimate form is UI-only until wired (e.g. Formspree).
- Equipment/process shots may show third-party machine brands (Ryno Worx, Wacker) — illustration only; site brand remains Giammarino.
