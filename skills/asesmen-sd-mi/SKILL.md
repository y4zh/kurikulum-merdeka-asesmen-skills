---
name: asesmen-sd-mi
description: "Design complete Indonesian Kurikulum Merdeka assessment packages for SD/MI only (Fase A-C, Kelas I-VI): a clarification gate before item writing, observation and performance assessment without written tests in Fase A, CP-TP kisi-kisi, item formats fitted to primary school (PG with 3 options in Kelas III and 4 options in Kelas IV-VI, PGK MCMA with dynamic scoring, simple PGK Kategori, Benar/Salah, matching, short answer, short essay, observation), functional stimulus and visuals, Bloom LOTS/MOTS/HOTS combined with SOLO, KKTP rubrics, remedial and enrichment follow-up using Mastery Learning, a mandatory quality self-audit, and optional JSON/CSV export for CBT/LMS platforms."
---

# Asesmen SD/MI (Fase A-C)

Skill for designing assessment packages and test items for Indonesian SD/MI schools (Fase A, B, and C, Kelas I-VI) under Kurikulum Merdeka (Kemendikdasmen). It produces a complete package, not loose questions: identity, kisi-kisi, stimulus and items, answer key and scoring guide, KKTP rubric, remedial and enrichment follow-up, and a quality audit. This skill covers SD/MI only; other jenjang have their own skills.

Verification status: the core framework claims in this skill have been checked against the primary documents: PPA Edisi Revisi 2025, Desain Pengembangan Soal AKM 2020, and Naskah Akademik Pembelajaran Mendalam. The per-claim status and page citations live in the reference files. One rule is deliberately not a regulation quote: the dynamic MCMA scoring rule (binary 1-0 for sumatif, partial 2-1-0 for formatif and diagnostik) is a practice rule carried from earlier item-writing guidance, not a quotation of the PPA or of any national test guidance. Before using a package for a high-stakes exam, check any rule you rely on in the official document. Details live in [references/regulasi-dan-format-soal-sd-mi.md](references/regulasi-dan-format-soal-sd-mi.md) and [references/kktp-solo-dan-tindak-lanjut-sd-mi.md](references/kktp-solo-dan-tindak-lanjut-sd-mi.md).

Sibling skills for this jenjang: modul-ajar-sd-mi plans the teaching and hands over the TP list; stimulus-sd-mi builds the reading passages and visuals; telaah-sd-mi reviews finished items independently; konverter-sd-mi converts a finished package into Kartu Soal, a print script, and CBT import files.

## When this skill applies

- The user asks for an assessment package (diagnostik, formatif, or sumatif) for SD/MI, Fase A, B, or C.
- The user asks for a CP-TP kisi-kisi matrix, KKTP rubrics, scoring guides, or remedial and enrichment plans for Kelas I-VI.
- The user works with LOTS, MOTS, HOTS, Bloom levels, or the SOLO taxonomy for SD/MI students.

Indonesia only. The skill is locked to the Indonesian context: Kurikulum Merdeka, Fase A-C, AKM Kelas 5. It does not apply to other jenjang, foreign tests, or general trivia quizzes.

## Step 1: Clarification gate

If the request is brief (a subject and a topic, nothing more), stop and ask before writing any item. Ask for:

1. Fase, kelas, and mata pelajaran.
2. Jenis asesmen: diagnostik, formatif, or sumatif, and whether the result feeds a report card.
3. Composition: how many items of each format, or confirmation to use the defaults below.
4. Cognitive target: the default LOTS:MOTS:HOTS split for SD/MI, or a custom split.
5. KKTP approach: Deskripsi Kriteria, Rubrik, Skala atau Interval Nilai, or Persentase (the four approaches named in PPA Edisi Revisi 2025, p. 48; the PPA list is open, so another approach is allowed).
6. Whether a JSON or CSV export is needed.

Skip the gate when the request already specifies these points, or when the user says to proceed with standard settings. In that case state the defaults you used at the top of the package.

## Step 2: Defaults for SD/MI

- Fase A (Kelas I-II): formative assessment runs WITHOUT written tests, through observation, performance, or play (PPA Edisi Revisi 2025, p. 45, stated for PAUD and SD in Fase A). Written PG starts at Fase B. Even for sumatif, Fase A prioritises performance, observation, and picture-based items delivered orally.
- PG option counts follow the AKM design ladder (Desain Pengembangan Soal AKM 2020, printed p. 4): Kelas 1-3 use 3 options (A-C), Kelas 4-9 use 4 options (A-D). Applied to SD/MI: Kelas III uses 3 options; Kelas IV-VI use 4 options (A-D).
- Package default of this skill (a school package design default, not an AKM quota): LOTS:MOTS:HOTS = 30:50:20, derived from the verified AKM Numerasi Kelas 5 distribution (Knowing/Applying/Reasoning 30/50/20; Desain Pengembangan Soal AKM 2020, printed p. 87). For Literasi Membaca Kelas 5 the AKM distribution is different: Menemukan Informasi 50%, Memahami 40%, Mengevaluasi dan Merefleksi 10% (printed p. 20). Use the ladder that matches the subject.
- Write in standard Indonesian (EYD V), communicative and unambiguous, with sentences short enough for the fase. In the kisi-kisi, each PG item measures one operational verb (KKO); an essay item may measure more than one.

## Step 3: Stimulus and visuals

Every item that carries a stimulus must need it. A picture, table, or short text passes only if the item cannot be answered correctly without reading it; decoration fails the audit. Stimulus calibration per fase and visual production belong to stimulus-sd-mi; the working rules are:

- Fase A: oral or visual stimulus only, concrete and close to the child's own experience.
- Fase B: one short paragraph or a labelled picture or simple table.
- Fase C: one simple text in a personal or socio-cultural context, supported by a picture or table, with items graded in cognitive level inside a small set.
- As a writing-practice rule, never leak the formula an item is testing into its stimulus, especially in numeracy items; the item then measures copying instead of reasoning. This is a practice consideration of this skill, not an AKM regulation.

## Step 4: Item formats and scoring

Supported formats at SD/MI: PG (single answer), PGK MCMA (multiple correct answers, checkbox), PGK Kategori in a simple form for Fase C (a few statements, each judged Benar/Salah), Benar/Salah, Menjodohkan, Isian or Jawaban Singkat, Uraian pendek, and Observasi or Unjuk Kerja for non-test assessment. Whichever format is chosen, the technique and instrument must stay aligned with the tujuan pembelajaran (Permendikdasmen No. 1 Tahun 2026, Pasal 8).

Scoring rules that must not be improvised:

- PG: 1 for correct, 0 for wrong.
- PGK MCMA is dynamic. For sumatif it is binary: 1 only when every correct option is chosen and no wrong option is chosen, otherwise 0. For formatif and diagnostik it is partial 2-1-0: 2 for a fully correct selection, 1 when some correct options are chosen with no wrong option, 0 when any wrong option is chosen. Never use free fractions such as 1/3 or 2/3.
- PGK Kategori: 1 point per statement judged correctly.
- Uraian Objektif (URO): list every keyword or step in the expected answer, 1 point per element present.
- Uraian Non-Objektif (URN): graded rubric built on SOLO levels, and the lowest rubric score is 0, never 1.

Full construction rules per format are in the first reference file; the scoring and follow-up detail is in the second.

## Step 5: Cognitive levels, KKTP, and follow-up

Tag every item twice: a Bloom level (C1-C6, grouped as LOTS = C1-C2, MOTS = C3, HOTS = C4-C6) and, for essays and KKTP descriptions, a SOLO level (Prastruktural, Unistruktural, Multistruktural, Relasional, Berpikir Abstrak yang Mendalam). Berpikir Abstrak yang Mendalam is the term the Naskah Akademik Pembelajaran Mendalam uses for the fifth SOLO level (pp. 44-45); "Extended Abstract" is Biggs & Collis's original English term for the same level.

KKTP is descriptive, not one uniform passing number like the old KKM (PPA Edisi Revisi 2025, p. 64). Use the approach chosen at the gate: Deskripsi Kriteria (Perlu bimbingan, Cukup, Baik, Sangat baik, the PPA's labels, p. 64), Rubrik, Skala atau Interval Nilai, or Persentase of TP indicators mastered.

Post-remedial grades follow Prinsip 1, Mastery Learning, the principle this skill adopts: the recorded grade is the highest score the student achieves after remedial. Fairness condition: students who already passed must get an equal chance to improve their score too. The PPA sets no post-remedial grade formula at all: the word "remedial" appears only five times in the whole PPA, and its stated aim for remedial is raising achievement through guided relearning of the unmet criteria, not merely repairing the grade (p. 54). Prinsip 1 is therefore school policy, not a regulation quote, and the package must label it as such.

Hard rule: diagnostik and formatif results never determine report grades, promotion, or graduation (PPA Edisi Revisi 2025, p. 44).

## Step 6: Output package

Deliver these seven parts in order, plus the export when requested:

1. Identitas Asesmen: school (placeholder when unknown), fase and kelas, subject, assessment type, time allocation, item count.
2. Matriks Kisi-Kisi: item number, Elemen or CP, TP, core material, indicator with its KKO, cognitive level, item format.
3. Naskah Stimulus dan Butir Soal, grouped by format, each group with its work instructions.
4. Kunci Jawaban dan Pedoman Penskoran, including URO keyword lists and the SOLO rubric for URN.
5. Rubrik KKTP dan Pengolahan Nilai for the chosen approach.
6. Matriks Tindak Lanjut: remedial and enrichment actions per achievement band, differentiated by content, process, or product.
7. Catatan Telaah Mutu: the self-audit report from Step 7.
8. Optional export: JSON or CSV for a CBT or LMS, using the schema in the second reference file. For Kartu Soal, print scripts, and GIFT or Moodle XML, hand the finished package to konverter-sd-mi.

## Step 7: Mandatory self-audit

Run the audit before delivering, and print its result as part 7 of the package:

- Key distribution for PG: compute R = (number of PG items / number of options) + 3. No key letter may appear more than R times. Example: 20 items with 4 options gives R = 8, so a key appearing 10 times must be rebalanced.
- Stimulus function test: remove each visual mentally. If the item is still answerable, the visual fails.
- Distractor and construction check: options homogeneous and similar in length, no "Semua jawaban di atas benar/salah", no double negatives, no item that depends on another item's answer, no formula leaked into a stimulus, URN rubric minimum is 0.
- Language and ethics check: standard Indonesian at the fase's reading level, no SARA content, no violence, no local or cultural bias that advantages one group of students.
- Fase A check: no written formative test anywhere in the package.

## Gotchas

- Do not write PG formative items for Fase A. Fase A formative assessment is observation, performance, or play.
- Do not use formatif or diagnostik results for report grades or promotion decisions.
- Do not give Kelas III four options or Kelas IV-VI three; the ladder is 3 options for Kelas 1-3 and 4 options for Kelas 4-6.
- Do not place the tested formula inside a numeracy stimulus.
- Do not start a URN rubric at 1. The minimum is 0.
- Do not present rules beyond their verified status. The framework claims carry page citations in the reference files; the MCMA dynamic scoring rule and the package defaults are practice rules or school-package design defaults and must never be presented as regulation.
