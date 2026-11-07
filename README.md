<div align="center">

# UMKM Storefront

**Katalog produk online untuk usaha kecil (UMKM)** — React SPA dengan kategori produk, galeri gambar, dan halaman profil usaha.

[![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square)](#)
[![React](https://img.shields.io/badge/React-18-61DAFB?style=flat-square&logo=react&logoColor=black)](https://react.dev)
[![React Router](https://img.shields.io/badge/React%20Router-6-CA4245?style=flat-square&logo=react-router&logoColor=white)](https://reactrouter.com)

</div>

---

## Tentang

Website katalog untuk usaha kecil yang menjual aneka produk: **tas, dompet, sepatu, topi, bouquet, dan aksesoris**. Dibuat karena banyak UMKM hanya mengandalkan feed media sosial yang sulit dinavigasi — di sini produk dikelompokkan per kategori dan mudah dicari.

> Ini adalah **katalog**, bukan toko dengan checkout. Transaksi diarahkan ke kontak penjual (WhatsApp/Instagram).

## Fitur

- Beranda menampilkan daftar kategori (`public/API/Home.json`), masing-masing menaut ke halamannya.
- Enam halaman kategori: Tas, Dompet, Sepatu, Topi, Bouquet, dan Aksesoris.
- Tiap kategori berisi beberapa foto produk (8 gambar untuk Tas, misalnya), dimuat dengan `react-lazy-load`.
- Halaman About berisi profil usaha, dan route tak dikenal jatuh ke halaman 404.

## Tech Stack

| Bagian | Teknologi |
| --- | --- |
| Framework | React 18 (CRA) |
| Routing | React Router 6 |
| Data | JSON statis di `public/API/` |
| Styling | CSS modules per halaman |
| Optimasi | `react-lazy-load`, `web-vitals` |
| Deploy | GitHub Pages (`gh-pages`) |

## Menjalankan

### 1. Clone & install

```bash
git clone https://github.com/Ilhamaji/umkm-storefront.git
cd umkm-storefront
npm install
```

### 2. Jalankan

```bash
npm start
```

Buka [http://localhost:3000](http://localhost:3000).

### 3. Build & deploy

```bash
npm run build
npm run deploy
```

## Struktur

```
public/
  API/Home.json              # data beranda
  API/Products.json          # data produk
  Products/{Kategori}/       # gambar produk per kategori
src/
  Pages/
    Home.jsx                 # beranda
    Products.jsx             # daftar semua produk
    Products/
      Tas.jsx, Dompet.jsx, Sepatu.jsx, Topi.jsx,
      Bouquet.jsx, Aksesoris.jsx
    About.jsx                # profil usaha
    NotFound.jsx             # halaman 404
  Components/
    Navbar.jsx, Footer.jsx
```

## Menambah Produk

1. Tambahkan gambar ke `public/Products/<Kategori>/`.
2. Daftarkan entri di `public/API/Products.json`:

```json
{
  "id": 1,
  "jenis": "Tas",
  "nama": "Nama Produk",
  "harga": 150000,
  "image": "/Products/Tas/tas-1.jpg"
}
```

---

<div align="center">
Dibuat oleh <a href="https://github.com/Ilhamaji">Ilham Aji</a>
</div>
