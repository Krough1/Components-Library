# PillTopCards

Three pill-top (arch-top) cards with a shared modal. The middle card is "featured" with a taller image. All card buttons open a single dialog modal with an image, heading, body text, and a CTA link.

## Usage

```astro
---
import PillTopCards from './PillTopCards.astro';
---

<PillTopCards
  heading="¿Y tú cómo quieres ser parte?"
  subtitle="Elige la forma en que sientes el llamado."
  cards={[
    { title: 'Consagra tu hogar', desc: '...', imageSrc: '/card-1.jpg', imageAlt: '...', btnLabel: 'Consagrar mi hogar' },
    { title: 'Haz una donación',  desc: '...', imageSrc: '/card-2.jpg', imageAlt: '...', btnLabel: 'Quiero donar', featured: true },
    { title: 'Sé voluntario',     desc: '...', imageSrc: '/card-3.jpg', imageAlt: '...', btnLabel: 'Ser voluntario' },
  ]}
  quote='"Ella llegó hace 500 años con un mensaje para todos."'
  modalImageSrc="/modal-image.jpg"
  modalHeading="¡Gracias por tu interés!"
  modalText="Estamos trabajando en esto. Regístrate antes que nadie."
  modalCtaLabel="Regístrarme"
  modalCtaHref="https://forms.example.com/..."
/>
```

## Props

| Prop              | Type      | Default                        |
|-------------------|-----------|--------------------------------|
| `heading`         | `string`  | Placeholder heading            |
| `subtitle`        | `string`  | Placeholder subtitle           |
| `cards`           | `Card[]`  | 3 placeholder cards            |
| `quote`           | `string`  | Placeholder closing quote      |
| `modalImageSrc`   | `string`  | `'/placeholder-modal.jpg'`     |
| `modalHeading`    | `string`  | `'¡Gracias por tu interés!'`   |
| `modalText`       | `string`  | Placeholder modal text         |
| `modalCtaLabel`   | `string`  | `'Regístrarme'`                |
| `modalCtaHref`    | `string`  | `'#'`                          |

```ts
interface Card {
  title:    string;
  desc:     string;
  imageSrc: string;
  imageAlt: string;
  btnLabel: string;
  featured?: boolean;  // taller image
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
  --font-display: 'YourDisplayFont', serif;
  --font-body: 'YourFont', sans-serif;
  --weight-bold: 700;
  --weight-regular: 400;
  --tracking-tight: -0.02em;
  --leading-tight: 1.1;
  --leading-snug: 1.3;
  --text-base: 1rem;
  --space-2: 0.5rem;
  --space-5: 1.25rem;
  --space-12: 3rem;
  --space-16: 4rem;
  --space-20: 5rem;
  --space-24: 6rem;
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

- The modal uses the native `<dialog>` element — no JS library required.
- Clicking the backdrop (outside `.pc-modal__card`) closes the modal.
- The Escape key closes the modal automatically (native `<dialog>` behavior).
- All buttons with class `.js-open-modal` trigger the same modal.
- Card color alternates: odd-indexed (0, 2) → `card--muted` (green-muted), even-indexed (1) → `card--dark` (green-dark).
