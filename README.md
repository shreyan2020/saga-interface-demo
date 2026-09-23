# SAGA interface demo

A small Vue interface prototype for Qaring's SAGA concept. It lets a viewer select a healthcare scenario and inspect the corresponding card. The repository contains the interface, assets, and routing.

This is an early demo. Scenario descriptions are placeholders and the Play button is not connected to a journey player. There is no backend or AI generation pipeline in this repository.

## Run locally

```bash
npm ci
npm run dev
```

Open the URL printed by Vite. The home page introduces SAGA; `/demo` contains the scenario selector.

## Development

```bash
npm run type-check
npm run build
```

`npm run lint` applies fixes, and `npm run format` formats `src/`. The app uses Vue 3, TypeScript tooling, Vite, Bootstrap, and MDB Vue components.

The main components are [`HomeViewer.vue`](src/components/HomeViewer.vue), [`DemoViewer.vue`](src/components/DemoViewer.vue), and [`Dropdown.vue`](src/components/Dropdown.vue). Healthcare scenarios are demonstration content.
