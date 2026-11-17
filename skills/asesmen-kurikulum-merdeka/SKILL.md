---
name: asesmen-kurikulum-merdeka
description: "Design complete Indonesian Kurikulum Merdeka assessment packages for PAUD and Fase A-F: clarification gate before item writing, CP-TP kisi-kisi, Pusmendik/TKA item formats (PG, PGK MCMA, PGK Kategori, Benar/Salah, matching, short answer, essay, observation), functional stimulus and visuals, Bloom LOTS/MOTS/HOTS combined with SOLO, dynamic scoring, KKTP rubrics, remedial and enrichment follow-up using Mastery Learning, a mandatory quality self-audit, and optional JSON/CSV export for CBT/LMS such as NINEXAM."
---

# Asesmen Kurikulum Merdeka

Skill for designing assessment packages and test items for Indonesian schools under Kurikulum Merdeka (Kemendikdasmen), from PAUD through Fase A-F (SD, SMP, SMA, SMK). It produces a complete package, not loose questions: identity, kisi-kisi, stimulus and items, answer key and scoring guide, KKTP rubric, remedial and enrichment follow-up, and a quality audit.

Source note: this skill was rebuilt in Muse's own format from a Gemini research conversation Jennifer shared on 2026-11-17 (title: "Keyword Soal Kurikulum Merdeka"). The regulatory citations it names are Gemini's research output and have not been independently verified against the official Kemendikdasmen documents. Before using a package for a high-stakes exam, check the cited rule in the official document. Details live in [references/regulasi-dan-format-soal.md](references/regulasi-dan-format-soal.md) and [references/kktp-solo-dan-tindak-lanjut.md](references/kktp-solo-dan-tindak-lanjut.md).

## When this skill applies

- The user asks for an assessment package (diagnostik, formatif, or sumatif) for PAUD or Fase A-F.
- The user asks for items in Pusmendik or TKA formats, a CP-TP kisi-kisi matrix, KKTP rubrics, scoring guides, or remedial and enrichment plans.
- The user asks for a CBT or LMS item-bank export, for example for NINEXAM's bank soal.
- The user works with LOTS, MOTS, HOTS, Bloom levels, or the SOLO taxonomy in an Indonesian school context.

Indonesia only. The skill is locked to the Indonesian context: Kurikulum Merdeka, Fase A-F, AKM, TKA, and Ujian Sekolah. It does not apply to foreign tests such as SAT, IELTS, or TOEFL, and not to general trivia quizzes.

## Step 1: Clarification gate

If the request is brief (a subject and a topic, nothing more), stop and ask before writing any item. Ask for:

1. Jenjang, fase, kelas, and mata pelajaran.
2. Jenis asesmen: diagnostik, formatif, or sumatif, and whether the result feeds a report card.
3. Composition: how many items of each format, or confirmation to use the defaults below.
4. Cognitive target: the default LOTS:MOTS:HOTS split for the jenjang, or a custom split.
5. KKTP approach: Deskripsi Kriteria, Rubrik, Interval Nilai, or Persentase.
6. Whether a JSON or CSV export is needed.

Skip the gate when the request already specifies these points, or when the user says to proceed with standard settings. In that case state the defaults you used at the top of the package.

## Step 2: Defaults per jenjang

- SD (Fase B-C): multiple choice has 4 options (A-D). LOTS:MOTS:HOTS = 30:50:20.
- SMP (Fase D): 4 options (A-D). Split 25:50:25.
- SMA and SMK (Fase E-F): 5 options (A-E). Split 20:50:30.
- PAUD and Fase A (Kelas I-II): no written multiple-choice formative test. Use observation, performance, or play, with oral or visual stimulus that is concrete and close to the child's own experience.

Write in standard Indonesian (EYD V), communicative and unambiguous. In the kisi-kisi, each multiple-choice item measures one operational verb (KKO); an essay item may measure more than one.

## Step 3: Stimulus and visuals

Every item that carries a stimulus must need it. A graphic, map, table, or photo passes only if the item cannot be answered correctly without reading it; decoration fails the audit.

- Group items under a stimulus in small sets (the TKA pattern is 2-6 items per stimulus), with cognitive levels graded inside the set.
- Prefer visuals rendered in code when the data is structured: Markdown tables, Mermaid diagrams for flows and cycles, simple charts.
- Use a real internet image only when the context needs a real photo, map, or phenomenon and an image search tool is available. Wikimedia is the preferred source; the image must match the context exactly.
- When a visual is too complex to render and no suitable image exists, write a [SPESIFIKASI ILUSTRASI] box instead: visual type, the numbers it must show, axis labels, legend, and key objects, precise enough for a teacher or illustrator to draw it.
- Never leak the formula an item is testing into its stimulus, especially in numeracy and science items.

Gradation across phases and the per-format construction rules are in [references/regulasi-dan-format-soal.md](references/regulasi-dan-format-soal.md).

## Step 4: Item formats and scoring

Supported formats: PG (single answer), PGK MCMA (multiple correct answers, checkbox), PGK Kategori (several statements, each judged in a binary category), Benar/Salah, Menjodohkan, Isian or Jawaban Singkat, Uraian, and Observasi or Unjuk Kerja for non-test assessment.

Scoring rules that must not be improvised:

- PG: 1 for correct, 0 for wrong.
- PGK MCMA is dynamic. For sumatif and exams it is binary: 1 only when every correct option is chosen and no wrong option is chosen, otherwise 0. For formatif and diagnostik it is partial 2-1-0: 2 for a fully correct selection, 1 when some correct options are chosen with no wrong option, 0 when any wrong option is chosen. Never use free fractions such as 1/3 or 2/3.
- PGK Kategori: 1 point per statement judged correctly.
- Uraian Objektif (URO): list every keyword or step in the expected answer, 1 point per element present.
- Uraian Non-Objektif (URN): graded rubric built on SOLO levels, and the lowest rubric score is 0, never 1.

Full construction rules per format are in the first reference file; the scoring and follow-up detail is in the second.

## Step 5: Cognitive levels, KKTP, and follow-up

Tag every item twice: a Bloom level (C1-C6, grouped as LOTS = C1-C2, MOTS = C3, HOTS = C4-C6) and, for essays and KKTP descriptions, a SOLO level (Prastruktural, Unistruktural, Multistruktural, Relasional, Extended Abstract). The working map is C1-C2 to Unistruktural, C3 to Multistruktural, C4 to Relasional, C5-C6 to Extended Abstract.

KKTP is descriptive, not one uniform passing number like the old KKM. Use the approach chosen at the gate: Deskripsi Kriteria (Perlu Bimbingan, Cukup, Baik, Sangat Baik), Rubrik, Interval Nilai, or Persentase of TP indicators mastered.

Post-remedial grades follow Prinsip 1, Mastery Learning, the principle Jennifer's source conversation settled on: the recorded grade is the highest score the student achieves after remedial. Fairness condition: students who already passed must get an equal chance to improve their score too. Note in the package that the official guidance sets no standard post-remedial formula, so this is school policy, not a regulation quote.

Hard rule: diagnostik and formatif results never determine report grades, promotion, or graduation.

## Step 6: Output package

Deliver these seven parts in order, plus the export when requested:

1. Identitas Asesmen: school (placeholder when unknown), fase and kelas, subject, assessment type, time allocation, item count.
2. Matriks Kisi-Kisi: item number, Elemen or CP, TP, core material, indicator with its KKO, cognitive level, item format.
3. Naskah Stimulus dan Butir Soal, grouped by format, each group with its work instructions.
4. Kunci Jawaban dan Pedoman Penskoran, including URO keyword lists and the SOLO rubric for URN.
5. Rubrik KKTP dan Pengolahan Nilai for the chosen approach.
6. Matriks Tindak Lanjut: remedial and enrichment actions per achievement band, differentiated by content, process, or product.
7. Catatan Telaah Mutu: the self-audit report from Step 7.
8. Optional export: JSON or CSV for a CBT or LMS, using the schema in the second reference file.

## Step 7: Mandatory self-audit

Run the audit before delivering, and print its result as part 7 of the package:

- Key distribution for PG: compute R = (number of PG items / number of options) + 3. No key letter may appear more than R times. Example: 20 items with 5 options gives R = 7, so a key appearing 9 times must be rebalanced.
- Stimulus function test: remove each visual mentally. If the item is still answerable, the visual fails.
- Distractor and construction check: options homogeneous and similar in length, no "Semua jawaban di atas benar/salah", no double negatives, no item that depends on another item's answer, no formula leaked into a stimulus, URN rubric minimum is 0.
- Language and ethics check: standard Indonesian, no SARA content, no violence, no local or cultural bias that advantages one group of students.

## Subject notes

- Seni Budaya and PJOK, and all of Fase A: prefer observation sheets, performance, portfolios, or play over written tests.
- Subjects named in the source design include Geografi, Matematika Wajib and Matematika Tingkat Lanjut, Fisika, Ekonomi, IPA, IPS, and Seni Budaya. Apply the same construction rules to other subjects; state any subject-specific deviation in the audit note.

## Gotchas

- Do not write PG formative items for PAUD or Fase A.
- Do not use formatif or diagnostik results for report grades or promotion decisions.
- Do not place the tested formula inside a numeracy or science stimulus.
- Do not start a URN rubric at 1. The minimum is 0.
- Do not present Gemini's regulatory citations from the source conversation as verified law. Flag any rule the user plans to rely on for verification against the official Kemendikdasmen document.
