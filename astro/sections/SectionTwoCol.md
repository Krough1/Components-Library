# SectionTwoCol

Two-column section: dot-divider section label, centered h2 with optional accent color, then an image column and text column side by side.

## Usage

```astro
---
import SectionTwoCol from './SectionTwoCol.astro';
---

<SectionTwoCol
  label="LA MISIÓN"
  heading="Llevar a Jesús a millones de hogares"
  headingAccent="a través de María"
  subheading="Un llamado urgente frente al 2031."
  paragraphs={[
    'Vivimos en un mundo desgastado por la división...',
    'Una madre dejó un mensaje que necesita ser escuchado de nuevo.',
  ]}
  imageSrc="/your-image.jpg"
  imageAlt="Descripción de la imagen"
/>
```

## Props

| Prop             | Type       | Default                          |
|------------------|------------|----------------------------------|
| `label`          | `string`   | `'LA SECCIÓN'`                   |
| `heading`        | `string`   | Placeholder heading              |
| `headingAccent`  | `string`   | `'a través de María'`            |
| `subheading`     | `string`   | Placeholder subheading           |
| `paragraphs`     | `string[]` | 3 placeholder paragraphs         |
| `imageSrc`       | `string`   | `'/placeholder-image.jpg'`       |
| `imageAlt`       | `string`   | `'Descripción de la imagen'`     |

`paragraphs` items support HTML via `set:html` — use `<strong>` for bold text.

## Required CSS variables

```css
:root {
  --color-bg: #f5f4f0;
  --color-ink: #1f1f1f;
  --color-green-muted: #97afa1;
  --color-green-mid: #5a7a68;
  --font-body: 'YourFont', sans-serif;
  --weight-bold: 700;
  --weight-regular: 400;
  --tracking-tight: -0.02em;
  --tracking-wider: 0.1em;
  --leading-tight: 1.1;
  --leading-loose: 1.7;
  --leading-snug: 1.3;
  --text-base: 1rem;
  --text-lg: 1.125rem;
  --space-4: 1rem;
  --space-5: 1.25rem;
  --space-8: 2rem;
  --space-10: 2.5rem;
  --space-12: 3rem;
  --space-16: 4rem;
  --space-20: 5rem;
  --space-24: 6rem;
  --gutter-mobile: 1rem;
  --gutter-tablet: 2rem;
  --gutter-desktop: 4rem;
  --container-wide: 1400px;
  --radius-sm: 8px;
}
```
