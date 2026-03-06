# EZ LED E-Poster — Site Style Guide & Content Map

## Colors
| Token | Hex | Usage |
|-------|-----|-------|
| Primary | `#0066FF` | Buttons, links, accents, stats |
| Accent | `#00D4FF` | Gradients, highlights, spec headers |
| Dark | `#0A0A0A` | Hero bg, footer, dark sections |
| Gray | `#6B7280` | Body text, descriptions |
| Light | `#F8FAFC` | Stats bar bg, card backgrounds |
| White | `#FFFFFF` | Page bg, card bg |

## Typography
- **Font:** Inter (Google Fonts) — weights 300–900
- **Hero title:** clamp(36px–64px), weight 900, letter-spacing -2px
- **Section titles:** clamp(28px–48px), weight 800, letter-spacing -1.5px
- **Body:** 14–18px, weight 400–500, line-height 1.7
- **Labels/tags:** 12–13px, uppercase, letter-spacing 1–2px, weight 600–700

## Layout
- Max content width: **1200px**, centered
- Section padding: **100px vertical**, 24px horizontal
- Grid gaps: 20–60px depending on section
- Border radius: 8–16px on cards

## Sections (top to bottom)

### 1. Navigation (fixed)
- Dark bg with blur backdrop
- Logo: "EZ" white + "LED" accent color
- Links: Features, Specifications, Applications, Get a Quote (CTA button)

### 2. Hero
- Dark gradient background with blue radial glow
- Badge: "Next-Gen Outdoor Display"
- H1: "E-Poster P2.5mm Outdoor LED Display"
- Subtitle describing the product
- Two buttons: primary (Request Quote) + outline (Download Spec Sheet)
- Right side: animated poster mockup visual

### 3. Stats Bar
- 4 columns: P2.5 (pitch), 5000+ (nits), IP65 (rating), 100K+ (lifespan)
- Light background, large bold numbers in primary blue

### 4. Features (6 cards, 3-col grid)
| Card | Icon | Title | Content |
|------|------|-------|---------|
| 1 | ☀️ | 5000+ Nits Brightness | Sunlight visibility, auto-brightness |
| 2 | 🌧️ | IP65 Weatherproof | Rain/snow/dust, -20°C to 60°C |
| 3 | 📡 | Remote Management | 4G/WiFi cloud CMS, remote updates |
| 4 | ⚡ | Ultra-Slim Design | 65mm depth, wall/pole mount |
| 5 | 🎨 | 160,000 Colors | 16-bit HDR, 160° viewing angle |
| 6 | 🔧 | Front Serviceability | Magnetic modules, front-access swap |

### 5. Specifications (dark section, 2-col)
**Left column:**
- Display: pitch, LED type, resolution, brightness, contrast, refresh, color depth, viewing angle
- Panel Sizes: standard (640×1920mm), compact (480×1600mm), module size, depth, weight

**Right column:**
- Environment: IP65, temp range, humidity, lifespan, MTBF
- Power: consumption, max, voltage, connectivity, control
- Content: video/image formats, max resolution

### 6. Applications (8 cards, 4-col grid)
| Card | Icon | Title |
|------|------|-------|
| 1 | 🏪 | Retail & Storefronts |
| 2 | 🏟️ | Venues & Stadiums |
| 3 | 🚏 | Transit & Street |
| 4 | 🏢 | Corporate & Campus |
| 5 | 🏥 | Healthcare |
| 6 | 🎓 | Education |
| 7 | ⛽ | Gas Stations & QSR |
| 8 | 🏨 | Hospitality |

### 7. CTA Section
- Dark gradient bg
- H2: "Ready to Light Up Your Space?"
- Two buttons: Get a Quote + Call number

### 8. Footer
- Copyright line, dark bg

## How to Modify

### Change product specs
All specs are plain HTML in the `#specs` section. Search for `spec-row` divs:
```html
<div class="spec-row"><span class="label">Pixel Pitch</span><span class="value">2.5mm</span></div>
```

### Change colors
Update CSS variables at the top of `<style>`:
```css
:root{--primary:#0066FF;--dark:#0a0a0a;--gray:#6b7280;--light:#f8fafc;--accent:#00d4ff}
```

### Add/remove feature cards
Each card follows this pattern inside `.features-grid`:
```html
<div class="feature-card">
  <div class="feature-icon">EMOJI</div>
  <h3>Title</h3>
  <p>Description</p>
</div>
```

### Add/remove application cards
Same pattern inside `.apps-grid`:
```html
<div class="app-card">
  <div class="app-icon">EMOJI</div>
  <h4>Title</h4>
  <p>Description</p>
</div>
```

### Change hero text
Search for `<h1>` in the hero section. The gradient-colored word is wrapped in `<span>`.

### Change branding
- Logo text: search for `class="logo"` in nav
- Page title: `<title>` tag in `<head>`
- Footer: bottom `<footer>` tag

## File Structure
```
ez-led-eposter/
├── index.html          ← entire site (self-contained, no dependencies)
├── STYLE-GUIDE.md      ← this file
└── CLAUDE.md           ← context for Claude Code
```

## Notes
- Single HTML file — all CSS is inline in `<style>`, no external deps except Google Fonts
- Fully responsive (mobile breakpoint at 768px)
- No JavaScript required (pure CSS animations)
- To add real product images: replace the `.poster-mockup` div with an `<img>` tag
