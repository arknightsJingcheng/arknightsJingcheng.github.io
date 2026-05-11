# Personal Academic Website

Static site for Jingcheng's academic homepage. Plain HTML + CSS — no build step.

## Files

```
website/
├── index.html      Main page (edit content here)
├── style.css       Styling
├── photo.jpg       Profile photo (add your own; 400x400 px recommended)
├── paper.pdf       Job market paper (add when ready)
├── slides.pdf      Slide deck (add when ready)
├── cv.pdf          Full CV (add when ready)
└── README.md       This file
```

## Deploy to GitHub Pages

### Option A — `username.github.io` repo (recommended)

Hosts at `https://<username>.github.io/` (clean root URL).

```bash
# from inside the website/ folder
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/arknightsJingcheng/arknightsJingcheng.github.io.git
git push -u origin main
```

The site will be live at **https://arknightsjingcheng.github.io/** within a minute or two. (GitHub serves the URL lowercase regardless of the username casing.)

### Option B — Project repo with Pages enabled

Hosts at `https://<username>.github.io/<repo-name>/`.

1. Create a repo (any name).
2. Push these files to the `main` branch.
3. In GitHub → Settings → Pages → Source: `Deploy from a branch` → `main` → `/ (root)` → Save.

## Custom domain (optional)

Add a `CNAME` file containing just your domain (e.g. `jingcheng.com`), and point an `A` / `CNAME` DNS record at GitHub Pages per [their docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).

## Editing

- **Bio / sections** — edit text directly inside `index.html`.
- **Colors / fonts** — top of `style.css`. Accent color is `#8a1538` (a deep crimson; change in one place via find-replace).
- **Add a paper** — duplicate the `<article class="paper">` block in `index.html`.
- **Add a section** — copy a `<section>` block and add a matching `<a>` in the nav.

## Local preview

Open `index.html` directly in a browser, or run a tiny local server:

```bash
# Python 3
python -m http.server 8000
# then visit http://localhost:8000
```

## TODOs before publishing

- [ ] Add `cv.pdf` (currently linked but file missing)
- [ ] Optional: self-host paper PDFs locally instead of Dropbox links
- [ ] Optional: add Google Scholar / SSRN / ORCID links to Contact section
