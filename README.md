# Project Overview: For the HTML&CSS Assignment

This document outlines the architectural approach and technical specifications for the project implementation using HTML & CSS.

---

## Structure & Approach

The project follows a **Desktop-First** methodology, ensuring the core content is prioritized for large screens before enhancing the experience for smaller viewports.

*   **Component-Based Architecture:** The UI is broken down into reusable, modular components to ensure maintainability and scalability.
*   **Layout Engine:** Utilizes **CSS Grid** for macro-layouts (the main page skeleton) and **Flexbox** for micro-layouts (navigation items, card content).
*   **Styling Strategy:** Implemented using **BEM (Block Element Modifier)** naming conventions to prevent style leakage and ensure CSS specificity remains low.
*   **Asset Optimization:** Images utilize `Extract from pdf` for responsive delivery, and  SVG icons(from Font awesome) are used for resolution independence.

---

## Breakpoints

The design scales fluidly across devices using the following defined breakpoints:

| Breakpoint | Range | Target Device |
| :--- | :--- | :--- |
| **Small (sm)** | `0px - 576px` | Mobile Portrait/Landscape |
| **Medium (md)** | `577px - 1023px` | Tablets & Foldables |
| **Large (lg)** | `1024px - 1279px` | Laptops / Large Monitors |


> **Note:** We use `em` or `rem` units for media queries to ensure the layout responds correctly to browser zoom and user font-size preferences.

---

##  Assumptions & Limitations

### Assumptions
*   **Browser Support:** The project targets modern evergreen browsers (Chrome, Firefox). 
*   **Interactivity:** good but have problem
*   **Content:** Dynamic content is assumed to follow the character limits defined in the UI mockups to prevent layout breaking.

### Limitations
*   **Legacy Browsers:** No support is provided for Internet Explorer 11 or legacy versions of Edge.
*   **High-Contrast Mode:** While accessible, specific "High Contrast" themes for Windows have not been fully audited.
*   **Data Usage:** High-resolution assets may impact performance on extremely slow 2G/3G connections, though lazy-loading is implemented to mitigate this.