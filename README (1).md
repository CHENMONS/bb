# Untuk Kamu 🤍 — Website Ucapan Ulang Tahun

Konsep: **buku kenangan digital**. Website satu halaman yang tampil seperti
jurnal/scrapbook — bisa "dibuka" halaman demi halaman, tiap halaman ada slot
foto ala polaroid + tulisan romantis singkat. Tanpa perlu install apa-apa,
tinggal edit teks, taruh foto, lalu upload ke GitHub Pages.

## Struktur file
```
index.html     -> semua halaman (teks, layout, animasi) ada di sini
foto/           -> taruh foto-foto kamu di sini
```

## 1. Ganti teks & urutan halaman
Buka `index.html`, cari bagian `const PAGES = [ ... ]` di paling bawah.
Setiap objek di dalam array itu = satu halaman. Tinggal ubah:
- `title`, `eyebrow`, `text` → tulisan
- `photo` (atau `photos` untuk halaman terakhir) → path ke foto

Mau nambah halaman? Tinggal copy salah satu objek `{ type: "content", ... }`
dan tempel lagi di dalam array, urutannya otomatis mengikuti urutan array.

## 2. Pasang foto
- Simpan foto ke folder `foto/`, beri nama sesuai yang ditulis di `PAGES`
  (misalnya `foto/foto1.jpg`).
- Kalau file foto belum ada / namanya belum cocok, halaman otomatis
  menampilkan kotak placeholder yang rapi — jadi website tetap aman dibuka
  sebelum semua foto siap.
- Format foto potret (4:5) akan terlihat paling pas di slot polaroid-nya.

## 3. Pasang lagu latar (musik romantis)
Website ini sudah punya tombol musik mengambang (ikon equalizer, pojok kanan
atas) dan sudah siap memutar lagu — tinggal kamu isi filenya sendiri, karena
lagu berhak cipta tidak bisa disertakan otomatis di sini.

1. Buat folder `audio/` (sejajar dengan `index.html`).
2. Taruh file lagu kamu di situ dan beri nama **`lagu.mp3`**
   (atau ubah path-nya di `index.html`, cari baris `<audio id="bgAudio" ...>`).
3. Musik akan otomatis mencoba diputar saat orangnya klik **"Buka Halaman"**
   di sampul, dan bisa dinyalakan/dimatikan lewat tombol equalizer kapan saja.
4. Kalau belum ada file lagu, tombolnya tetap muncul tapi tidak melakukan
   apa-apa — tidak akan error di halaman lain.

**Rekomendasi lagu:** pakai lagu yang memang berkesan buat kalian berdua
(lebih personal), atau kalau butuh musik instrumental romantis yang aman
dipakai publik (bebas hak cipta), cari di:
- YouTube Audio Library (musik → mood "Romantic" atau "Sentimental")
- Pixabay Music (pixabay.com/music) — kategori "Romantic" / "Love"
- Uppbeat / Free Music Archive

## 4. Coba dulu di komputer sendiri
Cukup buka file `index.html` langsung di browser (double click) — tidak
butuh server, tidak butuh install apa pun.

## 5. Deploy gratis lewat GitHub Pages
1. Buat repository baru di GitHub (public), misalnya `untuk-kamu`.
2. Upload `index.html`, `README.md`, dan folder `foto/` (beserta isinya)
   ke repo tersebut.
3. Masuk ke **Settings → Pages**.
4. Di bagian **Build and deployment**, pilih **Deploy from a branch**,
   branch **main**, folder **/(root)** → klik **Save**.
5. Tunggu 1–2 menit, link website akan muncul di halaman Pages, formatnya:
   `https://namakamu.github.io/untuk-kamu/`
6. Kirim link itu ke orangnya 🤍

## Ide pengembangan lanjutan (opsional)
- Tambah halaman "tebak-tebakan" atau kuis kecil sebelum halaman terakhir.
- Ganti ikon hati di sampul dengan foto berdua yang bulat (cover polaroid).
