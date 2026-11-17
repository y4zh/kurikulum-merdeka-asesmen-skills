# Adapter Muse

Muse membaca custom skill dari `~/workspace/custom-skills/`. Setiap folder skill di repositori ini sudah membawa `skill.yaml` (metadata Muse: nama, judul, deskripsi, kategori, dan `include_in_prompt`), jadi tidak ada penyesuaian isi yang diperlukan. Satu-satunya perbedaan: nama folder dan kolom `name` di Muse memakai garis bawah (snake_case), sedangkan repositori memakai tanda hubung.

## Peta nama

| Folder repositori (`skills/`) | Folder Muse (`~/workspace/custom-skills/`) |
| --- | --- |
| `asesmen-kurikulum-merdeka` | `asesmen_kurikulum_merdeka` |
| `modul-ajar-kurikulum-merdeka` | `modul_ajar_kurikulum_merdeka` |
| `stimulus-dan-ilustrasi-asesmen` | `stimulus_dan_ilustrasi_asesmen` |
| `telaah-validasi-butir-soal` | `telaah_validasi_butir_soal` |
| `konverter-naskah-ujian-dan-cbt` | `konverter_naskah_ujian_dan_cbt` |

## Cara pasang

Salin tiap folder ke nama garis bawahnya, contoh untuk skill inti:

```bash
cp -r skills/asesmen-kurikulum-merdeka ~/workspace/custom-skills/asesmen_kurikulum_merdeka
```

Ulangi untuk keempat skill lain mengikuti tabel di atas, lalu mulai percakapan baru agar skill termuat. Frontmatter Agent Skills di kepala `SKILL.md` versi repositori boleh dibiarkan; Muse membaca metadata dari `skill.yaml`. Bila ingin persis sama dengan pemasangan lokal pemilik repo, hapus blok frontmatter itu setelah menyalin.
