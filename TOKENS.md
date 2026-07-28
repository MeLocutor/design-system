# TOKENS.md — Referência Plana de Tokens (Alinhada ao DESIGN.md)

> Documentação humana dos tokens canônicos: nome (bate com DESIGN.md YAML e `tokens/*.json`), valor, papel semântico, quando usar/não usar, notas de contraste/prioridade.

---

## 1. Color Tokens

### 1.1 Base Palette

| Token | HEX | OKLCH | Pantone | Papel | Quando usar | Quando NÃO usar |
|-------|-----|-------|---------|-------|-------------|-----------------|
| `tinta` | `#1F2C3D` | `oklch(24% 0.045 252)` | 533 C | Primária (~30%) | Wordmark, nav, button bg, case headlines, structural icons | Long body text, large backgrounds, metric accent |
| `brasa` | `#C1502E` | `oklch(56% 0.15 42)` | 1665 C | Acento (≤10%) | Metrics highlight, primary CTA, active link, badges, 1 highlight icon/screen | Small text (fails WCAG AA), large backgrounds, Rodrigo photo (clothing/bg/light), >1 element/composition |
| `bronze` | `#B08D57` | `oklch(65% 0.08 78)` | 4515 C | Rare accent | 1 proof/achievement element per page (e.g., gamification badge) | Body text, multiple/page, combined with brasa in same piece |

### 1.2 Neutral Scale (Cinza-Morno, H≈50°)

| Token | HEX | OKLCH | Uso típico |
|-------|-----|-------|------------|
| `neutral_50`  | `#FAF8F6` | `oklch(98% 0.005 50)` | Page bg (light) |
| `neutral_100` | `#F2EEEA` | `oklch(95% 0.008 50)` | Secondary context blocks |
| `neutral_200` | `#E4DDD6` | `oklch(89% 0.012 50)` | Borders, dividers |
| `neutral_300` | `#CBC0B6` | `oklch(79% 0.02 50)` | Placeholder, very secondary text |
| `neutral_400` | `#A89C90` | `oklch(66% 0.025 50)` | Tertiary text, neutral icon (dark) |
| `neutral_500` | `#8B7F76` | `oklch(55% 0.02 50)` | Secondary text |
| `neutral_600` | `#6B615A` | `oklch(44% 0.018 50)` | Strong secondary text |
| `neutral_700` | `#4F4842` | `oklch(33% 0.015 50)` | Neutral icon (light) |
| `neutral_800` | `#332E2A` | `oklch(22% 0.012 50)` | Surface dark |
| `neutral_900` | `#1C1917` | `oklch(13% 0.008 50)` | Primary text (light) |

### 1.3 Semantic Tokens (Web)

| Token | Light | Dark | Uso | Nota contraste |
|-------|-------|------|-----|----------------|
| `background` | `#FAF8F6` | `#141C28` | Page bg | — |
| `surface` | `#FFFFFF` | `#1E2A3B` | Cards, panels, modals | — |
| `text_primary` | `#1C1917` | `#F2EEEA` | Body, headings | AAA both |
| `text_secondary` | `#6B615A` | `#CBC0B6` | Captions, metadata | AA both |
| `border` | `#E4DDD6` | `#33425A` | Dividers, card/input borders | — |
| `primary_button` | `#1F2C3D` | `#D0673F` | Primary CTA bg (dark = brasa) | AA dark: use dark text `#1C1917` on brasa |
| `link` | `#2F5C86` | `#5C93C4` | Inline links | AA both |
| `success` | `#2F6B45` | — | Positive states | AA light |
| `warning` | `#8A611F` | — | Alerts (large text/icon) | AA light |
| `error` | `#A32E22` | — | Form errors, negative states | AA light |

**Hover/Active (mechanical OKLCH L-adjust, same H/C):**
- `primary_button_hover`: `oklch(30% 0.05 252)` / `#2A3C52` (+6 L)
- `primary_button_active`: `oklch(18% 0.04 252)` / `#141D29` (−6 L)
- `link_hover`: `oklch(30% 0.09 252)` / `#24455F`

### 1.4 Proportion by Context (Hard Rules)

| Context | Neutrals | Tinta | Brasa | Bronze |
|---------|----------|-------|-------|--------|
| Site / Portfolio | 60% | 30% | ≤10% | Optional 1×/page |
| LinkedIn Post (img) | 55–65% | 25–35% | ≤10% | Rare |
| Slides | 60–70% | 25–30% | ≤10% (metric only) | Rare |
| Documents/PDF | Neutro + Tinta headers | — | Callout/metric only | Not recommended |
| Product UI (future) | 60% | 30% | ≤10% (CTA/state) | N/A |

**Hard rule:** Brasa > 10% → revert immediately. No exceptions.

**Dark mode inversion:** Brasa becomes primary action; Tinta becomes background/structure.

**Brasa never touches Rodrigo photo** (clothing, bg, key light) — conflicts Deep Winter colorimetry.

### 1.5 WCAG Quick Reference

| Pair | Contrast | Level | Note |
|------|----------|-------|------|
| text_primary / background (light) | ~15.8:1 | AAA | Free use |
| text_secondary / background (light) | ~5.6:1 | AA | Body text ok |
| link / background (light) | ~5.2:1 | AA | Links ok |
| **brasa as text / white** | **~3.3:1** | **❌ FAIL AA** | **Never use brasa for small text** — only button (dark text), icon, bg |
| text_primary / background (dark) | ~13.9:1 | AAA | — |
| primary_button_text / primary_button (dark, brasa) | ~5.1:1 | AA | Use dark text `#1C1917`, not white |
| error / background (light) | ~6.5:1 | AA | — |
| success / background (light) | ~6.1:1 | AA | — |

**Color blindness:** success (green) & error (red) have distinct lightness for deuteranopia/protanopia. **Always pair with icon (✓/✕) or explicit text.**

### 1.6 Print (Pantone/CMYK)

| Use | Spec |
|-----|------|
| Business card / letterhead | Tinta dominant (text/logo), Brasa only verso or hairline — never 50/50 |
| Offset spot (Pantone) | 533 C + 1665 C directly |
| CMYK standard | Use base table equivalents — confirm physical proof before run |
| Coated (couché) | Preferred for Brasa saturation |
| Uncoated (offset/recycled) | Tinta gets matte/grayer — ok for sober tone; adjust if Brasa looks "washed" |

---

## 2. Typography Tokens

### 2.1 Families & Roles (Strict — Never Blend)

| Role | Family | Weights | Source | License |
|------|--------|---------|--------|---------|
| `display` / `headlines` | Sentient | Medium, Bold | Fontshare | ITF Free (commercial ok) |
| `body` | Switzer | Regular, Medium | Fontshare | ITF Free |
| `metric` | Trench Slab | SemiBold, Bold | Fontshare | ITF Free |

**Forbidden:** script/hand-lettering, blackletter, slab as primary/body, distressed/worn fonts.

### 2.2 Modular Scale (ratio ~1.25, base 16px)

| Token | Desktop | Mobile | Line-height | Family | Weight | Uso |
|-------|---------|--------|-------------|--------|--------|-----|
| `display` | 56px | 36px | 1.1 | Sentient | Bold | Hero home, case cover — 1×/page |
| `h1` | 40px | 28px | 1.15 | Sentient | Bold | Case title, article title |
| `h2` | 32px | 24px | 1.2 | Sentient | Medium/Bold | Main sections |
| `h3` | 24px | 20px | 1.3 | Sentient | Medium | Subsections, card title |
| `h4` | 20px | 18px | 1.35 | Switzer | Medium | Block labels, component headers |
| `body_lg` | 18px | 16px | 1.6 | Switzer | Regular | Opening paragraph, lede |
| `body` | 16px | 15px | 1.6 | Switzer | Regular | Standard body text |
| `caption` | 14px | 13px | 1.4 | Switzer | Regular | Metadata, legends, sector tags |
| `metric_display` | 64px | 40px | 1.05 | Trench Slab | SemiBold/Bold | Proof strip, case anchor number |
| `metric_inline` | 28px | 22px | 1.1 | Trench Slab | SemiBold | Metric inside card/paragraph |

**Interpolation rule:** New size → interpolate at ratio ~1.25, don't invent arbitrary value.

### 2.3 Channel Guidelines

| Canal | Aplicação |
|-------|-----------|
| Web/Framer | Full scale; Sentient + Switzer via self-host or Fontshare CDN |
| LinkedIn | No type control — hierarchy simulated by short line breaks + strong 1st sentence |
| Slides | Reduce to 3 levels: Title (H1/H2), Body (Body Large), Metric (Trench Slab) |
| PDF/Documentos | Sentient headers, Switzer body — test P&B print |

---

## 3. Spacing Tokens

### 3.1 Base Unit & Scale

| Token | Value | Usage |
|-------|-------|-------|
| `space_1` | 4px | Fine tune (icon + label) |
| `space_2` | 8px | Min space between related elements |
| `space_3` | 16px | Small component internal padding |
| `space_4` | 24px | Card padding, grid gutter |
| `space_5` | 32px | Space between blocks within section |
| `space_6` | 48px | Space between subsections |
| `space_7` | 64px | Major section spacing (mobile) |
| `space_8` | 96px | Major section spacing (desktop) |
| `space_9` | 128px | Hero breath, page opening |
| `space_10` | 160px | Rare — large editorial block separation |

**Base:** 8px. Geometric-soft scale — same "weight grows slowly" logic as typography & icon stroke.

### 3.2 Grid

| Breakpoint | Columns | Gutter | Margin |
|------------|---------|--------|--------|
| Desktop (≥1200px) | 12 | 24px | 80px |
| Tablet (768–1199px) | 6 | 16px | — |
| Mobile (<768px) | 4 | 16px | 24px |

**Compatibility:** Icon grid 24px = layout grid submultiple (24 = 8×3) → icon, spacing, column always align.

### 3.3 Density by Context

| Context | Density | Note |
|---------|---------|------|
| Site/portfolio | Low (generous) | Min 30% negative space/section |
| LinkedIn post/carousel | Medium-high | Mobile-first, 1–3 lines/paragraph |
| Slides | Low | Max 1 idea/slide, generous space around data |
| PDF/document | Medium | Standard print margins 2–2.5cm, headers follow type scale |

---

## 4. Radius Tokens

| Token | Value | Usage | Rule |
|-------|-------|-------|------|
| `sm` | 2px | Icons, small controls | — |
| `md` | 4px | Buttons, inputs | — |
| `lg` | 8px | Cards, large containers | — |
| `pill` | **FORBIDDEN** | Never | Contradicts Sábio structural register |

---

## 5. Elevation/Shadow Tokens

| Token | Value | Usage |
|-------|-------|-------|
| `card` | `0 1px 2px rgba(28,25,23,0.06), 0 2px 8px rgba(28,25,23,0.04)` | Interactive cards only — indicates clickable |
| `default` | `none` | Flat is default everywhere else |

**Never:** drop shadows under text, on illustrations/icons, decorative shadows, glassmorphism.

---

## 6. Motion Tokens

| Token | Value | Usage | Forbidden |
|-------|-------|-------|-----------|
| `fast` | 120ms | Icon hover | bounce, elastic, spring |
| `base` | 150–200ms | Button/color state change | infinite auto-loop |
| `slow` | 300–500ms | Section/illustration reveal (stagger 60–80ms/layer) | decorative path-draw |
| `ease_standard` | `cubic-bezier(0.16, 1, 0.3, 1)` | ease-out (reveal hierarchy) | — |
| `ease_linear` | `linear` | Opacity-only fades | — |

**Principle:** Motion reveals hierarchy — never entertains. No auto-loop without user interaction.

---

## 7. Breakpoint Tokens

| Token | Value |
|-------|-------|
| `mobile` | `<768px` |
| `tablet` | `768–1199px` |
| `desktop` | `≥1200px` |

---

## 8. Z-Index Tokens

| Token | Value | Usage |
|-------|-------|-------|
| `base` | 0 | Default |
| `dropdown` | 100 | Dropdowns, popovers |
| `modal` | 200 | Modals, drawers |
| `toast` | 300 | Toasts, notifications |
| `tooltip` | 400 | Tooltips |

---

## 9. Referência Rápida de Nomes Canônicos

Use estes nomes exatos no código (batem com DESIGN.md YAML e `tokens/*.json`):

```
color: tinta, brasa, bronze, neutral_50..neutral_900
color.semantic: background, surface, text_primary, text_secondary, border, primary_button, link, success, warning, error
typography.families: display, body, metric
typography.scale: display, h1, h2, h3, h4, body_lg, body, caption, metric_display, metric_inline
spacing: space_1..space_10, grid
radius: sm, md, lg
elevation: card, default
motion: fast, base, slow, ease_standard, ease_linear
breakpoints: mobile, tablet, desktop
z: base, dropdown, modal, toast, tooltip
```