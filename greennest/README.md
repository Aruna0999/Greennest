# GreenNest – Plant Care App 🌿

Complete responsive React + Vite demo with **login first**, registration, home, catalog, plant details, indoor/outdoor plants, saved plants, seven-day watering schedule, care guide and profile.

## Run locally

1. Extract ZIP and open the `greennest_complete` folder in VS Code.
2. Open Terminal and run:

```bash
npm install
npm run dev
```

3. Open the localhost URL printed by Vite. Create an account, then log in.

## Fix GitHub Pages 404

This project is configured for **https://aruna0999.github.io/greennest/**.

- `vite.config.js` uses `base: '/greennest/'` (must match the repository name exactly).
- `HashRouter` is used to prevent refresh 404s on `/login`, `/home`, etc.
- The published GitHub Pages branch must contain the **built `dist` output**, not the React source folder.

### Deploy using gh-pages

From the project folder (the one containing `package.json`):

```bash
npm install
npm run deploy
```

In GitHub repository Settings → Pages choose **Deploy from a branch**, branch **gh-pages**, folder **/(root)**, and Save. Allow a few minutes for publishing.

Site: https://aruna0999.github.io/greennest/ (login appears at `#/login`).

To update your source code on GitHub, commit and push the extracted project files to the repository separately. Avoid accidentally nesting the project folder if you intend to run commands from the repository root.

## Important security note

This is a **frontend learning demo**, not a secure production login system. Accounts and passwords are stored in localStorage as plain text. **Use dummy credentials only.** A real deployment needs backend authentication and password hashing.

Plant photos use remote Unsplash image URLs and require an internet connection; emoji fallbacks remain visible if an image fails to load.


## GitHub Pages deployment (important)
Run `npm install` and `npm run deploy` from this folder. In GitHub Settings > Pages, select Deploy from a branch, `gh-pages`, `/ (root)`. Do not upload `src` or the unbuilt `index.html` as the website: the source HTML references `/src/main.jsx` which is not available on GitHub Pages. The Vite build generates `dist/index.html` with bundled assets. `base` is `/greennest/` for repository `greennest`; change it if your repo has a different name.
