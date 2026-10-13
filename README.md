# Brainery Solutions — landing page

A single-page static website. All files sit in one folder, with no sub-folders, so every file uploads
correctly through GitHub's web uploader.

```
index.html             the whole page (HTML, CSS and vanilla JavaScript)
brainery-logo.png      the company logo (header and footer)
icon.png               browser tab icon
apple-touch-icon.png   iPhone / iPad home-screen icon
og-image.png           link-preview image (WhatsApp, LinkedIn, Slack)
.nojekyll              tells GitHub Pages to serve files as they are
vercel.json            settings if you also deploy on Vercel
.gitignore             keeps node_modules, .env files, keys and OS files out of Git
```

All image paths are relative (for example `src="brainery-logo.png"`), so the site works at
`https://USERNAME.github.io/REPOSITORY/`, on Vercel, or opened straight from your computer.
Fonts load from Google Fonts.

## GitHub Pages

Repository → Settings → Pages → Source: **Deploy from a branch**, Branch: **main**, Folder: **/ (root)**.

The link-preview image uses the full address
`https://dianaabosaleh.github.io/forex-presentation-10/og-image.png`. If the site moves to another
address, update the `og:image` line in `index.html` to match.

## Preview locally

Open `index.html` in a browser, or run `python3 -m http.server 8000` in this folder and open
http://localhost:8000.
