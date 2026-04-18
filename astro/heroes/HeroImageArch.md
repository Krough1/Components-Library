# HeroImageArch

Light hero variant with arch-bottom cutout, image background, white gradient scrim, and dark text. Single CTA button.

## Usage

```astro
---
import HeroImageArch from './HeroImageArch.astro';
---

<HeroImageArch
  imageSrc="/your-hero-image.jpg"
  heading="Un llamado de Ella.<br />Un proyecto de todos."
  subtext="Guiados por el Espíritu Santo, y en comunión con la iglesia."
  ctaLabel="Descubre más"
  ctaHref="#historia"
/>
```

## Props

| Prop        | Type     | Default                                           |
|-------------|----------|---------------------------------------------------|
| `imageSrc`  | `string` | `'/placeholder-hero.jpg'`                         |
| `imageAlt`  | `string` | `''`                                              |
| `heading`   | `string` | `'Un llamado de Ella.<br />Un proyecto de todos.'`|
| `subtext`   | `string` | `'Guiados por el Espíritu Santo...'`              |
| `ctaLabel`  | `string` | `'Descubre más'`                                  |
| `ctaHref`   | `string` | `'#'`                                             |

The `heading` prop supports HTML (rendered via `set:html`) — use `<br />` for line breaks.

## Required CSS variables

```css
:root {
  --color-bg: #f5f4f0;
  --color-ink: #1f1f1f;
  --color-white: #ffffff;
  --color-green-muted: #97afa1;
  --color-green-dark: #2a3d32;

  --font-body: 'YourFont', sans-serif;
  --weight-bold: 700;
  --weight-regular: 400;

  --tracking-tight: -0.02em;
  --leading-tight: 1.1;

  --space-2: 0.5rem;
  --space-5: 1.25rem;

  --gutter-mobile: 1rem;
  --gutter-tablet: 2rem;
  --gutter-desktop: 4rem;

  --radius-sm: 8px;
  --duration-fast: 150ms;
  --ease-default: ease;
}
```

## Notes

- The arch shape is created with `border-radius: 0 0 50% 50% / 0 0 50vw 50vw` — the page `background-color` must match `--color-bg` for seamless blending.
- The white scrim fades from 90% opacity at top to transparent at 60%, keeping text legible over any image.
- Image is positioned `center 30%` by default to keep faces in frame.
