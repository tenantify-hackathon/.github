---

## 👥 Tim Pengembang

**Nama Tim: Saya Dapet Laporan Ada Hackathon di UNESA**

| Nama | Peran |
|---|---|
| Muhammad Kevin Alvarel | Fullstack Engineer |
| Muhammad Sahrul Ramadhan | Fullstack Engineer |
| Muhammad Sausan Syafiq | AI Engineer |

---

## 📚 Repository & Sumber Proyek

Tenantify dikembangkan dalam beberapa repository yang saling terintegrasi untuk membangun satu ekosistem digital. Berikut adalah repository resmi yang dapat diakses untuk melihat implementasi dan dokumentasi setiap komponen.

| Komponen | Repository | Deskripsi |
|---|---|---|
| **Organization** | [tenantify-hackathon](https://github.com/tenantify-hackathon) | Halaman utama organisasi dan pusat seluruh pengembangan proyek Tenantify. |
| **Web Application** | [tenantify-web-app](https://github.com/tenantify-hackathon/tenantify-web-app) | Aplikasi utama Tenantify yang mencakup pengelolaan Association, Seller, dan Consumer. |
| **Machine Learning** | [tenantify-ml-models](https://github.com/tenantify-hackathon/tenantify-ml-models) | Backend AI untuk rekomendasi produk UMKM dan moderasi komentar berbasis NLU. |

### Tautan Aplikasi

| Platform | URL |
|---|---|
| Customer Application | [tenantify.store](https://tenantify.store) |
| Seller & Association Dashboard | [seller.tenantify.store](https://seller.tenantify.store) |

Seluruh repository merupakan bagian dari pengembangan **Tenantify — Ekosistem Digital untuk Pengelolaan Bazaar dan Food Court**.

---

# 🚀 Tenantify
### Ekosistem Digital untuk Pengelolaan Bazaar dan Food Court

**Tenantify** adalah platform digital untuk mendigitalisasi dan mengelola aktivitas penjualan UMKM di area komersial seperti **Bazaar, Food Court, dan pusat kuliner**.

Tenantify menghubungkan tiga peran utama — **Association, Seller, dan Consumer** — dalam satu ekosistem terintegrasi yang mencakup pengelolaan tenant, penjualan produk, pemetaan lokasi, rekomendasi produk berbasis AI, hingga pengalaman berbelanja yang lebih terorganisir.


## ✨ Fitur Utama

- **Manajemen Multi-Role** — Dashboard terpisah untuk Association (pengelola area), Seller (pemilik tenant), dan Consumer (pembeli).
- **Rekomendasi Produk Berbasis AI** — Rekomendasi produk lintas tenant menggunakan semantic similarity dan complementary scoring.
- **Peta Tenant & Denah Area** — Visualisasi tata letak zona dan lokasi booth/tenant yang dapat dikelola Association dan dilihat Consumer.
- **Sistem Pemesanan Ganda** — Mendukung pemesanan online melalui aplikasi dan transaksi langsung melalui POS kasir.
- **Manajemen Katalog & Stok** — Pengelolaan katalog produk, stok, promosi, ulasan, dan statistik penjualan.
- **Tagihan Sewa Tenant** — Penerbitan tagihan sewa tenant bulanan beserta pemantauan status pembayaran.
- **Moderasi Komentar Berbasis AI** — Klasifikasi dan moderasi komentar untuk membantu menjaga kualitas interaksi pengguna.
- **Autentikasi & Otorisasi** — Sistem autentikasi dan otorisasi berbasis role menggunakan Better Auth.

---

## 🔑 Akun Demo untuk Juri

Untuk memudahkan proses pengujian dan eksplorasi fitur Tenantify, berikut akun demo yang dapat digunakan oleh juri berdasarkan masing-masing role.

| Role | Email | Password |
|---|---|---|
| Consumer | `juri@tenantify.store` | `password123` |
| Seller | `admin@kopikita.com` | `password123` |
| Association | `cilegonjuare@gmail.com` | `cilegonjuare` |

### Panduan Login

Tenantify menyediakan dua alamat aplikasi berdasarkan kebutuhan pengguna:

| Alamat Website | Pengguna |
|---|---|
| [https://tenantify.store](https://tenantify.store) | Customer |
| [https://seller.tenantify.store](https://seller.tenantify.store) | Seller & Association |

**Langkah Pengujian:**

1. Buka alamat website sesuai role yang ingin diuji.
2. Pilih menu **Masuk / Login**.
3. Masukkan email dan password menggunakan akun demo yang telah disediakan.
4. Setelah berhasil login, sistem akan mengarahkan pengguna ke halaman sesuai role dan hak akses masing-masing.

**Catatan:** Gunakan akun demo di atas untuk keperluan pengujian dan eksplorasi fitur selama proses penilaian hackathon.

---

## 🏗️ Arsitektur Sistem

Tenantify dibangun menggunakan dua komponen utama yang saling terintegrasi:

### 1. Aplikasi Utama Tenantify

Aplikasi utama yang menangani seluruh proses bisnis, pengelolaan data, autentikasi, transaksi, dan interaksi pengguna.

**Teknologi yang Digunakan:**

| Lapisan | Teknologi |
|---|---|
| Framework | Next.js 16 (App Router, Turbopack, Server Actions) |
| UI Library | React 19 |
| Bahasa Pemrograman | TypeScript |
| Database | PostgreSQL (Neon) |
| ORM | Drizzle ORM |
| Autentikasi | Better Auth |
| Styling | Tailwind CSS v4 |
| Komponen UI | Base UI, shadcn/ui |
| Form & Validasi | React Hook Form, Zod |
| Caching | Upstash Redis |
| Penyimpanan File | Vercel Blob |
| Animasi | Motion |

### 2. Tenantify AI Backend

Microservice REST API yang menyediakan kemampuan kecerdasan buatan untuk rekomendasi produk UMKM dan moderasi teks.

**Teknologi yang Digunakan:**

| Lapisan | Teknologi |
|---|---|
| Bahasa Pemrograman | Python 3.10 |
| API & Dokumentasi | Gradio / REST API |
| Model Embedding | BAAI/bge-m3 |
| Pencarian Vektor | FAISS |
| Metode Rekomendasi | Content-Based Filtering |
| Pemrosesan Bahasa | Text Classification & Moderation |
| Deployment | Hugging Face Spaces |

**Kemampuan AI:**

- **Rekomendasi Produk Semantik** — Menggunakan multilingual embedding untuk menemukan produk yang relevan berdasarkan kemiripan makna.
- **Rekomendasi Produk Pelengkap** — Memberikan rekomendasi produk pelengkap berdasarkan produk yang dipilih atau isi keranjang pesanan.
- **Moderasi Teks** — Mengklasifikasikan komentar pengguna untuk membantu proses moderasi konten.
- **Moderasi Komentar Massal** — Memproses beberapa komentar sekaligus melalui satu endpoint.

---

## 🔌 Dokumentasi API AI

| Metode | Endpoint | Deskripsi |
|---|---|---|
| GET | `/docs` | Dokumentasi API |
| GET | `/health` | Pemeriksaan status layanan |
| GET | `/products` | Mengambil daftar produk |
| GET | `/orders` | Mengambil riwayat pesanan |
| POST | `/recommend/by-product` | Rekomendasi berdasarkan produk pilihan |
| POST | `/recommend/by-order` | Rekomendasi produk pelengkap berdasarkan pesanan |
| POST | `/comments/classify` | Klasifikasi satu komentar pembeli |
| POST | `/comments/moderate-batch` | Moderasi beberapa komentar sekaligus |

---

## 📂 Struktur Proyek

Berikut gambaran struktur direktori aplikasi utama Tenantify:

```text
app/                  # Routing dan halaman aplikasi
components/           # Komponen UI yang dapat digunakan ulang
context/              # React context
data/                 # Data demo dan seed statis
db/                   # Skema Drizzle dan modul query
hooks/                # Custom React hooks
lib/                  # Utilitas, autentikasi, cache, dan AI client
migrations/           # Migrasi database
servers/              # Server actions berdasarkan domain
types/                # Definisi tipe TypeScript
validations/          # Skema validasi Zod
```

---

## ⚙️ Panduan Instalasi

### Prasyarat

- Node.js 20+ (disarankan Node.js 24)
- npm
- Database PostgreSQL (Neon)
- Akun Upstash Redis (opsional)
- Token Vercel Blob

### Menjalankan Proyek

```bash
# Clone repository
git clone <URL_REPOSITORY>

# Masuk ke direktori proyek
cd tenantify

# Instal dependensi
npm install

# Jalankan server development
npm run dev
```

Buka [http://localhost:3000](http://localhost:3000) untuk mengakses aplikasi.

### Variabel Lingkungan

Buat file `.env` di direktori utama proyek:

```env
# Database
DATABASE_URL=postgresql://...

# Better Auth
BETTER_AUTH_SECRET=...
BETTER_AUTH_URL=http://localhost:3000
BASE_URL=http://localhost:3000
NEXT_PUBLIC_BASE_URL=http://localhost:3000

# Upstash Redis
UPSTASH_REDIS_REST_URL=...
UPSTASH_REDIS_REST_TOKEN=...

# Vercel Blob
BLOB_READ_WRITE_TOKEN=...

# AI Service
AI_SERVICE_URL=https://s4usan-tenantify-models.hf.space
```

### Perintah yang Tersedia

| Perintah | Deskripsi |
|---|---|
| `npm run dev` | Menjalankan server development |
| `npm run build` | Membuat build aplikasi untuk produksi |
| `npm start` | Menjalankan aplikasi hasil build |
| `npm run lint` | Menjalankan ESLint |
| `npm run db:generate` | Membuat file migrasi dari skema |
| `npm run db:migrate` | Menjalankan migrasi database |
| `npm run db:push` | Menerapkan skema langsung ke database |
| `npm run db:studio` | Membuka Drizzle Studio |

---

## 🎯 Tujuan Pengembangan

Tenantify dikembangkan sebagai solusi digital untuk membantu pengelola area komersial dan pelaku UMKM dalam mengelola aktivitas bisnis secara lebih terintegrasi.

Melalui kombinasi teknologi web modern dan kecerdasan buatan, Tenantify bertujuan menciptakan ekosistem perdagangan yang lebih efisien, terorganisir, serta memberikan pengalaman berbelanja yang lebih baik bagi konsumen.

---

<p align="center">
  Dibuat dengan ❤️ oleh <strong>Tim Saya Dapet Laporan Ada Hackathon di UNESA</strong>
</p>
