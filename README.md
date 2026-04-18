# Components Library

A personal collection of production-ready UI components extracted from real projects, organized by framework. Copy-paste ready — no build system or package manager required.

## Structure

```
/astro/
  heroes/       Hero section variants
  navigation/   Header and footer components
  accordions/   FAQ and accordion components
  quotes/       Full-bleed quote sections
  sections/     Content sections (two-column, ornament-text)
  bento/        Bento grid layouts
  cards/        Card components
  cta/          Call-to-action sections
  teams/        Team grid components
/react/
/vanilla/
```

Each component has its own `.astro` file + a `.md` file with props, CSS variables, assets needed, and a usage example.

## Components

### Astro — Heroes

| Component | Description |
|-----------|-------------|
| [HeroVideoArch](./astro/heroes/HeroVideoArch.astro) | Dark video background with arch-bottom cutout and floating image |
| [HeroImageArch](./astro/heroes/HeroImageArch.astro) | Light hero with arch-bottom cutout, image background, white scrim, dark text |

### Astro — Navigation

| Component | Description |
|-----------|-------------|
| [HeaderPill](./astro/navigation/HeaderPill.astro) | Floating pill header with scroll-aware show/hide + mobile hamburger menu |
| [Footer](./astro/navigation/Footer.astro) | Dark footer with brand column, nav columns, social icons, and copyright |

### Astro — Accordions

| Component | Description |
|-----------|-------------|
| [FaqAccordion](./astro/accordions/FaqAccordion.astro) | Numbered FAQ accordion using native `<details>` — no JavaScript |

### Astro — Quotes

| Component | Description |
|-----------|-------------|
| [QuoteFullBleedLeft](./astro/quotes/QuoteFullBleedLeft.astro) | Full-bleed image, gradient left overlay, quote + body at bottom-left |
| [QuoteFullBleedCenter](./astro/quotes/QuoteFullBleedCenter.astro) | Full-bleed image, multiply overlay, centered quote + attribution |

### Astro — Sections

| Component | Description |
|-----------|-------------|
| [SectionTwoCol](./astro/sections/SectionTwoCol.astro) | Dot-divider label + centered h2 + image/text two-column grid |
| [SectionTwoColCallout](./astro/sections/SectionTwoColCallout.astro) | Dot-divider label + large heading left + text/blockquote/CTA right |
| [SectionOrnamentText](./astro/sections/SectionOrnamentText.astro) | Centered ornament (flipped) + italic centered paragraphs |

### Astro — Bento

| Component | Description |
|-----------|-------------|
| [BentoGrid](./astro/bento/BentoGrid.astro) | 1-large + N-stacked bento card grid with cover images and optional logos bar |

### Astro — Cards

| Component | Description |
|-----------|-------------|
| [PillTopCards](./astro/cards/PillTopCards.astro) | Three arch-top cards with shared modal dialog, alternating colors, featured center card |

### Astro — CTA

| Component | Description |
|-----------|-------------|
| [CtaImageOverlay](./astro/cta/CtaImageOverlay.astro) | Background image + foreground overlay image + centered heading + CTA button |

### Astro — Teams

| Component | Description |
|-----------|-------------|
| [TeamGrid](./astro/teams/TeamGrid.astro) | Arch-top photo card grid with label, heading, italic subtext, callout, and optional editable first card |
