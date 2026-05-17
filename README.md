# YallaFit Legal Site

This repo hosts the public Privacy Policy and Terms of Service for the YallaFit mobile app.

It's a tiny Jekyll site served by GitHub Pages.

## Live URLs (after you enable Pages)

- `https://<your-username>.github.io/<repo-name>/` — landing page
- `https://<your-username>.github.io/<repo-name>/privacy/` — Privacy Policy
- `https://<your-username>.github.io/<repo-name>/terms/` — Terms of Service

Use the `/privacy/` and `/terms/` URLs in your App Store Connect and Google Play Console listings.

## How to deploy (one-time setup, ~3 minutes)

1. **Create a new GitHub repo** at https://github.com/new
   - Name it something like `yallafit-legal` (lowercase, no spaces)
   - Public (Pages requires it on free accounts)
   - Don't initialize with anything — leave it empty

2. **Push this folder to the repo**. From this folder in a terminal:
   ```bash
   git init
   git add .
   git commit -m "Initial publish: privacy + terms"
   git branch -M main
   git remote add origin https://github.com/<your-username>/yallafit-legal.git
   git push -u origin main
   ```
   (Or use GitHub Desktop / drag-and-drop in the web UI — any path works.)

3. **Enable GitHub Pages**:
   - Go to your repo on github.com
   - Settings → Pages (left sidebar)
   - Under "Build and deployment":
     - Source: **Deploy from a branch**
     - Branch: **main**, folder: **/ (root)**
   - Save
   - Wait ~30–60 seconds for the first build. The page will show your live URL when ready.

4. **Verify it works** — open the three URLs above in a browser. You should see the landing page, the privacy policy, and the terms of service.

5. **Plug the URLs into your stores**:
   - Google Play Console → App content → Privacy policy → paste `/privacy/` URL
   - App Store Connect → App Information → Privacy Policy URL → paste `/privacy/` URL
   - Both stores let you add a Terms of Service URL too — use the `/terms/` URL

## Updating the policies later

When you update the in-app legal files (`legal/privacy.md` and `legal/terms.md` inside the main YallaFit repo), copy the new content over the `privacy.md` / `terms.md` files in this repo (keeping the front-matter block at the top), commit, and push. GitHub Pages rebuilds within a minute.

## Notes

- The `_config.yml` uses the `jekyll-theme-cayman` theme. If you want a different look, browse https://pages.github.com/themes/ and swap the `theme:` line — that's it.
- These are exact copies of what users see inside the app, so the two stay in sync as long as you update both when the policy changes.
