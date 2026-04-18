# BentoGrid

Bento-style card grid: one large card on the left and N stacked cards on the right. Optional logos/CTA bar below. Cards use cover images with gradient overlays.

## Usage

```astro
---
import BentoGrid from './BentoGrid.astro';
---

<BentoGrid
  label="LA INICIATIVA"
  heading="¿Cómo vamos a hacerlo?"
  cards={[
    {
      eyebrow:  'La película',
      title:    'La Tilma',
      desc:     'Una producción de escala internacional.',
      imageSrc: '/card-1.jpg',
    },
    {
      eyebrow:  'La plataforma',
      desc:     'Un ecosistema digital para conectar creyentes.',
      imageSrc: '/card-2.jpg',
    },
    {
      eyebrow:  'La comunidad',
      desc:     'Un movimiento vivo de testimonios.',
      imageSrc: '/card-3.jpg',
    },
  ]}
  logosBar={{
    left:        [{ src: '/logo-a.png', alt: 'Logo A' }],
    ctaEyebrow:  'TÚ TAMBIÉN PUEDES',
    ctaTitle:    'SER PARTE',
    ctaLabel:    'Descubre cómo',
    ctaHref:     '#',
    right:       [{ src: '/logo-b.png', alt: 'Logo B' }],
  }}
/>
```

## Props

| Prop       | Type           | Default                  |
|------------|----------------|--------------------------|
| `label`    | `string`       | `'LA INICIATIVA'`        |
| `heading`  | `string`       | Placeholder heading      |
| `cards`    | `BentoCard[]`  | 3 placeholder cards      |
| `logosBar` | `LogosBar?`    | Placeholder logos bar    |

```ts
interface BentoCard {
  eyebrow:  string;
  title?:   string;  // only shown if provided
  desc:     string;
  imageSrc: string;
}

interface LogosBar {
  left?:       { src: string; alt: string }[];
  ctaEyebrow?: string;
  ctaTitle?:   string;
  ctaLabel?:   string;
  ctaHref?:    string;
  right?:      { src: string; alt: string }[];
}
```

## Required CSS variables

```css
:root {
  --color-bg: #f5f4f0;
  --color-ink: #1f1f1f;
  --color-white: #ffffff;
  --color-green-muted: #97afa1;
  --color-green-dark: #2a3d32;
  --color-green-mid: #5a7a68;
  --color-divider: #e0e0e0;
  --font-body: 'YourFont', sans-serif;
  --weight-bold: 700;
  --weight-regular: 400;
  --tracking-tight: -0.02em;
  --tracking-wider: 0.1em;
  --tracking-wide: 0.05em;
  --leading-tight: 1.1;
  --leading-snug: 1.3;
  --text-base: 1rem;
  --text-lg: 1.125rem;
  --space-2: 0.5rem;
  --space-3: 0.75rem;
  --space-4: 1rem;
  --space-5: 1.25rem;
  --space-6: 1.5rem;
  --space-8: 2rem;
  --space-10: 2.5rem;
  --space-16: 4rem;
  --space-20: 5rem;
  --gutter-mobile: 1rem;
  --gutter-tablet: 2rem;
  --gutter-desktop: 4rem;
  --container-wide: 1400px;
  --radius-sm: 8px;
  --duration-fast: 150ms;
  --ease-default: ease;
}
```

## Notes

- The first card in `cards[]` is always rendered as the large left card; remaining cards are stacked on the right.
- Pass `logosBar: undefined` (or omit it) to hide the logos bar entirely.
- On mobile (≤767px) the grid switches to a single column and each card gets `min-height: 420px`.
