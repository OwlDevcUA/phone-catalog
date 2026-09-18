# Product Catalog – Nice Gadgets

A modern, responsive e-commerce web application for discovering and purchasing tech devices. Built with **React**, **TypeScript**, and **Vite**, featuring interactive product sliders, full-text search, persistent shopping cart, favorites management, and multi-language support.

## Live Demo & Design
* **Live Demo:** [Nice Gadgets Store](https://owldevcua.github.io/phone-catalog/)
* **Design Reference:** [Figma Design (Dark Mode)](https://www.figma.com/file/BUusqCIMAWALqfBahnyIiH/Phone-catalog-(V2)-Original-Dark)

---

## Comprehensive Features

* **Home & Landing Experience:**
  * **Hero Picture Slider:** Auto-playing banner carousel for featured promotions (`Swiper`).
  * **Product Carousels:** "Hot Prices" and "Brand New Models" blocks with dynamic sorting and horizontal scroll.
  * **Category Navigation:** Direct access to Phones, Tablets, and Accessories with item counters.

* **Product Catalog & Details Page:**
  * **Dynamic Filtering & Pagination:** URL-synced controls for items-per-page and sorting (by price, year, or age).
  * **Interactive Details View:** Full product specifications, expandable image gallery, and breadcrumb navigation.
  * **Search Functionality:** Real-time search with query parameters integrated into the navigation bar.

* **Cart & Favorites Management:**
  * **Persistent State:** Cart items and favorited products remain saved across sessions via `localStorage`.
  * **Cart Interactions:** Dynamic price calculations, quantity adjustments, item removal, and checkout modal simulation.

* **Architecture & Utilities:**
  * **Custom Provider Composition:** Clean context aggregation using a custom `compose` utility to wrap state providers without prop-drilling.
  * **Motion:** Smooth UI transitions (`Headless UI` / `React Transition Group`).

---

## Technical Challenges & Solutions

* **Context State Scalability:**
  * *Challenge:* Managing separate contexts for Products, Cart, Favorites, Phones, Tablets, and Accessories led to deep nesting in the root tree.
  * *Solution:* Implemented a custom functional `compose` utility to cleanly chain multiple `React Context` providers at the root level.

* **GitHub Pages Routing & Asset Resolution:**
  * *Challenge:* Deploying a single-page application (SPA) with nested paths to a subfolder repository resulted in 404 errors and broken assets.
  * *Solution:* Migrated to `HashRouter` and configured relative base paths in Vite (`base: './'`) to ensure seamless navigation on static hosting.

* **Dart Sass & Modern Build Pipelines:**
  * *Challenge:* Legacy SCSS `@import` rules triggered deprecation warnings in newer Dart Sass versions during Vite builds.
  * *Solution:* Refactored global and component-level style imports to the modern `@use` module system with explicit namespaces and mixins.
