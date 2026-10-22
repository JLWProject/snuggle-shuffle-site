# SnuggleShuffle website (GitHub Pages)

The public pages App Store Connect needs: a **Privacy Policy URL** and a **Support URL**. This folder is the source; copy its contents to the **root** of the public site repo.

| File | Purpose |
|---|---|
| `index.html` | Home page (also usable as the Marketing URL) |
| `privacy.html` | Privacy Policy, for App Store Connect › App Privacy › Privacy Policy URL |
| `support.html` | Support, for App Store Connect › version › Support URL |
| `style.css`, `icon.png` | Shared styling and icon. No external fonts, scripts or trackers |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are (no Jekyll build) |

## Publish
1. Copy everything in this folder, **including `.nojekyll`**, into the root of the public repo, then commit and push.
2. In that repo, go to **Settings › Pages › Build and deployment**, choose **Deploy from a branch**, set it to `main` and `/ (root)`, and save.
3. After a minute or two the site is live at `https://<github-user>.github.io/<repo>/`:
   - Privacy: `https://<github-user>.github.io/<repo>/privacy.html`
   - Support: `https://<github-user>.github.io/<repo>/support.html`
4. Optional custom domain, e.g. `snuggleshuffle.jlwproject.co.uk`:
   - Add a DNS **CNAME** record: `snuggleshuffle` pointing to `<github-user>.github.io`.
   - In **Settings › Pages › Custom domain**, enter the domain, save it, then tick **Enforce HTTPS** once it's offered. GitHub adds a `CNAME` file to the repo.
5. Open both URLs in a private browser window to check they load without a login. Then paste them into App Store Connect, and send them to me so I can add them to the app's About section.

## Before publishing
- [ ] The email `snuggleshuffle@jlwproject.co.uk` exists and receives mail (it's on every page).
- [ ] The effective date in `privacy.html` is still right.

## Keep in step with the app
Update `privacy.html` (and its effective date) **before** shipping anything that changes what happens to data: iCloud sync, analytics, accounts, or any network call. The App Store "App Privacy" answers must match it ("Data Not Collected" today).
