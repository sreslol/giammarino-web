# Giammarino Paving & Sealcoating — Marketing Site

Draft static brochure site for **Giammarino Paving & Sealcoating**.

**Live (GitHub Pages):** https://sreslol.github.io/giammarino-web/

## Stack

- Single-page `index.html` at repo root (GitHub Pages from `main` / `/`)
- Tailwind CSS via CDN + Font Awesome CDN
- Small vanilla JS for mobile nav toggle
- No npm build, no framework, no backend

Same hosting shape as [sreslol.github.io](https://github.com/sreslol/sreslol.github.io) (sophiarescinitilcsw.com) — different brand styling (asphalt + amber, not therapy blue).

## Local preview

Open `index.html` in a browser, or from this folder:

```bash
python3 -m http.server 8080
```

Then visit http://localhost:8080

## Custom domain (CNAME + Cloudflare) — not set yet

This repo has **no `CNAME` file yet**. Domain will be wired via Cloudflare later, following the therapy site pattern.

### 1. Add CNAME in this repo

At the repo root, create a file named `CNAME` with a single line (your final domain):

```
www.example.com
```

Commit and push to `main`. GitHub Pages will serve that hostname.

### 2. Cloudflare DNS

In the Cloudflare dashboard for the domain:

1. Add a **CNAME** record:
   - **Name:** `www` (or `@` if using apex via CNAME flattening)
   - **Target:** `sreslol.github.io`
   - **Proxy status:** DNS only (grey cloud) while verifying, or Proxied (orange) once HTTPS works
2. In **GitHub → Settings → Pages → Custom domain**, enter the same hostname and wait for DNS check.
3. Enable **Enforce HTTPS** in GitHub Pages after the certificate provisions.
4. Optional: apex redirect — Cloudflare Page Rule or Redirect Rule from `example.com` → `https://www.example.com`.

### 3. Update OG / canonical URLs

After the custom domain is live, update `og:url` and `og:image` in `index.html` to the production hostname.

## Photo notes

Source photos were Facebook-export thumbnails (~206×206). They live under `assets/photos/` with kebab-case names. Prefer constrained `object-cover` cards over full-bleed blow-ups until higher-res assets are available.

## Demo content

Contact phone/email and testimonials are **placeholders** for layout. Replace before public launch. Equipment photo may show third-party machine lettering — used for process illustration only.
