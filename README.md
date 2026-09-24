# CPbOX

A lightweight static website for organizing Facebook Lite, Messenger, and APK download resources.

## Website pages

- `index.html` — main homepage
- `pages/apk.html` — APK library page
- `pages/facebook-lite.html` — Facebook Lite download links
- `pages/messenger.html` — official Messenger download link
- `Allapk.html` — app collection page
- `fb11lite.html` — Facebook Lite version collection
- `messenger3.html` — Messenger version collection
- `Messenger3.html` — compatibility copy of the Messenger collection page
- `fb11ite.html` — redirect to `fb11lite.html`

## Assets

- `assets/css/style.css` — styles for the main website pages
- `assets/js/script.js` — footer year updater
- `style.css` — styles for the app collection pages
- `script.js` — theme, menu, language, and download interactions
- `assets/manifest.webmanifest` — web app manifest

## Download source policy

- Prefer official Google Play Store links whenever available.
- APK links should point to trusted and verified repository release assets.
- Verify APK integrity and review requested permissions before installation.
- This website provides information and links only; users are responsible for downloads and installations.

## Local preview

Run the following command from the repository root:

```bash
python3 -m http.server 8000
```

Then open:

- http://localhost:8000/

## Deployment

The site is configured for GitHub Pages at:

https://mhitlimited.github.io/11lite/

The sitemap and robots file are available at the repository root for search engine discovery.
