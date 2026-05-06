# Neron Sifflore — Personal Site

Editorial-style academic site, plain HTML/CSS, no build step.

## Files

```
index.html        — Home
research.html     — Research papers
projects.html     — Tools & estimators
blog.html         — Blog posts
contact.html      — Contact info
styles.css        — Shared styling for all pages
photos/           — Featured SVG figures (homepage cards)
Figures/          — Inline figures within research papers
Papers/           — PDF drafts linked from research page
cv.pdf            — Your CV (link from nav)
```

## What you need to add yourself

Copy these from your existing repo into the new site folder before deploying:

- `photos/DPEP_RD_GRAPH2.svg` — homepage figure 1
- `photos/boy_intensity_graph_modified.svg` — homepage figure 2
- `Figures/Graph_test.svg` — Nigeria UPE paper figure
- `Figures/tourism_results_big.svg` — Tourism paper figure
- `Papers/draft-plant-locations.pdf` — Tourism working paper
- `cv.pdf` — Your CV

The HTML references these by exact filename, so just drop the existing files in.

## Things to update before going live

1. **Email address** in `contact.html` — currently a placeholder
2. **CV PDF** — confirm `cv.pdf` is in the root
3. **Affiliation line** in contact page — adjust if needed

## Deploying to GitHub Pages

If your site repo is `Nts4real/Nts4real.github.io`:

```bash
# In the existing Quarto repo, you'll want to either:
# (a) Replace contents entirely (back up the Quarto source first)
# (b) Create a new branch with this static version

git checkout -b plain-html
# Copy these files into the repo root, replacing Quarto-generated ones
git add .
git commit -m "Switch to plain HTML editorial design"
git push origin plain-html

# Then in GitHub repo settings → Pages → set source to plain-html branch
```

Or simpler: create a fresh repo for the new site, set it as your `username.github.io` source, and archive the Quarto one.

## Customisation tips

- All colours live as CSS variables at the top of `styles.css` (`--accent`, `--paper`, etc.) — change once, applies everywhere
- To add a new page, copy any existing `.html` file and update the masthead crest and nav `active` class
- The cream paper background and subtle noise come from inline SVG in `body` — no extra image needed
