# 💻 Portfolio — Benjamin

> Developer's personal portfolio. Green terminal theme. Built with Astro + GitHub Pages.

[![Deploy](https://github.com/Ic3drago/Ic3drago.github.io/actions/workflows/deploy.yml/badge.svg)](https://github.com/Ic3drago/Ic3drago.github.io/actions/workflows/deploy.yml)
[![Astro](https://img.shields.io/badge/Astro-4.x-orange?logo=astro)](https://astro.build)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-deployed-brightgreen)](https://Ic3drago.github.io/)

**🌐 Live demo:** [https://Ic3drago.github.io](https://Ic3drago.github.io/)

---

## ✨ Features

- **Green Terminal Theme** — Hacker/retro aesthetic with monospaced fonts and scanline effects.
- **Clean Architecture** — Centralized data via `src/data/site.ts` (a single config file to edit everything).
- **5 Core Pages** — Home, Projects, About, Writing, Contact.
- **Auto-deploy** — GitHub Actions automatically deploys on every push to the `main` branch.
- **100% Static** — No backend, no database, zero hosting costs.
- **Mobile Responsive** — Fully optimized for mobile screens.

---

## 📁 Project Structure

```text
portfolio/
├── src/
│   ├── data/
│   │   └── site.ts          ← ⭐ EDIT HERE: personal info, projects, and posts
│   ├── layouts/
│   │   └── BaseLayout.astro ← Shared Header, Nav, Footer
│   ├── components/
│   │   └── ProjectCard.astro
│   ├── pages/
│   │   ├── index.astro      ← /home
│   │   ├── projects.astro   ← /projects
│   │   ├── about.astro      ← /about
│   │   ├── writing.astro    ← /writing
│   │   └── contact.astro    ← /contact
│   └── styles/
│       └── global.css
├── public/
│   └── avatar.jpg           ← Profile picture (replace it)
├── .github/
│   └── workflows/
│       └── deploy.yml       ← GitHub Pages CI/CD
├── astro.config.mjs
└── package.json
```

---

## 🚀 Deployment on GitHub Pages (Step-by-Step)

### 1. Clone and Setup

```bash
git clone https://github.com/Ic3drago/Ic3drago.github.io.git
cd Ic3drago.github.io
npm install
```

### 2. Edit Your Information

Open **`src/data/site.ts`** and modify the core variables:

```ts
export const siteConfig = {
  name: "Benjamin Avila Garcia",
  role: "Junior Developer // SecOps",
  email: "avilagarciabenjamin@gmail.com",
  socials: {
    github: "https://github.com/Ic3drago",
    // ...
  },
};
```

You can also update your projects and posts array in the same file.

### 3. Update `site` in astro.config.mjs

```js
export default defineConfig({
  site: "https://Ic3drago.github.io",
  base: "/", // ← root path for User Pages
});
```

### 4. Update Profile Picture

Replace `public/avatar.jpg` with your own photo (square, at least 200×200px).

### 5. Push to GitHub

```bash
git init
git add .
git commit -m "feat: init portfolio system"
git branch -M main
git remote add origin https://github.com/Ic3drago/Ic3drago.github.io.git
git push -u origin main
```

### 6. Enable GitHub Pages

1. Go to your repository → **Settings** → **Pages**
2. Under **Source**, select **GitHub Actions**
3. Wait ~2 minutes and your site will be live at:
   `https://Ic3drago.github.io/`

---

## 💻 Local Development

```bash
npm run dev      # Spin up local server at http://localhost:4321
npm run build    # Compile production build
npm run preview  # Preview production build locally
```

---

## 🛠️ Stack

| Tool                         | Usage                     |
| ---------------------------- | ------------------------- |
| [Astro](https://astro.build) | Static web framework      |
| TypeScript                   | Static typing             |
| CSS Variables                | Terminal theme styling    |
| GitHub Actions               | Automated CI/CD pipeline  |
| GitHub Pages                 | Free hosting              |

---

## 📄 License

MIT — Feel free to use this as a base for your own terminal portfolio.

---

_Built with ☕ and too much time staring at a green screen._
