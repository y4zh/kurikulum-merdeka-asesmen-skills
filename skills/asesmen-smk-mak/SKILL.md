---
name: asesmen-smk-mak
description: "Design complete Indonesian Kurikulum Merdeka assessment packages for SMK/MAK Fase E-F (Kelas X-XII), general and vocational subjects alike: clarification gate before item writing, CP-TP kisi-kisi, five-option Pusmendik/TKA written item formats (PG, PGK MCMA, PGK Kategori, Benar/Salah, matching, short answer, essay) alongside rubric-scored practical and performance assessment built on workplace criteria (safety/K3, procedure sequence, result accuracy, time, work attitude), Teaching Factory and competency-test readiness contexts, portfolio evidence, dynamic scoring, KKTP rubrics, remedial and enrichment follow-up using Mastery Learning, a mandatory quality self-audit with the key-distribution check, and optional JSON/CSV export for CBT/LMS platforms."
---

# Asesmen SMK/MAK (Fase E-F)

Skill for designing assessment packages and test items for Indonesian vocational schools (SMK/MAK) under Kurikulum Merdeka (Kemendikdasmen), Fase E (Kelas X) and Fase F (Kelas XI-XII). It covers general subjects and vocational subjects (mapel kejuruan in a konsentrasi keahlian) in one jenjang scope, and it treats written items and practical performance assessment as two halves of the same package: identity, kisi-kisi, stimulus and items, answer key and scoring guide, performance rubric, KKTP, remedial and enrichment follow-up, and a quality audit.

Verification status: the core framework claims in this skill have been checked against the primary documents: PPA Edisi Revisi 2025, Desain Pengembangan Soal AKM 2020, Buletin Asesmen Vol-1 2025, Permendikdasmen No. 1 Tahun 2026, and Naskah Akademik Pembelajaran Mendalam. The per-claim status and page citations live in the reference files. One rule is deliberately not a regulation quote: the dynamic MCMA scoring rule (binary 1-0 for sumatif, partial 2-1-0 for formatif and diagnostik) is a practice rule carried from earlier item-writing guidance, not a quotation of the PPA or of the TKA technical guidance; TKA scoring itself is centralized and uses IRT. Before using a package for a high-stakes exam, check any rule you rely on in the official document. Details live in [references/regulasi-dan-format-soal.md](references/regulasi-dan-format-soal.md) and [references/kktp-solo-dan-tindak-lanjut.md](references/kktp-solo-dan-tindak-lanjut.md).

This skill is one of five for SMK/MAK. Its siblings are modul-ajar-smk-mak (teaching modules and TP lists), stimulus-smk-mak (workplace stimulus and visuals), telaah-smk-mak (independent item and rubric review), and konverter-smk-mak (Kartu Soal, print scripts, practical assessment sheets, and CBT exports). Stay inside this jenjang: rules for Fase A-D live in other jenjang skills and never apply here.

## When this skill applies

- The user asks for an assessment package (diagnostik, formatif, or sumatif) for SMK/MAK, Fase E or Fase F, in a general or a vocational subject.
- The user asks for written items in Pusmendik or TKA formats, a CP-TP kisi-kisi matrix, KKTP rubrics, scoring guides, or remedial and enrichment plans for this jenjang.
- The user asks for a practical or performance assessment: a work task, a performance rubric, a product portfolio assessment, or preparation material for a school competency test (uji kompetensi).
- The user asks for a CBT or LMS item-bank export for this jenjang, for example for a school CBT item bank, or works with LOTS, MOTS, HOTS, Bloom levels, or the SOLO taxonomy in an SMK/MAK context.

Indonesia only. The skill is locked to the Indonesian context: Kurikulum Merdeka, Fase E-F, AKM, TKA, and Ujian Sekolah. It does not apply to foreign tests such as SAT, IELTS, or TOEFL, and not to general trivia quizzes.

## Step 1: Clarification gate

If the request is brief (a subject and a topic, nothing more), stop and ask before writing any item. Ask for:

1. Fase, kelas, mata pelajaran, and whether the subject is a general subject or a vocational subject (and if vocational, the konsentrasi keahlian and the competency element).
2. Jenis asesmen: diagnostik, formatif, or sumatif, and whether the result feeds a report card.
3. Composition: how much of the package is written items and how much is practical or performance assessment, or confirmation to use the defaults below.
4. Cognitive target: the default LOTS:MOTS:HOTS split for Fase E-F, or a custom split.
5. KKTP approach: Deskripsi Kriteria, Rubrik, Skala atau Interval Nilai, or Persentase (the four approaches named in PPA Edisi Revisi 2025, p. 48; the PPA list is open, so another approach is allowed).
6. Whether a JSON or CSV export is needed.

Skip the gate when the request already specifies these points, or when the user says to proceed with standard settings. In that case state the defaults you used at the top of the package.

## Step 2: Defaults for Fase E-F

- PG always has 5 options (A-E) in this jenjang. The AKM design ladder sets Kelas 10-12 at 5 options (Desain Pengembangan Soal AKM 2020, printed p. 4), and PG in TKA for SMK/MAK also uses 5 options (Buletin Asesmen Vol-1 2025, p. 12).
- Written items: LOTS:MOTS:HOTS = 20:50:30. This split is derived from the verified AKM Numerasi cognitive distribution for Kelas 11 (Knowing/Applying/Reasoning = 20/50/30; Desain Pengembangan Soal AKM 2020, printed p. 87); it is a school package design default, not an AKM or TKA quota.
- Practical packages: apply the 20:50:30 split to the supporting-knowledge dimension (the written or oral questions around the task). The main score comes from the performance rubric in Step 3, never from the written split.
- Write in standard Indonesian (EYD V), communicative and unambiguous. In the kisi-kisi, each multiple-choice item measures one operational verb (KKO); an essay item may measure more than one.

## Step 3: The vocational half: practical and performance assessment

What makes an SMK/MAK package different from a general-school package is the practical half. Design it with the same rigour as the written half:

- The task is a real work task: produce, repair, assemble, configure, serve, or document something against a job specification, a work order, or a client brief, in the workshop, laboratory, studio, kitchen, or Teaching Factory unit.
- The rubric scores observable work criteria, at minimum: keselamatan kerja (K3) and correct use of protective equipment; urutan prosedur (the work steps in the right order, with the right tools); ketepatan hasil (the product or service meets the specification, tolerance, or standard given); waktu (completion inside the allocated time); and sikap kerja (orderliness, tool care, honesty in reporting results).
- Each rubric aspect carries descriptors for tuntas and belum tuntas, so two assessors watching the same performance reach the same judgement. State any critical rule the school applies, for example that a serious safety violation closes the attempt, as a rule of the package, not as a regulation quote.
- Support competency readiness: align task difficulty with the competency elements of the konsentrasi keahlian, keep a product portfolio (photos, job reports, logbooks) as assessment evidence, and let Teaching Factory orders serve as authentic task contexts. Frame certification-style language as school assessment practice; do not present specific LSP or BNSP rules, because no such rules are in this skill's sources.

## Step 4: Stimulus and visuals

Every item that carries a stimulus must need it. A document, drawing, table, or photo passes only if the item cannot be answered correctly without reading it; decoration fails the audit.

- Vocational stimulus is authentic workplace material: SOP excerpts, work drawings (gambar kerja), equipment manuals, specification tables, work orders, price and stock lists, and short industry case studies. General subjects use informational and literary texts as in other Fase E-F work.
- Group items under a stimulus in small sets (the TKA pattern is 2-6 items per stimulus, Buletin Asesmen Vol-1 2025, p. 11), with cognitive levels graded inside the set.
- Prefer visuals rendered in code when the data is structured: Markdown tables, Mermaid diagrams for work flows and procedures, simple charts, and clean technical sketches.
- Use a real internet image only when the context needs a real photo or phenomenon and an image search tool is available (Wikimedia preferred; the image must match the context exactly). When a visual is too complex to render and no suitable image exists, write a [SPESIFIKASI ILUSTRASI] box instead: visual type, the numbers it must show, labels, legend, and key objects, precise enough for a teacher or illustrator to draw it. The stimulus-smk-mak skill holds the full production guidance for this jenjang.
- As a writing-practice rule, never leak the formula or the work procedure an item is testing into its stimulus; the item then measures copying instead of reasoning. This is a practice consideration of this skill, not an AKM regulation.

## Step 5: Item formats and scoring

Supported written formats: PG (single answer), PGK MCMA (multiple correct answers, checkbox), PGK Kategori (several statements, each judged in a binary category), Benar/Salah, Menjodohkan, Isian or Jawaban Singkat, and Uraian. The non-test family is Unjuk Kerja (practical performance, Step 3), product assessment, and portfolio. Whichever format is chosen, the technique and instrument must stay aligned with the tujuan pembelajaran (Permendikdasmen No. 1 Tahun 2026, Pasal 8).

Scoring rules that must not be improvised:

- PG: 1 for correct, 0 for wrong.
- PGK MCMA is dynamic (a practice rule carried from earlier item-writing guidance; see the second reference file). For sumatif and exams it is binary: 1 only when every correct option is chosen and no wrong option is chosen, otherwise 0. For formatif and diagnostik it is partial 2-1-0: 2 for a fully correct selection, 1 when some correct options are chosen with no wrong option, 0 when any wrong option is chosen. Never use free fractions such as 1/3 or 2/3.
- PGK Kategori: 1 point per statement judged correctly.
- Uraian Objektif (URO): list every keyword or step in the expected answer, 1 point per element present.
- Uraian Non-Objektif (URN): graded rubric built on SOLO levels, and the lowest rubric score is 0, never 1.
- Unjuk Kerja: score per rubric aspect from the observed performance; never convert a rubric judgement into a guessed percentage without the descriptors.

Full construction rules per format are in the first reference file; the scoring and follow-up detail is in the second.

## Step 6: Cognitive levels, KKTP, and follow-up

Tag every written item twice: a Bloom level (C1-C6, grouped as LOTS = C1-C2, MOTS = C3, HOTS = C4-C6) and, for essays and KKTP descriptions, a SOLO level (Prastruktural, Unistruktural, Multistruktural, Relasional, Berpikir Abstrak yang Mendalam). Berpikir Abstrak yang Mendalam is the term the Naskah Akademik Pembelajaran Mendalam uses for the fifth SOLO level (pp. 44-45); "Extended Abstract" is Biggs & Collis's original English term for the same level.

KKTP is descriptive, not one uniform passing number like the old KKM (PPA Edisi Revisi 2025, p. 64). Use the approach chosen at the gate: Deskripsi Kriteria (Perlu bimbingan, Cukup, Baik, Sangat baik, the PPA's labels, p. 64), Rubrik, Skala atau Interval Nilai, or Persentase of TP indicators mastered. For practical assessment, state KKTP as performance descriptors: per rubric aspect, what tuntas work looks like and what belum tuntas work looks like, so the pass decision rests on observed criteria, not on a bare number.

Post-remedial grades follow Prinsip 1, Mastery Learning, the principle this skill adopts: the recorded grade is the highest score the student achieves after remedial. Fairness condition: students who already passed must get an equal chance to improve their score too. The PPA sets no post-remedial grade formula at all: the word "remedial" appears only five times in the whole PPA, and its stated aim for remedial is raising achievement through guided relearning of the unmet criteria, not merely repairing the grade (p. 54). Prinsip 1 is therefore school policy, not a regulation quote, and the package must label it as such. For practical remedial, the student repeats the failed aspects of the task under guidance, not necessarily the whole job. Hard rule: diagnostik and formatif results never determine report grades, promotion, or graduation (PPA Edisi Revisi 2025, p. 44).

## Step 7: Output package

Deliver these parts in order, plus the export when requested:

1. Identitas Asesmen: school (placeholder when unknown), fase and kelas, subject and konsentrasi keahlian where relevant, assessment type, time allocation, item and task count.
2. Matriks Kisi-Kisi: item or task number, Elemen or CP, TP, core material or competency element, indicator with its KKO, cognitive level, format.
3. Naskah Stimulus dan Butir Soal, grouped by format, each group with its work instructions; for practical tasks, the work order, specification, tools and materials list, time limit, and safety notes.
4. Kunci Jawaban dan Pedoman Penskoran, including URO keyword lists, the SOLO rubric for URN, and the full performance rubric for Unjuk Kerja.
5. Rubrik KKTP dan Pengolahan Nilai for the chosen approach, including the per-aspect performance descriptors for practical work.
6. Matriks Tindak Lanjut: remedial and enrichment actions per achievement band, differentiated by content, process, or product; for practical work, which task aspects are repeated or extended.
7. Catatan Telaah Mutu: the self-audit report from Step 8.
8. Optional export: JSON or CSV for a CBT or LMS, using the schema in the second reference file; the konverter-smk-mak skill produces the full delivery set.

## Step 8: Mandatory self-audit

Run the audit before delivering, and print its result as part 7 of the package:

- Key distribution for PG: compute R = (number of PG items / number of options) + 3. No key letter may appear more than R times. Example: 20 items with 5 options gives R = 7, so a key appearing 9 times must be rebalanced.
- Stimulus function test: remove each visual or document mentally. If the item is still answerable, the stimulus fails.
- Distractor and construction check: options homogeneous and similar in length, no "Semua jawaban di atas benar/salah", no double negatives, no item that depends on another item's answer, no formula or procedure leaked into a stimulus, URN rubric minimum is 0.
- Practical check: every rubric aspect is observable during the performance, safety (K3) is scored rather than assumed, the specification the product is judged against is printed in the package, and the time limit is realistic for the task.
- Language and ethics check: standard Indonesian, no SARA content, no violence, no local or cultural bias that advantages one group of students.

## Gotchas

- Do not import rules from other jenjang: in SMK/MAK, PG has 5 options and the written split is 20:50:30, whatever a lower-jenjang package used.
- Do not score practical work with a written-test mindset. A performance is judged against the rubric's work criteria and the job specification, not against a classmate's result.
- Do not present certification-body rules as if they were in this skill's sources. Competency-test readiness is framed as school assessment practice.
- Do not place the tested formula or procedure inside a stimulus.
- Do not start a URN rubric at 1. The minimum is 0.
- Do not present rules beyond their verified status. The framework claims carry page citations in the reference files; the MCMA dynamic scoring rule, the package defaults, and the stimulus length defaults are practice rules or school-package design defaults and must never be presented as regulation.
