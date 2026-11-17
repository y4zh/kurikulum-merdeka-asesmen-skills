# Changelog

## 2.0.0 - 2026-11-17

Restrukturisasi per jenjang. Lima skill gabungan dipecah menjadi 25 skill: lima peran (asesmen, modul ajar, stimulus, telaah, konverter) untuk masing-masing lima jenjang (PAUD & TK/RA, SD/MI Fase A-C, SMP/MTs Fase D, SMA/MA Fase E-F, SMK/MAK Fase E-F). Setiap skill kini hanya memuat aturan jenjangnya sendiri agar aturan antar jenjang tidak tercampur saat dipakai.

- Penamaan baru mengikuti pola `<peran>-<jenjang>`: asesmen-paud-tk, asesmen-sd-mi, asesmen-smp-mts, asesmen-sma-ma, asesmen-smk-mak, dan pola yang sama untuk modul-ajar-, stimulus-, telaah-, dan konverter-.
- Isi setiap skill adalah versi tersaring dari skill gabungan 1.1.0 (termasuk seluruh sitasi terverifikasi dokumen primer), ditambah kekhasan jenjangnya: PAUD & TK/RA tanpa tes tulis dengan pelaporan BB/MB/BSH/BSB dan konverter dokumen observasi tanpa ekspor CBT; SD/MI dengan tangga opsi kelas 3 = 3 opsi dan kelas 4-6 = 4 opsi serta Fase A tanpa PG tertulis; SMK/MAK dengan komponen asesmen praktik berubrik kriteria pekerjaan (K3, prosedur, ketepatan hasil, waktu, sikap kerja) dan lembar penilaian praktik pada konverternya.
- Skill gabungan lama (asesmen-kurikulum-merdeka, modul-ajar-kurikulum-merdeka, stimulus-dan-ilustrasi-asesmen, telaah-validasi-butir-soal, konverter-naskah-ujian-dan-cbt) dihapus dan digantikan oleh ke-25 skill baru.
- Adapter lintas AI diperbarui ke struktur per jenjang: instruksi ChatGPT dan Gemini kini mewajibkan penetapan jenjang di langkah pertama dan memuat tabel parameter per jenjang; peta nama adapter Muse mengikuti pola garis bawah yang sama.
- Metadata skill.yaml pada skill baru memakai include_in_prompt: false agar daftar skill yang tampil di prompt tetap ringkas; skill ditemukan lewat pencarian berdasarkan nama jenjang dan perannya.

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
