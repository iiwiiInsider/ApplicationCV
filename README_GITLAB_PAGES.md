# Host on GitLab Pages

This repo is set up to deploy a static site via GitLab Pages.

## What gets published
- `Kyle_Blackburn_CV_clean.html` is deployed as `public/index.html`
- All `*.pdf`, `*.png`, and `*.jpeg` files in the repo root are copied into `public/` for the Qualifications viewer and images.

## Steps (one-time)
1. Create a new project on GitLab (blank project is fine).
2. Add the GitLab remote locally:
   - `git remote add gitlab <your-gitlab-repo-url>`
3. Push your default branch:
   - `git push -u gitlab main`
   - If your default branch is `master`, use `master` instead.

## Enable Pages
- In GitLab: **Settings → Pages** (or **Deploy → Pages**) and confirm it’s enabled.
- After the pipeline completes, GitLab will show the Pages URL.

## Notes
- If you rename or move files, keep references in the HTML consistent.
- Some mobile browsers restrict opening `file://` HTML locally; GitLab Pages avoids that by serving over HTTPS.
