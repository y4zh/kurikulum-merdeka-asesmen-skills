# Adapter Claude

Folder `skills/` di repositori ini sudah dalam format Agent Skills standar: setiap `SKILL.md` memiliki frontmatter `name` dan `description`, dan rujukan mendalam ada di folder `references/` masing-masing skill. Tidak ada berkas tambahan yang perlu dibuat.

## Claude Code

Salin folder skill yang diinginkan ke salah satu lokasi:

- Per proyek: `<proyek>/.claude/skills/<nama-skill>/`
- Global untuk semua proyek: `~/.claude/skills/<nama-skill>/`

Contoh untuk kelima skill sekaligus:

```bash
cp -r skills/* ~/.claude/skills/
```

## Claude (aplikasi dan web)

Pada paket yang mendukung pengunggahan skill, unggah folder skill apa adanya (SKILL.md beserta references/). Bila fitur skill tidak tersedia, tempel isi `SKILL.md` skill yang relevan sebagai instruksi proyek dan unggah berkas `references/`-nya sebagai bahan proyek.

## Catatan

- Berkas `skill.yaml` di tiap folder adalah metadata untuk Muse (lihat adapter Muse). Claude mengabaikannya dengan aman.
- Nama folder memakai tanda hubung (hyphen), sesuai kolom `name` pada frontmatter.
