# Homey Homes & Co.

Boutique Chicago short-term rental management website.

## What this is

A simple static HTML/CSS site. No build process, no React, no framework dependencies.
Just files a browser reads. This makes it:

- ⚡ Fast (loads in under 1 second)
- 🔍 Excellent for SEO
- 💰 Free to host on Netlify forever
- ✏️ Easy to edit (just text in HTML files)

## File structure

```
homey-homes/
├── index.html          ← Homepage (built — preview this first)
├── about.html          ← About page (coming next)
├── services.html       ← Services page (coming next)
├── pricing.html        ← Pricing page (coming next)
├── case-studies.html   ← Properties / case studies (coming next)
├── resources.html      ← Blog + checklist (coming next)
├── contact.html        ← Contact form (coming next)
├── privacy.html        ← Privacy policy placeholder (coming next)
├── terms.html          ← Terms placeholder (coming next)
├── css/
│   └── style.css       ← All styling (one file, one source of truth)
├── images/             ← All photos
└── netlify.toml        ← Deployment config
```

## How to preview locally

1. Open the project folder in VS Code
2. Right-click on `index.html` → "Open with Live Server" (install the Live Server extension if needed)
3. OR just double-click `index.html` to open in your browser

## How to edit

All page content is in HTML files. To change a headline:
1. Open the relevant `.html` file in VS Code
2. Find the text you want to change
3. Edit it
4. Save (Cmd+S)
5. Refresh your browser

To change colors, fonts, or styling site-wide, edit `css/style.css` and look at
the `:root { ... }` block at the top — those are the brand variables.

## How to deploy to Netlify

### Option A: Drag and drop (simplest)
1. Go to your Netlify dashboard → "Add new site" → "Deploy manually"
2. Drag the entire `homey-homes` folder onto the page
3. Live in 30 seconds

### Option B: GitHub + auto-deploy (recommended for ongoing edits)
1. Push this folder to a new GitHub repo
2. In Netlify: "Add new site" → "Import from Git"
3. Pick the repo, click deploy
4. Future edits: push to GitHub, Netlify auto-deploys

## Brand details

- **Name:** Homey Homes & Co.
- **Tagline:** Boutique Chicago short-term rental management
- **Colors:**
  - Cream (#FAF7F2) — background
  - Forest green (#2D3D2C) — primary accent
  - Terracotta (#B8654A) — secondary accent
  - Charcoal (#1F1F1D) — text
- **Fonts:**
  - Fraunces (display serif) — for headlines
  - DM Sans (body) — for everything else
- **Contact:** deold03@gmail.com · 732-713-7337 · @homeyhomes.co
