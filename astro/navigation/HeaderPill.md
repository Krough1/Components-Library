# HeaderPill

Floating pill header with scroll-aware show/hide behavior. Hidden inside the hero section, slides in when scrolling up past the hero, hides when scrolling down. Mobile collapses to hamburger + full-screen overlay menu.

## Usage

```astro
---
import HeaderPill from './HeaderPill.astro';
---

<HeaderPill
  logoSrc="/your-logo.png"
  logoAlt="Your Brand"
  navLinks={[
    { label: 'Sección 1', href: '#section-1' },
    { label: 'Sección 2', href: '#section-2' },
    { label: 'Nosotros',  href: '/nosotros'  },
  ]}
  ctaLabel="Quiero ser parte"
  ctaHref="#cta"
/>
```

## Props

| Prop        | Type          | Default                        |
|-------------|---------------|--------------------------------|
| `logoSrc`   | `string`      | `'/placeholder-logo.png'`      |
| `logoAlt`   | `string`      | `'Logo'`                       |
| `navLinks`  | `NavLink[]`   | 3 placeholder links            |
| `ctaLabel`  | `string`      | `'Quiero ser parte'`           |
| `ctaHref`   | `string`      | `'#cta'`                       |

```ts
interface NavLink {
  label: string;
  href:  string;
}
```

## Required CSS variables

```css
:root {
  --color-ink: #1f1f1f;
  --color-white: #ffffff;
  --color-green-muted: #97afa1;

  --font-body: 'YourFont', sans-serif;
  --weight-regular: 400;

  --text-base: 1rem;
  --text-sm: 0.875rem;
  --text-2xl: 1.5rem;
  --text-lg: 1.125rem;
  --text-xl: 1.25rem;

  --tracking-wide: 0.05em;

  --radius-md: 12px;
  --radius-sm: 8px;

  --space-2: 0.5rem;
  --space-3: 0.75rem;
  --space-4: 1rem;
  --space-5: 1.25rem;
  --space-6: 1.5rem;
  --space-8: 2rem;

  --duration-base: 300ms;
  --duration-fast: 150ms;
  --ease-out: ease-out;
  --ease-default: ease;

  --z-sticky: 100;
  --z-modal: 200;
}
```

## Notes

- The header requires a `.hero` or `.hero-ns` element in the page — scroll hide/show is triggered relative to 85% of that element's height.
- On mobile (≤767px) the desktop nav and CTA button are hidden; the hamburger button appears instead.
- The mobile menu overlay uses `z-index: var(--z-modal)` — ensure this is above all other content.
- Escape key closes the mobile menu.
