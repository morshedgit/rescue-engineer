# Vibe Code Rescue & Fractional Engineering

> Turn AI-built prototypes (Cursor, Lovable, Bolt, Replit, v0) into secure, scalable, production-ready software.

[![Built with Astro](https://img.shields.io/badge/Built%20with-Astro%207-BC52EE.svg)](https://astro.build)
[![Tailwind CSS v4](https://img.shields.io/badge/Tailwind-v4.0-38BDF8.svg)](https://tailwindcss.com)
[![Deployed on Cloudflare Pages](https://img.shields.io/badge/Hosted%20on-Cloudflare%20Pages-F38020.svg)](https://pages.cloudflare.com)

---

## 🎯 Overview

This repository powers the landing page for **Vibe Code Rescue**, a specialized fractional engineering consultancy helping non-technical founders, operators, and creators whose AI-generated applications hit the "Vibe Coding Wall" (security breaches, open database tables, broken payments, and unbuildable deployments).

See the full product specifications in [`docs/PRDs/vibe_code_rescue_landing_page.md`](file:///users/sadeq/projects/rescue-engineer/docs/PRDs/vibe_code_rescue_landing_page.md).

---

## 🛠️ Architecture & Tech Stack

* **Framework**: [Astro 7](https://astro.build) — Generates zero-JS static HTML by default for sub-second load times.
* **Styling**: [Tailwind CSS v4](https://tailwindcss.com) via `@tailwindcss/vite` with custom glassmorphism and modern typography (`Plus Jakarta Sans` and `JetBrains Mono`).
* **Interactive Islands**: Vanilla TypeScript for tabbed code teardown comparison and dynamic intake booking.
* **Hosting**: Native [Cloudflare Pages](https://pages.cloudflare.com) edge deployment via Git connection.

---

## 🚀 Quick Start (Local Development)

### 1. Prerequisites
* Node.js `>= 22.12.0`
* npm `>= 10.0.0`

### 2. Install Dependencies
```bash
npm install
```

### 3. Start Development Server
```bash
npm run dev
```
Open `http://localhost:4321` in your browser.

### 4. Build for Production
```bash
npm run build
```
The static build artifacts will be generated in `dist/`.

---

## 📁 Project Structure

```text
├── .agents/                    # Workspace agent rules & skills
│   ├── rules/
│   │   ├── autonomous_workflow.md
│   │   └── quality_and_testing.md
│   └── skills.json
├── docs/                       # Project specifications & PRDs
│   └── PRDs/
│       └── vibe_code_rescue_landing_page.md
├── public/                     # Static assets & favicons
├── src/
│   ├── components/             # Reusable UI components
│   │   ├── Navbar.astro        # Header with mobile drawer
│   │   ├── Hero.astro          # Hero value prop + terminal diff
│   │   ├── ProblemBreakdown.astro # The 4 failure modes
│   │   ├── Process.astro       # 3-Step rescue roadmap
│   │   ├── CodeTeardown.astro  # Interactive before/after teardown
│   │   ├── Pricing.astro       # 3 Transparent service packages
│   │   ├── TechStack.astro     # Supported AI & stack chips
│   │   ├── IntakeSection.astro # Cal.com embed & fallback form
│   │   ├── FAQ.astro           # Accordion FAQ
│   │   └── Footer.astro        # Footer & guarantees
│   ├── layouts/
│   │   └── Layout.astro        # Base HTML layout & SEO metadata
│   ├── pages/
│   │   └── index.astro         # Main single-page landing
│   └── styles/
│       └── global.css          # Tailwind CSS v4 & theme variables
├── astro.config.mjs            # Astro configuration
└── package.json
```

---

## 📄 License
All rights reserved © Vibe Code Rescue Engineering.
