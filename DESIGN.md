---
project: "Rodrigo Melo — Portfolio & Brand System"
version: "1.0"
updated: "2026-07-27"
archetype:
  primary: "Sábio"
  secondary: "Explorador"
  shadow_filter: "Fora da Lei — ethical filter only, never visual identity"
principles:
  - "Estrutura antes de estética"
  - "Dado antes de adjetivo"
  - "Método visível (briefing → pergunta → decisão → resultado)"
  - "Acento é raro (Brasa ≤ 10% área)"
  - "Silêncio funcional (flat, espaço negativo, motion mínimo)"
  - "Consistência sobre novidade (reusar ícones/ilustrações fixas)"
# Minimal valid schema for @google/design.md — see tokens/*.json for full tokens with metadata
colors:
  primary: "#1F2C3D"        # tinta
  accent: "#C1502E"         # brasa
  bronze: "#B08D57"         # bronze (rare)
  neutral_50: "#FAF8F6"
  neutral_100: "#F2EEEA"
  neutral_200: "#E4DDD6"
  neutral_300: "#CBC0B6"
  neutral_400: "#A89C90"
  neutral_500: "#8B7F76"
  neutral_600: "#6B615A"
  neutral_700: "#4F4842"
  neutral_800: "#332E2A"
  neutral_900: "#1C1917"
  background_light: "#FAF8F6"
  background_dark: "#141C28"
  surface_light: "#FFFFFF"
  surface_dark: "#1E2A3B"
  text_primary_light: "#1C1917"
  text_primary_dark: "#F2EEEA"
  text_secondary_light: "#6B615A"
  text_secondary_dark: "#CBC0B6"
  border_light: "#E4DDD6"
  border_dark: "#33425A"
  primary_button_light: "#1F2C3D"
  primary_button_dark: "#D0673F"
  link_light: "#2F5C86"
  link_dark: "#5C93C4"
  success: "#2F6B45"
  warning: "#8A611F"
  error: "#A32E22"
# proportion: 60% neutral / 30% tinta / 10% brasa (bronze exception)

typography:
  fontFamily:
    display: "Sentient, Georgia, serif"
    body: "Switzer, -apple-system, sans-serif"
    metric: "Trench Slab, Georgia, serif"
  fontSize:
    display: "56px"
    h1: "40px"
    h2: "32px"
    h3: "24px"
    h4: "20px"
    body_lg: "18px"
    body: "16px"
    caption: "14px"
    metric_display: "64px"
    metric_inline: "28px"
  fontWeight:
    display: 700
    h1: 700
    h2: 500
    h3: 500
    h4: 500
    body_lg: 400
    body: 400
    caption: 400
    metric_display: 600
    metric_inline: 600
  lineHeight:
    display: 1.1
    h1: 1.15
    h2: 1.2
    h3: 1.3
    h4: 1.35
    body_lg: 1.6
    body: 1.6
    caption: 1.4
    metric_display: 1.05
    metric_inline: 1.1
# forbidden: script/hand-lettering, blackletter, slab as primary/body, distressed/worn fonts

spacing:
  base: 8
  scale: [4, 8, 16, 24, 32, 48, 64, 96, 128, 160]
  grid:
    desktop_cols: 12
    tablet_cols: 6
    mobile_cols: 4
    gutter_desktop: "24px"
    gutter_mobile: "16px"
    margin_desktop: "80px"
    margin_mobile: "24px"

rounded:
  sm: "2px"
  md: "4px"
  lg: "8px"
# pill: never (contradicts Sábio register)

elevation:
  card: "0 1px 2px rgba(28,25,23,0.06), 0 2px 8px rgba(28,25,23,0.04)"
  default: "none"

# motion not a recognized schema key — see tokens/motion.json
# motion:
#   fast: "120ms"
#   base: "150-200ms"
#   slow: "300-500ms"
#   ease: "cubic-bezier(0.16, 1, 0.3, 1)"
#   linear: "linear"
#   forbidden: ["bounce", "elastic", "spring", "infinite auto-loop", "decorative path-draw"]

components:
  case_card: {}
  proof_strip: {}
  proof_block_testimonial: {}
  post_cover: {}
  about_section: {}
  nav: {}
# Full component specs in COMPONENTS.md (anatomy, variants, states, a11y)
---

# DESIGN.md — Rodrigo Melo Portfolio & Brand System

> Root design reference for AI agents (Claude Code, Cursor) generating/editing this portfolio's UI, HTML/CSS, or Framer components. Every rule derives from archetype (Sábio + Explorador) and case metrics (+1048%, -54%, +237%) — never arbitrary aesthetics. Strategic rationale in `BRAND.md`; this file is the compact, implementation-facing version.

## 1. Overview

**Positioning:** Product Designer as "Arquiteto de Decisão de Produto". System proves *structure*, not decoration.  
**Core rule:** Numbers are proof → strongest visual weight (Trench Slab + Brasa). Nothing competes with a metric.

**Archetype → Visual:**
- Sábio (primary) → serif wordmark, structural navy (Tinta), rigid grid, flat surfaces, no ornament
- Explorador (secondary) → one warm accent (Brasa), one heavy slab weight, one asymmetric element/illustration
- Fora da Lei → never a visual style; only *absence* (iGaming never promoted/styled)

## 2. Colors

Source of truth: `colors` block above + `tokens/colors.json` (full metadata: oklch, Pantone, role, usage, WCAG).

- **Proportion:** 60% neutral / 30% Tinta / 10% Brasa. Bronze = rare exception (1×/page), not in ratio.
- **Brasa ≤ 10%** any composition. Exceeds → revert, no exception.
- **Dark mode inverts:** Brasa becomes primary action; Tinta becomes background/structure.
- **Brasa never touches Rodrigo photo** (clothing, bg, key light) — conflicts Deep Winter colorimetry.
- WCAG AA+ for all semantic pairs (see `TOKENS.md` / source card `Sistema de Cores`).

## 3. Typography

Three families, strict roles — never blend:

| Family | Role |
|--------|------|
| **Sentient** (serif humanist) | wordmark, headlines Display–H3 |
| **Switzer** (neutral sans) | all body, UI labels, captions |
| **Trench Slab** (heavy slab) | metrics ONLY (+1048%, -54%, +237%) — never body/headline/wordmark |

Use `typography.fontSize` + `typography.fontWeight` + `typography.lineHeight` for exact sizes (see YAML above). New size → interpolate ratio ~1.25, don't invent.

## 4. Layout & Spacing

- 12-col desktop / 6 tablet / 4 mobile, per `spacing.grid`
- 8px base scale (`spacing.scale`) — no arbitrary px outside list
- Min 30% negative space/section (editorial density, not app density)
- Section order: Hero → Proof → Content → CTA. Never bio first, never result before method.

## 5. Elevation

Flat by default. **Only** `elevation.card` on interactive cards = clickable. Never decorative, never under text, never on illustrations/icons.

## 6. Shapes

- Radius: 2px (icons), 4px (buttons/inputs), 8px (cards) — see `rounded`
- **Never pill/fully-rounded buttons**
- Icons: 1.5–2px stroke, 24px grid, flat, no fill/duotone, butt-cap, no round caps
- Illustrations: geometric, ≤1 organic concession, max 1 accent (Brasa XOR Bronze)

## 7. Components

See `COMPONENTS.md` for full anatomy/variants/states/errors/a11y. Summary contract:

| Component | Must include | Must never include |
|---|---|---|
| `case_card` | category icon, H3 title, 1-line problem, sector tag, Trench Slab metric, link | photo/screenshot thumb, adjective title, 2+ Brasa elements |
| `proof_strip` | ≤4 metrics, Trench Slab + Brasa, `·` separators | decorative icons per metric |
| `proof_block_testimonial` | quote Body Large, attribution Caption | author photo; **no invented quotes** — none exist yet |
| `post_cover` | 1 illustration (theme by category), overlaid Sentient title | lettering inside illustration, 2 accent colors |
| `about_section` | secondary-register photo, 3 blocks (Quem sou / Como trabalho / Transição) | performative enthusiasm, fandom props as subject |
| `nav` | 5 fixed items (Home·Work·About·Contact·Résumé), Brasa underline on active only | >5 items, >1 active accent |

## 8. Do / Don't

**Do:**
- Lead every case/post: brief → question → decision → metric
- Keep Trench Slab exclusive to numbers
- Test icon/illustration legibility at render size before ship
- Motion = reveal hierarchy only
- Name sector plainly: "iGaming → translates to fintech/health"

**Don't:**
- Brasa > 10% any screen
- Corporate memphis, mascots, cartoons
- Drop shadows, gradients, glassmorphism
- Bounce/elastic/spring/auto-loop animation
- Invent testimonial content
- Brasa on Rodrigo photo (clothing/bg/lighting)
- Pill buttons or decorative radii

---

*Source of truth: `BRAND.md`. If this file and vault cards disagree, vault wins — update this file.*