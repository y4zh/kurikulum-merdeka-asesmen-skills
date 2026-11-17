---
name: konverter-smk-mak
description: "Convert a finished Kurikulum Merdeka assessment package for SMK/MAK Fase E-F (Kelas X-XII) into ready-to-use administrative and delivery formats without changing its content: one Kartu Soal per written item or practical task for school administration and supervision files, a print-ready Naskah Ujian with header, instructions, and answer sheet layout, a print-ready Lembar Penilaian Praktik (practical assessment sheet) carrying the performance rubric, time record, and observation notes per student, and CBT/LMS import files in GIFT, Moodle XML, CSV, and the SMK/MAK assessment skill's JSON schema with five-option items, preserving the source package's scoring policy exactly (LMS fraction fields are transport encoding only, summative MCMA stays all-or-nothing) and running a pre-export validation pass that flags missing keys, mismatched option counts, unresolved stimulus references, and leftover placeholders back to the author instead of silently fixing them."
---

# Konverter Naskah Ujian & CBT SMK/MAK

Companion skill to asesmen-smk-mak. The core skill designs the assessment; this skill packages a finished one for SMK/MAK Fase E (Kelas X) and Fase F (Kelas XI-XII). It turns a complete assessment package into the formats schools and exam systems actually consume: Kartu Soal for administration files, a print-ready exam script, a print-ready practical assessment sheet for performance tasks, and import files for CBT and LMS platforms.

Conversion is a packaging job, not an editing job. Wording, keys, scoring, rubrics, and cognitive tags come from the source package and leave unchanged. If something in the source is broken or missing, this skill reports it back instead of repairing it silently.

Format details, templates, and worked examples live in [references/spesifikasi-format-ekspor.md](references/spesifikasi-format-ekspor.md) (Kartu Soal, the print layouts, the Lembar Penilaian Praktik, and GIFT) and [references/spesifikasi-cbt-xml-csv.md](references/spesifikasi-cbt-xml-csv.md) (Moodle XML and CSV).

This skill is one of five for SMK/MAK. Its siblings are asesmen-smk-mak (assessment packages, written and practical), modul-ajar-smk-mak (teaching modules and TP lists), stimulus-smk-mak (workplace stimulus and visuals), and telaah-smk-mak (independent item and rubric review). Stay inside this jenjang: every written item here has 5 options (A-E).

## When this skill applies

- The user has a finished package from asesmen-smk-mak (or an equivalent item and task set) and asks for Kartu Soal, a printable exam script, a practical assessment sheet, or an import file.
- The user asks for a bank soal in GIFT, Moodle XML, CSV, or JSON form, for example for a Moodle-based CBT or another LMS.
- The user wants the same item set in more than one delivery format at once.

It does not apply to writing or improving items, tasks, or rubrics. Send that work to asesmen-smk-mak for design and to telaah-smk-mak for validation; convert only after the set is final.

## Inputs required

Do not start converting until the input has:

1. Item set with stable numbering and one entry per item: stem, stimulus reference where used, options where the format has them. In this jenjang PG and MCMA items carry 5 options (A-E).
2. A key for every objectively scored item, and a scoring guide or rubric for every Uraian item.
3. For every practical task: the work order or task brief, the job specification, the tools and materials list, the time limit, and the performance rubric with its aspects and descriptors.
4. The scoring policy per format, above all the assessment type (diagnostik, formatif, or sumatif), because it decides how MCMA is encoded.
5. Identity data for the headers: school, subject, konsentrasi keahlian where relevant, fase and kelas, semester, assessment type, time allocation.
6. Planning data for Kartu Soal: CP, TP, core material or competency element, and the indicator with its cognitive level per item.
7. Pembahasan per item when the target format carries it (JSON and CSV do; the printed student script never does).

If any of these are absent, list exactly what is missing and stop. A converted file with invented keys or guessed scoring is worse than no file.

## Outputs

Produce only the formats the user asked for:

- Kartu Soal: one card per item, holding identity, planning fields (CP, TP, material or competency element, indicator, Bloom and SOLO levels), the full item, its key, and its score weight or rubric. For a practical task, the card holds the work order, specification, and rubric instead of options and a key. This is the administration and supervision record.
- Naskah Ujian: the student-facing print script for the written sections. Header (kop) with school and exam identity, general instructions, items grouped by format with a short instruction per group, and a separate answer sheet layout for the objective sections. No keys, no pembahasan, no KKTP data anywhere in this document.
- Lembar Penilaian Praktik: the assessor-facing print sheet for a performance task, one per student per task. Identity fields, the task and specification summary, the time record (start, finish, duration), one row per rubric aspect with its descriptors and a score or judgement column, a notes column for observed events (skipped steps, safety incidents), the critical-rule outcome where the package declares one, and the assessor's name and signature line. The layout spec is in the reference file.
- GIFT: plain-text import for Moodle and compatible LMS, one block per item.
- Moodle XML: the same set as a well-formed XML quiz file with a category path that names kurikulum, fase, and cognitive grouping.
- CSV: one row per item with the flattened columns defined in the reference file, including pembahasan and the type-specific key columns.
- JSON: the core skill's schema (metadata, stimulus, items) exactly as defined in asesmen-smk-mak's second reference file, section 8, including the practical-task entry shape. Do not invent a parallel JSON shape.

Practical tasks do not convert into GIFT, Moodle XML, or CSV question rows; an LMS cannot observe a performance. In a mixed delivery, the written items go to the CBT files and the practical tasks go to the Lembar Penilaian Praktik, and the export notes state that split explicitly.

## Scoring conversion rule

The source package's scoring policy governs. Fraction fields in GIFT and Moodle XML are only a transport encoding: they describe how the LMS should add up a response, they are not a new scoring policy, and they never override the policy written in the package.

- PG stays trivial everywhere: full credit for the key, zero for everything else.
- Sumatif MCMA is binary in the package (1 only when every correct option is chosen and no wrong option is chosen, otherwise 0). Encode it all-or-nothing in GIFT and Moodle XML: the correct options share +100 percent in total (each correct option carries 100 divided by the number of correct options), and every wrong option carries -100 percent, so choosing any wrong option cancels the credit from the correct ones. The LMS total for the item is then floored at zero: a response scores the item maximum only when its raw total reaches 100, and 0 otherwise. State this encoding and the floor rule in the export notes that accompany the file.
- Warning that must travel with every sumatif MCMA export: whether the encoding behaves as true all-or-nothing depends on the target LMS. Moodle's multiple-response grading, rounding of repeating fractions such as 33.33333, and negative-total handling differ between versions and question behaviours. Test-import one MCMA item, answer it three ways (fully correct, partially correct with no wrong pick, and correct plus one wrong pick), and confirm the grades are 1, 0, and 0 before importing the whole set.
- Formatif and diagnostik MCMA follow the package's partial 2-1-0 rule. Map it proportionally in the encoding: correct options share the full credit so a fully correct selection earns the maximum, a partial selection with no wrong option earns a proportional share, and any wrong option carries a penalty large enough to bring the total to zero. Say plainly in the export notes that this is a proportional approximation of 2-1-0, because an LMS computes per-option fractions and cannot reproduce the exact three-step scale; the teacher's grade processing still follows the package.
- PGK Kategori keeps its own rule, 1 point per statement judged correctly. Export each statement as its own scorable unit (its own GIFT or XML question, or its own CSV row group) instead of collapsing the item into one all-or-nothing question.
- URO keyword points and URN rubrics do not compress into option fractions. In CBT formats that cannot grade essays automatically, export Uraian as an essay question type with the scoring guide placed in the grader information field, and mark it as manually graded in the export notes.
- Performance rubric scores are never encoded into CBT fractions. They travel only on the Lembar Penilaian Praktik and, when the school records them digitally, as the aspect scores exactly as the assessor entered them.

## Pre-export validation checklist

Run this pass before writing any output file, and report the result with the delivery:

- Every objectively scored item has exactly the key its format requires: one key for PG, a defined key set for MCMA, a category key per statement for PGK Kategori.
- Every Uraian item has its scoring guide or rubric attached; a URN rubric starts at 0.
- Option counts match this jenjang: 5 options (A-E) for every PG and MCMA item, unless the source package states a deliberate deviation. A 4-option item in an SMK/MAK set is a validation failure to report, not to pad silently.
- Every practical task has its work order, specification, tools and materials list, time limit, and rubric; every rubric aspect has tuntas and belum tuntas descriptors, and the safety aspect is present where the task is hazardous.
- Every stimulus_id or stimulus reference in an item resolves to a stimulus that exists in the set, and every stimulus is used by at least one item.
- Item and task numbering is continuous, and the counts match the identity data and the kisi-kisi.
- No leftover placeholders anywhere: no bracketed tokens such as [Nama Sekolah] in a file meant for direct use, no empty option, stem, or pembahasan fields. Placeholders are acceptable only in a template the user explicitly asked for.
- Bloom and SOLO tags are present on every row or record that carries those columns.
- The assessment type is recorded, so the MCMA encoding choice can be checked against it.

Any failure stops the export for the affected items. List the failures by item number and hand them back; do not guess a key, drop an item quietly, or fill a placeholder with invented data.

## Gotchas

- Never change item content during conversion. A stem that looks wrong, a suspect key, a weak distractor, or a vague rubric descriptor gets flagged back to the author or the review skill, not fixed inside the export. A converter that edits silently destroys the audit trail between the validated set and the delivered file.
- XML must be well-formed or the LMS rejects the whole file. Escape ampersands, angle brackets, and quotes in text, or wrap question and answer text in CDATA sections; never mix raw HTML into an unescaped text node. Validate the file's structure before delivering it.
- GIFT has its own escaping: characters such as = ~ # { } and : inside answer text must be backslash-escaped, and an unescaped closing brace ends the answer block early.
- CSV quoting is strict. Wrap any field containing a comma, a quote, or a line break in double quotes, and double every quote inside such a field. Write the file as UTF-8 so Indonesian text survives the round trip, and keep one row per item with no line breaks outside quoted fields.
- Keep keys and pembahasan out of student-facing output. The Naskah Ujian and its answer sheet contain no key material; keys live in Kartu Soal, the scoring guide, and the CBT files only. The Lembar Penilaian Praktik is assessor-facing: it may carry the rubric and specification, but it is never handed to students as their task sheet; the student receives the work order without the descriptors.
- One source, many outputs: generate every requested format from the same validated item set in the same pass, so the print script, the cards, the practical sheets, and the CBT file can never drift into different versions of an item.
