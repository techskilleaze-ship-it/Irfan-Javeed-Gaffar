# Irfan Javeed Gaffar — Portfolio

Personal portfolio site for Irfan Javeed Gaffar, Business Development Director based in Dubai.

A static site with plain HTML, CSS and a small vanilla-JS file. There's no build step and no dependencies.

## Structure

```
index.html                     page markup
assets/css/styles.css          all styles (responsive, reduced-motion aware)
assets/js/main.js              mobile menu, market route map, experience accordion
assets/img/irfan-gaffar-portrait.jpg
assets/img/favicon.svg
assets/docs/Irfan-Javeed-Gaffar-CV.pdf   linked from every "Download CV" button
.nojekyll                      tells GitHub Pages to serve files as-is
```

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Publish on GitHub Pages

```bash
git init
git add .
git commit -m "Portfolio site"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

Then in the repository, go to **Settings → Pages**. Under "Build and deployment" choose **Deploy from a branch**, then **main** and **/ (root)**, and save. After a minute the site is live at `https://<your-username>.github.io/<repo-name>/`.

## Before going live

Search `index.html` for `[` to find the placeholders:

- **LinkedIn**: replace `[Add LinkedIn profile URL]` in the contact section with a link.
- **Selected outcomes**: replace the three `[Market · Year]` cards with real results, or delete the `<section id="outcomes">` block.
- **Phone**: `0554 7787736` is copied from the CV. It has one digit more than a standard UAE mobile number, so check it, and update both the visible text and the `tel:` link.

## Customising

- **Accent colour**: change `--accent` (and `--accentLight` for dark sections) on the first `<div>` inside `<body>`. In `assets/js/main.js`, also update `ACCENT_LIGHT`.
- **CV**: replace `assets/docs/Irfan-Javeed-Gaffar-CV.pdf` with a new file of the same name.
- **Photo**: replace `assets/img/irfan-gaffar-portrait.jpg`. A portrait at least 1200 px wide looks sharper on high-resolution screens.
