# Jelajah Wisata Bali

Portal informasi dan eksplorasi budaya pariwisata Bali yang dibuat sebagai proyek akhir mata kuliah **Desain Web** untuk **Expo Kampus 2026**. Situs ini memperkenalkan destinasi wisata Bali berdasarkan kategori, menampilkan estimasi tiket dan fasilitas dalam bentuk tabel, serta menyediakan formulir permintaan tiket kunjungan.

**Teknologi:** HTML5 murni dalam satu file (`index.html`). Tidak memakai CSS eksternal, JavaScript, framework, maupun backend.
**Bahasa tampilan:** Indonesia
**Format harga:** Rupiah (IDR)

---

## 1. Ringkasan Fitur

### Pengunjung
- Navigasi menu ke seluruh bagian halaman: Beranda, Destinasi, Paket Wisata, Pemesanan, dan Tim Kami.
- Pemutar musik latar bernuansa Bali (`<audio controls>`).
- Banner beranda dengan judul, ajakan eksplorasi, dan tiga informasi singkat (8 kabupaten + 1 kota, UNESCO Subak, Tri Hita Karana).
- Pengantar singkat tentang Bali dan filosofi Tri Hita Karana.
- **5 destinasi populer** lengkap dengan foto, lokasi, rating, deskripsi, dan daya tarik utama.
- **12 destinasi lainnya** dalam 4 kategori (masing-masing 3 tempat): Pantai & Bahari, Pura & Warisan Budaya, Pegunungan & Alam Sejuk, dan Desa Wisata Adat.
- **Tabel kategori wisata** berisi nama tempat, kabupaten, estimasi tiket, dan fasilitas utama, dengan gambar pendamping di sisi kanan.
- **Formulir pemesanan tiket** (nama, destinasi, tanggal kunjungan, jumlah tiket).
- Footer berisi deskripsi proyek, identitas tim pengembang, dan hak cipta.

### Daftar destinasi

| Bagian | Destinasi |
|---|---|
| Populer | Pura Luhur Uluwatu, Pura Tanah Lot, Terasering Tegallalang, Pantai Kelingking, Pura Ulun Danu Bratan |
| Pantai & Bahari | Pantai Pandawa, Pantai Sanur, Pantai Melasti |
| Pura & Warisan Budaya | Pura Agung Besakih, Pura Tirta Empul, Pura Taman Ayun |
| Pegunungan & Alam Sejuk | Kaldera Gunung Batur, Air Terjun Sekumpul, Bukit Campuhan |
| Desa Wisata Adat | Desa Adat Penglipuran, Desa Tenganan, Desa Seni & Budaya Ubud |

---

## 2. Struktur Halaman

```
index.html
│
├── Navigasi + pemutar musik
├── Hero / Beranda (#beranda)
├── Sekilas Pulau Dewata
├── Destinasi (#destinasi)
│     ├── Destinasi Populer (5 kartu)
│     └── Jelajah Wisata Lainnya (4 kategori x 3 kartu)
├── Paket Wisata (#paket-wisata)  -> tabel rowspan/colspan + gambar
├── Pemesanan (#pemesanan)        -> formulir tiket
└── Footer / Tim Kami (#tim-kami)
```

Tata letak dibuat dengan tabel bersarang dan atribut HTML (`bgcolor`, `width`, `height`, `align`, `cellpadding`), karena proyek dibatasi hanya memakai HTML.

---

## 3. Cara Menjalankan

Tidak perlu instalasi apa pun.

1. Simpan `index.html`, seluruh file foto, dan `lagu.mp3` **dalam satu folder yang sama**.
2. Klik dua kali `index.html` untuk membukanya di browser (Chrome, Edge, atau Firefox).

### Struktur folder

```
jelajah-bali/
├── index.html
├── lagu.mp3
├── kelingking.jpg          (banner beranda + kartu Kelingking)
├── uluwatu.jpg
├── tanahlot.jpg
├── tegallalang.jpg
├── puraulun.jpg
├── pantaipandawa.jpg
├── pantaisanur.jpg
├── pantaimelasti.jpg
├── purabesakih.jpg
├── puratirtaempul.jpg
├── puratamanayun.jpg
├── kalderagunungbatur.jpg
├── airterjunsekumpul.jpg
├── bukitcampuhan.jpg
├── penglipuran.jpg
├── tenganan.jpg
├── ubud.jpg
└── gambarakhir.jpg         (gambar di samping tabel)
```

Nama file harus sama persis dengan yang ditulis di `src`, termasuk huruf besar dan kecilnya.

### Ukuran foto

| Lokasi | Ukuran (px) |
|---|---|
| Banner beranda | 1200 x 420 |
| Kartu destinasi populer | 400 x 300 |
| Kartu destinasi lainnya | 360 x 240 |
| Gambar di samping tabel | 380 x 520 |

Ukuran diatur lewat atribut `width` dan `height`. Gunakan foto dengan rasio yang sama (atau potong dulu) agar tidak gepeng.

---

## 4. Konfigurasi yang Perlu Disesuaikan

| Bagian | Yang perlu diubah |
|---|---|
| `<form action="mailto:email@contoh.com">` | Ganti dengan email penerima pemesanan yang asli |
| `<source src="lagu.mp3">` | Ganti jika nama file musik berbeda |
| `alt` pada banner | Sesuaikan dengan foto yang dipakai (saat ini foto Kelingking) |
| Identitas tim di footer | Perbarui nama dan NPM bila ada perubahan |

---

## 5. Tim Pengembang

| Nama | NPM |
|---|---|
| Risma Destiantri | 25312118 |
| Rinn Novitasari | 25312117 |
| I Made Dwi Anggara | 25312113 |
| Tio Adi Saputra | 25312064 |

---

## 6. Status Pengerjaan

### Sudah selesai
- Struktur lengkap dari navigasi sampai footer.
- Seluruh konten destinasi (5 populer + 12 lainnya) beserta foto lokal berukuran tetap.
- Tabel kategori dengan `rowspan` dan `colspan`, lengkap dengan gambar pendamping.
- Formulir pemesanan dan pemutar musik latar.
- Identitas tim dan hak cipta di footer.

### Belum selesai / perlu dilakukan
- [ ] Membungkus foto dengan tag `<a>` agar bisa diklik dan dibuka dalam ukuran besar.
- [ ] Memperbaiki teks `alt` banner agar sesuai foto.
- [ ] Mengganti `email@contoh.com` dengan email asli.
- [ ] Menguji semua foto dan musik muncul setelah folder dipindahkan ke komputer lain / dipamerkan.
- [ ] Menguji tampilan di layar yang berbeda (laptop dan HP).

---

## 7. Batasan dan Asumsi

- **Hanya HTML.** Karena tidak memakai JavaScript, formulir tidak bisa menghitung total harga atau menampilkan e-ticket. Data dikirim lewat `mailto:` dan bergantung pada aplikasi email di perangkat pengunjung.
- **Tidak ada pilihan bahasa.** Halaman hanya berbahasa Indonesia.
- **Tidak ada pop-up foto.** Memperbesar foto hanya bisa lewat tautan ke tab baru, bukan lightbox.
- **Lebar tetap.** Tabel kartu memakai lebar tetap sekitar 1260 px, sehingga di layar kecil (HP) halaman perlu digeser ke samping.
- **Atribut lama.** Tag `<font>` dan atribut `bgcolor` sudah usang menurut standar HTML5, tetapi masih berjalan di semua browser utama.
- **Tidak ada backend.** Tidak ada database, login, atau penyimpanan data pemesanan.
- **Harga tiket bersifat estimasi.** Harga pada tabel dan formulir dapat berubah sewaktu-waktu; periksa kembali ke pengelola tiap destinasi.
- **Hak foto.** Pastikan foto yang dipakai milik sendiri atau berlisensi bebas, dan cantumkan sumbernya bila diperlukan.

---

## 8. Rencana Pengembangan (Opsional)

1. **Foto bisa diklik** (prioritas tinggi, paling mudah): bungkus setiap `<img>` dengan `<a href="nama-foto.jpg" target="_blank">`.
2. **Peta lokasi** dengan Google Maps `<iframe>` di bagian destinasi atau pemesanan.
3. **Kontak langsung** lewat tautan WhatsApp (`https://wa.me/62...`) di samping formulir.
4. **FAQ** yang bisa dibuka-tutup dengan `<details>` dan `<summary>`.
5. **Contoh itinerary** 3 hari dan 5 hari dalam bentuk tabel.
6. **Tampilan HP:** jika proyek nantinya boleh memakai CSS, ubah tata letak tabel menjadi grid yang menyesuaikan lebar layar.
