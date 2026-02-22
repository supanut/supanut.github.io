# Supanut's Personal Website

![Nuxt 4](https://img.shields.io/badge/Nuxt-4.0.0-00DC82?logo=nuxt.js&logoColor=white)
![Vue 3](https://img.shields.io/badge/Vue.js-3.5.0-4FC08D?logo=vuedotjs&logoColor=white)
![Nuxt UI v3](https://img.shields.io/badge/Nuxt_UI-v3_Alpha-00DC82?logo=nuxt.js&logoColor=white)
![Tailwind CSS v4](https://img.shields.io/badge/Tailwind_CSS-v4-38B2AC?logo=tailwind-css&logoColor=white)
![Bun](https://img.shields.io/badge/Bun-%23000000.svg?style=for-the-badge&logo=bun&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white)

> A blazing fast, modern, and statically generated personal portfolio and blog built with the cutting-edge Nuxt 4 ecosystem.

This repository (`supanut.github.io`) contains the source code and GitHub Actions deployment pipeline for my personal website. It has been meticulously bootstrapped to embrace the latest advancements in the Vue/Nuxt ecosystem, utilizing `bun` for package management and Nitro for optimal static site generation (SSG).

## 🚀 Architecture & Technical Stack

The architecture of this application is deliberately kept minimal yet extremely powerful to serve static content dynamically via GitHub Pages.

*   **Framework**: [Nuxt 4](https://nuxt.com/) (running in strict compatibility mode).
*   **UI Library**: [Nuxt UI v3 (Alpha)](https://ui3.nuxt.dev/) - providing beautifully crafted, accessible components based on Headless UI and specialized for Vue.
*   **Styling**: [Tailwind CSS v4](https://tailwindcss.com/) - integrated directly through Nuxt UI for rapid UI development and atomic CSS generation.
*   **Package Manager & Runtime**: [Bun](https://bun.sh/) - replacing standard Node/npm for lightning-fast dependency resolution and script execution.
*   **Hosting & CI/CD**: [GitHub Pages](https://pages.github.com/) & [GitHub Actions](https://github.com/features/actions) - entirely bypassing Jekyll for a pure statically generated Vue application.

## 🛠️ Local Development

To run this project locally, ensure you have [Bun](https://bun.sh/) installed on your machine.

### 1. Clone the repository

```bash
git clone https://github.com/supanut/supanut.github.io.git
cd supanut.github.io
```

### 2. Install dependencies

```bash
bun install
```

### 3. Start the development server

```bash
bun run dev
```

The application will now be running at `http://localhost:3000`. Hot Module Replacement (HMR) is enabled by default.

## 🏗️ Build & Deployment

This project relies on continuous deployment via GitHub Actions. We do **not** use the legacy GitHub Pages branch (e.g., `gh-pages`) or Jekyll.

### Static Site Generation (SSG)

To manually build the application for production and output raw static HTML files into the `.output/public` directory:

```bash
bun run generate
```

You can preview the generated static site locally using a minimal HTTP server:

```bash
npx serve .output/public
```

### GitHub Actions Pipeline

The deployment process is automated whenever code is pushed to the `main` branch. 

Check `.github/workflows/deploy.yml` for the CI/CD pipeline logic. The pipeline executes the following sequence:
1.  Checkouts the code.
2.  Sets up Node 20 and Bun.
3.  Installs dependencies (`bun install`).
4.  Generates the static build (`bun run generate`). Nitro will automatically create a `.nojekyll` file.
5.  Uploads the `.output/public` artifact directly to GitHub's internal Pages server.

### GitHub Repository Settings

For the deployment architecture to work, the repository settings must be configured correctly:
1.  Navigate to **Settings** > **Pages**.
2.  Under **Build and deployment** -> **Source**, ensure it is set to **GitHub Actions**.

## 🌲 Directory Structure

```text
.
├── .github/
│   └── workflows/
│       └── deploy.yml      # CI/CD instructions for GitHub Actions
├── public/                 # Static assets (images, favicon, etc.)
├── server/                 # Nitro server api routes (if required)
├── app.vue                 # Main application entry component
├── nuxt.config.ts          # Core Nuxt 4 configuration (modules, compatibility)
├── package.json            # Scripts & dependencies
└── bun.lockb               # Bun state dependency lockfile
```

## 📜 License

[MIT License](LICENSE) (or proprietary, specify accordingly).

---
*“Talk is cheap. Show me the code.”* — Linus Torvalds
