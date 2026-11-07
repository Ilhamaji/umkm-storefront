<div align="center">

# UMKM Storefront

**An online product catalogue for a small business** — a React SPA with product categories, image galleries, and a shop profile page.

[![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square)](#)
[![React](https://img.shields.io/badge/React-18-61DAFB?style=flat-square&logo=react&logoColor=black)](https://react.dev)
[![React Router](https://img.shields.io/badge/React%20Router-6-CA4245?style=flat-square&logo=react-router&logoColor=white)](https://reactrouter.com)

**English** · [Bahasa Indonesia](README.id.md)

</div>

---

## About

A catalogue site for a small business selling **bags, wallets, shoes, hats, bouquets, and accessories**. Many small shops rely entirely on a social media feed, which is hard to browse — here products are grouped by category and easy to find.

> This is a **catalogue**, not a checkout flow. Transactions are handed off to the seller's own contact (WhatsApp/Instagram).

## Features

- The home page lists categories (`public/API/Home.json`), each linking to its page.
- Six category pages: Bags, Wallets, Shoes, Hats, Bouquets, and Accessories.
- Each category holds several product photos (8 images for Bags, for example), loaded with `react-lazy-load`.
- An About page with the shop profile, and a 404 page for unknown routes.

## Tech Stack

| Layer | Technology |
| --- | --- |
| Framework | React 18 (CRA) |
| Routing | React Router 6 |
| Data | Static JSON in `public/API/` |
| Styling | Per-page CSS modules |
| Optimisation | `react-lazy-load`, `web-vitals` |
| Deployment | GitHub Pages (`gh-pages`) |

## Getting Started

### 1. Clone and install

```bash
git clone https://github.com/Ilhamaji/umkm-storefront.git
cd umkm-storefront
npm install
```

### 2. Run

```bash
npm start
```

Open [http://localhost:3000](http://localhost:3000).

### 3. Build and deploy

```bash
npm run build
npm run deploy
```

## Project Layout

```
public/
  API/Home.json              # home page data
  API/Products.json          # product data
  Products/{Category}/       # product images per category
src/
  Pages/
    Home.jsx                 # home page
    Products.jsx             # all products
    Products/
      Tas.jsx, Dompet.jsx, Sepatu.jsx, Topi.jsx,
      Bouquet.jsx, Aksesoris.jsx
    About.jsx                # shop profile
    NotFound.jsx             # 404 page
  Components/
    Navbar.jsx, Footer.jsx
```

## Adding a Product

1. Put the image in `public/Products/<Category>/`.
2. Register an entry in `public/API/Products.json`:

```json
{
  "id": 1,
  "jenis": "Tas",
  "nama": "Product name",
  "harga": 150000,
  "image": "/Products/Tas/tas-1.jpg"
}
```

> The data keys (`jenis`, `nama`, `harga`) are in Indonesian because the JSON is consumed as-is by the existing components.

---

<div align="center">
Built by <a href="https://github.com/Ilhamaji">Ilham Aji</a>
</div>
