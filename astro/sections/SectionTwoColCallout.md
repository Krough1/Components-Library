# SectionTwoColCallout

Two-column section: dot-divider label, then large heading on the left and paragraphs + blockquote callout + CTA button on the right.

## Usage

```astro
---
import SectionTwoColCallout from './SectionTwoColCallout.astro';
---

<SectionTwoColCallout
  label="ACERCA DE LA PELÍCULA"
  heading="Una producción de escala internacional"
  paragraphs={[
    'Durante siglos, la Virgen de Guadalupe ha transformado corazones.',
    'La Tilma contará la historia sobrenatural y real del signo.',
  ]}
  callout={[
    'Este proyecto no comenzó como una iniciativa convencional.',
    'Hoy estamos en la fase más importante del desarrollo.',
  ]}
  ctaLabel="Conoce más sobre la producción"
  ctaHref="/nosotros"
/>
```

## Props

| Prop         | Type       | Default                         |
|--------------|------------|---------------------------------|
| `label`      | `string`   | `'ACERCA DE LA SECCIÓN'`        |
| `heading`    | `string`   | Placeholder heading             |
| `paragraphs` | `string[]` | 3 placeholder paragraphs        |
| `callout`    | `string[]` | 2 placeholder callout lines     |
| `ctaLabel`   | `string`   | `'Conoce más'`                  |
| `ctaHref`    | `string`   | `'#'`                           |

## Required CSS variables

Same as `SectionTwoCol` plus `--color-white`, `--space-6`, `--space-7`.
