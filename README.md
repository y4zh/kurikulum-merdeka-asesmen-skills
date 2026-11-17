# Kurikulum Merdeka Asesmen Skills

A set of AI agent skills for Indonesian Kurikulum Merdeka (Kemendikdasmen) teaching
and assessment work: teaching modules (modul ajar), stimulus design, assessment
writing, item review (telaah), and exam/CBT conversion.

The package is organised as **one self-contained skill per school level**, so the
rules of one level never leak into another. Each level skill holds five sections:
Modul Ajar, Stimulus & Ilustrasi, Asesmen, Telaah, and Konverter, with the detailed
rules in its `references/` folder.

## The five level skills

| Skill | Level | Key parameters |
| --- | --- | --- |
| `kurikulum-merdeka-paud-tk` | PAUD & TK/RA | No written tests; observation and play-based assessment; BB/MB/BSH/BSB reporting |
| `kurikulum-merdeka-sd-mi` | SD/MI (Fase A-C) | Fase A formative without written tests; PG 3 options in Kelas 3, 4 options in Kelas 4-6; 30:50:20 |
| `kurikulum-merdeka-smp-mts` | SMP/MTs (Fase D) | PG 4 options; 25:50:25 |
| `kurikulum-merdeka-sma-ma` | SMA/MA (Fase E-F) | PG 5 options; 20:50:30; full TKA formats |
| `kurikulum-merdeka-smk-mak` | SMK/MAK (Fase E-F) | PG 5 options; 20:50:30 written; practical assessment with work-criteria rubrics |

## Install

This repository is a plugin for several agent platforms; every manifest points at
the same `skills/` folder. See [GUIDE.md](GUIDE.md) for all routes, including:

- Claude Code, Codex, Cursor, Cline, Kimi Code, and generic agent marketplaces
  (manifests in the dot-folders and `package.json`).
- Any Agent Skills client: copy the folders under `skills/`.
- ChatGPT and Gemini: see `adapters/`. For Gemini, upload the single-file build for
  your level from `adapters/gemini/` (one Markdown file per level, references
  included).

The always-on core rules in `rules/` route every task: determine the level first,
then work inside that level's skill.

## Repository structure

```text
skills/            the five level skills (source of truth)
rules/             always-on core rules (Markdown + Cursor .mdc)
.claude-plugin/    Claude Code plugin manifest
.codex-plugin/     Codex plugin manifest
.cursor-plugin/    Cursor plugin manifest
.cline-plugin/     Cline plugin entry point
.kimi-plugin/      Kimi Code plugin manifest
.agents/, .omp-plugin/   marketplace listings
adapters/          ChatGPT, Gemini (incl. single-file builds), Claude, Muse
GUIDE.md           installation and usage guide
ROADMAP.md         what is planned
CONTRIBUTING.md    contribution rules (cite or label, one level per skill)
```

## Verification status

The framework claims in the skills have been checked against the primary
Kemendikdasmen documents: Panduan Pembelajaran dan Asesmen Edisi Revisi 2025,
Desain Pengembangan Soal AKM 2020, Buletin Asesmen dan Tes Kemampuan Akademik
Vol-1 2025, and Permendikdasmen No. 1 Tahun 2026, with page citations kept in the
reference files. Rules that are practice guidance or school policy rather than
regulation (dynamic MCMA scoring, the post-remedial Mastery Learning principle) are
labelled as such inside the skills. A small number of citations (the current BSKAP
Capaian Pembelajaran decision and the Pusmendik review card) have not yet been
independently verified against the official documents; the skills say so where they
rely on them. For high-stakes use, verify against the official documents.

## License

MIT. See [LICENSE](LICENSE).
