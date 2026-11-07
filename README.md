# VOTE SA installable web app

This is a static Progressive Web App (PWA) prototype. It includes a fingerprint-style logo, install prompt, manifest and service worker for caching the shell offline.

## Publish with GitHub Pages
1. Upload the contents of this folder into the root of `khotsomurphy/VOTE-SA` on the `main` branch (keep `.github/workflows/pages.yml`).
2. In the repository, open **Settings → Pages** and choose **GitHub Actions** as the build and deployment source.
3. Ensure the workflow has permission to deploy Pages, then check the **Actions** tab for a successful deployment.
4. The public address will normally be `https://khotsomurphy.github.io/VOTE-SA/` after deployment succeeds. Do not share it as live until it opens successfully over HTTPS.
5. On Android Chrome, open the published HTTPS address and use **Install app** / **Add to Home screen**. On iPhone Safari, use **Share → Add to Home Screen**.

## Important limitations
This is a demonstration, not an official IEC service. The party list is illustrative and incomplete. Poll responses are stored only in the current device's browser; there is no central database, live national tally, voter identity verification, official ballot or biometric authentication. The fingerprint is a logo only. Do not present prototype results as election results.
