# Kavya Chaturvedi — Portfolio Website

A single-file, zero-build portfolio site. Everything lives in `index.html` (HTML + CSS + JS), so there is nothing to install or compile.

## Deploy to Vercel (2 minutes)

**Option A — drag and drop (easiest)**
1. Go to https://vercel.com/new (log in with GitHub or email).
2. Drag this whole folder onto the page.
3. Click Deploy. You get a live URL like `kavya-portfolio.vercel.app`.

**Option B — via GitHub**
1. Create a new repo (e.g. `portfolio`) on GitHub and upload `index.html`.
2. On https://vercel.com/new, import that repo and click Deploy.
3. Every future edit you push auto-deploys.

**Option C — CLI**
```bash
npm i -g vercel
cd kavya-portfolio
vercel --prod
```

## Custom domain

In your Vercel project → Settings → Domains, add `kavyachaturvedi.info` and follow the DNS instructions shown there.

## Editing content

Open `index.html` in any editor — all text is plain HTML:
- Hero and stats: near the top under `<header>`
- Experience: `<section id="experience">`
- Projects: `<section id="projects">` (each project is one `.card` block; `data-cat` controls which filter chips it appears under)
- Case studies, awards, beyond work, contact: their own sections below

Client prototype work is intentionally anonymized (no client brand names).
