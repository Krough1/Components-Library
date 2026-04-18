# TeamGrid

Team member grid with arch-top photo cards. Includes a dot-divider label, bold heading, italic subtext quote, bold callout, and a 4-column responsive grid. The first card optionally renders an editable text input for interactive "put your name here" experiences.

## Usage

```astro
---
import TeamGrid from './TeamGrid.astro';
---

<TeamGrid
  label="EL PROYECTO"
  heading="Los Juan Diegos"
  subtext='"Ella no busca a los más sabios, sino a los que tienen fuego en el corazón".'
  callout="Detrás de este proyecto hay profesionales unidos por una misión y un llamado."
  members={[
    { name: 'Escribe tu nombre aquí', title: 'Equipo Fundador', photo: '/member-placeholder.jpg' },
    { name: 'Ana García',  title: 'Dirección Creativa',  photo: '/ana.jpg' },
    { name: 'Carlos Ruiz', title: 'Producción',          photo: '/carlos.jpg' },
  ]}
  editableFirstCard={true}
/>
```

## Props

| Prop                | Type       | Default                             |
|---------------------|------------|-------------------------------------|
| `label`             | `string`   | `'EL PROYECTO'`                     |
| `heading`           | `string`   | `'El Equipo'`                       |
| `subtext`           | `string`   | Placeholder italic quote            |
| `callout`           | `string`   | Placeholder bold callout            |
| `members`           | `Member[]` | 4 placeholder members               |
| `editableFirstCard` | `boolean`  | `true`                              |

```ts
interface Member {
  name:   string;
  title:  string;
  photo:  string;
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
  --font-body: 'YourFont', sans-serif;
  --weight-bold: 700;
  --weight-regular: 400;
  --tracking-tight: -0.02em;
  --leading-tight: 1.1;
  --leading-snug: 1.3;
  --text-base: 1rem;
  --space-5: 1.25rem;
  --space-10: 2.5rem;
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

- Set `editableFirstCard={false}` to render all cards as static.
- The editable input matches the bold name typography exactly — users type their name and it appears styled.
- Grid is 4 columns desktop → 2 columns tablet/mobile.
- Photo aspect ratio is `3/4` with arch-top (`border-radius: 500px 500px 20px 20px`).
