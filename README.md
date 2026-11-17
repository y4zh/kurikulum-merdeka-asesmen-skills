# Kurikulum Merdeka Asesmen Skills

Kumpulan Agent Skills untuk merancang perangkat pembelajaran, stimulus, butir soal, audit mutu, dan ekspor bank soal CBT/LMS untuk sekolah Indonesia dengan Kurikulum Merdeka (Kemendikdasmen), dari PAUD sampai Fase A-F.

## Kenapa dipisah per jenjang

Sejak versi 2.0.0 ekosistem ini dipecah per jenjang: **25 skill = 5 jenjang × 5 peran**. Setiap skill hanya memuat aturan jenjangnya sendiri, supaya aturan satu jenjang tidak pernah tercampur ke jenjang lain (jumlah opsi PG, proporsi level kognitif, bentuk soal yang sah, dan cara tindak lanjut semuanya berbeda antar jenjang).

Lima jenjang:

| Kode jenjang | Cakupan | Ciri penentu |
| --- | --- | --- |
| `paud-tk` | PAUD dan TK/RA | Tanpa tes tulis; observasi, unjuk kerja, permainan, portofolio; pelaporan BB/MB/BSH/BSB |
| `sd-mi` | SD/MI, Fase A-C | Fase A tanpa PG tertulis; PG kelas 3 = 3 opsi, kelas 4-6 = 4 opsi; proporsi 30:50:20 |
| `smp-mts` | SMP/MTs, Fase D | PG 4 opsi; proporsi 25:50:25 |
| `sma-ma` | SMA/MA, Fase E-F | PG 5 opsi; proporsi 20:50:30; format TKA lengkap |
| `smk-mak` | SMK/MAK, Fase E-F | PG 5 opsi; proporsi 20:50:30; ditambah asesmen praktik dengan rubrik kriteria pekerjaan |

Lima peran di setiap jenjang, bekerja berurutan:

```text
CP ──► modul-ajar-<jenjang> ──► TP, ATP, modul ajar ──► asesmen-<jenjang> ──► paket asesmen ──► telaah-<jenjang> ──► konverter-<jenjang> ──► Kartu Soal, naskah cetak, CBT
                                        ▲                        ▲
                                        └── stimulus-<jenjang> (wacana dan visual fungsional) ──┘
```

| Peran | Fungsi |
| --- | --- |
| `modul-ajar-<jenjang>` | Menurunkan CP menjadi TP dan ATP, merancang pengalaman Pembelajaran Mendalam (Memahami, Mengaplikasi, Merefleksi) terpetakan ke SOLO, LKPD diferensiasi, dan skenario intervensi kelas dari hasil asesmen. |
| `stimulus-<jenjang>` | Meracik stimulus teks terkalibrasi per jenjang, tabel data, diagram Mermaid, grafik dan diagram SVG fungsional, gambar terkurasi (Wikimedia Commons, BMKG, BPS, BIG), dan kotak [SPESIFIKASI ILUSTRASI]. |
| `asesmen-<jenjang>` | Merakit paket asesmen lengkap: identitas, kisi-kisi CP-TP, bentuk soal yang sah di jenjang itu, penskoran dinamis MCMA, rubrik KKTP, tindak lanjut remedial dan pengayaan Prinsip 1 Mastery Learning, audit mandiri, dan ekspor JSON/CSV opsional. |
| `telaah-<jenjang>` | Penelaah independen: telaah kualitatif Kartu Pusmendik (Materi, Konstruksi, Bahasa), bedah pengecoh dari miskonsepsi murid, dan analisis butir kuantitatif (kesukaran P, daya pembeda D, efektivitas pengecoh) untuk jenjang yang memakai butir soal tertulis. |
| `konverter-<jenjang>` | Mengemas paket jadi Kartu Soal per butir, Naskah Ujian siap cetak, dan berkas impor GIFT, Moodle XML, CSV, atau JSON, tanpa mengubah isi soal dan tanpa mengubah kebijakan skornya. Khusus `konverter-paud-tk`: luaran berupa dokumen observasi dan laporan perkembangan siap pakai, tanpa ekspor CBT. |

Nama folder lengkap mengikuti pola `<peran>-<kode-jenjang>`, misalnya `asesmen-sma-ma`, `modul-ajar-sd-mi`, `konverter-paud-tk`. Daftar lengkapnya ada di folder `skills/`.

## Memakai di AI lain

Ekosistem yang sama dapat dipasang di Claude, ChatGPT, Gemini, dan Muse. Mekanismenya berbeda per platform (Agent Skills, Custom GPT, Gem, custom skills Muse) dan semuanya didokumentasikan di [adapters/](adapters/README.md).

## Landasan yang dirujuk

Alur kerja skill mengacu pada dokumen berikut: Panduan Pembelajaran dan Asesmen Edisi Revisi 2025; Desain Pengembangan Soal AKM 2020; Buletin Asesmen Vol. 1 Tahun 2025; Permendikdasmen No. 10/2025 (SKL); No. 12/2025 (Standar Isi); No. 13/2025 dan SK Kepala BSKAP No. 046/H/KR/2025 (CP); No. 1/2026 (Standar Proses); No. 9/2025 dan No. 9/2026 (TKA dan AN); Naskah Akademik Pembelajaran Mendalam; kaidah penulisan soal Pusmendik.

**Catatan sumber:** klaim kerangka utama dalam repo ini telah diverifikasi terhadap dokumen primer: Panduan Pembelajaran dan Asesmen Edisi Revisi 2025, Desain Pengembangan Soal AKM 2020, Buletin Asesmen Vol. 1 Tahun 2025, Permendikdasmen No. 1 Tahun 2026 tentang Standar Proses, dan Naskah Akademik Pembelajaran Mendalam. Status verifikasi per klaim dicatat di berkas referensi masing-masing skill. Beberapa hal tetap bukan kutipan regulasi: aturan skor dinamis PGK MCMA adalah kaidah praktik dari pedoman penulisan soal terdahulu (penskoran TKA terpusat memakai IRT), dan angka kalibrasi wacana di luar mata uji Bahasa Indonesia TKA adalah default praktis penyusun. Untuk keputusan resmi di sekolah, periksa selalu dokumen aslinya.

## Struktur repo

```text
kurikulum-merdeka-asesmen-skills/
├── README.md
├── LICENSE
├── CHANGELOG.md
├── skills/
│   ├── asesmen-paud-tk/        asesmen-sd-mi/        asesmen-smp-mts/
│   ├── asesmen-sma-ma/         asesmen-smk-mak/
│   ├── modul-ajar-paud-tk/     modul-ajar-sd-mi/     modul-ajar-smp-mts/
│   ├── modul-ajar-sma-ma/      modul-ajar-smk-mak/
│   ├── stimulus-paud-tk/       stimulus-sd-mi/       stimulus-smp-mts/
│   ├── stimulus-sma-ma/        stimulus-smk-mak/
│   ├── telaah-paud-tk/         telaah-sd-mi/         telaah-smp-mts/
│   ├── telaah-sma-ma/          telaah-smk-mak/
│   ├── konverter-paud-tk/      konverter-sd-mi/      konverter-smp-mts/
│   └── konverter-sma-ma/       konverter-smk-mak/
│       (setiap folder: SKILL.md, skill.yaml, references/)
└── adapters/                   (panduan Claude, ChatGPT, Gemini, Muse)
```

## Lisensi

MIT. Lihat [LICENSE](LICENSE).
