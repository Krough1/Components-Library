# Hero — Arch-bottom dark video hero

Full-viewport hero with a dark video background, a bottom arch cutout (using `border-radius`), a floating image that rises from the arch, and a centered text + CTA layer.

## Preview

```
┌─────────────────────────────────────┐
│           [logo]                    │
│        Heading text here            │
│        Subtext below heading        │
│     [Primary CTA]  [Outline CTA]    │
│                                     │
│   ╭─────────────────────────╮       │  ← dark arch bottom edge
│   │    [floating image]     │       │
└───┴─────────────────────────┴───────┘
```

## Usage

```astro
---
import Hero from './Hero.astro';
---

<Hero
  heading="Your headline goes here"
  subtext="Supporting subtext."
  ctaPrimary={{ label: 'Primary CTA', href: '#section' }}
  ctaOutline={{ label: 'Secondary CTA', href: '#other' }}
  logoSrc="/your-logo.png"
  logoAlt="Brand name"
  videoSrc="/your-video.mp4"
  floatSrc="/your-image.png"
  floatSrcMobile="/your-image-mobile.png"
/>
```

## Props

| Prop              | Type                        | Default                    |
|-------------------|-----------------------------|----------------------------|
| `heading`         | `string`                    | `'Your headline goes here'` |
| `subtext`         | `string`                    | `'Your supporting subtext goes here.'` |
| `ctaPrimary`      | `{ label, href }`           | `{ label: 'Primary CTA', href: '#' }` |
| `ctaOutline`      | `{ label, href }`           | `{ label: 'Secondary CTA', href: '#' }` |
| `logoSrc`         | `string`                    | `'/placeholder-logo.png'`  |
| `logoAlt`         | `string`                    | `'Logo'`                   |
| `videoSrc`        | `string`                    | `'/placeholder-video.mp4'` |
| `floatSrc`        | `string`                    | `'/placeholder-float.png'` |
| `floatSrcMobile`  | `string`                    | `'/placeholder-float-mobile.png'` |

## Required CSS variables

Define these in your global stylesheet before using this component:

```css
:root {
  /* Colors */
  --color-bg: #f5f4f0;          /* page background — must match for arch blend */
  --color-white: #ffffff;
  --color-ink: #1f1f1f;
  --color-green-dark: #3a4e42;  /* primary CTA hover */

  /* Typography */
  --font-display: 'YourDisplayFont', serif;
  --font-body: 'YourBodyFont', sans-serif;
  --weight-regular: 400;

  /* Spacing */
  --space-2: 0.5rem;
  --space-5: 1.25rem;
  --gutter-mobile: 1rem;
  --gutter-tablet: 2rem;
  --gutter-desktop: 4rem;
  --container-wide: 1400px;

  /* Typography scale */
  --text-base: 1rem;
  --leading-tight: 1.1;
  --tracking-tight: -0.02em;

  /* Transitions */
  --duration-fast: 150ms;
  --ease-default: ease;

  /* Misc */
  --radius-sm: 6px;
}
```

## Assets needed

| Asset | Description | Recommended size |
|-------|-------------|-----------------|
| Logo  | White/light version for dark background | SVG or PNG @2x |
| Video | Background loop, no audio | MP4, compressed, 1080p max |
| Float image (desktop) | PNG with transparent bg, anchored at bottom | ~1060px wide |
| Float image (mobile) | Wider crop of the float image | Full viewport width |

## Notes

- The arch effect is achieved with `border-radius: 0 0 50% 50% / 0 0 50vw 50vw` — the `50vw` vertical radius keeps it a perfect circle at all viewport sizes.
- `--color-bg` **must match** your page background color for the arch corners to blend seamlessly.
- The floating image sits outside the clipped `.hero__bg` container so it's never cut off by the arch.
- Autoplay fallback script handles browsers that block autoplay until user interaction.
