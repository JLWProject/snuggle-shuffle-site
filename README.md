# SnuggleShuffle website (GitHub Pages)

The public pages App Store Connect needs: a **Privacy Policy URL** and a **Support URL**. This folder is the source; copy its contents to the **root** of the public site repo.

| File | Purpose |
|---|---|
| `index.html` | Home page (also usable as the Marketing URL) |
| `privacy.html` | Privacy Policy, for App Store Connect › App Privacy › Privacy Policy URL |
| `support.html` | Support, for App Store Connect › version › Support URL |
| `style.css`, `icon.png` | Shared styling and icon. No external fonts, scripts or trackers |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are (no Jekyll build) |
| `images/shot-0*.jpg` | Home page screenshot gallery: 480 px web copies of `appcontent/screenshots/*.png` (see below) |

## Refreshing the screenshots
After `make appstore-screenshots`, recreate the web copies from the repo root:

```sh
i=1; for f in "01 Spin for your next date" "02 Let the wheel decide" "03 All your ideas, organised" "04 Make it yours" "05 Your photo, behind the wheel" "06 One-time Plus"; do
  sips -s format jpeg -s formatOptions 78 --resampleWidth 480 "appcontent/screenshots/$f.png" --out "site/images/shot-0$i.jpg"; i=$((i+1)); done
```

