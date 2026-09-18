# Product Catalog – Nice Gadgets

A modern, responsive e-commerce web application for discovering and purchasing tech devices. Built with **React**, **TypeScript**, and **Vite**, featuring interactive product sliders, full-text search, persistent shopping cart, favorites management, and multi-language support.

## Live Demo & Design
* **Live Demo:** [Nice Gadgets Store](https://owldevcua.github.io/phone-catalog/)
* **Design Reference:** [Figma Design (Dark Mode)](https://www.figma.com/file/BUusqCIMAWALqfBahnyIiH/Phone-catalog-(V2)-Original-Dark)

---

## Features

* **Hero Picture Slider:** Auto-playing banner carousel for featured promotions (`Swiper`).
* **Product Carousels:** "Hot Prices" and "Brand New Models" blocks with dynamic sorting and horizontal scroll.
* **Category Navigation:** Direct access to Phones, Tablets, and Accessories with item counters.
* **Dynamic Filtering & Pagination:** URL-synced controls for items-per-page and sorting (by price, year, or age).
* **Interactive Details View:** Full product specifications, expandable image gallery, and breadcrumb navigation.
* **Search Functionality:** Real-time search with query parameters integrated into the navigation bar.
* **Persistent State:** Cart items and favorited products remain saved across sessions via `localStorage`.
* **Cart Interactions:** Dynamic price calculations, quantity adjustments, item removal, and checkout modal simulation.
* **Custom Provider Composition:** Clean context aggregation using a custom `compose` utility to wrap state providers without prop-drilling.
* **Smooth Motion:** Seamless UI transitions powered by `Headless UI` and `React Transition Group`.

---

## Technical Challenges & Solutions

* **Context State Scalability:** Solved deep context nesting at the root level by implementing a custom functional `compose` utility.
* **GitHub Pages Routing & Asset Resolution:** Resolved 404 errors and broken static assets on subfolder hosting by migrating to `HashRouter` and setting relative base paths (`base: './'`) in Vite.
* **Dart Sass & Modern Build Pipelines:** Eliminated SCSS `@import` deprecation warnings by refactoring global and component styles to the modern `@use` module system with explicit namespaces.
