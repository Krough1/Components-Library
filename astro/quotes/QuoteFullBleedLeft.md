# QuoteFullBleedLeft

Full-bleed image section with a left-to-right gradient overlay. Quote and body text are anchored to the bottom-left. On mobile the gradient switches to bottom-to-top.

## Usage

```astro
---
import QuoteFullBleedLeft from './QuoteFullBleedLeft.astro';
---

<QuoteFullBleedLeft
  imageSrc="/your-image.jpg"
  quote="¿No estoy yo aquí, que soy tu Madre?"
  body="Mírame, hijo mío. No dejes que nada te aflija, pues te llevo en el hueco de mi manto."
/>
```

## Props

| Prop       | Type     | Default                          |
|------------|----------|----------------------------------|
| `imageSrc` | `string` | `'/placeholder-quote.jpg'`       |
| `quote`    | `string` | Placeholder quote text           |
| `body`     | `string` | Placeholder body text            |

## Required CSS variables

```css
:root {
  --color-white: #ffffff;
  --font-display: 'YourDisplayFont', serif;
  --font-body: 'YourFont', sans-serif;
  --weight-regular: 400;
  --leading-loose: 1.7;
  --space-6: 1.5rem;
  --space-10: 2.5rem;
  --space-24: 6rem;
  --gutter-mobile: 1rem;
  --gutter-tablet: 2rem;
  --gutter-desktop: 4rem;
  --container-wide: 1400px;
}
```
