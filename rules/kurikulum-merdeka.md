# Kurikulum Merdeka: core rules for AI agents

These rules are always on when this package is installed. They route the work; the
level skills in `skills/` carry the detail.

## Rule 1: Determine the level first

Before any teaching or assessment work, establish the school level (jenjang) from the
request: PAUD & TK/RA, SD/MI, SMP/MTs, SMA/MA, or SMK/MAK. If the level is not stated
and cannot be inferred safely, ask. Then load exactly one level skill and stay inside it:

- PAUD & TK/RA: `skills/kurikulum-merdeka-paud-tk/`
- SD/MI (Fase A-C): `skills/kurikulum-merdeka-sd-mi/`
- SMP/MTs (Fase D): `skills/kurikulum-merdeka-smp-mts/`
- SMA/MA (Fase E-F): `skills/kurikulum-merdeka-sma-ma/`
- SMK/MAK (Fase E-F): `skills/kurikulum-merdeka-smk-mak/`

Never import another level's parameters into a package: option counts, cognitive
proportions, and reporting scales differ per level by design.

## Rule 2: One skill per level, five sections inside

Each level skill is self-contained. Inside it, work in the section that matches the task:
1. Modul Ajar (teaching modules and TP lists), 2. Stimulus & Ilustrasi (stimulus texts and
visuals), 3. Asesmen (assessment packages and items), 4. Telaah (independent item review),
5. Konverter (Kartu Soal, print scripts, practical sheets where relevant, CBT exports).
Read the reference files the section points to before producing output.

## Rule 3: Level parameters at a glance

| Level | PG options | Cognitive default (LOTS:MOTS:HOTS) | Notes |
| --- | --- | --- | --- |
| PAUD & TK/RA | no written tests | n/a | Observation, performance, play, portfolio; report BB/MB/BSH/BSB |
| SD/MI | Kelas 3: 3 options; Kelas 4-6: 4 | 30:50:20 | Fase A formative work uses no written tests |
| SMP/MTs | 4 | 25:50:25 | Fase D |
| SMA/MA | 5 | 20:50:30 | Full TKA formats |
| SMK/MAK | 5 | 20:50:30 (written part) | Adds practical assessment with work-criteria rubrics |

## Rule 4: Do not invent regulations

Framework claims in the skills carry page citations to the primary Kemendikdasmen
documents (PPA Edisi Revisi 2025, Desain Pengembangan Soal AKM 2020, Buletin Asesmen
Vol-1 2025, Permendikdasmen No. 1 Tahun 2026). Rules labelled practice rules or school
policy in a skill (for example dynamic MCMA scoring and the post-remedial Mastery
Learning principle) must be presented with that label, never as regulation quotes.
When a claim has no citation, treat it as unverified and say so.

## Rule 5: Clarify before writing items

When a request names only a subject and a topic, run the clarification gate in the
level skill's Asesmen section (fase, assessment type, composition, cognitive target,
KKTP approach, export needs) before writing any item. When the user asks to proceed
with defaults, state the defaults used at the top of the package.
