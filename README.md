# Kurikulum Merdeka Asesmen Skills

Kumpulan Agent Skills untuk merancang perangkat pembelajaran, stimulus, butir soal, audit mutu, dan ekspor bank soal CBT/LMS untuk sekolah Indonesia dengan Kurikulum Merdeka (Kemendikdasmen), dari PAUD sampai Fase A-F.

Satu ekosistem, lima skill yang bekerja berurutan:

```text
CP ──► modul-ajar ──► TP, ATP, modul ajar ──► asesmen ──► paket asesmen ──► telaah-validasi ──► konverter ──► Kartu Soal, naskah cetak, CBT
                            ▲                      ▲
                            └── stimulus-dan-ilustrasi (wacana dan visual fungsional) ──┘
```

## Kelima skill

| Skill | Peran |
| --- | --- |
| `modul-ajar-kurikulum-merdeka` | Menurunkan CP menjadi TP dan ATP, merancang pengalaman Pembelajaran Mendalam (Memahami, Mengaplikasi, Merefleksi) terpetakan ke SOLO, LKPD diferensiasi, dan skenario intervensi kelas dari hasil asesmen. |
| `stimulus-dan-ilustrasi-asesmen` | Meracik stimulus teks terkalibrasi per fase, tabel data, diagram Mermaid, grafik dan diagram SVG fungsional, gambar terkurasi (Wikimedia Commons, BMKG, BPS, BIG), dan kotak [SPESIFIKASI ILUSTRASI]. |
| `asesmen-kurikulum-merdeka` | Merakit paket asesmen lengkap: identitas, kisi-kisi CP-TP, tujuh bentuk soal Pusmendik/TKA, penskoran dinamis MCMA, rubrik KKTP, tindak lanjut remedial dan pengayaan Prinsip 1 Mastery Learning, audit mandiri, dan ekspor JSON/CSV opsional. |
| `telaah-validasi-butir-soal` | Penelaah independen: telaah kualitatif Kartu Pusmendik (Materi, Konstruksi, Bahasa), bedah pengecoh dari miskonsepsi murid, dan analisis butir kuantitatif (kesukaran P, daya pembeda D, efektivitas pengecoh). |
| `konverter-naskah-ujian-dan-cbt` | Mengemas paket jadi Kartu Soal per butir, Naskah Ujian siap cetak, dan berkas impor GIFT, Moodle XML, CSV, atau JSON, tanpa mengubah isi soal dan tanpa mengubah kebijakan skornya. |

## Memakai di AI lain

Ekosistem yang sama dapat dipasang di Claude, ChatGPT, Gemini, dan Muse. Mekanismenya berbeda per platform (Agent Skills, Custom GPT, Gem, custom skills Muse) dan semuanya didokumentasikan di [adapters/](adapters/README.md).

## Contoh utuh

[examples/geografi-fase-f-mitigasi-bencana/](examples/geografi-fase-f-mitigasi-bencana/) berisi satu paket sumatif Geografi Fase F Kelas XI (5 PG, 2 PGK MCMA, 1 PGK Kategori, 2 Uraian) yang dihasilkan dengan skill inti, lengkap dengan kisi-kisi, pedoman penskoran, catatan telaah mutu, dan berkas `ekspor.json` yang valid.

## Landasan yang dirujuk

Alur kerja skill mengacu pada dokumen berikut, sebagaimana dihimpun dalam riset penyusunannya: Panduan Pembelajaran dan Asesmen Edisi Revisi 2025; Permendikdasmen No. 10/2025 (SKL); No. 12/2025 (Standar Isi); No. 13/2025 dan SK Kepala BSKAP No. 046/H/KR/2025 (CP); No. 1/2026 (Standar Proses); No. 9/2025 dan No. 9/2026 (TKA dan AN); kaidah penulisan soal Pusmendik dan desain AKM.

**Penafian:** sitasi regulasi dalam repo ini berasal dari riset berbantuan AI dan belum diverifikasi baris per baris ke dokumen resmi Kemendikdasmen. Angka kalibrasi wacana di skill stimulus adalah default praktis penyusun, bukan kutipan aturan resmi. Untuk keputusan resmi di sekolah, periksa selalu dokumen aslinya.

## Struktur repo

```text
kurikulum-merdeka-asesmen-skills/
├── README.md
├── LICENSE
├── CHANGELOG.md
├── skills/
│   ├── asesmen-kurikulum-merdeka/        (SKILL.md, skill.yaml, references/)
│   ├── modul-ajar-kurikulum-merdeka/     (SKILL.md, skill.yaml, references/)
│   ├── stimulus-dan-ilustrasi-asesmen/   (SKILL.md, skill.yaml, references/)
│   ├── telaah-validasi-butir-soal/       (SKILL.md, skill.yaml, references/)
│   └── konverter-naskah-ujian-dan-cbt/   (SKILL.md, skill.yaml, references/)
├── adapters/                             (panduan Claude, ChatGPT, Gemini, Muse)
└── examples/
    └── geografi-fase-f-mitigasi-bencana/ (paket-asesmen.md, ekspor.json)
```

## Lisensi

MIT. Lihat [LICENSE](LICENSE).
