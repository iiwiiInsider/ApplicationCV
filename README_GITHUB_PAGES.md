# Host on GitHub (Public Repo + GitHub Pages)

This repo is set up to deploy a static site via **GitHub Pages** using GitHub Actions.

## What gets published
- `Kyle_Blackburn_CV_clean.html` is deployed as `index.html`
- All `*.pdf`, `*.png`, and `*.jpeg` files in the repo root are copied to the published site so the Qualifications viewer and images work.

## Steps
1. Create a new GitHub repository and set it to **Public**.
2. Add the GitHub remote locally:
   - `git remote add origin <your-github-repo-url>`
3. Push:
   - `git push -u origin main`

## Enable Pages
1. In GitHub: **Settings → Pages**
2. Under **Build and deployment**, choose:
   - **Source**: GitHub Actions
3. Wait for the Actions workflow **Deploy to GitHub Pages** to finish.
4. Your site URL will appear in **Settings → Pages** and in the workflow summary.

## Notes
- If your default branch is `master`, update `.github/workflows/pages.yml` to use `master` or rename your branch to `main`.
- Some mobile browsers restrict opening `file://` HTML locally; Pages avoids this by serving over HTTPS.
