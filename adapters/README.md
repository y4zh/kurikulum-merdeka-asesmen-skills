# Adapter Lintas AI

Satu sumber kebenaran, empat cara memakai. Isi skill hidup di folder `skills/`; folder ini hanya menjelaskan cara memasang ekosistem yang sama di platform AI yang berbeda.

| Platform | Mekanisme | Berkas yang dipakai | Panduan |
| --- | --- | --- | --- |
| Claude (Code, aplikasi, web) | Agent Skills standar: frontmatter `name` + `description` di `SKILL.md` | Folder `skills/` apa adanya | [claude/README.md](claude/README.md) |
| ChatGPT | Custom GPT: kolom Instructions (maks 8.000 karakter) + unggahan Knowledge | [chatgpt/custom-gpt-instructions.md](chatgpt/custom-gpt-instructions.md) ditempel ke Instructions; semua `skills/*/SKILL.md` dan `skills/*/references/*.md` diunggah ke Knowledge | Lihat kepala berkas ChatGPT |
| Gemini | Gem: kolom instruksi + berkas unggahan; Gemini CLI memakai Agent Skills langsung | [gemini/gem-instructions.md](gemini/gem-instructions.md) ditempel ke instruksi Gem; berkas skill diunggah sebagai bahan | Lihat kepala berkas Gemini |
| Muse | Custom skills di `~/workspace/custom-skills/` dengan metadata `skill.yaml` | Folder `skills/` disalin dengan nama garis bawah (peta nama tersedia) | [muse/README.md](muse/README.md) |

Prinsip yang dijaga di semua platform:

- Sejak versi 2.0.0 skill dipecah per jenjang (25 skill: 5 peran × 5 jenjang). Di platform tanpa mekanisme skill (Custom GPT, Gem), instruksi ringkasnya mewajibkan penetapan jenjang di langkah pertama dan memuat tabel parameter per jenjang; berkas Knowledge yang diunggah adalah SKILL.md dan references dari folder jenjang yang relevan.
- Teks instruksi ringkas (ChatGPT dan Gemini) adalah aturan yang selalu aktif; kedalaman materi tetap di berkas skill dan referensinya. Bila keduanya bertentangan, berkas skill yang menang dan perbedaan itu layak dilaporkan sebagai temuan.
- Aturan skor tidak berubah antar platform: MCMA sumatif biner 1-0, formatif 2-1-0, tanpa pecahan bebas di naskah; pecahan pada berkas ekspor CBT hanyalah encoding transport.
- Adapter tidak menambahkan aturan baru. Adapter hanya menerjemahkan cara pemasangan.
