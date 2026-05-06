# ECOLLABO8 Masterclass Page — Design System & Redesign Guide

> Dokumen ini berisi panduan design system untuk redesign halaman Masterclass (ecollabo8.com/masterclass/) agar selaras dengan brand guidelines Ecollabo8 dan konsisten dengan homepage utama.

---

## 1. Brand Identity

### Brand Name
- **ECOLLABO8** (dengan angka 8 sebagai aksen warna biru/cyan)
- Logo: "ECOLLABO" (hitam/putih) + "8" (cyan/biru)

### Brand Personality
- Industrial-Professional
- Business-First
- Clean & Minimalist
- High-Contrast
- Trustworthy & Proven

### Tagline/Positioning
- "Turn Plastic Into Industrial Opportunity"
- Fokus pada real business, bukan teori

---

## 2. Color System

### Primary Colors (Website — dari Brand Guidelines)

| Token | Hex | Usage |
|-------|-----|-------|
| `--color-black` | `#000000` | Backgrounds gelap, header bar, teks utama |
| `--color-navy` | `#1E2654` | Backgrounds section gelap, aksen profesional |
| `--color-blue` | `#236CE4` | Primary CTA buttons, aksen, highlights, link hover |

### Extended Palette (dari Homepage Live)

| Token | Hex | Usage |
|-------|-----|-------|
| `--color-white` | `#FFFFFF` | Background utama, teks di atas dark bg |
| `--color-light-gray` | `#F5F5F5` | Section background alternatif |
| `--color-text-dark` | `#222222` | Heading text, dark elements |
| `--color-text-body` | `#999999` | Body text, secondary text |
| `--color-text-medium` | `#777777` | Nav links, medium emphasis text |
| `--color-border` | `#EEEEEE` | Borders, dividers |
| `--color-cyan-accent` | `#00AEEF` | Logo "8", floating elements (legacy) |
| `--color-whatsapp` | `#25D366` | WhatsApp floating button |

### Color Usage Rules
1. **Background utama**: White (`#FFFFFF`) atau Light Gray (`#F5F5F5`)
2. **Dark sections**: Black (`#000000`) atau Navy (`#1E2654`)
3. **CTA Buttons**: Blue (`#236CE4`) dengan teks putih
4. **Headings**: Dark (`#222222`) di atas light bg, White di atas dark bg
5. **Body text**: Medium gray (`#999999`) untuk readability
6. **Overlay pada parallax/hero**: `rgba(0, 0, 0, 0.80)` atau `rgba(30, 38, 84, 0.85)`

---

## 3. Typography

### Font Families

| Role | Font | Weight | Fallback |
|------|------|--------|----------|
| **Headings** | Montserrat | 400, 600, 700 | sans-serif |
| **Body** | Open Sans | 400, 600 | sans-serif |
| **Icons** | Font Awesome | — | — |

### Font Sizes (Desktop)

| Element | Size | Weight | Transform | Letter-spacing | Line-height |
|---------|------|--------|-----------|----------------|-------------|
| Hero H1 (utama) | 100px | 700 | uppercase | 0 | 1.1 |
| H1 (section) | 36px | 700 | uppercase | 3px | 1.2 |
| H2 (section title) | 28px | 600 | uppercase | 2px | 1.3 |
| H4 (subsection) | 18px | 600 | uppercase | 1px | 1.4 |
| H5 (item title) | 16px | 600 | none | 0 | 1.5 |
| Body (p) | 14px | 400 | none | 0 | 24px |
| Small/Meta | 12px | 400 | uppercase | 1px | 1.5 |
| Button text | 14-16px | 600 | uppercase | 0 | 1 |

### Font Sizes (Mobile ≤767px)

| Element | Size |
|---------|------|
| Hero H1 | 36px |
| H1 (section) | 28px |
| H2 | 22px |
| H4 | 16px |
| Body | 14px |

### Typography Rules
- Headings selalu **uppercase** (kecuali `.big-title`)
- Body text menggunakan warna `#999999` untuk kontras yang nyaman
- Heading text menggunakan `#222222` (light bg) atau `#FFFFFF` (dark bg)
- Line-height body: `24px` untuk readability optimal
- Max paragraph width: ~700px (centered) untuk comfortable reading

---

## 4. Spacing System

### Section Padding

| Context | Desktop | Tablet (≤1024px) | Mobile (≤767px) |
|---------|---------|-------------------|-----------------|
| Section (vertical) | 100px top/bottom | 80px | 60px |
| Section (horizontal) | 20px left/right | 20px | 15px |
| Between sections | 0 (sections stack) | 0 | 0 |
| Section title → content | 100px margin-bottom | 60px | 40px |

### Component Spacing

| Context | Value |
|---------|-------|
| Grid gutter | 4% (between columns) |
| Grid row gap | 20px |
| Card internal padding | 30-50px |
| Icon → text | 15-20px |
| Heading → paragraph | 20px |
| Paragraph → paragraph | 15px |
| Button padding (large) | 15px 25px |
| Button padding (medium) | 10px 15px |
| Form field spacing | 20px between fields |

### Container Widths

| Breakpoint | Container Max-Width |
|------------|---------------------|
| > 1300px | 1180px |
| ≤ 1300px | 920px |
| ≤ 1024px | 600px |
| ≤ 767px | 400px |
| ≤ 479px | 280px |

---

## 5. Buttons

### Primary CTA Button

```css
.btn-primary {
  background-color: #236CE4;
  color: #FFFFFF;
  font-family: 'Montserrat', sans-serif;
  font-size: 14px;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0;
  padding: 15px 25px;
  border-radius: 50px; /* pill-shaped */
  border: none;
  display: inline-block;
  transition: all 0.3s ease;
  cursor: pointer;
}
.btn-primary:hover {
  background-color: #1E2654;
  transform: translateY(-2px);
  box-shadow: 0 4px 15px rgba(35, 108, 228, 0.3);
}
```

### Secondary/Outline Button

```css
.btn-outline {
  background: transparent;
  color: #222222;
  font-family: 'Montserrat', sans-serif;
  font-size: 14px;
  font-weight: 600;
  text-transform: uppercase;
  padding: 15px 25px;
  border: 2px solid #222222;
  border-radius: 50px;
  transition: all 0.3s ease;
}
.btn-outline:hover {
  background-color: #222222;
  color: #FFFFFF;
}
```

### White Outline Button (untuk dark backgrounds)

```css
.btn-outline-white {
  background: transparent;
  color: #FFFFFF;
  border: 2px solid #FFFFFF;
  border-radius: 50px;
  padding: 15px 25px;
  font-family: 'Montserrat', sans-serif;
  font-size: 14px;
  font-weight: 600;
  text-transform: uppercase;
  transition: all 0.3s ease;
}
.btn-outline-white:hover {
  background-color: #FFFFFF;
  color: #222222;
}
```

### Button Sizes

| Size | Font-size | Padding | Border-radius |
|------|-----------|---------|---------------|
| Small | 12px | 5px 9px 7px 9px | 50px |
| Medium | 14px | 10px 15px | 50px |
| Large | 16px | 15px 25px | 50px |
| Full-width | 14px | 15px 25px | 50px |

---

## 6. Layout & Grid

### Grid System

| Columns | Width per column | Gutter |
|---------|-----------------|--------|
| 2 cols | 48% | 4% |
| 3 cols | 30.6% | 4% |
| 4 cols | 22% | 4% |

### Page Structure (Masterclass)

```
┌─────────────────────────────────────────────┐
│ HEADER (fixed, black bar, full-width)       │
├─────────────────────────────────────────────┤
│ HERO SECTION (full-width, dark bg/overlay)  │
│   - H1 centered, white                     │
│   - Subtitle paragraph                     │
│   - CTA Button (blue, pill)                │
├─────────────────────────────────────────────┤
│ SECTION: What This Program Delivers        │
│   (white bg, centered text, icon grid)     │
├─────────────────────────────────────────────┤
│ SECTION: Proof, Not Theory                 │
│   (light-gray bg, 2-col icon+text)         │
├─────────────────────────────────────────────┤
│ SECTION: Why This Program Exists           │
│   (white bg, 2x2 grid with icons)          │
├─────────────────────────────────────────────┤
│ SECTION: The Full Story                    │
│   (navy/dark bg, centered narrative)       │
├─────────────────────────────────────────────┤
│ SECTION: What You Will Learn               │
│   (white bg, 3-col curriculum grid)        │
├─────────────────────────────────────────────┤
│ SECTION: Partnership (Conduit Impact)      │
│   (light-gray bg, centered)               │
├─────────────────────────────────────────────┤
│ SECTION: Program Structure                 │
│   (white bg, 2-col phases)                 │
├─────────────────────────────────────────────┤
│ SECTION: Outcome                           │
│   (navy bg, white text, bullet list)       │
├─────────────────────────────────────────────┤
│ SECTION: Who This Is For                   │
│   (white bg, 2-col)                        │
├─────────────────────────────────────────────┤
│ SECTION: What Makes This Different         │
│   (light-gray bg, 4-col features)          │
├─────────────────────────────────────────────┤
│ SECTION: Program Format                    │
│   (white bg, simple 2-col)                 │
├─────────────────────────────────────────────┤
│ SECTION: Video / See How We Built It       │
│   (dark bg, embedded video)                │
├─────────────────────────────────────────────┤
│ SECTION: Apply / Form                      │
│   (white bg, centered form)               │
├─────────────────────────────────────────────┤
│ FOOTER                                      │
└─────────────────────────────────────────────┘
```

---

## 7. Components

### Section Title Pattern

```css
.section-title {
  text-align: center;
  max-width: 700px;
  margin: 0 auto 100px auto;
}
.section-title h4 {
  font-family: 'Montserrat', sans-serif;
  font-size: 18px;
  font-weight: 600;
  text-transform: uppercase;
  color: #222222;
  letter-spacing: 1px;
  margin-bottom: 20px;
}
.section-title .border {
  background: #236CE4;
  height: 2px;
  width: 100px;
  margin: 0 auto 40px auto;
}
.section-title p {
  font-family: 'Open Sans', sans-serif;
  font-size: 14px;
  color: #999999;
  line-height: 24px;
}
```

### Icon Circle (Service/Feature Item)

```css
.icon-circle {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  background-color: #236CE4;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 20px auto;
}
.icon-circle i {
  color: #FFFFFF;
  font-size: 28px;
}
```

### Feature Card (untuk "What You Will Learn", "What Makes This Different")

```css
.feature-card {
  text-align: center;
  padding: 30px 20px;
}
.feature-card h5 {
  font-family: 'Montserrat', sans-serif;
  font-size: 16px;
  font-weight: 600;
  color: #222222;
  margin-bottom: 15px;
}
.feature-card p {
  font-family: 'Open Sans', sans-serif;
  font-size: 14px;
  color: #999999;
  line-height: 24px;
}
```

### Phase/Timeline Card

```css
.phase-card {
  padding: 30px;
  background: #FFFFFF;
  border-radius: 8px;
  box-shadow: 0 2px 20px rgba(0, 0, 0, 0.05);
}
.phase-card h5 {
  font-family: 'Montserrat', sans-serif;
  font-size: 16px;
  font-weight: 700;
  color: #236CE4;
  margin-bottom: 15px;
  text-transform: uppercase;
}
.phase-card p {
  font-family: 'Open Sans', sans-serif;
  font-size: 14px;
  color: #777777;
  line-height: 24px;
}
```

### Form Styling

```css
.form-field input,
.form-field textarea,
.form-field select {
  width: 100%;
  padding: 12px 15px;
  font-family: 'Open Sans', sans-serif;
  font-size: 14px;
  color: #222222;
  border: 1px solid #EEEEEE;
  border-radius: 3px;
  background: #F5F5F5;
  transition: border-color 0.3s ease;
}
.form-field input:focus,
.form-field textarea:focus {
  border-color: #236CE4;
  outline: none;
}
.form-field label {
  font-family: 'Montserrat', sans-serif;
  font-size: 12px;
  font-weight: 600;
  text-transform: uppercase;
  color: #222222;
  letter-spacing: 1px;
  margin-bottom: 8px;
  display: block;
}
```

---

## 8. Animations & Transitions

### Default Transition
```css
transition: all 0.3s ease;
```

### Hover Effects
- Buttons: `translateY(-2px)` + `box-shadow`
- Cards: `translateY(-5px)` + increased `box-shadow`
- Links: color change with `0.3s ease`
- Icons: `scale(1.1)` with `0.2s ease`

### Scroll Animations (entrance)
- Elements fade in from bottom: `opacity: 0` → `opacity: 1`, `translateY(30px)` → `translateY(0)`
- Stagger delay: 0.1s between items
- Duration: 0.6s ease-out

### Parallax
- Background sections with `background-attachment: fixed`
- Overlay: `rgba(0, 0, 0, 0.80)` atau `rgba(30, 38, 84, 0.85)` (navy)

---

## 9. Navigation (Header)

### Desktop Header
```css
/* Fixed horizontal black bar */
.header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 80px;
  background-color: #000000;
  z-index: 1000;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 40px;
}
.header .logo img {
  height: 40px;
  width: auto;
}
.header nav a {
  font-family: 'Open Sans', sans-serif;
  font-size: 14px;
  font-weight: 400;
  color: #FFFFFF;
  text-transform: uppercase;
  letter-spacing: 1px;
  margin-left: 30px;
  transition: color 0.3s ease;
}
.header nav a:hover,
.header nav a.active {
  color: #236CE4;
}
```

### Mobile Header
- Hamburger menu (3 lines → X animation)
- Off-canvas slide dari kanan (500px width, dark bg)
- Transition: `300ms cubic-bezier(0.86, 0, 0.07, 1)`

---

## 10. Responsive Breakpoints

| Breakpoint | Target |
|------------|--------|
| > 1300px | Large desktop |
| ≤ 1300px | Desktop |
| ≤ 1024px | Tablet landscape |
| ≤ 767px | Tablet portrait / Mobile |
| ≤ 479px | Small mobile |

### Responsive Rules
- Grid columns collapse to 100% width at ≤1024px
- Font sizes reduce proportionally at mobile
- Section padding reduces from 100px → 60px at mobile
- Container width adapts per breakpoint
- Navigation switches to hamburger at ≤1024px

---

## 11. Dark Section Styling (Navy/Black)

```css
.section-dark {
  background-color: #1E2654;
  color: #FFFFFF;
}
.section-dark h1,
.section-dark h2,
.section-dark h4,
.section-dark h5 {
  color: #FFFFFF;
}
.section-dark p {
  color: rgba(255, 255, 255, 0.75);
}
.section-dark .border {
  background: #236CE4;
}
```

```css
.section-black {
  background-color: #000000;
  color: #FFFFFF;
}
```

---

## 12. Design Principles untuk Redesign Masterclass

### DO:
1. Gunakan generous whitespace (100px section padding)
2. Centered layout untuk content utama (max-width 700px untuk text)
3. High-contrast typography (bold uppercase headings)
4. Alternating section backgrounds (white → light-gray → white → dark)
5. Pill-shaped CTA buttons dengan warna biru `#236CE4`
6. Icon circles dengan background biru untuk feature items
7. Clean, scannable hierarchy
8. Parallax/overlay sections untuk visual break
9. Konsisten dengan homepage aesthetic

### DON'T:
1. Jangan gunakan terlalu banyak warna — stick to the 3 primary colors
2. Jangan gunakan font selain Montserrat (headings) dan Open Sans (body)
3. Jangan buat section terlalu padat — breathing room is key
4. Jangan gunakan border-radius kecil untuk buttons (selalu pill/50px)
5. Jangan gunakan warna selain `#236CE4` untuk primary CTA
6. Jangan gunakan gambar tanpa overlay di dark sections

---

## 13. Assets & Resources

### Logo Files
- `Logo_ecollabo8_main.png` — Logo utama
- `logo-ecollabo8-blue.png` — Logo versi biru

### Icon Library
- Font Awesome (fa-stack, fa-circle, fa-inverse pattern)
- Icon size dalam circle: `fa-3x` (28px visual)

### Image Treatment
- Product images: high-quality, full-bleed
- Background images: dengan overlay `rgba(0,0,0,0.80)` atau `rgba(30,38,84,0.85)`
- Portfolio grid: square aspect ratio, hover scale `1.1`

---

## 14. Masterclass Page Content Structure (untuk Redesign)

### Sections yang perlu di-redesign:

1. **Hero** — Full-width, dark overlay, H1 + subtitle + CTA
2. **What This Program Delivers** — Centered intro + key value props
3. **Proof, Not Theory** — Stats/metrics dengan icon circles
4. **Why This Program Exists** — Story-driven, icon + text grid
5. **The Full Story** — Narrative section (dark bg)
6. **What This Opportunity Is** — 2-col feature highlight
7. **What You Will Learn** — 3-col curriculum (Market, Operations, Scale)
8. **Partnership (Conduit Impact)** — Trust/credibility section
9. **Program Structure** — 2 phases, timeline/card layout
10. **Outcome** — Dark bg, bullet list of deliverables
11. **Who This Is For** — 2-col target audience
12. **What Makes This Different** — 4-col differentiators
13. **Program Format** — Simple info (6 weeks, limited cohort)
14. **Video Section** — Embedded YouTube
15. **Apply/Form** — Application form + CTA

---

## 15. Implementation Notes

### Tech Stack
- **Approach**: Custom HTML/CSS Page Template (self-contained)
- **File**: `masterclass.html` — standalone file, bisa di-preview langsung di browser
- **Integration**: Paste ke WordPress via Custom HTML widget atau page template

### WordPress Integration Options

**Option A — Elementor Custom HTML Widget (Simplest)**
1. Edit halaman Masterclass di Elementor
2. Hapus semua existing widgets/sections
3. Tambah 1 widget "Custom HTML"
4. Paste seluruh isi `masterclass.html` (dari `<style>` sampai `</script>`)
5. Publish

**Option B — WordPress Page Template (Cleanest)**
1. Buat file `page-masterclass.php` di folder theme
2. Isi dengan custom template yang load HTML kita
3. Assign template ke halaman Masterclass
4. Ini menghindari conflict dengan theme CSS

**Option C — Custom Page via functions.php**
1. Enqueue custom CSS file terpisah
2. Load HTML via shortcode atau template part

### CSS Scoping
- Semua CSS di-scope via `.ec8-masterclass` prefix
- Tidak akan conflict dengan tema Newave existing
- Font di-load via Google Fonts CDN
- Icons via Font Awesome CDN

### File Structure
```
D:\laragon\www\ecollabo\
├── masterclass.html          ← Full page template (preview & integration)
├── design.md                 ← Design system documentation (this file)
├── program-overview.md       ← Program knowledge base
├── ECOLLABO8_BRAND_GUIDELINES.pdf
├── Logo_ecollabo8_main.png
└── logo-ecollabo8-blue.png
```

### Form Integration
- Form saat ini menggunakan HTML native
- Untuk WordPress, ganti dengan Contact Form 7 atau WPForms
- Atau gunakan form action ke Google Forms / webhook
- Class naming sudah disiapkan untuk easy mapping ke CF7 fields

### Catatan Penting
- CTA "Apply to ECOLLABO8 Masterclass" → link ke #program-overview section
- CTA "Program Overview" → link ke PDF/page terpisah (sesuaikan URL)
- CTA "Apply Now" dihilangkan sesuai instruksi
- Submit button: "REGISTER TO ECOLLABO8 MASTERCLASS"

---

*Document generated: May 2026*
*Based on: Brand Guidelines PDF, Homepage live analysis, CSS theme analysis*
