---
name: asesmen-sma-ma
description: "Design complete Indonesian Kurikulum Merdeka assessment packages for SMA/MA Fase E-F (Kelas 10-12): clarification gate before item writing, CP-TP kisi-kisi, the full TKA item format set with 5-option PG (PG, PGK MCMA, PGK Kategori, Benar/Salah, matching, short answer, essay), functional stimulus, Bloom LOTS/MOTS/HOTS at the 20:50:30 Fase E-F split combined with SOLO, dynamic MCMA scoring, KKTP rubrics, remedial and enrichment follow-up using Mastery Learning, a mandatory quality self-audit, and optional JSON/CSV export for CBT/LMS platforms."
---

# Asesmen SMA/MA (Fase E-F)

Skill for designing assessment packages and test items for Indonesian SMA/MA under Kurikulum Merdeka (Kemendikdasmen), Fase E (Kelas 10) and Fase F (Kelas 11-12) only. It produces a complete package, not loose questions: identity, kisi-kisi, stimulus and items, answer key and scoring guide, KKTP rubric, remedial and enrichment follow-up, and a quality audit. School packages at this level mirror the TKA formats; TKA scoring itself is centralized and uses IRT, so a school package imitates the formats, never the IRT scoring.

This is one of five SMA/MA skills. Its siblings at this level: modul-ajar-sma-ma (teaching modules and TP lists), stimulus-sma-ma (stimulus texts and visuals), telaah-sma-ma (independent item review), konverter-sma-ma (Kartu Soal, print scripts, and CBT exports). Other levels have their own skill sets; do not import their rules here.

Verification status: the core framework claims in this skill have been checked against the primary documents: PPA Edisi Revisi 2025, Desain Pengembangan Soal AKM 2020, Buletin Asesmen Vol-1 2025, Permendikdasmen No. 1 Tahun 2026, and Naskah Akademik Pembelajaran Mendalam. The per-claim status and page citations live in the reference files. One rule is deliberately not a regulation quote: the dynamic MCMA scoring rule (binary 1-0 for sumatif, partial 2-1-0 for formatif and diagnostik) is a practice rule carried from earlier item-writing guidance, not a quotation of the PPA or of the TKA technical guidance. Before using a package for a high-stakes exam, check any rule you rely on in the official document. Details live in [references/regulasi-dan-format-soal.md](references/regulasi-dan-format-soal.md) and [references/kktp-solo-dan-tindak-lanjut.md](references/kktp-solo-dan-tindak-lanjut.md).

## When this skill applies

- The user asks for an assessment package (diagnostik, formatif, or sumatif) for SMA/MA, Fase E or Fase F.
- The user asks for items in TKA or Pusmendik formats, a CP-TP kisi-kisi matrix, KKTP rubrics, scoring guides, or remedial and enrichment plans for Kelas 10-12.
- The user asks for a CBT or LMS item-bank export of an SMA/MA package.
- The user works with LOTS, MOTS, HOTS, Bloom levels, or the SOLO taxonomy for SMA/MA students.

Indonesia only, SMA/MA only. The skill is locked to Kurikulum Merdeka Fase E-F, AKM Kelas 11, TKA SMA, and Ujian Sekolah at this level. It does not apply to other levels (PAUD, SD/MI, SMP/MTs, SMK/MAK), to foreign tests such as SAT, IELTS, or TOEFL, or to general trivia quizzes.

## Step 1: Clarification gate

If the request is brief (a subject and a topic, nothing more), stop and ask before writing any item. Ask for:

1. Fase (E or F), kelas, and mata pelajaran.
2. Jenis asesmen: diagnostik, formatif, or sumatif, and whether the result feeds a report card.
3. Composition: how many items of each format, or confirmation to use the defaults below.
4. Cognitive target: the default LOTS:MOTS:HOTS split for Fase E-F, or a custom split.
5. KKTP approach: Deskripsi Kriteria, Rubrik, Skala atau Interval Nilai, or Persentase (the four approaches named in PPA Edisi Revisi 2025, p. 48; the PPA list is open, so another approach is allowed).
6. Whether a JSON or CSV export is needed.

Skip the gate when the request already specifies these points, or when the user says to proceed with standard settings. In that case state the defaults you used at the top of the package.

## Step 2: Fase E-F defaults

- PG always has 5 options (A-E) at this level: the AKM design ladder sets Kelas 10-12 at 5 options (Desain Pengembangan Soal AKM 2020, printed p. 4), and PG in TKA for SMA/MA/Sederajat uses 5 options (Buletin Asesmen Vol-1 2025, p. 12).
- Default cognitive split LOTS:MOTS:HOTS = 20:50:30. It is derived from the verified AKM Numerasi distribution for Kelas 11 (Knowing 20 / Applying 50 / Reasoning 30; Desain Pengembangan Soal AKM 2020, printed p. 87) and is a school package design default, not an AKM or TKA quota.
- For Literasi-based packages, the verified Kelas 11 reading distribution is Menemukan Informasi 30%, Memahami 40%, Mengevaluasi dan Merefleksi 30% (Desain Pengembangan Soal AKM 2020, printed p. 20).
- Fase E (Kelas 10) builds the foundation breadth of the subject; Fase F (Kelas 11-12) deepens it toward specialization and TKA readiness. Keep Fase E items closer to guided application and let Fase F carry the full HOTS and multi-text load.

Write in standard Indonesian (EYD V), communicative and unambiguous. In the kisi-kisi, each PG item measures one operational verb (KKO); an essay item may measure more than one.

## Step 3: Stimulus and visuals

Every item that carries a stimulus must need it. A graphic, map, table, or photo passes only if the item cannot be answered correctly without reading it; decoration fails the audit. Detailed calibration for this level lives in the stimulus-sma-ma skill.

- Group items under a stimulus in small sets: in TKA one stimulus serves 2-6 items (Buletin Asesmen Vol-1 2025, p. 11), with cognitive levels graded inside the set.
- Prefer visuals rendered in code when the data is structured: Markdown tables, Mermaid diagrams for flows and cycles, simple charts.
- Use a real internet image only when the context needs a real photo, map, or phenomenon and an image search tool is available. Wikimedia is the preferred source; the image must match the context exactly.
- When a visual is too complex to render and no suitable image exists, write a [SPESIFIKASI ILUSTRASI] box instead: visual type, the numbers it must show, axis labels, legend, and key objects, precise enough for a teacher or illustrator to draw it.
- As a writing-practice rule, never leak the formula an item is testing into its stimulus, especially in numeracy and science items; the item then measures copying instead of reasoning. This is a practice consideration of this skill, not an AKM regulation.

## Step 4: Item formats and scoring

Supported formats, the full TKA set: PG (single answer, 5 options), PGK MCMA (multiple correct answers, checkbox), PGK Kategori (several statements, each judged in a binary category), Benar/Salah, Menjodohkan, Isian or Jawaban Singkat, Uraian, and Observasi or Unjuk Kerja for non-test assessment. Whichever format is chosen, the technique and instrument must stay aligned with the tujuan pembelajaran (Permendikdasmen No. 1 Tahun 2026, Pasal 8).

Scoring rules that must not be improvised:

- PG: 1 for correct, 0 for wrong.
- PGK MCMA is dynamic. For sumatif and exams it is binary: 1 only when every correct option is chosen and no wrong option is chosen, otherwise 0. For formatif and diagnostik it is partial 2-1-0: 2 for a fully correct selection, 1 when some correct options are chosen with no wrong option, 0 when any wrong option is chosen. Never use free fractions such as 1/3 or 2/3. This dynamic rule is a practice rule from earlier item-writing guidance, labelled as such, not a PPA or TKA quotation.
- PGK Kategori: 1 point per statement judged correctly.
- Uraian Objektif (URO): list every keyword or step in the expected answer, 1 point per element present.
- Uraian Non-Objektif (URN): graded rubric built on SOLO levels, and the lowest rubric score is 0, never 1.

Full construction rules per format are in the first reference file; the scoring and follow-up detail is in the second.

## Step 5: Cognitive levels, KKTP, and follow-up

Tag every item twice: a Bloom level (C1-C6, grouped as LOTS = C1-C2, MOTS = C3, HOTS = C4-C6) and, for essays and KKTP descriptions, a SOLO level (Prastruktural, Unistruktural, Multistruktural, Relasional, Berpikir Abstrak yang Mendalam). Berpikir Abstrak yang Mendalam is the term the Naskah Akademik Pembelajaran Mendalam uses for the fifth SOLO level (pp. 44-45); "Extended Abstract" is Biggs & Collis's original English term for the same level. The experience-stage map is: Memahami covers Unistruktural and Multistruktural, Mengaplikasi is Relasional, Merefleksi is Berpikir Abstrak yang Mendalam, and Prastruktural is the status "Belum Memahami" with no stage.

KKTP is descriptive, not one uniform passing number like the old KKM (PPA Edisi Revisi 2025, p. 64). Use the approach chosen at the gate: Deskripsi Kriteria (Perlu bimbingan, Cukup, Baik, Sangat baik, the PPA's labels, p. 64), Rubrik, Skala atau Interval Nilai, or Persentase of TP indicators mastered.

Post-remedial grades follow Prinsip 1, Mastery Learning, the principle this skill adopts: the recorded grade is the highest score the student achieves after remedial. Fairness condition: students who already passed must get an equal chance to improve their score too. The PPA sets no post-remedial grade formula at all: the word "remedial" appears only five times in the whole PPA, and its stated aim for remedial is raising achievement through guided relearning of the unmet criteria, not merely repairing the grade (p. 54). Prinsip 1 is therefore school policy, not a regulation quote, and the package must label it as such.

Hard rule: diagnostik and formatif results never determine report grades, promotion, or graduation (formatif is not high-stakes, PPA Edisi Revisi 2025, p. 44).

## Step 6: Output package

Deliver these seven parts in order, plus the export when requested:

1. Identitas Asesmen: school (placeholder when unknown), fase and kelas, subject, assessment type, time allocation, item count.
2. Matriks Kisi-Kisi: item number, Elemen or CP, TP, core material, indicator with its KKO, cognitive level, item format.
3. Naskah Stimulus dan Butir Soal, grouped by format, each group with its work instructions.
4. Kunci Jawaban dan Pedoman Penskoran, including URO keyword lists and the SOLO rubric for URN.
5. Rubrik KKTP dan Pengolahan Nilai for the chosen approach.
6. Matriks Tindak Lanjut: remedial and enrichment actions per achievement band, differentiated by content, process, or product.
7. Catatan Telaah Mutu: the self-audit report from Step 7.
8. Optional export: JSON or CSV for a CBT or LMS, using the schema in the second reference file. For Kartu Soal, print scripts, or GIFT and Moodle XML, hand the finished package to konverter-sma-ma.

## Step 7: Mandatory self-audit

Run the audit before delivering, and print its result as part 7 of the package:

- Key distribution for PG: compute R = (number of PG items / 5 options) + 3. No key letter may appear more than R times. Example: 20 items with 5 options gives R = 7, so a key appearing 9 times must be rebalanced.
- Stimulus function test: remove each visual mentally. If the item is still answerable, the visual fails.
- Distractor and construction check: options homogeneous and similar in length, no "Semua jawaban di atas benar/salah", no double negatives, no item that depends on another item's answer, no formula leaked into a stimulus, URN rubric minimum is 0.
- Language and ethics check: standard Indonesian, no SARA content, no violence, no local or cultural bias that advantages one group of students.

## Gotchas

- Do not use 3 or 4 options for PG at this level. Fase E-F is 5 options, in school packages and in TKA alike.
- Do not use formatif or diagnostik results for report grades or promotion decisions.
- Do not place the tested formula inside a numeracy or science stimulus.
- Do not start a URN rubric at 1. The minimum is 0.
- Do not present rules beyond their verified status. The framework claims carry page citations in the reference files; the MCMA dynamic scoring rule and the package defaults are practice rules or school-package design defaults and must never be presented as regulation.
- Do not claim a school package reproduces TKA scoring. TKA is scored centrally with IRT; the package borrows its formats only.
