# FaqAccordion

Numbered FAQ section using native `<details>`/`<summary>` — no JavaScript required. Each row shows a zero-padded number, question text, and a CSS-only +/× icon that animates on open.

## Usage

```astro
---
import FaqAccordion from './FaqAccordion.astro';

const faqs = [
  { q: '¿Qué es este proyecto?', a: 'Una respuesta clara y concisa.' },
  { q: '¿Cómo puedo participar?', a: 'Descripción de cómo participar.' },
];
---

<FaqAccordion heading="Preguntas frecuentes" items={faqs} />
```

## Props

| Prop      | Type        | Default                    |
|-----------|-------------|----------------------------|
| `heading` | `string`    | `'Preguntas frecuentes'`   |
| `items`   | `FaqItem[]` | 3 placeholder items        |

```ts
interface FaqItem {
  q: string;  // question
  a: string;  // answer
}
```

## Required CSS variables

```css
:root {
  --color-bg: #f5f4f0;
  --color-ink: #1f1f1f;
  --color-green-muted: #97afa1;   /* number, question and icon color */
  --color-divider: #e0e0e0;       /* border between items */

  --font-body: 'YourFont', sans-serif;
  --weight-regular: 400;
  --weight-bold: 700;

  --leading-tight: 1.1;
  --leading-snug: 1.3;
  --leading-loose: 1.7;
  --text-base: 1rem;

  --space-5: 1.25rem;
  --space-10: 2.5rem;
  --space-16: 4rem;
  --space-20: 5rem;
  --space-24: 6rem;

  --gutter-mobile: 1rem;
  --gutter-tablet: 2rem;
  --gutter-desktop: 4rem;
  --container-wide: 1400px;

  --duration-fast: 150ms;
  --ease-default: ease;
}
```

## Notes

- Numbers are auto-generated (zero-padded) from the array index — no need to include them in the data.
- The +/× icon is pure CSS using `::before` / `::after` pseudoelements — no JS, no SVG.
- Answer text is indented to align with the question (not the number).
- The `<dl>` wrapper preserves semantic meaning for screen readers even though items are `<details>` internally.
