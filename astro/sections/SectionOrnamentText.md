# SectionOrnamentText

Minimal section: a centered decorative ornament image (flipped vertically) followed by centered italic paragraphs. No heading — used for reflective or quote-style copy blocks.

## Usage

```astro
---
import SectionOrnamentText from './SectionOrnamentText.astro';
---

<SectionOrnamentText
  ornamentSrc="/your-ornament.png"
  paragraphs={[
    'Guadalupe 2031 es un proyecto sin fines de lucro, nacido de la fe.',
    'Lo que inició como una inquietud en el corazón, desencadenó un movimiento.',
  ]}
/>
```

## Props

| Prop           | Type       | Default                            |
|----------------|------------|------------------------------------|
| `ornamentSrc`  | `string`   | `'/placeholder-ornament.png'`      |
| `paragraphs`   | `string[]` | 3 placeholder paragraphs           |

`paragraphs` items support HTML via `set:html`.

## Required CSS variables

```css
:root {
  --color-bg: #f5f4f0;
  --color-ink: #1f1f1f;
  --font-body: 'YourFont', sans-serif;
  --weight-regular: 400;
  --space-6: 1.5rem;
  --space-10: 2.5rem;
  --space-24: 6rem;
  --gutter-mobile: 1rem;
  --gutter-tablet: 2rem;
  --gutter-desktop: 4rem;
  --container-wide: 1400px;
}
```

## Notes

- The ornament image is flipped vertically via `transform: scaleY(-1)` — ensure the image is oriented correctly before applying this transform.
- Text max-width is capped at 650px for readability.
