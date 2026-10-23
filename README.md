# OmniPOS / SAKAPOS

Aplikasi kasir POS sederhana untuk UMKM di Indonesia yang berjalan sebagai halaman web statis dan dapat dipasang sebagai PWA.

## Fitur utama

- Manajemen produk
  - tambah, ubah, hapus produk
  - harga jual per produk
  - produk dapat diarsipkan
- Penerimaan barang harian
  - catat barang yang diterima setiap hari
  - stok dihitung berdasarkan penerimaan dan penjualan
- Kasir / transaksi penjualan
  - pencarian produk cepat
  - keranjang belanja
  - diskon
  - metode pembayaran: Tunai, Transfer, Lainnya
  - validasi stok sebelum checkout
  - struk otomatis
- Laporan harian
  - ringkasan uang masuk, transaksi, stok masuk, stok terjual
  - riwayat penjualan
  - refund/transaksi dibatalkan
  - ekspor CSV stok dan penjualan
  - bagikan laporan lewat WhatsApp / salin teks
- Pengaturan toko
  - nama toko, nama kasir, lokasi, kontak, Instagram, TikTok
  - pajak
  - tema terang/gelap/sistem
  - backup dan restore data JSON
- PWA
  - dapat diinstall seperti aplikasi
  - dapat dibuka secara offline setelah pertama kali dimuat

## Struktur file

- `omnipos.html` — aplikasi utama
- `index.html` — halaman redirect untuk GitHub Pages
- `manifest.webmanifest` — metadata PWA
- `sw.js` — service worker untuk cache offline
- `icon.svg` — ikon aplikasi
- `README.md` — dokumentasi proyek

## Cara menjalankan

Karena aplikasi ini adalah halaman web statis, Anda bisa menjalankannya dengan dua cara:

### 1. Buka langsung dari browser

Buka file `omnipos.html` secara langsung di browser.

### 2. Jalankan lokal server

Di folder proyek, jalankan:

```bash
python -m http.server 8000
```

Lalu buka:

```text
http://localhost:8000
```

## Deploy ke GitHub Pages

1. Push repository ke GitHub.
2. Buka repository → Settings → Pages.
3. Pilih:
   - Source: Deploy from a branch
   - Branch: `main`
   - Folder: `/root`
4. Simpan.
5. Aplikasi akan tersedia di:

```text
https://<username>.github.io/<repository-name>/
```

Contoh:

```text
https://elkahfi91.github.io/SAKAPOS/
```

## Catatan penting

- Data aplikasi disimpan di `localStorage` browser, bukan di server.
- Jika browser dibersihkan atau data localStorage dihapus, data POS bisa hilang.
- Gunakan fitur backup JSON di menu Pengaturan secara rutin.

## Lisensi

Proyek ini dibuat untuk kebutuhan operasional UMKM dan dapat dikembangkan lebih lanjut sesuai kebutuhan bisnis.
