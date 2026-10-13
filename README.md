# Brainery Solutions — landing page

A single-page static website: one `index.html` (HTML, CSS and vanilla JavaScript) plus image assets.
There is no framework, no build step and no dependencies to install.

```
index.html        the whole page
assets/           logo, favicon, Apple touch icon, social preview image
vercel.json       Vercel settings (clean URLs, caching, security headers)
.gitignore        keeps node_modules, .env files, keys and OS files out of Git
```

Fonts (Montserrat, Instrument Sans) load from Google Fonts. Everything else is served from this folder.

## Preview locally

Open `index.html` directly in a browser, or serve the folder:

```bash
python3 -m http.server 8000     # then open http://localhost:8000
# or
npx serve .
```

## Deploy on Vercel

Import the GitHub repository in Vercel with these settings:

- Framework Preset: **Other**
- Build Command: *(leave empty)*
- Output Directory: *(leave empty, the project root)*
- Install Command: *(leave empty)*

No environment variables are needed.

## After the first deployment

The social preview image (`og:image`) uses a relative path. Some link-preview services (WhatsApp, LinkedIn)
need a full URL, so once you know your live address, change this line in `index.html`:

```html
<meta property="og:image" content="/assets/og-image.png">
```

to, for example:

```html
<meta property="og:image" content="https://your-project.vercel.app/assets/og-image.png">
```
