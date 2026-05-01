# 💻 Portfolio — Benjamin

> Developer's personal portfolio. Green terminal theme. Built with Astro + Vercel.

[![Astro](https://img.shields.io/badge/Astro-4.x-orange?logo=astro)](https://astro.build)
[![Vercel](https://img.shields.io/badge/Vercel-deployed-black)](https://ic3drago-github-io.vercel.app/)

**🌐 Live demo:** [https://ic3drago-github-io.vercel.app](https://ic3drago-github-io.vercel.app/)

---

## ✨ Features

- **Green Terminal Theme** — Hacker/retro aesthetic with monospaced fonts and scanline effects.
- **Clean Architecture** — Centralized data via `src/data/site.ts` (a single config file to edit everything).
- **5 Core Pages** — Home, Projects, About, Writing, Contact.
- **Auto-deploy** — Vercel automatically deploys on every push to the `main` branch.
- **100% Static** — Fast, secure, zero-database architecture.
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
├── astro.config.mjs
└── package.json
```

---

## 🚀 Deployment on Vercel (Step-by-Step)

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
  site: "https://ic3drago-github-io.vercel.app",
  base: "/", // ← root path
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

### 6. Deploy to Vercel

1. Log in to [Vercel](https://vercel.com).
2. Click **Add New** → **Project**.
3. Import your GitHub repository (`Ic3drago.github.io`).
4. Vercel will automatically detect Astro. Click **Deploy**.
5. Wait ~1 minute and your site will be live at:
   `https://ic3drago-github-io.vercel.app`

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
| Vercel                       | CI/CD & Global CDN Hosting|

---

## 📄 License

MIT — Feel free to use this as a base for your own terminal portfolio.

---

_Built with ☕ and too much time staring at a green screen._
