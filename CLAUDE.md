# CLAUDE.md — EZ LED E-Poster Product Site

## What This Is
Single-page product/marketing site for the EZ LED E-Poster P2.5mm Outdoor LED display unit.
One self-contained HTML file — all styles inline, no build step, no JS framework.

## Stack
- Pure HTML + CSS (no JavaScript)
- Google Fonts (Inter)
- CSS animations (keyframes for glow effects)
- Responsive (mobile breakpoint 768px)

## Files
- `index.html` — the entire site
- `STYLE-GUIDE.md` — colors, typography, section breakdown, how to modify each part
- `CLAUDE.md` — this file

## How to Run
```bash
npx serve .          # or python3 -m http.server 8888
```

## How to Edit
- All content is in `index.html`
- CSS variables at top of `<style>` block control colors
- Each section is clearly commented
- See `STYLE-GUIDE.md` for detailed section map and modification guide

## Key Design Decisions
- Dark hero/specs sections, light features/applications — creates visual rhythm
- Poster mockup is pure CSS (no image needed)
- Stats bar breaks up hero from content
- Cards use hover animations for interactivity
- No JS = fast load, no dependencies to break

## Product Specs in the Site
These are based on standard P2.5mm outdoor LED poster specs. If the actual EZ LED datasheet has different values, update the spec-row values in the #specs section.
