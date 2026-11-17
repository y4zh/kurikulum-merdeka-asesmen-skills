# Adapter Muse

Muse membaca custom skill dari `~/workspace/custom-skills/`. Setiap folder skill di repositori ini sudah membawa `skill.yaml` (metadata Muse: nama, judul, deskripsi, kategori, dan `include_in_prompt`), jadi tidak ada penyesuaian isi yang diperlukan. Satu-satunya perbedaan: nama folder dan kolom `name` di Muse memakai garis bawah (snake_case), sedangkan repositori memakai tanda hubung.

## Peta nama

Sejak versi 2.0.0 ada 25 skill dengan pola nama `<peran>-<jenjang>`. Peta namanya mengikuti satu aturan: ganti tanda hubung dengan garis bawah.

| Pola repositori (`skills/`) | Pola Muse (`~/workspace/custom-skills/`) |
| --- | --- |
| `asesmen-<jenjang>` | `asesmen_<jenjang>` |
| `modul-ajar-<jenjang>` | `modul_ajar_<jenjang>` |
| `stimulus-<jenjang>` | `stimulus_<jenjang>` |
| `telaah-<jenjang>` | `telaah_<jenjang>` |
| `konverter-<jenjang>` | `konverter_<jenjang>` |

dengan `<jenjang>` salah satu dari: `paud-tk`, `sd-mi`, `smp-mts`, `sma-ma`, `smk-mak` (di Muse: `paud_tk`, `sd_mi`, `smp_mts`, `sma_ma`, `smk_mak`). Contoh: `asesmen-sma-ma` menjadi `asesmen_sma_ma`; `konverter-paud-tk` menjadi `konverter_paud_tk`.

## Cara pasang

Salin tiap folder ke nama garis bawahnya, contoh untuk satu skill:

```bash
cp -r skills/asesmen-sma-ma ~/workspace/custom-skills/asesmen_sma_ma
```

Ulangi untuk skill lain yang diperlukan mengikuti pola di atas, lalu mulai percakapan baru agar skill termuat. Frontmatter Agent Skills di kepala `SKILL.md` versi repositori boleh dibiarkan; Muse membaca metadata dari `skill.yaml`. Bila ingin persis sama dengan pemasangan lokal pemilik repo, hapus blok frontmatter itu setelah menyalin.

Catatan: `skill.yaml` pada skill versi 2.0.0 memakai `include_in_prompt: false`. Skill tidak tampil otomatis di prompt, tetapi tetap ditemukan lewat pencarian skill berdasarkan nama jenjang dan perannya.
