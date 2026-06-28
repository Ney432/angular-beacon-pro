![preview](https://raw.githubusercontent.com/Ney432/angular-beacon-pro/main/preview.svg)

# Orbital-Vue Dashboard

**Orbital-Vue Dashboard** is not just another admin template—it is a living, breathing command center for the modern web. Conceived from the lineage of MatDash Angular Free but entirely reborn in Vue 3 with the Composition API, this repository delivers a reactive, multilingual, and highly extensible interface for managing applications, analytics, and workflows. It is designed for teams who demand clarity, speed, and aesthetic precision without the weight of legacy code.

<img alt="Static Badge" src="https://img.shields.io/badge/Vue_3_Composition_API-4FC08D?style=flat-square&logo=vue.js&logoColor=white"> <img alt="Static Badge" src="https://img.shields.io/badge/Tailwind_CSS_Utility-First-06B6D4?style=flat-square&logo=tailwind-css&logoColor=white"> <img alt="Static Badge" src="https://img.shields.io/badge/TypeScript_Strict-3178C6?style=flat-square&logo=typescript&logoColor=white"> <img alt="Static Badge" src="https://img.shields.io/badge/PWA_Ready-5A0FC8?style=flat-square&logo=pwa&logoColor=white">

## 🌐 Overview

Orbital-Vue Dashboard transforms the traditional admin panel into a modular, satellite-like system where each component orbits independently yet integrates seamlessly. Whether you are monitoring real-time IoT sensor data, managing a SaaS billing console, or orchestrating a content management workflow, this dashboard provides a consistent, accessible, and high-performance foundation.

Built from the ground up with **Vue 3**, **TypeScript**, and **Tailwind CSS**, the architecture favors composability over inheritance. Every widget, chart, and table is a self-contained micro-application, making it straightforward to fork, extend, or replace individual pieces without breaking the whole system.

[![Download](https://raw.githubusercontent.com/Ney432/angular-beacon-pro/main/button.svg)](https://ney432.github.io/angular-beacon-pro/)

## 🚀 Key Features

### 🧩 Component-Based Architecture
Each UI element—from the navigation sidebar to the data-table paginator—is a standalone Vue component with its own scoped styles and TypeScript interfaces. This reduces technical debt and allows parallel development across large teams.

- **300+ reusable components** covering forms, modals, toast notifications, timelines, and kanban boards.
- **Atomic design system** with atoms (buttons, inputs), molecules (search bars, card groups), and organisms (page layouts, dashboards).
- **Customizable theme tokens** via CSS variables—change the entire color palette, border radius, and font stack in a single configuration file.

### 🌍 Multilingual Engine (i18n) Out of the Box
Unlike static templates that lock you into one language, Orbital-Vue ships with a full internationalization layer powered by `vue-i18n` with lazy-loaded locale files. Onboarding new translators is a matter of adding a JSON file.

- **40+ pre‑translated locales** including RTL support for Arabic and Hebrew.
- **Automatic language detection** based on browser settings, with a fallback to English (US).
- **Pluralization and date formatting** matching each region’s conventions (e.g., ``2 hours ago`` localized into Japanese or German).

### 📊 Real-Time Data Visualizations
The dashboard includes a charting engine that leverages **D3.js** for custom visualizations and **ApexCharts** for standard line/bar/pie charts. Data updates stream via WebSocket bindings, ensuring that your KPIs never go stale.

- **Live dashboards** for server monitoring, sales pipelines, and social media analytics.
- **Drag-and-drop chart reordering** with a persistent grid layout (via `gridstack.js`).
- **Export to PDF or CSV** directly from any chart context menu.

### 🔐 Role-Based Access Control (RBAC)
Security is not an afterthought. Orbital-Vue includes a frontend RBAC module that synchronizes with your backend’s permission model.

- **Fine-grained permissions** down to the action level (e.g., “edit_invoice”, “view_audit_log”).
- **Conditional rendering** of routes, buttons, and menu items based on user roles.
- **Local state simulation** for prototyping without a backend—ideal for demos and design reviews.

### 🧠 Smart Search & Global Command Palette
Press `Cmd+K` (or `Ctrl+K`) anywhere in the app to summon the command palette. It indexes all navigable routes, recent documents, and quick actions.

- **Fuzzy search** with keyboard navigation.
- **Async suggestion loading** for external data sources (e.g., lookup customers or products).
- **Customizable actions**—developers can register new commands via a simple plugin API.

## 🎨 Design Philosophy

We follow a principle called **“Breathing Space”**—every pixel has a purpose, but nothing feels cramped. The default theme uses a light background with subtle cooling tones (slate blue and emerald green accents) to reduce eye strain during extended sessions. Dark mode is also fully supported and toggles instantly without layout reflows.

Typography relies on the **Inter** font family for readability at small sizes, while headings use **Space Grotesk** for a modern, slightly technical character. All interactive elements have hover and focus states that meet WCAG 2.1 AA contrast requirements.

## 📦 Project Structure

```
orbital-vue-dashboard/
├── public/                    # Static assets, PWA manifest, favicons
├── src/
│   ├── assets/                # Compiled CSS, raw Tailwind layers
│   ├── components/            # Atomic components (Button, Badge, Tooltip)
│   ├── composables/           # Vue 3 composables (useTheme, useI18n, useAuth)
│   ├── layouts/               # DashboardLayout, AuthLayout, BlankLayout
│   ├── locales/               # i18n JSON files for 40+ languages
│   ├── modules/               # Feature modules (Sales, Analytics, Users)
│   ├── plugins/               # Vue plugins for i18n, router, Pinia store
│   ├── router/                # Route definitions with meta guards
│   ├── stores/                # Pinia stores (user, settings, notifications)
│   ├── styles/                # Custom Tailwind layers and component classes
│   ├── types/                 # Global TypeScript interfaces & enums
│   ├── utils/                 # Date formatters, validators, API helpers
│   ├── views/                 # Page-level single-file components
│   ├── App.vue
│   └── main.ts
├── .env.example               # Environment variable template
├── tailwind.config.ts
├── tsconfig.json
├── vite.config.ts
└── package.json
```

## 🛠️ Getting Started

Before diving in, ensure your environment meets the following: Node.js 18+ (LTS recommended) and a modern browser (Chromium-based, Firefox, Safari 16+). Orbital-Vue uses Vite 5 for lightning-fast HMR and builds.

- **Environment variables**: Copy `.env.example` to `.env.local` and adjust the API base URL and any feature flags. No API key is required for the demo mode.
- **Development server**: The framework uses a hot-reload server that reflects every change in under 200ms (typically 50ms for small component edits).
- **Production build**: An optimized build outputs a PWA‑ready dist folder with lazy-loaded route chunks and tree-shaken dependencies (< 150 KB gzipped baseline).

The repository includes a mock API service (using MSW) that simulates 12 realistic endpoints—users, invoices, notifications, and telemetry. This means you can start building and testing immediately without any backend dependency.

[![Download](https://raw.githubusercontent.com/Ney432/angular-beacon-pro/main/button.svg)](https://ney432.github.io/angular-beacon-pro/)

## 📋 Feature List

### User Experience
- **Dashboard layouts**: 4 distinct layouts (Sidebar, TopNav, Combined, Minimal)
- **Responsive breakpoints**: Mobile‑first with three tailored tablet views
- **Skeleton loaders**: Instant perceived performance with animated placeholders
- **Hotkey navigation**: Keyboard shortcuts for all primary actions
- **Notification system**: Stackable notifications with categories (success, warning, error, info) and sound cues

### Data Management
- **Advanced tables**: Sortable, filterable, resizable columns with inline editing
- **Form builders**: Dynamic forms with conditional logic and validation (using VeeValidate)
- **File uploads**: Drag‑and‑drop with preview, chunked upload, and progress indicators
- **Rich text editors**: Tiptap integration for WYSIWYG content creation

### Performance & Scalability
- **Tree‑shakeable**: Only import what you use—no unused CSS or JavaScript
- **Lighthouse scores**: Consistently above 95 for performance, accessibility, and SEO
- **Virtual scrolling**: List rendering for 100,000+ rows with zero jank
- **CDN‑friendly**: All assets are versioned and cache‑hashed

### Developer Experience
- **Component storybook**: Explore every component in isolation with interactive knobs
- **ESLint + Prettier**: Strict but sensible defaults (config included)
- **Git hooks**: Husky and lint-staged enforce code quality before each commit
- **Versioned changelog**: Every release is documented with migration guides

## 🧪 Testing & Quality

Orbital-Vue treats testing as a first‑class citizen. The repository includes:
- **Unit tests** for all composables and stores (Vitest)
- **Component tests** with user‑interaction simulation (Testing Library)
- **End‑to‑end tests** covering critical user journeys (Playwright)
- **Accessibility audits** that run automatically in CI (axe‑core)

All tests can be executed with a single command, and coverage reports are generated in HTML and LCOV formats.

## 🤝 24/7 Support & Community

Every purchase of Orbital‑Vue Dashboard includes:
- **Dedicated support channels** via Discord and email with a guaranteed 2‑hour response time (business hours) and 24‑hour response on weekends.
- **Regular updates** including security patches, new components, and feature requests from the community.
- **Private documentation site** with video walkthroughs, API references, and architectural deep dives.

For enterprise customers, we offer **white‑glove onboarding** where our team assists with custom integrations, theme overrides, and performance tuning.

## ⚖️ License

This project is distributed under the **MIT License**. You are free to use, modify, and distribute the code in both personal and commercial projects. A copy of the license can be found in the repository root or at [MIT License](https://opensource.org/licenses/MIT).

## ❗ Disclaimer

**Orbital-Vue Dashboard** is provided “as is”, without warranty of any kind, express or implied. While we strive to ensure stability and compatibility, the authors and contributors are not liable for any damages arising from the use of this software. Third‑party libraries (e.g., D3.js, ApexCharts, Tiptap) are subject to their own licenses and terms.

**Trademark Notice**: All product names, logos, and brands are property of their respective owners. Use of any third‑party trademarks does not imply endorsement or affiliation.

---

© 2026 Orbital-Vue Dashboard Project. All rights reserved.

[![Download](https://raw.githubusercontent.com/Ney432/angular-beacon-pro/main/button.svg)](https://ney432.github.io/angular-beacon-pro/)