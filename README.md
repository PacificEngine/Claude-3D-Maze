# 3D Maze

A browser-based, randomly generated first-person maze game. No build step, no
dependencies — a single self-contained `index.html` file.

## Play locally

Just open `index.html` in a browser, or serve the folder with any static
file server, e.g.:

```
python3 -m http.server
```

then visit `http://localhost:8000`.

## Deploy to GitHub Pages

This repo is already set up for it:

1. Push this folder to a new GitHub repository (the default branch must be
   named `main`, since that's what the workflow below watches).
2. In the repo, go to **Settings → Pages**, and under **Build and
   deployment → Source**, choose **GitHub Actions**.
3. Push to `main` (or re-run manually from the **Actions** tab). The
   included workflow at `.github/workflows/deploy.yml` will build and
   publish the site automatically.
4. Your game will be live at `https://<your-username>.github.io/<repo-name>/`.

If you'd rather not use GitHub Actions, you can instead set **Source** to
**Deploy from a branch** and pick `main` / `(root)` — GitHub will serve
`index.html` directly with no workflow needed. The `.nojekyll` file in this
repo just tells GitHub Pages to skip Jekyll processing, which isn't needed
here and could otherwise interfere with files that happen to start with an
underscore in the future.

## Controls

- `W` / `↑` — move forward, `S` / `↓` — move back
- `A` / `←` — turn left, `D` / `→` — turn right
- `M` — toggle minimap
- `R` — generate a new maze
