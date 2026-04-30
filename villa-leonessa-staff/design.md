# Design Document — Villa Leonessa Staff Attire

## 1. Profile Baseline Declaration

- **Profile selection**: `profiles/promotion.md` — Brand launch / culture showcase profile
- **Selection rationale**: Villa Leonessa is a luxury heritage brand. The staff uniform presentation functions as a brand culture showcase, displaying the sartorial identity of the house. This aligns with high-end fashion/brand visual systems.
- **Referenced dimensions**: Design philosophy (visual impact, less-is-more, brand consistency), low information density, image-dominant ratio, color guidance (brand-first), bold layout, content expression techniques (mask overlay, bleed images, ambient lighting), decoration prohibitions.
- **Deviation notes**: 
  - The presentation is only **one page**, so we treat it as a brand board / lookbook single page rather than a multi-slide narrative.
  - No table of contents, chapter pages, or closing page — just a single composition.

## 2. Style Baseline Declaration

- **Style anchor selection**: 
  - **Villa Leonessa Brand Book (HTML reference)** — Color scheme, typographic treatments (Cinzel uppercase tracking, Cormorant Garamond italic display), ornamental gold lines, dark-night background, and Moroccan-Italian fusion mood.
  - **Monocle magazine** — Editorial grid discipline, image-heavy layouts, restrained typography, premium cultural feel.
- **Referenced dimension explanation**: 
  - From Villa Leonessa: color palette (Night, Atlas Gold, Ivory, Stone), ornamental borders, uppercase tracked labels, the "VL" monogram spirit, and dark-premium atmosphere.
  - From Monocle: clean grid-based image layouts for showcasing multiple photographs on one page with elegant spacing.
- **Reference scope declaration**: Style + color scheme + layout (brand book HTML as the primary reference).

## 3. Style Details

### Color Design Principles
- **Color tendency**: Conservative & steady with striking gold accents on dark — luxury hospitality brand expression.
- **Temperature**: Warm, mineral, papery — drawn from ochre palaces and earthen walls.
- **Primary**: Atlas Gold `#C9A84C` — the brand's dominant accent, used for titles, labels, ornaments, and highlights.
- **Background**: Leonessa Night `#0D0A06` — deep warm black, the primary canvas.
- **Text**: Ivory Parchment `#F5EFE0` — primary text on dark backgrounds.
- **Secondary**: Atlas Stone `#8A7F72` — muted warm grey for secondary text, captions, and subtle dividers.
- **Accent**: Marrakech Rose `#C4543A` — used extremely sparingly, only for small ornamental dots or wax-seal references if needed.
- **Surface**: Leonessa Dusk `#2C241A` — slightly lighter dark for card backgrounds or subtle depth layers.

### Font Usage Principles
- **Display / Hero titles**: Oranienbaum — high-contrast serif with classical temperament, emulates Cormorant Garamond's elegant display quality. Used for the main page title in italic.
- **Title / Labels / Role names**: Oranienbaum — set in uppercase with wide letter-spacing (3–4px) to emulate Cinzel's inscription style. Small sizes (13–16px) for role labels.
- **Body / Captions**: QuattrocentoSans — classic elegant sans-serif, highly readable at small sizes. Used for any supplementary body text (kept minimal).

### Font Size Hierarchy
- Page title: 36–42px (Oranienbaum, italic, ivory)
- Brand subtitle / ornament: 11–12px (Oranienbaum, uppercase, letter-spacing 4px, gold, opacity 0.6)
- Role labels: 14px (Oranienbaum, uppercase, letter-spacing 3px, gold)
- Caption / footer: 12px (QuattrocentoSans, stone color, letter-spacing 1px)

### Text Box and Container Styles
- No rounded rectangles. All containers use sharp corners.
- Image cards: No visible borders; images sit directly on the dark background with subtle spacing.
- Content separation: Whitespace + thin horizontal gold lines (`#C9A84C` at 30–40% opacity) as ornamental dividers.
- Decorative elements: Thin gold horizontal rule lines, small gold ornamental dots, and subtle geometric patterns.

### Image Style
- Photography: Full-bleed images within their grid cells, no clipping shapes (rectangular only), preserving the warm golden-hour photography aesthetic.
- No icons, charts, or tables — this is a pure image + typography brand board.

## 4. Layout System

### Global Layout Characteristics
- **Page size**: 1280 x 720 (16:9)
- **Page margins**: 50px left/right, 40px top/bottom
- **Grid**: 3-column image grid with 20px column gaps; 2 rows with 30px row gaps.
- **Unified elements**: 
  - Top-center brand ornament line with "VILLA LEONESSA" label.
  - Bottom-center thin gold rule + tagline.

### Single Page Layout (Hero Board)
- **Top zone** (y: 30–120): 
  - Centered small-caps brand label "VILLA LEONESSA · BAB ATLAS · MARRAKECH" in gold, letter-spaced.
  - Thin gold ornamental line beneath.
  - Page title in large italic Oranienbaum: "The House Attire" or "Uniforms of the House" in ivory.
- **Image grid zone** (y: 140–640):
  - 3 columns × 2 rows of staff photographs.
  - Each image: approximately 380px wide × 210px tall.
  - Below each image: a centered uppercase role label in gold (e.g., "CULINARY ARTS", "GARDEN & GROUNDS", "HOUSEKEEPING", "RESIDENCE MANAGER", "ENGINEERING", "SECURITY").
- **Bottom zone** (y: 660–720):
  - Thin gold rule line.
  - Small tagline: "Eleven centuries of Italian nobility, resting now in the shadow of the Atlas." in stone color, italic.

## 5. Style Usage Rules

- `title` textStyle: Page hero title — Oranienbaum italic, ivory, large.
- `brandLabel` textStyle: Small uppercase tracked labels — Oranienbaum, gold.
- `roleLabel` textStyle: Staff role names under images — Oranienbaum uppercase, gold, small.
- `caption` textStyle: Footer tagline and secondary text — QuattrocentoSans, stone.
- Colors:
  - `$primary` (Atlas Gold): titles, labels, ornamental lines, accents.
  - `$background` (Leonessa Night): page background.
  - `$text` (Ivory Parchment): main title text.
  - `$secondary` (Atlas Stone): captions, secondary info.
  - `$surface` (Leonessa Dusk): subtle depth if needed.

## 6. Risk Prohibitions

- [ ] Do NOT use rounded rectangles — keep all corners sharp for the luxury architectural feel.
- [ ] Do NOT use blue, purple, or gradient rainbow colors — stick strictly to the brand palette.
- [ ] Do NOT cram images edge-to-edge without gaps — maintain the 20px grid gaps.
- [ ] Do NOT use overly large body text — this is an image-dominant brand board; text is minimal.
- [ ] Do NOT place light text on light backgrounds — everything sits on the dark Night background.
- [ ] Do NOT use inconsistent alignment — all grid items and text must be perfectly centered or grid-aligned.
- [ ] Minimum font size: 12px for captions, 14px for labels, 36px for titles.

## 7. Theme Definition

```yaml
theme:
  colors:
    primary: "#C9A84C"
    background: "#0D0A06"
    text: "#F5EFE0"
    secondary: "#8A7F72"
    surface: "#2C241A"
    accent: "#C4543A"
  textStyles:
    title:
      fontSize: 40
      color: "$text"
      fontFamily: "Oranienbaum"
      fontStyle: "italic"
      lineHeight: 1.2
      letterSpacing: 1
    brandLabel:
      fontSize: 11
      color: "$primary"
      fontFamily: "Oranienbaum"
      letterSpacing: 4
      lineHeight: 1.3
    roleLabel:
      fontSize: 14
      color: "$primary"
      fontFamily: "Oranienbaum"
      letterSpacing: 3
      lineHeight: 1.3
    caption:
      fontSize: 12
      color: "$secondary"
      fontFamily: "QuattrocentoSans"
      lineHeight: 1.5
      letterSpacing: 1
```
