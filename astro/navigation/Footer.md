# Footer

Dark background footer with brand column (logo + tagline + social icons), N navigation columns, and copyright line.

## Usage

```astro
---
import Footer from './Footer.astro';
---

<Footer
  logoSrc="/your-logo.png"
  logoAlt="Your Brand"
  brandName="BRAND"
  brandSub="studios"
  tagline="Your brand tagline goes here."
  columns={[
    { heading: 'PRODUCTO', links: [{ label: 'Features', href: '/features' }] },
    { heading: 'EMPRESA',  links: [{ label: 'Nosotros', href: '/nosotros' }] },
  ]}
  socials={[
    { label: 'Instagram', href: 'https://instagram.com/...', icon: 'instagram' },
    { label: 'YouTube',   href: 'https://youtube.com/...',   icon: 'youtube'   },
  ]}
  copyright="© 2025 Your Brand. All rights reserved."
/>
```

## Props

| Prop         | Type       | Default                              |
|--------------|------------|--------------------------------------|
| `logoSrc`    | `string`   | `'/placeholder-logo.png'`            |
| `logoAlt`    | `string`   | `'Logo'`                             |
| `brandName`  | `string`   | `'BRAND'`                            |
| `brandSub`   | `string`   | `'studios'`                          |
| `tagline`    | `string`   | `'Your brand tagline goes here.'`    |
| `columns`    | `NavCol[]` | 3 placeholder columns                |
| `socials`    | `Social[]` | Instagram, Facebook, YouTube         |
| `copyright`  | `string`   | Dynamic year copyright string        |

```ts
interface NavLink { label: string; href: string }
interface NavCol  { heading: string; links: NavLink[] }
interface Social  { label: string; href: string; icon: 'instagram' | 'facebook' | 'youtube' }
```

## Required CSS variables

```css
:root {
  --color-green-dark: #2a3d32;
  --color-bg: #f5f4f0;
  --color-green-muted: #97afa1;
  --color-white: #ffffff;

  --font-body: 'YourFont', sans-serif;
  --weight-bold: 700;
  --weight-regular: 400;

  --text-base: 1rem;
  --text-sm: 0.875rem;

  --tracking-wider: 0.1em;
  --tracking-wide: 0.05em;
  --leading-snug: 1.3;

  --space-2: 0.5rem;
  --space-3: 0.75rem;
  --space-5: 1.25rem;
  --space-8: 2rem;
  --space-10: 2.5rem;

  --gutter-mobile: 1rem;
  --gutter-tablet: 2rem;
  --gutter-desktop: 4rem;
  --container-wide: 1400px;

  --duration-fast: 150ms;
  --ease-default: ease;
}
```

## Notes

- Social icons are rendered inline from SVG — supported values: `'instagram'`, `'facebook'`, `'youtube'`.
- The `copyright` prop supports HTML via `set:html` — wrap `<a>` tags for links if needed.
- On mobile (≤767px) layout switches to 2 columns; brand column spans full width.
- On very small screens (≤479px) layout becomes 1 column.
