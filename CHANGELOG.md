# Changelog

## 1.1.0 - 2026-11-17

Pendalaman berbasis verifikasi dokumen primer (Panduan Pembelajaran dan Asesmen Edisi Revisi 2025, Desain Pengembangan Soal AKM 2020, Buletin Asesmen Vol. 1 Tahun 2025, Permendikdasmen No. 1 Tahun 2026, Naskah Akademik Pembelajaran Mendalam).

- Jumlah opsi PG mengikuti tangga Desain AKM 2020: kelas 1-3 = 3 opsi, kelas 4-9 = 4 opsi, kelas 10-12 = 5 opsi. Default paket sekolah sebelumnya kini eksplisit berlabel default desain, dibedakan dari acuan AKM/TKA.
- Tabel proporsi level kognitif Numerasi AKM (30/50/20, 25/50/25, 20/50/30) dan distribusi Literasi Membaca ditambahkan dengan sitasi halaman; default LOTS/MOTS/HOTS dinyatakan sebagai turunannya.
- Atribusi PGK Kategori dipisahkan per sumber (Buletin TKA: 3 pernyataan, Benar/Salah, Sesuai/Tidak Sesuai, Setuju/Tidak Setuju; Ya/Tidak dari Desain AKM). Pola soal grup TKA 2-6 soal per stimulus diberi sitasi; klaim "AKM minimal 3 soal per stimulus" dihapus karena tidak ditemukan di Desain AKM.
- Angka teks 250-300 kata dan kalimat 8-12 kata dipersempit ruang lingkupnya: hanya karakteristik teks mata uji Bahasa Indonesia pada TKA SMA/MA/SMK. Larangan mencantumkan rumus pada soal numerasi ditulis ulang sebagai pertimbangan praktik, bukan aturan resmi. Aturan menjodohkan dilunakkan menjadi anjuran sesuai kata "sebaiknya" di Desain AKM.
- KKTP: nama pendekatan ketiga dilengkapi menjadi "skala atau interval nilai" dan daftar pendekatan dinyatakan terbuka; label kategori rubrik disesuaikan persis ("Perlu bimbingan", "Cukup", "Baik", "Sangat baik"); sel interval 61-80 dikutip presisi; sitasi halaman PPA ditambahkan di seluruh kerangka KKTP, tindak lanjut, dan pengolahan nilai rapor.
- Ketiadaan rumus nilai pasca-remedial di PPA ditegaskan sebagai hasil verifikasi; prinsip pengolahan nilai remedial tetap berlabel kebijakan sekolah.
- SOLO: istilah tingkat kelima mengikuti Naskah Akademik Pembelajaran Mendalam, "Berpikir Abstrak yang Mendalam" ("Extended Abstract" hanya sebagai istilah asli Biggs & Collis), dan pemetaan tahap diperbaiki: Memahami mencakup Unistruktural dan Multistruktural, Mengaplikasi = Relasional, Merefleksi = Berpikir Abstrak yang Mendalam, Prastruktural = status "Belum Memahami".
- Sitasi Permendikdasmen No. 1 Tahun 2026 ditambahkan (Pasal 8: teknik asesmen selaras tujuan pembelajaran; Pasal 15-19: penilaian proses dan refleksi diri pendidik minimal satu kali per semester).
- Catatan sumber di README dan SKILL.md diperbarui dari penafian umum menjadi ringkasan status verifikasi.

## 1.0.1 - 2026-11-17

- Seluruh penyebutan nama proyek atau sekolah tertentu dihapus dari deskripsi dan isi skill. Ekosistem ini universal untuk semua sekolah dan platform CBT/LMS, tidak terikat pada satu produk.
- Catatan asal-usul personal di semua SKILL.md dan berkas referensi dihapus dan diganti catatan sumber yang netral: sitasi regulasi tetap ditandai belum terverifikasi terhadap dokumen resmi Kemendikdasmen, tanpa menyebut nama orang, tanggal, atau percakapan sumber.

## 1.0.0 - 2026-11-17

Rilis pertama.

- Lima skill lengkap dengan SKILL.md ber-frontmatter standar Agent Skills, skill.yaml untuk Muse, dan berkas references masing-masing.
- Adapter lintas AI untuk Claude, ChatGPT (Custom GPT), Gemini (Gem), dan Muse.
- Contoh utuh Geografi Fase F (paket asesmen dan ekspor JSON).
- Koreksi atas draf awal: template SVG diperbaiki (xmlns bersih), angka kalibrasi wacana dilabeli default praktis bukan aturan resmi, encoding MCMA pada ekspor GIFT/Moodle diselaraskan dengan kebijakan skor dinamis skill inti, dan analisis butir dilengkapi aturan kelompok 27% serta kriteria efektivitas pengecoh.
