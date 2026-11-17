# Regulasi dan Format Soal

Reference for the asesmen_kurikulum_merdeka skill. Verification status: the framework claims below were checked against the primary documents (PPA Edisi Revisi 2025, Desain Pengembangan Soal AKM 2020, Buletin Asesmen Vol-1 2025, Permendikdasmen No. 1 Tahun 2026, Naskah Akademik Pembelajaran Mendalam) and carry page citations where they are verified. Rules marked as practice rules or package defaults are this skill's working choices, not regulation.

## 1. Regulatory basis

- Panduan Pembelajaran dan Asesmen (PPA), Edisi Revisi 2025.
- Permendikdasmen No. 10/2025 (Standar Kompetensi Lulusan) and No. 12/2025 (Standar Isi).
- Permendikdasmen No. 13/2025 and SK Kepala BSKAP No. 046/H/KR/2025 (CP).
- Permendikdasmen No. 1/2026 (Standar Proses).
- Permendikdasmen No. 9/2025 and No. 9/2026 (TKA and Asesmen Nasional).
- Pusmendik and AKM guidance; Naskah Akademik Pembelajaran Mendalam (BSKAP, 2025).

Known gaps, verified as absences: PPA 2025 gives no standard numeric formula for post-remedial grades (see the second reference file); the TKA guidance gives no manual MCMA scoring rule because TKA scoring is centralized with IRT; and the 2025 documents give no standard stimulus word-count table for every phase.

## 2. Three assessment types

- Diagnostik: maps starting ability before learning. Not graded for report cards. Assessment at the start of the school year is optional; what the PPA emphasises is assessment at the start of a topic or unit, before teaching it (PPA Edisi Revisi 2025, p. 44).
- Formatif: feedback during learning, guides the next teaching step. Not high-stakes; never decides report grades, promotion, or graduation (PPA Edisi Revisi 2025, p. 44). For PAUD and SD in Fase A, formative assessment runs through observation or performance, not written tests (PPA, p. 45).
- Sumatif: measures achievement at the end of a scope or period, and is the type that feeds report-card processing.

The CP-TP-ATP chain drives design: derive TP from CP, sequence them into an ATP, write the kisi-kisi from TP, and set KKTP per TP.

## 3. Item formats and construction rules

### PG (Pilihan Ganda Sederhana)

- Exactly one correct key. Option counts follow the AKM design ladder (Desain Pengembangan Soal AKM 2020, printed p. 4): Kelas 1-3 use 3 options (A-C), Kelas 4-9 use 4 options (A-D), Kelas 10-12 use 5 options (A-E). PG in TKA for SMA/MA/Sederajat and SMK/MAK uses 5 options (Buletin Asesmen Vol-1 2025, p. 12). The package defaults in SKILL.md (SD 4 options, SMP 4 options, SMA and SMK 5 options) are school package design defaults aligned with the Kelas 4-12 part of that ladder, not AKM or TKA quotas.
- Options homogeneous and logical, similar in length. Numbers and times ordered ascending, descending, or chronologically.
- The option "Semua jawaban di atas benar/salah" is forbidden. Distractors must be plausible enough to function, options must not cue each other, and no item may depend on another item's answer.
- Scoring 1 correct, 0 wrong. AKM coding also uses 9 for blank.

### PGK MCMA (Pilihan Ganda Kompleks, multiple answers)

- More than one correct answer, presented with checkboxes and an instruction to choose all correct statements.
- Every option relevant and homogeneous.
- Scoring is dynamic, see the second reference file: binary 1-0 for sumatif, partial 2-1-0 for formatif and diagnostik. Free fractions are not used.

### PGK Kategori

- Several statements under one stem or stimulus, each answered with a radio button in a binary category pair. Keep the two sources apart: in TKA an item carries three statements, with category pairs Benar/Salah, Sesuai/Tidak Sesuai, Setuju/Tidak Setuju, or another category pair (the Buletin's own worked example uses Tepat/Tidak Tepat) (Buletin Asesmen Vol-1 2025, p. 12). The Ya/Tidak pair comes from the AKM design's PGK column format (Desain Pengembangan Soal AKM 2020, printed p. 5), not from the Buletin.
- Each statement is judged independently. Scoring is 1 per correctly judged statement.

### Benar/Salah (single statement)

- One statement, two categories. Guessing chance is 50 percent, so balance true and false keys across the set and randomize their positions.

### Menjodohkan (matching)

- Two columns: numbered stems on the left, lettered options on the right. The AKM design advises (its word is "sebaiknya") that the right column carry more options than the left, so the last pairs cannot be solved by elimination alone; treat this as a design recommendation, not an absolute requirement (Desain Pengembangan Soal AKM 2020, printed p. 5). Sets are homogeneous, parallel, and ordered systematically or chronologically.

### Isian and Jawaban Singkat

- Exactly one definite short answer: a word, a number, or a short phrase. Isian is a statement with a blank; jawaban singkat answers a direct question. The stem gives no clue to the answer.

### Uraian

- Written as a question or a command, with firm limits on what the answer must contain, and always delivered with its scoring guide.
- URO (Uraian Objektif): the guide lists every keyword or step, 1 point each.
- URN (Uraian Non-Objektif): graded SOLO rubric, lowest score 0.

### Observasi and Unjuk Kerja

- The non-test family: observation, performance, play (PAUD and Fase A), plus self and peer assessment at higher phases.
- Every instrument ships with a rubric or observation guide that describes strengths, points to improve, and concrete next steps.
- First choice for Seni Budaya, PJOK, and Fase A, ahead of written tests.

## 4. Stimulus and visual rules

- A stimulus is functional or it fails: the item must be unanswerable, or materially harder, without reading it.
- Visuals must also be clear: readable, with labels and units where the data needs them.
- Three production methods, chosen by context: render in code (Markdown tables, Mermaid diagrams, simple charts); use a contextual internet image when a real photo, map, or phenomenon is needed and search is available (Wikimedia preferred); or write a [SPESIFIKASI ILUSTRASI] box describing the visual precisely for a human illustrator.
- The 2025 documents set no technical graphic specification (no DPI, palette, or font size rule). Suitability is judged qualitatively: functional and clear.
- Practice rule: do not place the formula being tested inside the stimulus; the item then measures copying instead of reasoning. No such prohibition was found in the Desain Pengembangan Soal AKM 2020, so this is a writing-practice consideration, not an AKM rule.

## 5. Stimulus gradation across phases

- PAUD and Fase A: oral or visual, concrete, close to personal experience. No written PG.
- SD upper grades (Kelas V-VI): one simple text, personal or socio-cultural context, supported by a picture or table. No official word limit in the 2025 documents.
- SMP (Fase D): mixed informational texts (procedure, concept) and fiction, with graphics. Complexity sits between SD and SMA.
- SMA and SMK (Fase E-F): single and multi-text stimuli, inter-paragraph conjunctions, contrast between texts. Scope the one verified figure precisely: a passage of 250-300 words with sentences of 8-12 words is the text characteristic for the Bahasa Indonesia test subject in TKA SMA/MA/Sederajat and SMK/MAK (Buletin Asesmen Vol-1 2025, p. 12); it does not set a length for other subjects or phases. A multi-text length of up to 700 words with an infographic is source-reported from ANBK Kelas XI reporting. For other subjects and phases, passage lengths stay this skill's practical defaults, not official rules.
- Grouping: one stimulus serves a single item or a small set; in TKA one stimulus serves 2-6 items (Buletin Asesmen Vol-1 2025, p. 11), with cognitive levels graded inside the set.

## 6. General writing rules

- Material: the item measures the indicator in the kisi-kisi, one KKO per PG item.
- Construction: stem is firm and necessary, options follow the format rules above, key is unambiguous.
- Language: standard Indonesian (EYD V), communicative, no double negatives, no bias by region, culture, or group, no SARA or violent content.

## 7. Working flow, kisi-kisi to item analysis

1. Analyze the CP and derive TP.
2. Build the kisi-kisi matrix.
3. Choose or write the stimulus.
4. Write items with keys and scoring guides.
5. Qualitative review and revision (the self-audit in SKILL.md Step 7).
6. Assemble the set: group by format, number the items, write instructions, prepare the answer sheet, balance PG keys.
7. After administration, quantitative item analysis: validity, reliability, difficulty, discrimination, distractor function. TKA uses IRT centrally.
