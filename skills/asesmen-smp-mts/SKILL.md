---
name: asesmen-smp-mts
description: "Design complete Indonesian Kurikulum Merdeka assessment packages for SMP/MTs (Fase D, Kelas VII-IX): clarification gate before item writing, CP-TP kisi-kisi, Pusmendik item formats with 4-option multiple choice (PG, PGK MCMA, PGK Kategori, Benar/Salah, matching, short answer, essay, project and performance), functional stimulus and visuals, Bloom LOTS/MOTS/HOTS at the 25:50:25 Fase D default combined with SOLO, dynamic MCMA scoring, KKTP rubrics, remedial and enrichment follow-up using Mastery Learning, a mandatory quality self-audit, and optional JSON/CSV export for CBT/LMS platforms."
---

# Asesmen SMP/MTs (Fase D)

Skill for designing assessment packages and test items for Indonesian SMP and MTs under Kurikulum Merdeka (Kemendikdasmen), Fase D only (Kelas VII-IX). It produces a complete package, not loose questions: identity, kisi-kisi, stimulus and items, answer key and scoring guide, KKTP rubric, remedial and enrichment follow-up, and a quality audit.

This skill is one of five for this jenjang. Its siblings are modul-ajar-smp-mts (teaching modules and TP lists), stimulus-smp-mts (stimulus texts and visuals), telaah-smp-mts (independent item review), and konverter-smp-mts (Kartu Soal, print scripts, and CBT exports). Other jenjang have their own skill sets with their own rules; do not borrow rules across jenjang.

Verification status: the core framework claims in this skill have been checked against the primary documents: PPA Edisi Revisi 2025, Desain Pengembangan Soal AKM 2020, Buletin Asesmen Vol-1 2025, Permendikdasmen No. 1 Tahun 2026, and Naskah Akademik Pembelajaran Mendalam. The per-claim status and page citations live in the reference files. One rule is deliberately not a regulation quote: the dynamic MCMA scoring rule (binary 1-0 for sumatif, partial 2-1-0 for formatif and diagnostik) is a practice rule carried from earlier item-writing guidance, not a quotation of the PPA or of the TKA technical guidance; TKA scoring itself is centralized and uses IRT. Before using a package for a high-stakes exam, check any rule you rely on in the official document. Details live in [references/regulasi-dan-format-soal.md](references/regulasi-dan-format-soal.md) and [references/kktp-solo-dan-tindak-lanjut.md](references/kktp-solo-dan-tindak-lanjut.md).

## When this skill applies

- The user asks for an assessment package (diagnostik, formatif, or sumatif) for SMP or MTs, Kelas VII, VIII, or IX.
- The user asks for Fase D items in Pusmendik formats, a CP-TP kisi-kisi matrix, KKTP rubrics, scoring guides, or remedial and enrichment plans.
- The user asks for a CBT or LMS item-bank export for a Fase D package (the conversion itself belongs to konverter-smp-mts).
- The user works with LOTS, MOTS, HOTS, Bloom levels, or the SOLO taxonomy for Fase D learners.

Indonesia only. The skill is locked to the Indonesian context: Kurikulum Merdeka, Fase D, AKM Kelas 8, and Ujian Sekolah at SMP/MTs. It does not apply to other jenjang, to foreign tests such as SAT, IELTS, or TOEFL, or to general trivia quizzes.

## Step 1: Clarification gate

The jenjang and fase are fixed: SMP/MTs, Fase D. If the request is brief (a subject and a topic, nothing more), stop and ask before writing any item. Ask for:

1. Kelas (VII, VIII, or IX) and mata pelajaran.
2. Jenis asesmen: diagnostik, formatif, or sumatif, and whether the result feeds a report card.
3. Composition: how many items of each format, or confirmation to use the defaults below.
4. Cognitive target: the Fase D default LOTS:MOTS:HOTS split of 25:50:25, or a custom split.
5. KKTP approach: Deskripsi Kriteria, Rubrik, Skala atau Interval Nilai, or Persentase (the four approaches named in PPA Edisi Revisi 2025, p. 48; the PPA list is open, so another approach is allowed).
6. Whether a JSON or CSV export is needed.

Skip the gate when the request already specifies these points, or when the user says to proceed with standard settings. In that case state the defaults you used at the top of the package.

## Step 2: Fase D defaults

- Multiple choice at this jenjang has 4 options (A-D). This follows the AKM design ladder (Desain Pengembangan Soal AKM 2020, printed p. 4): Kelas 4-9 use 4 options (A-D). Never write 5-option PG for SMP/MTs.
- LOTS:MOTS:HOTS = 25:50:25. This package default is derived from the verified AKM Numerasi cognitive distribution for Kelas 8 (Knowing 25 / Applying 50 / Reasoning 25; Desain Pengembangan Soal AKM 2020, printed p. 87). It is a school package design default, not an AKM quota.
- For Literasi items, the AKM Kelas 8 distribution is Menemukan Informasi 40%, Memahami 40%, Mengevaluasi dan Merefleksi 20% (printed p. 20); use it to pitch reading items at this jenjang.
- Fase D learners handle abstract reasoning in concrete contexts: mixed informational texts (procedure, concept, fact) and mid-level fiction, data tables, bar and line charts, and cycle diagrams are all in range.

Write in standard Indonesian (EYD V), communicative and unambiguous. In the kisi-kisi, each multiple-choice item measures one operational verb (KKO); an essay item may measure more than one.

## Step 3: Stimulus and visuals

Every item that carries a stimulus must need it. A graphic, map, table, or photo passes only if the item cannot be answered correctly without reading it; decoration fails the audit. Stimulus construction for this jenjang belongs to stimulus-smp-mts; this skill states what the package needs from it.

- Group items under a stimulus in small sets (the TKA pattern is 2-6 items per stimulus, Buletin Asesmen Vol-1 2025, p. 11), with cognitive levels graded inside the set.
- Prefer visuals rendered in code when the data is structured: Markdown tables, Mermaid diagrams for flows and cycles, simple charts.
- Use a real internet image only when the context needs a real photo, map, or phenomenon and an image search tool is available. Wikimedia is the preferred source; the image must match the context exactly.
- When a visual is too complex to render and no suitable image exists, write a [SPESIFIKASI ILUSTRASI] box instead: visual type, the numbers it must show, axis labels, legend, and key objects, precise enough for a teacher or illustrator to draw it.
- As a writing-practice rule, never leak the formula an item is testing into its stimulus, especially in numeracy and science items; the item then measures copying instead of reasoning. This is a practice consideration of this skill, not an AKM regulation.

Gradation and the per-format construction rules are in [references/regulasi-dan-format-soal.md](references/regulasi-dan-format-soal.md).

## Step 4: Item formats and scoring

Supported formats at Fase D: PG (single answer, 4 options), PGK MCMA (multiple correct answers, checkbox), PGK Kategori (several statements, each judged in a binary category), Benar/Salah, Menjodohkan, Isian or Jawaban Singkat, Uraian, and Observasi or Unjuk Kerja and Proyek for non-test assessment. Whichever format is chosen, the technique and instrument must stay aligned with the tujuan pembelajaran (Permendikdasmen No. 1 Tahun 2026, Pasal 8).

Scoring rules that must not be improvised:

- PG: 1 for correct, 0 for wrong.
- PGK MCMA is dynamic. For sumatif and exams it is binary: 1 only when every correct option is chosen and no wrong option is chosen, otherwise 0. For formatif and diagnostik it is partial 2-1-0: 2 for a fully correct selection, 1 when some correct options are chosen with no wrong option, 0 when any wrong option is chosen. Never use free fractions such as 1/3 or 2/3.
- PGK Kategori: 1 point per statement judged correctly.
- Uraian Objektif (URO): list every keyword or step in the expected answer, 1 point per element present.
- Uraian Non-Objektif (URN): graded rubric built on SOLO levels, and the lowest rubric score is 0, never 1.

Full construction rules per format are in the first reference file; the scoring and follow-up detail is in the second.

## Step 5: Cognitive levels, KKTP, and follow-up

Tag every item twice: a Bloom level (C1-C6, grouped as LOTS = C1-C2, MOTS = C3, HOTS = C4-C6) and, for essays and KKTP descriptions, a SOLO level (Prastruktural, Unistruktural, Multistruktural, Relasional, Berpikir Abstrak yang Mendalam). Berpikir Abstrak yang Mendalam is the term the Naskah Akademik Pembelajaran Mendalam uses for the fifth SOLO level (pp. 44-45); "Extended Abstract" is Biggs & Collis's original English term for the same level. The working map is C1-C2 to Unistruktural, C3 to Multistruktural, C4 to Relasional, C5-C6 to Berpikir Abstrak yang Mendalam.

KKTP is descriptive, not one uniform passing number like the old KKM (PPA Edisi Revisi 2025, p. 64). Use the approach chosen at the gate: Deskripsi Kriteria (Perlu bimbingan, Cukup, Baik, Sangat baik, the PPA's labels, p. 64), Rubrik, Skala atau Interval Nilai, or Persentase of TP indicators mastered.

Post-remedial grades follow Prinsip 1, Mastery Learning, the principle this skill adopts: the recorded grade is the highest score the student achieves after remedial. Fairness condition: students who already passed must get an equal chance to improve their score too. The PPA sets no post-remedial grade formula at all: the word "remedial" appears only five times in the whole PPA, and its stated aim for remedial is raising achievement through guided relearning of the unmet criteria, not merely repairing the grade (p. 54). Prinsip 1 is therefore school policy, not a regulation quote, and the package must label it as such.

Hard rule: diagnostik and formatif results never determine report grades, promotion, or graduation (PPA Edisi Revisi 2025, p. 44).

## Step 6: Output package

Deliver these seven parts in order, plus the export when requested:

1. Identitas Asesmen: school (placeholder when unknown), Fase D and kelas, subject, assessment type, time allocation, item count.
2. Matriks Kisi-Kisi: item number, Elemen or CP, TP, core material, indicator with its KKO, cognitive level, item format.
3. Naskah Stimulus dan Butir Soal, grouped by format, each group with its work instructions.
4. Kunci Jawaban dan Pedoman Penskoran, including URO keyword lists and the SOLO rubric for URN.
5. Rubrik KKTP dan Pengolahan Nilai for the chosen approach.
6. Matriks Tindak Lanjut: remedial and enrichment actions per achievement band, differentiated by content, process, or product.
7. Catatan Telaah Mutu: the self-audit report from Step 7.
8. Optional export: JSON or CSV for a CBT or LMS, using the schema in the second reference file. Full conversion to Kartu Soal, print, GIFT, or Moodle XML belongs to konverter-smp-mts.

## Step 7: Mandatory self-audit

Run the audit before delivering, and print its result as part 7 of the package:

- Key distribution for PG: compute R = (number of PG items / number of options) + 3. No key letter may appear more than R times. Example: 20 items with 4 options gives R = 8, so a key appearing 10 times must be rebalanced.
- Stimulus function test: remove each visual mentally. If the item is still answerable, the visual fails.
- Distractor and construction check: options homogeneous and similar in length, no "Semua jawaban di atas benar/salah", no double negatives, no item that depends on another item's answer, no formula leaked into a stimulus, URN rubric minimum is 0.
- Language and ethics check: standard Indonesian, no SARA content, no violence, no local or cultural bias that advantages one group of students.

## Gotchas

- Do not write 5-option PG at this jenjang. Fase D uses 4 options (A-D); the 5-option ladder rung belongs to Kelas 10-12.
- Do not use formatif or diagnostik results for report grades or promotion decisions.
- Do not place the tested formula inside a numeracy or science stimulus.
- Do not start a URN rubric at 1. The minimum is 0.
- Do not import the 250-300 word passage figure into this jenjang. That figure is the text characteristic for the Bahasa Indonesia test subject in TKA at SMA level; Fase D stimulus lengths are the practical defaults of stimulus-smp-mts.
- Do not present rules beyond their verified status. The framework claims carry page citations in the reference files; the MCMA dynamic scoring rule and the package defaults are practice rules or school-package design defaults and must never be presented as regulation.
