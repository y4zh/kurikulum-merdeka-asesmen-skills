# Regulasi dan Format Soal SMK/MAK

Reference for the asesmen_smk_mak skill, filtered to Fase E-F (Kelas X-XII). Verification status: the framework claims below were checked against the primary documents (PPA Edisi Revisi 2025, Desain Pengembangan Soal AKM 2020, Buletin Asesmen Vol-1 2025, Permendikdasmen No. 1 Tahun 2026, Naskah Akademik Pembelajaran Mendalam) and carry page citations where they are verified. Rules marked as practice rules or package defaults are this skill's working choices, not regulation.

## 1. Regulatory basis

- Panduan Pembelajaran dan Asesmen (PPA), Edisi Revisi 2025.
- Permendikdasmen No. 10/2025 (Standar Kompetensi Lulusan) and No. 12/2025 (Standar Isi).
- Permendikdasmen No. 13/2025 and SK Kepala BSKAP No. 046/H/KR/2025 (CP).
- Permendikdasmen No. 1/2026 (Standar Proses).
- Permendikdasmen No. 9/2025 and No. 9/2026 (TKA and Asesmen Nasional).
- Pusmendik and AKM guidance; Naskah Akademik Pembelajaran Mendalam (BSKAP, 2025).

Known gaps, verified as absences: PPA 2025 gives no standard numeric formula for post-remedial grades (see the second reference file); the TKA guidance gives no manual MCMA scoring rule because TKA scoring is centralized with IRT; and the 2025 documents give no standard stimulus word-count table for every subject.

## 2. Three assessment types

- Diagnostik: maps starting ability before learning, including readiness for workshop practice. Not graded for report cards. Assessment at the start of the school year is optional; what the PPA emphasises is assessment at the start of a topic or unit, before teaching it (PPA Edisi Revisi 2025, p. 44).
- Formatif: feedback during learning, guides the next teaching step. Not high-stakes; never decides report grades, promotion, or graduation (PPA Edisi Revisi 2025, p. 44).
- Sumatif: measures achievement at the end of a scope or period, and is the type that feeds report-card processing. In vocational subjects it normally combines written items with a performance task.

The CP-TP-ATP chain drives design: derive TP from CP, sequence them into an ATP, write the kisi-kisi from TP, and set KKTP per TP. For vocational subjects, the CP element names the competency the task must show, so the kisi-kisi row for a practical task cites the same element as the written rows around it.

## 3. Item formats and construction rules

### PG (Pilihan Ganda Sederhana)

- Exactly one correct key, with 5 options (A-E). Option counts follow the AKM design ladder (Desain Pengembangan Soal AKM 2020, printed p. 4): Kelas 10-12 use 5 options. PG in TKA for SMK/MAK also uses 5 options (Buletin Asesmen Vol-1 2025, p. 12). The 20:50:30 written split in SKILL.md is a school package design default derived from the AKM Numerasi distribution, not an AKM or TKA quota.
- Options homogeneous and logical, similar in length. Numbers, measurements, and times ordered ascending, descending, or chronologically.
- The option "Semua jawaban di atas benar/salah" is forbidden. Distractors must be plausible enough to function, options must not cue each other, and no item may depend on another item's answer.
- Scoring 1 correct, 0 wrong. AKM coding also uses 9 for blank.

### PGK MCMA (Pilihan Ganda Kompleks, multiple answers)

- More than one correct answer, presented with checkboxes and an instruction to choose all correct statements.
- Every option relevant and homogeneous.
- Scoring is dynamic, see the second reference file: binary 1-0 for sumatif, partial 2-1-0 for formatif and diagnostik. Free fractions are not used. This rule is a practice rule from earlier item-writing guidance, not a PPA or TKA quotation.

### PGK Kategori

- Several statements under one stem or stimulus, each answered with a radio button in a binary category pair. Keep the two sources apart: in TKA an item carries three statements, with category pairs Benar/Salah, Sesuai/Tidak Sesuai, Setuju/Tidak Setuju, or another category pair (the Buletin's own worked example uses Tepat/Tidak Tepat) (Buletin Asesmen Vol-1 2025, p. 12). The Ya/Tidak pair comes from the AKM design's PGK column format (Desain Pengembangan Soal AKM 2020, printed p. 5), not from the Buletin.
- Each statement is judged independently. Scoring is 1 per correctly judged statement.

### Benar/Salah (single statement)

- One statement, two categories. Guessing chance is 50 percent, so balance true and false keys across the set and randomize their positions.

### Menjodohkan (matching)

- Two columns: numbered stems on the left, lettered options on the right. The AKM design advises (its word is "sebaiknya") that the right column carry more options than the left, so the last pairs cannot be solved by elimination alone; treat this as a design recommendation, not an absolute requirement (Desain Pengembangan Soal AKM 2020, printed p. 5). Sets are homogeneous, parallel, and ordered systematically or chronologically. A natural vocational use is matching tools, components, or fault symptoms to their functions or causes.

### Isian and Jawaban Singkat

- Exactly one definite short answer: a word, a number with its unit, or a short phrase. Isian is a statement with a blank; jawaban singkat answers a direct question. The stem gives no clue to the answer. For measurement answers, state the accepted unit and tolerance in the key.

### Uraian

- Written as a question or a command, with firm limits on what the answer must contain, and always delivered with its scoring guide.
- URO (Uraian Objektif): the guide lists every keyword or step, 1 point each.
- URN (Uraian Non-Objektif): graded SOLO rubric, lowest score 0.

### Unjuk Kerja, product, and portfolio assessment

- The non-test family for this jenjang: practical performance on a work task, assessment of the finished product or service, and portfolio review of accumulated evidence (job reports, logbooks, product photos, Teaching Factory order records).
- Every instrument ships with a rubric whose aspects are observable during the work: keselamatan kerja (K3), urutan prosedur, ketepatan hasil against the printed specification, waktu, and sikap kerja. Each aspect carries tuntas and belum tuntas descriptors.
- State the safety rule of the package explicitly (for example, which violations stop the attempt) as a package rule. Do not attribute it to a certification body; this skill's sources contain no LSP or BNSP rule set.

## 4. Stimulus and visual rules

- A stimulus is functional or it fails: the item must be unanswerable, or materially harder, without reading it.
- Vocational stimulus is workplace material: SOP excerpts, gambar kerja (work drawings with dimensions and tolerances), equipment manuals, specification tables, work orders, and industry case studies. General-subject stimulus follows the Fase E-F pattern: single and multi-text sets, informational and literary texts, contrast between texts.
- Visuals must also be clear: readable, with labels, units, and tolerances where the data needs them. A dimension or unit the answer depends on must be printed, never implied.
- Three production methods, chosen by context: render in code (Markdown tables, Mermaid diagrams for procedures and work flows, simple charts, technical sketches); use a contextual internet image when a real photo or phenomenon is needed and search is available (Wikimedia preferred); or write a [SPESIFIKASI ILUSTRASI] box describing the visual precisely for a human illustrator. The stimulus-smk-mak skill holds the full production guidance.
- Practice rule: do not place the formula or the work procedure being tested inside the stimulus; the item then measures copying instead of reasoning. No such prohibition was found in the Desain Pengembangan Soal AKM 2020, so this is a writing-practice consideration, not an AKM rule.
- Scope the one verified length figure precisely: a passage of 250-300 words with sentences of 8-12 words is the text characteristic for the Bahasa Indonesia test subject in TKA SMA/MA/Sederajat and SMK/MAK (Buletin Asesmen Vol-1 2025, p. 12); it does not set a length for other subjects. Vocational documents are calibrated by workplace realism (a real SOP excerpt length), not by that figure. A multi-text length of up to 700 words with an infographic is source-reported from ANBK Kelas XI reporting.
- Grouping: one stimulus serves a single item or a small set; in TKA one stimulus serves 2-6 items (Buletin Asesmen Vol-1 2025, p. 11), with cognitive levels graded inside the set.

## 5. General writing rules

- Material: the item measures the indicator in the kisi-kisi, one KKO per PG item.
- Construction: stem is firm and necessary, options follow the format rules above, key is unambiguous.
- Language: standard Indonesian (EYD V), communicative, no double negatives, no bias by region, culture, or group, no SARA or violent content. Technical terms follow the subject's trade usage; gloss a term only when the item does not test that term.

## 6. Working flow, kisi-kisi to item analysis

1. Analyze the CP and derive TP.
2. Build the kisi-kisi matrix, written rows and practical rows together.
3. Choose or write the stimulus; for practical tasks, write the work order and specification.
4. Write items with keys and scoring guides; write the performance rubric with the task.
5. Qualitative review and revision (the self-audit in SKILL.md Step 8; the telaah-smk-mak skill runs the independent second pass).
6. Assemble the set: group by format, number the items, write instructions, prepare the answer sheet, balance PG keys.
7. After administration, quantitative item analysis for written items: validity, reliability, difficulty, discrimination, distractor function. TKA uses IRT centrally.
