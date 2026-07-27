# Knotty — support & legal site

Static site hosted on GitHub Pages at **https://knottyapp.github.io** (org: `knottyapp`,
repo: `knottyapp.github.io`). Plain HTML + one stylesheet, no build step.

## Pages

| URL | File | Purpose |
| --- | --- | --- |
| `/` | `index.html` | Support/home — app overview, FAQ, legal links, contact email |
| `/privacy.html` | `privacy.html` | Privacy Policy (store-required URL) |
| `/terms.html` | `terms.html` | Terms & Conditions |
| `/impressum.html` | `impressum.html` | Impressum (§ 5 DDG legal disclosure) |

`style.css` is shared by every page (brand terracotta, light/dark, mobile-first).
`icon.png` is the app icon, used as favicon and header mark.
`.nojekyll` tells GitHub Pages to serve the files as-is (no Jekyll processing).

## Deploy (first time)

Create the `knottyapp` org and an empty **public** repo named exactly
`knottyapp.github.io` on GitHub, then from this folder:

```bash
git init -b main
git add -A
git commit -m "Knotty support & legal site"
git remote add origin https://github.com/knottyapp/knottyapp.github.io.git
git push -u origin main
```

In the repo: **Settings → Pages → Source = Deploy from a branch → main / (root)**.
Live within ~1 minute. Verify in an incognito window (no login required).

## Editing later

These pages are hand-written HTML. The source-of-truth prose also lives as Markdown
one level up (`../privacy_policy.md`, `../terms_conditions.md`, `../knotty-support.md`)
for review/versioning. When you change content:

1. Edit the Markdown source (keeps a readable diff), **and**
2. Mirror the change into the matching `.html` here,
3. `git commit` + `git push` — GitHub Pages redeploys automatically, same URL.

The privacy/terms **effective date** lines must be bumped whenever the substance changes.
