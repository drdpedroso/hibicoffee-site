# Hibi — website

The marketing site for **Hibi**, a calm companion for your daily coffee ritual.
Static HTML/CSS/JS — no build step, no dependencies. Trilingual (EN / PT / ES) with
automatic language detection from the browser.

```
.
├── index.html          # landing page (trilingual, language selector)
├── privacy.html        # privacy policy (trilingual)
├── support.html        # support / FAQ (trilingual)
├── styles.css          # shared styles for privacy & support
├── hibi-og.png         # social share image (1200×630)
├── favicon.png         # 256×256 favicon
├── apple-touch-icon.png# 180×180 home-screen icon
└── .nojekyll           # tells GitHub Pages to skip Jekyll processing
```

## Deploy to GitHub Pages

1. Create a new repository on GitHub (e.g. `hibi`).
2. Put these files in the repository root and push:
   ```bash
   git init
   git add .
   git commit -m "Hibi website"
   git branch -M main
   git remote add origin https://github.com/USERNAME/REPO.git
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages**. Under **Build and deployment**, set
   **Source = Deploy from a branch**, **Branch = `main`**, **Folder = `/ (root)`**, Save.
4. Wait ~1 minute. Your site goes live at:
   - Project site: `https://USERNAME.github.io/REPO/`
   - Or a user/org site if the repo is named `USERNAME.github.io`: `https://USERNAME.github.io/`

## One thing to edit before sharing: the OG image URL

Social previews (WhatsApp, X, LinkedIn, iMessage) need an **absolute** image URL.
In `index.html`, find the three `BASE_URL` placeholders in the `<head>` and replace
them with your live address, for example:

```html
<meta property="og:image"  content="https://USERNAME.github.io/REPO/hibi-og.png">
<meta property="og:url"    content="https://USERNAME.github.io/REPO/">
<meta name="twitter:image" content="https://USERNAME.github.io/REPO/hibi-og.png">
```

After deploying, test the preview with the
[Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/) and the
[X Card Validator](https://cards-dev.twitter.com/validator).

## Other placeholders to replace

- **Email:** `hello@hibicoffee.app` appears in `privacy.html` and `support.html`
  (and the footer Contact link in `index.html`). Swap in your real address.
- **Privacy policy:** set the effective date and the owning entity
  (`[Your name / company]`) in `privacy.html`.
- **Google Play button:** currently "Coming soon". Replace with the official Google
  Play badge and your Google Play link at launch.

## Custom domain (optional)

If you own a domain, add a file named `CNAME` (no extension) containing just the
domain, e.g. `hibicoffee.app`, then point a DNS `CNAME`/`A` record at GitHub Pages as
described in GitHub's docs. Remember to update the `BASE_URL` meta tags to the custom
domain.

## Local preview

Just open `index.html` in a browser, or run a tiny server:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Notes

- Language is detected from `navigator.language` on load (PT or ES, else EN) and can
  be switched with the EN/PT/ES control. The choice is **not** persisted across visits
  (kept dependency-free); add `localStorage` if you want it remembered.
- All assets are local and relative, so the site works from any subpath.
