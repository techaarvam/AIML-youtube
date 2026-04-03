# GitHub Pages Setup

## What is in this repo now

- `index.html`: landing page that lists the available HTML demos and renders the selected one in an iframe
- `pages.json`: the list of HTML files shown in the sidebar

## Current pages

- `area_preserving_transformation.html`
- `eigen_derivation_visual.html`
- `eigenvalues_real_vs_complex_dashboard.html`

## How to add another HTML page

1. Add the new `.html` file to the repo.
2. Add one entry to `pages.json`.

Example:

```json
{
  "title": "My New Demo",
  "path": "my_new_demo.html"
}
```

## How to enable GitHub Pages

1. Push the repo to GitHub.
2. Open the repository on GitHub.
3. Go to `Settings`.
4. Open `Pages`.
5. Under `Build and deployment`, choose `Deploy from a branch`.
6. Select the branch, usually `main`.
7. Select the folder `/ (root)`.
8. Save.

GitHub will publish the site at:

- `https://YOUR-USERNAME.github.io/AIML-youtube/`

## Local preview

Run this in the repo root:

```bash
python3 -m http.server 8000
```

Then open:

- `http://localhost:8000/`

## Important note

GitHub Pages does not expose a directory listing, so the landing page cannot auto-discover every `.html` file by itself. `pages.json` is the explicit list of publishable pages.
