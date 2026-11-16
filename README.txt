HEMAVIA 1.1 — PANDUAN PEMBARUAN

ISI FOLDER
- index.html : struktur dan isi halaman
- style.css  : desain, tata letak, dan responsivitas
- script.js  : navigasi, interaksi, dan kuis
- images/    : ilustrasi yang digunakan website

CARA MENJALANKAN
1. Ekstrak ZIP.
2. Buka index.html di browser untuk melihat website.
3. Pastikan folder images tetap berada satu tingkat dengan index.html.
4. Upload seluruh isi folder (index.html, style.css, script.js, images/) ke repository GitHub.

PENTING UNTUK GITHUB PAGES / NETLIFY
Semua file utama berada di root folder dan sudah menggunakan path relatif:
- style.css
- script.js
- images/nama-file.png

Netlify:
- Build command: kosong
- Publish directory: .
- Pastikan index.html berada di root repository.

MENAMBAHKAN VIDEO YOUTUBE
1. Buka video YouTube yang ingin ditampilkan.
2. Pilih Bagikan > Sematkan (Embed), lalu salin URL pada atribut src iframe.
3. Di index.html, cari bagian id="video" dan ganti blok <div class="video-placeholder">...</div> dengan kode berikut. Ganti VIDEO_ID dengan ID video Anda.

<div class="video-frame">
  <iframe
    src="https://www.youtube-nocookie.com/embed/VIDEO_ID"
    title="Video edukasi HEMAVIA"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
    referrerpolicy="strict-origin-when-cross-origin"
    allowfullscreen>
  </iframe>
</div>

4. Simpan. Tambahkan CSS berikut di bagian paling bawah style.css:

.video-frame {
  position: relative;
  width: 100%;
  max-width: 900px;
  aspect-ratio: 16 / 9;
  margin: auto;
  overflow: hidden;
  border-radius: 24px;
  background: #452D3B;
}
.video-frame iframe {
  width: 100%;
  height: 100%;
  border: 0;
}

CATATAN KONTEN KESEHATAN
- Angka 30,7% ditampilkan sebagai estimasi global perempuan usia 15–49 tahun (2023), bukan khusus remaja.
- Angka 51,4% merujuk pada remaja putri yang tidak mengonsumsi TTD dan menyebut belum mengetahui manfaatnya (SKI 2023).
- Angka prevalensi nasional 18% tidak dimasukkan karena perlu dicocokkan terlebih dahulu dengan tabel primer SKI yang tepat.
- Website merupakan media edukasi, bukan alat diagnosis atau pengganti konsultasi tenaga kesehatan.
- TTD mingguan adalah informasi program pencegahan; bukan dosis pengobatan individual untuk anemia yang sudah terdiagnosis.
- Sebelum publikasi, tinjau kembali referensi dan kebijakan kesehatan terbaru dari WHO dan Kementerian Kesehatan RI.

Selamat mengembangkan HEMAVIA!
