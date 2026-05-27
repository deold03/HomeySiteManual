# Homey Homes & Co. — Project Brief for Claude Code

This file is your standing context for this project. Read it at the start of every session.

## What this project is

A website for **Homey Homes & Co.**, a boutique Chicago short-term rental management business. The site lives in this folder as a static site (HTML/CSS/JS, deployed via Netlify per `netlify.toml`).

The current homepage is live at `https://homeysitemanual.netlify.app`. Other pages (`/services`, `/about`, `/contact`, etc.) are linked in navigation but currently return 404 — they need to be built.

We're in the middle of a redesign and buildout. The source of truth for what to build is `homey_homes_v3.xlsx` (place this in `_planning/` if not already there). Read it first when you start.

## Who Danny is (the founder, single operator)

- 11+ years hosting on Airbnb (started Brooklyn 2013, now Chicago)
- 4 years at Goldman Sachs in real estate investing
- 8 years in corporate strategy
- Licensed Chicago realtor
- Flagship property: his own 1906 Logan Square graystone, 4.99★, 160+ reviews, top 1% of Airbnb homes
- Also does short-term rental management for client properties across Airbnb, VRBO, Booking.com

Homey Homes is a solo operation. He does this personally — no team, no dispatchers.

## Voice and writing rules (apply site-wide)

1. **"I" not "we."** The site used to use "we" — change every instance to "I" / "my" / "me." Danny is one person and the site should reflect that.

2. **"Large property management companies"** — never "national property managers" or "national managers" in body copy. In the comparison table column header, use **"Large Managers"** (shorter, fits the column).

3. **Vendor coordination language.** Danny does NOT manage maintenance or repair vendors on the owner's behalf. He provides **trusted referrals** and **coordinates the introduction**. The owner schedules and pays vendors directly. Phrasing to use: "trusted vendor referrals," "I'll refer you to vendors I've worked with and trust, and coordinate the introduction." Never say "vendor coordination," "vendor management," or anything implying he books appointments.

4. **STR licensing.** Danny does NOT file Chicago STR license applications on behalf of owners. He advises. Phrasing: "I'll walk you through the requirements, advise on the application, and tell you exactly what to submit. You file the application yourself, but you won't be doing it blind."

5. **No time-bound promises.** Remove "within 2 business days" / "within 48 hours" / similar language wherever it appears. Danny will respond personally, but not on a guaranteed clock.

6. **Headline italic emphasis.** The site uses italic phrases for emphasis in display headlines, e.g. "hosted *like it's my own home*." Preserve this pattern when writing or editing headlines.

7. **Sage green + cream palette.** Existing aesthetic. Don't introduce new colors without asking.

8. **Fonts.** Fraunces (serif, for display) + Inter (sans, for body). These are loaded from Google Fonts in the existing site.

## Site taxonomy (v3)

Pages that exist or need to be built:

- **Home** (`/`) — LIVE, being redesigned. Finalized copy in v3 spreadsheet > "Home (FINAL COPY)" tab.
- **Services** (`/services`) — to be built. Copy in v3 > "Services (FINAL COPY)" tab.
- **Properties** (`/properties`) — to be built. Chicago managed portfolio only. Tiles link directly to Airbnb listings (no internal property detail pages for v1).
- **About** (`/about`) — to be built. Danny's full story.
- **FAQ** (`/faq`) — to be built. Copy in v3 > "FAQ Page (FINAL COPY)" tab.
- **Resources** (`/resources`) — to be built. Lead magnet + future blog posts + Amazon/Wayfair storefront links.
- **Contact** (`/contact`) — to be built. Lead form + direct text + Calendly. Form fields: Name, Email, Phone (optional), Property address/neighborhood, Property type, How can I help, Honeypot. No "currently renting" question, no time-bound promises.
- **Privacy** and **Terms** — standard legal templates, footer-only.

**Pages REMOVED from earlier plans:** Case Studies, Pricing. Pricing detail folds into Services > STR Management.

**Recommended nav order:** Services | Properties | About | FAQ | Resources | Get in Touch (button)

## Key structural changes to the homepage (vs. current live version)

1. **"Meet your host" moves up** — currently sits near the bottom, should land right after the "Why owners choose us" section. Order: Hero → Why owners choose us → Meet your host → Comparison table → Four ways I help → Properties teaser → Lead magnet → Final CTA.

2. **Comparison table condensed** from 7 rows to 4: Management fee | What's included | Guest communications | Who answers when you call.

3. **"Four ways we help" condensed visually** — was stacked vertical cards with long blurbs, should be a 2x2 grid with one-sentence blurbs.

4. **Properties teaser condensed** from 6 tiles to 3 (flagship + 2 standouts). Full grid moves to dedicated `/properties` page.

5. **Testimonials section HIDDEN** until real testimonials are collected. Do not ship "Testimonial coming soon" placeholders.

6. **Mobile padding reduced** — current site has too much top padding above the eyebrow line and too much section padding throughout. Use scaled padding: `py-12 md:py-20 lg:py-24` (or equivalent) instead of uniform.

## Photo assets

Photos provided by Danny are in the `photos/` or `images/` folder (or to be added). The v3 spreadsheet's "Photo Asset Map" tab maps every photo to its destination page/section with alt text. Highlights:

- **Homepage Meet Your Host headshot:** IMG_2561.jpeg (warm, navy polo, seated). Most approachable of the three.
- **About page hero headshot:** Image_3.jpg (gray suit, bay window). Most polished.
- **Press / Resources author bio headshot:** IMG_3187.jpeg (editorial, black on black).
- **Logan Square graystone flagship:** IMG_2479.jpeg is the hero shot (dining room with Corinthian columns).
- **Miami kitchen (IMG_1848.jpeg):** Lives ONLY on the Services > Interior Design section. Do NOT put it on the Properties page — Properties is Chicago managed inventory only. The Miami kitchen is a design portfolio piece, not a managed property.

## How to work with Danny

- He's a realtor and operator, not a developer. Explain technical changes in plain language.
- He sweats the details. Spacing, padding, hierarchy, mobile responsiveness — these matter to him.
- Always preview changes visually before considering them done. Run a local dev server if possible.
- He has the v3 spreadsheet open in another window for reference. When in doubt about copy, pull from there verbatim.
- When the finalized copy in the spreadsheet conflicts with anything in the current site files, the spreadsheet wins.

## Where things live in this folder

- `index.html` — current homepage
- `contact.html` — existing contact stub
- `css/` — stylesheets
- `js/` — scripts
- `images/` — site imagery
- `netlify.toml` — deploy config
- `README.md` — project readme (likely outdated; this CLAUDE.md supersedes it for AI context)
- `_planning/homey_homes_v3.xlsx` — site plan + finalized copy + photo asset map (single source of truth)

## Order of work (current priority)

1. Update the homepage to match v3 finalized copy and structural changes.
2. Build the Services page from v3 finalized copy.
3. Then: FAQ page (copy is ready in v3).
4. Then: Properties, About, Contact, Resources (in any order — Danny will provide property neighborhood data + Airbnb links for Properties).

## Things NOT to do

- Don't write code that calls MCP server URLs from artifacts or embeds API keys.
- Don't introduce new pages, sections, or features not in the v3 spreadsheet without asking Danny first.
- Don't change the color palette, fonts, or core visual identity without checking.
- Don't add testimonial placeholders.
- Don't promise specific response times in copy.
- Don't say "national managers." Don't say "we." Don't say "vendor coordination." Don't say "license registration" (it's "license advice and application guidance").

## Other things to note
- When we make a project-level decision in a session (a new rule, a changed direction, a structural decision that affects future work), proactively suggest an update to this CLAUDE.md before the session ends. Don't write it without asking — show me the proposed change.
- Visual design work (HTML, CSS, page layout, typography choices) is being done in a separate Claude.ai conversation. When I bring new files into the project, your job is to integrate them — place files correctly, update cross-page navigation, check for conflicts with existing CSS, run the dev server. Don't redesign or restyle what I bring in unless I ask you to.
- _planning/brand-tokens.md — visual brand tokens (colors, fonts, spacing) pulled from css/styles.css. Source of truth for any new page or component.
- The main stylesheet is css/style.css (no trailing s). This is the correct filename. Any new HTML page must link to css/style.css.