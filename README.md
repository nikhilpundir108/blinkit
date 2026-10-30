# 🛒 Blinkit Landing Page Clone

A pixel-perfect, fully responsive clone of the [Blinkit](https://blinkit.com) homepage built using **HTML5 and CSS3 only** — no JavaScript, no frameworks.

---

## 📁 Project Structure

```
blinkit/
├── index.html              # Main HTML file
├── style.css               # All styles & responsive rules
├── README.md               # Project documentation
└── assets/
    └── images/             # All images used in the project
        ├── Frame-1437256605-2-2.jpg   # Hero banner image
        ├── pharmacy-WEB.avif          # Pharmacy promo card
        ├── pet_crystal_WEB-1.avif     # Pet care promo card
        ├── baby_crystal_WEB-1.avif    # Baby care promo card
        ├── paan-corner_web.avif       # Paan corner category
        ├── print_crystal_WEB.avif     # Print & stationery category
        └── Slice-*.avif               # Category tile images
```

---

## 🌐 Live Sections

| Section | Description |
|---|---|
| **Header / Navbar** | Logo, delivery time, location picker, search bar, Login & Cart buttons |
| **Hero Banner** | Promotional hero with floating image animation and badges |
| **Promo Cards** | Pharmacy, Pet Care, Baby Care — 3-column card layout |
| **Category Grid** | 26 product categories in a responsive auto-fill grid |
| **Offer Banner** | Dark gradient promotional section with discount code |
| **App Download** | iOS & Android badge download section |
| **Footer** | Links, categories, social icons, copyright bar |

---

## ✨ Features & Techniques Used

### 🏗️ HTML5
- **Semantic elements** — `<header>`, `<main>`, `<section>`, `<footer>`, `<nav>` used throughout for accessibility and SEO
- **SVG icons** — All icons (search, location, cart, user, social media) are inline SVGs for crisp rendering at any size and zero HTTP requests
- **`onerror` fallback** — Every `<img>` has an `onerror` attribute that loads a placeholder if the local image is missing
- **AVIF image format** — Modern, high-compression `.avif` images for category tiles
- **`<meta viewport>`** — Proper viewport tag for mobile rendering

### 🎨 CSS3

#### Layout
- **CSS Flexbox** — Used for the header, nav actions, promo cards, hero section, footer bottom bar, app download section, and all inline groupings
- **CSS Grid** — Used for the promo card 3-column layout, the 26-tile category grid (auto-fill), and the 4-column footer grid
- **`auto-fill` + `minmax()`** — Category grid automatically reflows based on available space without any media queries

#### Visual Design
- **CSS Custom Properties (Variables)** — All brand colors, spacing, shadows, font stack, and border-radii defined as `:root` variables for easy theming
  ```css
  --yellow: #F8C200;
  --green: #0c831f;
  --radius-lg: 20px;
  ```
- **CSS Gradients** — `linear-gradient()` used for the hero background, promo cards (pharmacy/pet/baby), offer banner, and footer
- **`box-shadow`** — Multi-layer shadows for cards, buttons, and floating hero badges
- **`border-radius`** — Consistent rounded corners across all UI elements
- **`overflow: hidden`** — Used on cards and category images to clip content cleanly
- **`backdrop-filter` / `filter`** — `drop-shadow` filter on hero image for a realistic floating shadow

#### Animations & Transitions
- **CSS `@keyframes` animation** — Smooth `float` animation on the hero grocery bag image
  ```css
  @keyframes float {
    0%, 100% { transform: translateY(0); }
    50%       { transform: translateY(-12px); }
  }
  ```
- **CSS `transition`** — Hover effects on buttons (`translateY`, `box-shadow`), category cards (border color, transform), nav buttons, social icons, and footer links
- **Image zoom on hover** — Category images scale up smoothly on hover using `transform: scale(1.08)` with `transition`

#### Typography
- **Google Fonts — Inter** — Loaded via `<link>` with weights 400, 500, 600, 700, 800
- **`letter-spacing`** — Used on labels, tags, and headings for visual hierarchy
- **`text-overflow: ellipsis`** — Location text truncates gracefully on small screens

#### Responsive Design
- **CSS Media Queries** — Four breakpoints cover all screen sizes:
  | Breakpoint | Target |
  |---|---|
  | `≤ 1024px` | Large tablets |
  | `≤ 900px` | Tablets & small laptops |
  | `≤ 600px` | Mobile phones |
  | `≤ 380px` | Small phones (iPhone SE, etc.) |
- **Mobile-first collapsing** — Desktop search bar hidden on mobile; a dedicated mobile search bar appears below the header
- **Delivery info + Login button** — Hidden on small screens to reduce header clutter
- **Hamburger menu toggle** — CSS-only visible toggle on mobile
- **No horizontal scroll** — `overflow-x: hidden` on `body`; all grids reflow naturally

#### Sticky Header
- `position: sticky; top: 0; z-index: 1000` keeps the header visible while scrolling

---

## 🎨 Design System (Brand Colors)

| Token | Value | Usage |
|---|---|---|
| `--yellow` | `#F8C200` | Primary CTA, logo, highlights |
| `--yellow-dark` | `#e0ad00` | Button hover state |
| `--yellow-light` | `#FFF9E0` | Section backgrounds |
| `--green` | `#0c831f` | Delivery time, hero text accent |
| `--black` | `#1a1a1a` | Body text, footer background |
| `--gray-100` | `#f3f4f6` | Page backgrounds, input fills |
| `--gray-200` | `#e5e7eb` | Borders, dividers |

---

## 📱 Responsive Behavior

| Screen Size | Layout |
|---|---|
| **Desktop (>1024px)** | Full navbar, 3-col promo cards, auto-fill category grid, 4-col footer |
| **Tablet (≤900px)** | Stacked hero, single-col promo cards, 4-col category grid, 2-col footer |
| **Mobile (≤600px)** | Compact header, mobile search bar, 3-col category grid, 2-col footer |
| **Small Mobile (≤380px)** | 3-col categories, single-col footer |

---

## 🚀 How to Run

No build tools or server required. Simply open `index.html` in any modern browser:

```bash
# Option 1: Double-click index.html in File Explorer

# Option 2: Open with VS Code Live Server
# Right-click index.html → Open with Live Server
```

> **Note:** Internet connection is needed on first load to fetch the **Inter** font from Google Fonts. Once cached, it works offline.

---

## 📋 Assignment Requirements Checklist

- [x] Header with logo, delivery info, search bar, login & cart buttons
- [x] Main hero/promotional banner with heading, image, and Shop Now button
- [x] Three promotional cards (Pharmacy, Pet Care, Baby Care)
- [x] Product category grid with images and names
- [x] Footer with useful links, categories, app download, social icons, copyright
- [x] Desktop responsive layout
- [x] Mobile responsive layout
- [x] Tablet responsive layout
- [x] No horizontal scrolling or overlapping elements
- [x] HTML5 and CSS3 only (no JavaScript, no frameworks)
- [x] Flexbox and CSS Grid used appropriately
- [x] CSS media queries for responsiveness
- [x] Clean, structured, commented code

---

## 🛠️ Technologies

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![Google Fonts](https://img.shields.io/badge/Google_Fonts-Inter-4285F4?style=flat&logo=google&logoColor=white)

---

*Built as a frontend assignment — Blinkit Homepage Clone.*

