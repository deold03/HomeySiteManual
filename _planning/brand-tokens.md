# Homey Homes & Co. — Brand Tokens

Single source of truth for colors, fonts, spacing, and component styles. Pulled from the existing `css/style.css`. Any new page or component built for this site must use these tokens.

If something here changes, update `css/style.css` first, then update this file.

## Colors

| Token | Hex | Use |
|---|---|---|
| `--cream` | `#FAF7F2` | Primary page background |
| `--cream-dark` | `#F0E9DD` | Alt section background (warm) |
| `--forest` | `#2D3D2C` | Primary brand color. Buttons, italic headline accents, dark sections |
| `--forest-dark` | `#1F2B1E` | Button hover, deeper dark variants |
| `--terracotta` | `#B8654A` | Accent color. Eyebrows, link hover, hairline accents, italic accent on dark sections (use #D4B89F for that specifically) |
| `--charcoal` | `#1F1F1D` | Primary body text |
| `--warm-gray` | `#6B6862` | Secondary text, leads, supporting copy |
| `--light-gray` | `#D9D4CB` | Borders, hairlines |
| `--white` | `#FFFFFF` | Card backgrounds (used sparingly, on cream backgrounds) |

**Dark section warm accent:** `#D4B89F` (a tan/sand) — used for italic headline emphasis on forest-green backgrounds. Not in the variable list but used in homepage CSS for `.comparison-section h2 em` and `.lead-magnet h2 em`.

## Typography

- **Display font:** Fraunces (serif). Weights used: 300, 400, 500. Italic 300 and 400.
- **Body font:** DM Sans (sans-serif). Weights used: 400, 500.

**Google Fonts URL pattern:**
```
https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,400;0,9..144,500;1,9..144,300;1,9..144,400&family=DM+Sans:wght@400;500&display=swap
```

**Heading scale:**
- `h1`: `clamp(2.75rem, 6vw, 5rem)` — weight 300
- `h2`: `clamp(2rem, 4vw, 3.25rem)` — weight 400
- `h3`: `clamp(1.5rem, 2.5vw, 2rem)` — weight 400
- `h4`: `1.25rem` — weight 500

**Italic emphasis pattern:** Headlines use `<em>` for the emphasized phrase. The `<em>` rendered italic, weight 300, in `--forest` color. On dark sections, `<em>` is colored `#D4B89F` instead.

**Eyebrow text:** `.eyebrow` class. 0.75rem, weight 500, letter-spacing 0.18em, uppercase, color terracotta.

**Body copy:** 1.0625rem, line-height 1.6. Secondary copy (`.lede` and `.subhead`) uses `--warm-gray` color at 1.125rem or 1.1875rem.

## Spacing scale

CSS variables for vertical and horizontal rhythm:

| Token | Value |
|---|---|
| `--space-xs` | 0.5rem |
| `--space-sm` | 1rem |
| `--space-md` | 2rem |
| `--space-lg` | 4rem |
| `--space-xl` | 6rem |
| `--space-2xl` | 9rem |

Standard section padding: `padding: var(--space-2xl) 0;` (mobile reduces to `--space-xl`).

## Container widths

- `--max-width`: 1280px (main container)
- `--content-width`: 1080px (narrow container for centered text content)

## Buttons

Pill-shaped, `border-radius: 999px`. Padding `0.875rem 1.75rem`. Font-size 0.9375rem, weight 500.

**`.btn-primary`:** Forest background, cream text. Hovers to forest-dark and lifts 1px (`transform: translateY(-1px)`).

**`.btn-secondary`:** Transparent background, charcoal border + text. Hovers to charcoal background, cream text.

**`.btn-arrow`:** Optional inner span. Adds `→` after button text that translates right 3px on hover.

**On dark sections:** Primary buttons should use terracotta background with cream text (override: `background-color: var(--terracotta)`).

## Section conventions

- Default section background: `--cream`
- Alt section background: `--cream-dark` (for warm tonal contrast)
- Dark section background: `--forest` (matches homepage comparison table and lead magnet treatment)
- All sections use `padding: var(--space-2xl) 0` (mobile `--space-xl`)

## Component patterns

- **Section header:** `.eyebrow` + `h2` (with italic `<em>` accent) + optional `.lede` paragraph below
- **Numbered pillars:** Italic Fraunces 300, terracotta color, displayed as a label above each pillar's `h3`
- **Hairline accents:** 1px lines in terracotta or light-gray, used as rule decoration above paragraphs or below feature lists

## File structure

- `css/style.css` — main site stylesheet, source of truth
- Per-page additions live in inline `<style>` blocks in that page's HTML, only for styles that don't exist in the main stylesheet (e.g., the sticky sub-nav, pricing pill, and FAQ accordion on `services.html`)

## Voice + content rules (cross-reference)

See `CLAUDE.md` in the project root for voice rules ("I" not "we," vendor referral language, license advisory framing, no time-bound promises, etc.). Brand tokens are visual only; voice rules govern copy.
