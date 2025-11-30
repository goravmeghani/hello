# Cookie Jar Co. Website

## Overview
A minimal **React** application built with **Vite** and **Tailwind CSS** that serves as a template for a cookie‑shop website. The project demonstrates a clean component structure, modern tooling, and a ready‑to‑customize UI that includes a header, hero section, product listings, testimonials, and contact information.

---

## Features
- **React 18** with functional components and JSX.
- **Vite** fast dev server and optimized production builds.
- **Tailwind CSS** for utility‑first styling and a custom theme (brand colors, fonts).
- **ESLint** + **Prettier** for consistent code quality.
- Ready‑made layout: header, hero, cookie catalog, testimonials, contact form.
- Simple build pipeline – one command to get a production‑ready bundle.

---

## Tech Stack
| Layer | Technology |
|-------|------------|
| UI Framework | React (via `react` & `react-dom`)
| Build Tool | Vite (`vite`)
| Styling | Tailwind CSS (`tailwindcss`), PostCSS (`postcss`, `autoprefixer`)
| Linting | ESLint (`eslint`, `eslint-plugin-react`)
| Language | JavaScript (ES2020) & JSX |

---

## Project Structure
```
├─ .gitignore                # Git ignore rules
├─ index.html                # HTML entry point
├─ package.json              # npm scripts, dependencies
├─ postcss.config.js         # PostCSS plugins (Tailwind, Autoprefixer)
├─ tailwind.config.js        # Tailwind custom configuration
├─ vite.config.js            # Vite configuration (React plugin)
├─ README.md                 # This file
├─ USER_MANUAL.md            # End‑user manual
└─ src/                      # Source files
   ├─ App.jsx                # Main App component (UI layout)
   ├─ main.jsx               # React entry point (renders <App/>)
   ├─ index.css              # Global Tailwind imports
   └─ assets/…               # (optional) images, icons, etc.
```

---

## Installation
```bash
# Clone the repository
git clone https://github.com/your‑username/cookie-jar-co-website.git
cd cookie-jar-co-website

# Install dependencies (npm or yarn)
npm install   # or: yarn install
```

---

## Development
Start the hot‑reloading dev server:
```bash
npm run dev   # or: yarn dev
```
Open `http://localhost:5173` (or the URL shown in the console) to view the site. Changes to JSX or CSS are reflected instantly.

---

## Building for Production
Create an optimized static bundle:
```bash
npm run build   # or: yarn build
```
The output is placed in the `dist/` folder. You can preview it locally with:
```bash
npm run preview   # or: yarn preview
```

---

## Linting & Formatting
```bash
# Run ESLint
npm run lint   # or: yarn lint

# Auto‑fix lint errors
npm run lint:fix   # or: yarn lint:fix
```
The project is pre‑configured with sensible React/JSX rules.

---

## Key Files & Their Purpose
| File | Role |
|------|------|
| `src/App.jsx` | Main UI component – renders header, hero, product list, testimonials, contact section. |
| `src/main.jsx` | Boots the React app by mounting `<App/>` into `#root`. |
| `index.html` | Minimal HTML shell that loads the Vite bundle. |
| `tailwind.config.js` | Extends Tailwind with brand colors (`cookieBrown`, `cookieCream`) and custom fonts. |
| `vite.config.js` | Enables React fast refresh via `@vitejs/plugin-react`. |
| `postcss.config.js` | Sets up Tailwind and Autoprefixer processing. |
| `package.json` | Scripts, dependencies, and project metadata. |

---

## Scripts Overview (`package.json`)
| Script | Description |
|--------|-------------|
| `dev` | Starts Vite dev server. |
| `build` | Generates production assets. |
| `preview` | Serves the `dist/` folder locally. |
| `lint` | Runs ESLint in read‑only mode. |
| `lint:fix` | Runs ESLint with `--fix` to auto‑correct issues. |

---

## Contributing
1. Fork the repo.
2. Create a feature branch (`git checkout -b feature/awesome‑feature`).
3. Commit your changes with clear messages.
4. Open a Pull Request.

---

## License
This project is licensed under the **MIT License** – see the `LICENSE` file for details.

---

*Happy coding!*