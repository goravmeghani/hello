# Cookie Jar Co. Website – User Manual

## Table of Contents
1. [Introduction](#introduction)
2. [System Requirements](#system-requirements)
3. [Installation Guide](#installation-guide)
4. [Running the Application](#running-the-application)
5. [Navigating the Site](#navigating-the-site)
6. [Customization](#customization)
7. [Troubleshooting](#troubleshooting)
8. [FAQ](#faq)
9. [Support & Feedback](#support--feedback)

---

## Introduction
The **Cookie Jar Co.** website is a ready‑to‑use, responsive web page that showcases a bakery’s cookie products. It is built with React, Vite, and Tailwind CSS, providing a smooth development experience and a fast, modern user interface.

---

## System Requirements
| Requirement | Minimum |
|-------------|---------|
| Operating System | Windows 10 / macOS 10.15 / Linux |
| Node.js | v14.0 or newer (recommended: latest LTS) |
| npm or Yarn | v6.0+ |
| Browser | Chrome, Firefox, Edge, Safari (latest) |

---

## Installation Guide
1. **Download the project**
   ```bash
   git clone https://github.com/your-username/cookie-jar-co-website.git
   cd cookie-jar-co-website
   ```
2. **Install dependencies**
   ```bash
   npm install   # or: yarn install
   ```
3. **(Optional) Verify the installation**
   ```bash
   npm run lint   # should report no errors
   ```

> **Note:** The first install may take a few minutes as Vite pulls in the Vite, React, and Tailwind packages.

---

## Running the Application
### Development Mode
```bash
npm run dev   # or: yarn dev
```
- The dev server starts at `http://localhost:5173` (or the URL shown in the terminal).
- Hot Module Replacement (HMR) updates the page instantly when you edit source files.

### Production Preview
After building the site (see *Building for Production* in the README), you can preview the static bundle:
```bash
npm run preview   # or: yarn preview
```
The preview runs on `http://localhost:4173` by default.

---

## Navigating the Site
| Section | What You’ll See |
|---------|-----------------|
| **Header** | Brand logo, navigation links (Home, Products, Testimonials, Contact). |
| **Hero** | Large banner with a tagline and a call‑to‑action button. |
| **Cookie Listings** | Grid of cookie cards – each shows an image, name, short description, and price. |
| **Testimonials** | Carousel‑style quotes from happy customers. |
| **Contact** | Simple contact form (name, email, message) – currently a placeholder; you can hook it to a service like Formspree. |
| **Footer** | Copyright notice and social media icons. |

---

## Customization
### 1. Changing Content
- **Text** – Edit the JSX in `src/App.jsx`. Look for headings (`<h1>`, `<h2>`), paragraphs, and button labels.
- **Images** – Replace files in `src/assets/` (or create the folder) and update the `src` attributes in the JSX.
- **Products** – The cookie cards are hard‑coded in `App.jsx`. Convert them to a JSON array and map over it for easier maintenance.

### 2. Styling
- **Tailwind Theme** – Open `tailwind.config.js`. You’ll find a `theme.extend` section where custom colors (`cookieBrown`, `cookieCream`) and fonts are defined. Add or modify values as needed.
- **Global Styles** – `src/index.css` imports Tailwind’s base, components, and utilities. Add custom CSS rules after the Tailwind imports if you need bespoke styles.

### 3. Adding New Pages
1. Create a new component file, e.g., `src/About.jsx`.
2. Import it in `src/App.jsx` and add a route or conditional rendering (the current template uses a single‑page layout, but you can integrate `react-router-dom` for multi‑page navigation).

### 4. Deploying
- After `npm run build`, upload the contents of the `dist/` folder to any static‑hosting provider (Netlify, Vercel, GitHub Pages, Firebase Hosting, etc.). Follow the provider’s docs for a one‑click deploy.

---

## Troubleshooting
| Symptom | Possible Cause | Fix |
|---------|----------------|-----|
| **Dev server fails to start** | Node version too old or missing dependencies | Ensure Node ≥14 LTS and run `npm install` again. |
| **Styles look broken / missing** | Tailwind not processing CSS | Verify `postcss.config.js` includes `tailwindcss` and `autoprefixer`. Run `npm run dev` after a clean install. |
| **Console shows `Module not found` for a component** | Wrong import path (case‑sensitivity) | Check the file name and import statement; paths are case‑sensitive on Linux/macOS. |
| **Form submission does nothing** | Placeholder form – no backend configured | Connect the form to an endpoint (e.g., Formspree, Netlify Forms) or implement a custom API. |

---

## FAQ
**Q:** *Do I need to know React to modify the site?*  
**A:** Basic familiarity with JSX and component structure helps, but most changes (text, images, Tailwind colors) can be done without deep React knowledge.

**Q:** *Can I replace Tailwind with another CSS framework?*  
**A:** Yes. Remove Tailwind from `package.json`, delete the Tailwind config, and adjust `src/index.css` accordingly. Keep in mind you’ll lose the utility‑first classes used throughout the JSX.

**Q:** *How do I add analytics (e.g., Google Analytics)?*  
**A:** Insert the GA script tag into `index.html` before the closing `</head>` tag, or use a React hook that loads the script on mount.

---

## Support & Feedback
If you encounter issues or have suggestions:
- Open an **Issue** on the GitHub repository.
- Submit a **Pull Request** with your improvements.
- Contact the maintainer at `support@cookiejarco.com`.

---

*Enjoy customizing your Cookie Jar Co. website!*