# Health Camper Website

Static website for **healthcamper** — promotes the Health Camper app (Calm-style landing page) and hosts the blog on mental health, motivation, and affirmations.

No build step, no dependencies. Plain HTML + CSS + a little JS. Works on any static host.

## Structure

```
index.html                  Landing page (app promo, features, affirmations, newsletter)
css/style.css               All styling (colors defined as CSS variables at the top)
blog/index.html             Blog listing page
blog/*.html                 Individual posts
blog/_post-template.html    Copy this to create a new post
```

## How to add a new blog post

1. Copy `blog/_post-template.html` → `blog/my-new-post.html` (use a short, hyphenated, keyword-rich filename — it becomes the URL).
2. Open it and follow the numbered `<!-- CHANGE -->` comments: title, description, category tag, and body.
3. Add a card for it on **both** `blog/index.html` and the "From the Health Camper blog" section of `index.html` — copy an existing `<a class="post-card">...</a>` block and edit the link, tag, title, and teaser. Banner styles available: `banner-mind` (green 🌲), `banner-motivation` (yellow 🔥), `banner-affirm` (blue ☀️).

## How to preview locally

```powershell
cd health-camper-website
python -m http.server 8330
```

Then open http://localhost:8330

## Hosting (already set up — July 2026)

Live at **https://healthcamper.com** via GitHub Pages:
- Repo: https://github.com/rujal-tuladhar/healthcamper (branch `main`, root folder)
- Custom domain via `CNAME` file (healthcamper.com) — don't delete that file
- Namecheap DNS: 4 A records `@` → 185.199.108/109/110/111.153, CNAME `www` → rujal-tuladhar.github.io

**To publish changes:** commit and push to `main` — the site redeploys automatically in 1–2 minutes:

```powershell
cd health-camper-website
git add -A
git commit -m "New blog post: ..."
git push
```

## Newsletter form

The signup form on `index.html` is currently a visual placeholder (it doesn't store emails). To collect real signups, the simplest option is [Formspree](https://formspree.io) (free tier): create a form there and set the `<form>` tag's `action` to your Formspree URL with `method="POST"`, removing the `onsubmit` attribute.

## Changing the look

All colors live at the top of `css/style.css` in the `:root` block (forest green, sage, cream, sun yellow). Change them there and the whole site updates.
