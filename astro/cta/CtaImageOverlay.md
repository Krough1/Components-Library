# CtaImageOverlay

CTA section with a full-width background image that drives the section height, a foreground overlay image positioned above it, and centered text + button anchored at the bottom.

## Usage

```astro
---
import CtaImageOverlay from './CtaImageOverlay.astro';
---

<CtaImageOverlay
  backgroundSrc="/back-circle-rectangle.png"
  overlaySrc="/section-kid.png"
  overlayAlt="Padre e hijo peregrinos"
  heading="Tu puedes hacer esto posible"
  subtext="Este es el proyecto de María ¿Cuál es tu respuesta?"
  body="No camines solo. Te invito a poner tu corazón en este proyecto."
  ctaLabel="DONAR"
  ctaHref="#donar"
/>
```

## Props

| Prop             | Type     | Default                          |
|------------------|----------|----------------------------------|
| `backgroundSrc`  | `string` | `'/placeholder-bg.png'`          |
| `overlaySrc`     | `string` | `'/placeholder-overlay.png'`     |
| `overlayAlt`     | `string` | `''`                             |
| `heading`        | `string` | `'Tu puedes hacer esto posible'` |
| `subtext`        | `string` | Placeholder subtext              |
| `body`           | `string` | Placeholder body text            |
| `ctaLabel`       | `string` | `'DONAR'`                        |
| `ctaHref`        | `string` | `'#'`                            |

## Required CSS variables

```css
:root {
  --color-bg: #f5f4f0;
  --color-white: #ffffff;
  --color-ink: #1f1f1f;
  --color-green-muted: #97afa1;
  --font-display: 'YourDisplayFont', serif;
  --font-body: 'YourFont', sans-serif;
  --weight-bold: 700;
  --weight-regular: 400;
  --tracking-wide: 0.05em;
  --space-2: 0.5rem;
  --space-3: 0.75rem;
  --space-4: 1rem;
  --space-5: 1.25rem;
  --space-6: 1.5rem;
  --space-16: 4rem;
  --radius-sm: 8px;
  --duration-fast: 150ms;
  --ease-default: ease;
}
```

## Notes

- The background image drives the section height — it should be a full-width decorative shape (e.g., circle + rectangle).
- The overlay image is positioned at `left: 50%; transform: translateX(-20%)` to sit slightly right of center.
- On mobile (≤767px) the `body` paragraph is hidden to keep the layout clean.
- The overlay image shrinks from 55% to 45% height on mobile.
