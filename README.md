# Components Library

A personal collection of production-ready UI components extracted from real projects, organized by framework. Copy-paste ready — no build system or package manager required.

## Structure

```
/astro/
  heroes/       Hero section variants
  accordions/   FAQ and accordion components
  modals/       Modal / dialog components
  cards/        Card components
/react/
/vanilla/
```

Each component has its own `.astro` file + a `.md` file with props, CSS variables, assets needed, and a usage example.

## Components

### Astro — Heroes

| Component | Description |
|-----------|-------------|
| [HeroVideoArch](./astro/heroes/HeroVideoArch.astro) | Dark video background with arch-bottom cutout and floating image |

### Astro — Accordions

| Component | Description |
|-----------|-------------|
| [FaqAccordion](./astro/accordions/FaqAccordion.astro) | Numbered FAQ accordion using native `<details>` — no JavaScript |
