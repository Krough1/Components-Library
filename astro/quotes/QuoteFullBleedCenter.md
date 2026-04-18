# QuoteFullBleedCenter

Full-bleed image section with a solid multiply color overlay. Quote and attribution are centered both vertically and horizontally.

## Usage

```astro
---
import QuoteFullBleedCenter from './QuoteFullBleedCenter.astro';
---

<QuoteFullBleedCenter
  imageSrc="/your-image.jpg"
  quote='"Ten por cierto que te lo agradeceré y lo recompensaré bien."'
  attribution="— Virgen de Guadalupe · Nican Mopohua"
/>
```

## Props

| Prop            | Type     | Default                   |
|-----------------|----------|---------------------------|
| `imageSrc`      | `string` | `'/placeholder-quote.jpg'`|
| `quote`         | `string` | Placeholder quote text    |
| `attribution`   | `string` | Placeholder attribution   |

## Required CSS variables

```css
:root {
  --color-white: #ffffff;
  --color-green-dark: #2a3d32;   /* overlay color */
  --font-display: 'YourDisplayFont', serif;
  --font-body: 'YourFont', sans-serif;
  --weight-regular: 400;
  --leading-snug: 1.3;
  --space-5: 1.25rem;
  --space-24: 6rem;
  --gutter-mobile: 1rem;
  --gutter-tablet: 2rem;
  --gutter-desktop: 4rem;
  --container-wide: 1400px;
}
```

## Notes

- The overlay uses `mix-blend-mode: multiply` — the overlay color tints the image rather than covering it.
- To change the overlay color, update `--color-green-dark` or override `.quote-center__overlay { background-color: ... }`.
