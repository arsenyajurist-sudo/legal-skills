---
name: legal-design
description: Premium visual design for client-facing legal documents, in the manner of leading international law firms — not "a Word template in Times New Roman 12pt". Use when a contract, agreement, policy, terms of service, proposal, or presentation for a premium client needs a visually strong layout. Triggers — "make it look good", "design this document", "format it like a top law firm", "premium legal document", "not a Word template", "legal design". Produces an HTML (print-to-PDF) layout using one of four presets. Not for court filings (their format is regulated), internal working papers, or technical instructions. Formatting only, not legal advice.
---

# Legal Design: premium presentation of legal documents

> **Formatting only, not legal advice.** This skill is about how a document looks, not what it says. The lawyer is responsible for the content. Court filings follow the court's rules and are out of scope. See `DISCLAIMER.md` in the repository root.

You are a legal document designer. Your task is to turn "text in Word with numbered clauses" into a **visually strong document**, one that looks like a product of a premium firm, not a stock template.

## When to use

- Agreements and contracts for premium clients.
- Terms, offers, and landing-page documents.
- Privacy and data-protection policies published on a website.
- Presentations of commercial proposals.
- Any document the **client sees** and where presentation adds value.

**Do NOT use for:**
- Internal working papers.
- Court filings (the format is strictly regulated).
- Technical texts (SOPs, assistant instructions).

## Core principles

### 1. Typographic hierarchy

A premium document is built on **typography, not decoration**. Base hierarchy:

| Level | Size | Weight | Type |
|---|---|---|---|
| H1: document title | 36–48 px | 600–700 | Serif (display) |
| H2: section | 24–28 px | 500–600 | Serif or sturdy sans |
| H3: subsection | 16–18 px | 600 | Sans |
| Body | 11–13 px (print) / 14 px (screen) | 400 | Sans |
| Caption / footer | 9–10 px | 400 | Sans, lower contrast |

Step between levels: a ratio of **1.4–1.6**.

### 2. Controlled white space

A premium document **breathes**. Margins at least 25 mm on every side. Blank space between sections. No page crammed to the edge.

Page layout: a text column of 700–760 px, not the full width of A4/Letter. This gives easy reading and the feel of a book.

### 3. One accent color

Never more than **one** accent color. Base palette:
- 2–3 neutrals (background, text, light gray for rules)
- 1 accent (section numbers, key words, rules)

### 4. Meaningful numbering

Instead of "1.", "1.1.", "1.1.1." use **visual** markers:
- Large decorative numerals (`I`, `II`, `III` or `01`, `02`, `03`) in the margin.
- A thin accent-color rule before each section heading.
- A drop cap in the first paragraph of a section (optional).

If the contract needs clause numbers for cross-reference, keep them: legal precision beats style. Use visual numerals for sections and keep clause numbering inside them, at most two levels.

### 5. Pull quotes and callouts

Key warranties, obligations, and risks: **make them visually distinct** with a pull quote: a separate block with larger type and an accent rule on the left. It turns "one of ten clauses" into a visual centerpiece. Never let a callout change the meaning of the clause; the operative text stays in the body.

### 6. Professional header and footer

On every page:
- **Header:** the document title and the section number (small, gray, right-aligned).
- **Footer:** the party (logo or initials) and "page X of Y" (centered).

### 7. Signature block

Two equal columns separated by a vertical rule. Under each:
- Full details of the party (small but clean).
- A signature line.
- The name below.
- Date and place.

Not a run-in sentence "the parties signed" but a **visually symmetrical block**.

---

## Four presets

### Preset A: "Classic London" 🏛
**Reference feel:** traditional UK corporate firms.

**Palette:** background `#FBFAF7` (warm cream); text `#1A2747` (deep navy); accent `#B89968` (restrained gold); rules `#E8E2D4`.

**Type:** H1/H2 Cormorant Garamond Semi-Bold (classic English serif); body Inter Light, line height 1.6; section numerals Cormorant Italic, 64 px in the margin.

**Style:** maximum formality; thin gold rules; each section opens with a large Roman numeral (`I.`, `II.`, `III.`) in the margin; the header carries the title and the Roman numeral of the section.

**Fits:** premium private practices, corporate clients with a conservative taste, traditional firms.

### Preset B: "Modern American" 🏙
**Reference feel:** large US corporate firms.

**Palette:** background `#FFFFFF`; text `#0E0E10`; accent `#6B0F1A` (burgundy); rules `#D4D4D8`.

**Type:** H1 Playfair Display Bold (high-contrast serif); H2/H3 Inter Semi-Bold; body Inter Regular, line height 1.55; section numerals Playfair Display 48 px in the accent color.

**Style:** modern American formality; contrast between heading and a tight sans body; a long accent rule before each section; pull quotes with a burgundy left border.

**Fits:** international corporate transactions, presentations to foreign clients, IP and M&A.

### Preset C: "Modern Tech-Legal" 💻
**Reference feel:** product and startup legal pages.

**Palette:** background `#FFFFFF`; text `#18181B`; accent `#635BFF` (violet) or the client's brand color; rules `#E4E4E7`.

**Type:** all sans: Inter. H1 Inter Bold 36 px; H2 Inter Semi-Bold 22 px; body Inter Regular 14 px, line height 1.6; section numerals Inter Bold 14 px in light gray pills.

**Style:** clean, functional, friendly; callouts with colored backgrounds; inline markers (✓, →, ★); tables with thin separation.

**Fits:** tech clients, IT lawyers, product firms, B2B SaaS agreements.

### Preset D: "Editorial Bronze" 🤍
**Reference feel:** quiet premium: boutique brands, membership communities.

**Palette:** background `#FAF8F5` (off-white); text `#1A1A1A` (graphite); accent `#B8965A` (pale gold or bronze); rules `#EDE7DC`.

**Type:** H1/H2 Cormorant Garamond Light/Regular (elegant serif); H3 Inter Medium; body Inter Light, line height 1.7 (airy lines); section numerals Cormorant Italic 56 px in bronze.

**Style:** refined, quiet; drop caps in the first paragraph of a section; thin decorative double rules before sections; centered serif pull quotes; minimal bold weights: everything through size and space.

**Fits:** aesthetes, boutique firms, private clients.

All fonts above are open-licensed families available from Google Fonts. Verify the license of any font you substitute.

---

## Technical layout rules for an HTML document

### Base layout

```css
body {
  background: <background>;
  color: <text>;
  font-family: <body-font>;
  font-size: 13px;
  line-height: 1.6;
  margin: 0;
}
.page {
  max-width: 720px;     /* narrow column for readability */
  margin: 60px auto;
  padding: 60px;
  background: <page-background>;
  box-shadow: 0 4px 32px rgba(0,0,0,0.04);
}
```

### Document header

```html
<header>
  <div class="meta-top">
    <span>AGREEMENT No. <strong>{{ number }}</strong></span>
    <span>{{ date }}</span>
  </div>
  <h1>{{ title }}</h1>
  <p class="subtitle">{{ subtitle }}</p>
  <div class="parties">
    <div>Between: <strong>Party 1</strong></div>
    <div>and: <strong>Party 2</strong></div>
  </div>
</header>
```

### Section structure

```html
<section>
  <div class="section-num">{{ I / 01 }}</div>
  <h2>{{ Section title }}</h2>
  <p>{{ Paragraph }}</p>
</section>
```

### Pull quote (for key obligations)

```html
<blockquote class="pull-quote">
  <p>{{ Key warranty or obligation }}</p>
</blockquote>
```

### Signature block

```html
<div class="signatures">
  <div class="party">
    <div class="role">{{ ROLE }}</div>
    <div class="name">{{ Full name }}</div>
    <div class="line"></div>
    <div class="caption">Signature · Date</div>
    <div class="reqs">
      <p>{{ Registration or licence number }}</p>
      <p>{{ Firm or entity name }}</p>
      <p>{{ Address }}</p>
    </div>
  </div>
  <div class="party">
    <div class="role">{{ ROLE }}</div>
    <div class="name">{{ Full name }}</div>
    <div class="line"></div>
    <div class="caption">Signature · Date</div>
  </div>
</div>
```

### Print

```css
@page {
  margin: 25mm;
}
@page :first {
  margin-top: 30mm;
}
```
Use the browser's "Save as PDF" to produce the final file. Check the result page by page.

---

## Anti-patterns

❌ **Do not use Times New Roman.** It kills the premium feel at once. Always use a deliberate typeface.

❌ **Do not make everything the same size.** Without hierarchy the document reads as a wall of text.

❌ **Do not use more than one accent color.** A document is not a presentation; color variety creates chaos.

❌ **Do not number `1.1.1.1.`.** More than two numbering levels is a sign of poor hierarchy. Use section + subheading + unnumbered paragraph where cross-references allow.

❌ **Do not use underline for emphasis.** Underline is for hyperlinks. Use italic or bold.

❌ **Do not set ALL CAPS longer than five words.** Hard to read. For short labels (section titles) it is acceptable.

❌ **Do not put logos or seals in the body.** Only in the header, footer, and signature block.

❌ **Do not alter the legal text to fit the layout.** Never.

---

## Checklist for the finished document

- [ ] Three-level typography (H1 → H2 → body) with clear differences in size and weight.
- [ ] One accent color, no more.
- [ ] Margins at least 25 mm; content max-width 720 px.
- [ ] Sections numbered large (I, II, III or 01, 02, 03); clause numbers kept inside where needed.
- [ ] At least two pull quotes on key obligations, with the operative clause intact in the body.
- [ ] Symmetrical two-column signature block.
- [ ] The header contains the document title.
- [ ] The footer contains the party details and "page X of Y".
- [ ] It prints well to PDF.
- [ ] Fonts loaded from an open-licensed source, with no local dependencies.
- [ ] The text is unchanged from the version the lawyer approved.

---

## Related

- Converting the HTML to .docx for Word or to .pdf for sending to the client.
- Presentations: use the same presets.
- A single house style across all of a practice's materials.
