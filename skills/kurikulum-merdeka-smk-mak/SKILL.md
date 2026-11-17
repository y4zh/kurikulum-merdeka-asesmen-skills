---
name: kurikulum-merdeka-smk-mak
description: "One jenjang-locked skill for Indonesian Kurikulum Merdeka vocational schools (SMK/MAK, Fase E-F, Kelas X-XII) combining all five roles: teaching modules that derive TP and ATP from CP with deep-learning stages and jobsheet LKPD, authentic workplace stimulus and functional visuals, assessment packages pairing five-option Pusmendik/TKA written items with rubric-scored practical and performance assessment on workplace criteria (safety/K3, procedure sequence, result accuracy against specification, time, work attitude) with Teaching Factory and portfolio contexts, independent Pusmendik-card review of items and performance rubrics with distractor surgery and quantitative item analysis, and conversion to Kartu Soal, print exam scripts, Lembar Penilaian Praktik, and CBT/LMS exports (GIFT, Moodle XML, CSV, JSON), with descriptive KKTP, dynamic MCMA scoring, Mastery Learning follow-up, and a mandatory quality audit."
---

# Kurikulum Merdeka SMK/MAK (Fase E-F)

One skill for Indonesian vocational schools (SMK/MAK) under Kurikulum Merdeka (Kemendikdasmen), Fase E (Kelas X) and Fase F (Kelas XI-XII), covering general subjects and vocational subjects (mapel kejuruan in a konsentrasi keahlian).
It holds all five roles of the assessment workflow in a single jenjang-locked file: (1) teaching modules, (2) stimulus and illustration, (3) assessment packages, (4) independent review and validation, and (5) conversion to print and CBT formats.
Because everything for this jenjang lives in one skill, no rule from another jenjang can leak in: PG here always has 5 options, the written cognitive split is 20:50:30, and practical performance assessment stands beside written items as an equal half of every package.
Indonesia only: Kurikulum Merdeka, Fase E-F, AKM, TKA, and Ujian Sekolah. It does not apply to foreign tests such as SAT, IELTS, or TOEFL, and not to general trivia quizzes.

## Cara memakai skill ini

Find the role for the task, read that section, and open its reference files before producing output.
The roles chain in order: a modul ajar produces the TP list, stimulus is built against the kisi-kisi, the assessment section assembles the package, telaah reviews it independently, and the konverter packages the final set.

| Tugas | Bagian | Berkas referensi |
| --- | --- | --- |
| Modul ajar, CP menjadi TP dan ATP, LKPD jobsheet, skenario kelas dari hasil asesmen | 1. Modul Ajar | [references/modul-ajar-kerangka-pembelajaran-mendalam.md](references/modul-ajar-kerangka-pembelajaran-mendalam.md) |
| Stimulus, dokumen kerja, gambar kerja, tabel data, visual fungsional | 2. Stimulus & Ilustrasi | [references/stimulus-panduan-visual-dan-wacana.md](references/stimulus-panduan-visual-dan-wacana.md) |
| Paket asesmen diagnostik, formatif, sumatif; butir tulis; tugas praktik dan rubrik unjuk kerja; KKTP dan tindak lanjut | 3. Asesmen | [references/asesmen-regulasi-dan-format-soal.md](references/asesmen-regulasi-dan-format-soal.md), [references/asesmen-kktp-solo-dan-tindak-lanjut.md](references/asesmen-kktp-solo-dan-tindak-lanjut.md) |
| Telaah butir soal dan rubrik praktik, bedah pengecoh, analisis butir kuantitatif | 4. Telaah & Validasi | [references/telaah-kartu-telaah-pusmendik.md](references/telaah-kartu-telaah-pusmendik.md) |
| Kartu Soal, Naskah Ujian cetak, Lembar Penilaian Praktik, ekspor GIFT, Moodle XML, CSV, JSON | 5. Konverter Naskah, Praktik & CBT | [references/konverter-spesifikasi-format-ekspor.md](references/konverter-spesifikasi-format-ekspor.md), [references/konverter-spesifikasi-cbt-xml-csv.md](references/konverter-spesifikasi-cbt-xml-csv.md) |

Verification status, stated once for the whole skill: the core framework claims have been checked against the primary documents: PPA Edisi Revisi 2025, Desain Pengembangan Soal AKM 2020, Buletin Asesmen Vol-1 2025, Permendikdasmen No. 1 Tahun 2026, and Naskah Akademik Pembelajaran Mendalam; per-claim status and page citations live in the reference files.
Rules that are deliberately not regulation quotes are labelled where they appear: the dynamic MCMA scoring rule (a practice rule from earlier item-writing guidance; TKA scoring itself is centralized and uses IRT), the package design defaults, and the stimulus length defaults.
Two things carry a weaker status and must be flagged wherever a formal document relies on them: the CP citation (SK Kepala BSKAP No. 046/H/KR/2025) has not been independently verified, and the telaah card content has not been independently checked against the official Pusmendik documents; the 27 percent group split and the 5 percent distractor criterion in section 4 are classical test theory conventions, adopted as this skill's working standards.
Before using a package for a high-stakes exam, check any rule you rely on in the official document.

## 1. Modul Ajar

This role works upstream of assessment: it turns a Capaian Pembelajaran (CP) into Tujuan Pembelajaran (TP), orders the TP into an Alur Tujuan Pembelajaran (ATP), and builds the learning experiences, jobsheets, and formative checkpoints that make those TP reachable in the classroom, the workshop, and the Teaching Factory unit.
It has two modes. Standalone mode: the user asks only for teaching planning; deliver the modul ajar package and stop, without adding test items.
Invoked mode: the deliverable that matters most is the TP list, each TP one measurable statement tagged with its CP element, its ATP position, its target SOLO level, the Dimensi Profil Lulusan it serves, and whether its evidence is written, practical, or both; section 3 builds the kisi-kisi and rubrics from it, so a vague TP list makes the whole chain vague.
Writing exam items or graded tasks inside a modul ajar is out of scope here; that is section 3's work.

Workflow:

1. Read the CP: element, phase (E or F), competencies and content. In vocational subjects the CP element names a competency of the konsentrasi keahlian; keep that wording intact. If the CP text (or at least subject, fase, and topic) is missing, ask before planning. Never invent CP wording and present it as official text; label paraphrases as paraphrases.
2. Derive TP: one verb, one content focus, one TP per statement, observable and checkable. For practical competencies the verb names the work performance (memasang, mengkalibrasi, mendiagnosis, menyajikan) together with the standard it must meet. Usually two to five TP per meeting sequence. Never stack verbs in one TP ("memahami dan menganalisis dan mengevaluasi"); split it.
3. Order the ATP: concrete to abstract, single-aspect to integrated, and in vocational subjects from guided basic operations toward independent complete jobs, so the order itself scaffolds learning.
4. Map each TP to a target SOLO level and one or two Dimensi Profil Lulusan. A TP that maps to neither is probably filler; rewrite or drop it. The mapping follows the Naskah Akademik Pembelajaran Mendalam (Tabel 3.1, pp. 44-45): Memahami covers Unistruktural and Multistruktural together, Mengaplikasi is Relasional, Merefleksi is Berpikir Abstrak yang Mendalam, and Prastruktural is not a stage but the status "Belum Memahami".
5. Design the three experience stages. Memahami: students meet the phenomenon, text, work drawing, or job specification and name the key facts, components, and safety requirements (SOLO: Unistruktural moving to Multistruktural). Mengaplikasi: students use the concept on a real case or carry out the job itself: a project, a workshop task against a specification, a Teaching Factory order (SOLO: Relasional). Merefleksi: students evaluate their own product and process, defend a quality judgement, diagnose what went wrong, or transfer the procedure to a new job variant (SOLO: Berpikir Abstrak yang Mendalam, the Naskah Akademik's term for the fifth SOLO level; "Extended Abstract" is Biggs & Collis's original English term). State for each stage what the teacher does, what the students do, and what product or answer shows the stage worked. Never skip Merefleksi to save time.
6. Place formative checkpoints between stages: a short check tied to one TP (an exit question, an observed work step, a measurement result, one jobsheet section) that catches a misconception or a faulty work habit before the sumatif does. The technique and instrument must stay aligned with the TP (Permendikdasmen No. 1 Tahun 2026, Pasal 8); the checkpoint's format, rubric, and scoring belong to section 3, here state only the evidence it must produce.
7. Plan differentiation before it is needed: a simplified entry point (fewer variables, a partly completed job, a worked example, guided first steps at the bench) and an extension (tighter tolerance, an open fault to diagnose, a real client order, a transfer job). Differentiate content, process, and support; never differentiate the KKTP expectation or the final grade standard.
8. Hand off: close with the clean TP list plus the misconception and work-habit watchlist the checkpoints watch for.

Output structure of a modul ajar, in order:

1. Identitas: school (placeholder when unknown), subject, konsentrasi keahlian, fase and kelas, semester, time allocation, meetings.
2. CP and element, quoted or labelled as paraphrased, with the source supplied.
3. TP list with evidence type per TP (written, practical, or both).
4. ATP sequence and why that order.
5. Dimensi Profil Lulusan targets, claimed only where an activity genuinely shows them (in vocational units Kesehatan carries workshop safety culture; Kolaborasi and Komunikasi carry teamwork and client-facing work); never claim all eight.
6. Learning experiences per meeting in the three stages, with teacher activity, student activity, and evidence.
7. LKPD plan in jobsheet form: aim, tools and materials, safety notes, work steps, observation or measurement table, conclusion questions, the TP each part serves, and simplified and challenge variants. Never drop the safety briefing from a practical plan; in this jenjang K3 is part of the competency, not an administrative extra.
8. Formative checkpoints: placement, TP checked, evidence expected.
9. Reflection instruments, teacher and student sets from the reference file; the teacher set serves the process assessment of Permendikdasmen No. 1 Tahun 2026, Pasal 15-19, which includes teacher self-reflection at least once per semester.
10. Handoff block: the TP list and the watchlist, formatted for section 3.

From assessment bands to classroom scenarios: when results come back grouped by KKTP descriptive band, turn each band into a runnable scenario (activity, material, grouping, exit evidence), not a table that repeats the bands.

- Perlu bimbingan (Prastruktural to Unistruktural): reteach or re-demonstrate in a smaller step, simplified jobsheet variant, worked example or guided first job, short supervised practice with the teacher or a trained peer tutor at the bench. Exit evidence: the student states the concept, names the safety requirements, and completes one guided job unaided.
- Cukup (Multistruktural): a connecting task: concept map, compare-two-cases, or the standard jobsheet with the linking and measurement sections emphasised. Exit evidence: the student explains how two parts relate and the product meets most of the specification.
- Baik (Relasional): no reteaching; move to the next TP at full difficulty against the full specification. Exit evidence comes from the next unit's first checkpoint.
- Sangat baik (Berpikir Abstrak yang Mendalam): a transfer or challenge task from the extension variant, or peer tutoring of the first group when tutoring requires explaining and justifying.

Keep section 3's grade rules intact while planning: remedial grades follow Prinsip 1, practical remedial repeats only the failed rubric aspects, and formatif results never decide report grades or promotion. The scenarios change the teaching, not the grade policy.

## 2. Stimulus & Ilustrasi

This role supplies the raw material of section 3: the stimulus texts, workplace documents, and visuals students must read or interpret. A weak stimulus caps every item built on it, so stimulus work comes before item writing.
Two modes. Standalone mode: deliver the calibrated text, document, or visual, its source or data note, and the list of key objects, then stop.
Invoked mode: section 3 calls this role after the kisi-kisi exists; the input is the kisi-kisi rows (indicator, KKO, target Bloom and SOLO level, subject, competency element) and the output is one stimulus per item group, pitched so the target level is reachable: a Relasional item needs parts that must be connected, a Berpikir Abstrak yang Mendalam item needs material that supports transfer to a new case or a fault not shown directly.

The functionality test governs everything: cover the stimulus up. If the item can still be answered correctly without reading it, the stimulus fails and gets rebuilt or cut.

- A functional visual holds data the student must extract, compare, or transform: a dimension on a work drawing, a value on a curve, a stage in a work flow.
- A functional document carries the facts, limits, or evidence the item reasons about: a tolerance in the SOP, a rating on the nameplate, a stock figure in the table.
- Name the key objects a student must read (the specific numbers, labels, dimensions, arrows, or legend entries the answer depends on) and list them with the stimulus. If you cannot name them, the visual is decoration.

For vocational subjects the default stimulus is an authentic document of the world of work, trimmed to what the item needs but never falsified:

- SOP and work instruction excerpts: numbered steps, warnings, and the one step or limit the item turns on.
- Gambar kerja (work drawings): orthographic views, sections, dimensions, and tolerances the student must read to choose, compute, or judge.
- Equipment manuals and nameplates: operating limits, maintenance intervals, ratings, and fault tables.
- Specification and data tables: material specifications, price and stock lists, measurement results, service schedules.
- Industry case studies: a short account of a real-shaped workplace problem (a rejected product batch, a recurring machine fault, a customer complaint) with the data needed to analyse it.

Safety is a working context, not decoration: where a document carries K3 warnings, protective-equipment requirements, or prohibition signs, keep them accurate and let items test them when the kisi-kisi targets safety. Never invent a safety limit; use the standard value the subject teaches or label the document as simulated.
For general subjects use the Fase E-F pattern: single and multi-text stimuli, informational and literary texts, inter-paragraph conjunctions, contrast between texts.
One stimulus serves one item or a small graded set (in TKA, one stimulus serves 2-6 items, Buletin Asesmen Vol-1 2025, p. 11); do not stretch one document across a whole exam.
Write in standard Indonesian (EYD V), keeping the trade's technical terms, in realistic Indonesian contexts: workshops and small industries, customer orders, local markets and prices, weather and seasons, national statistics.

Produce visuals in this order and stop at the first method that yields a functional, readable visual:

1. Render in code: Markdown tables for specification and multi-variable data, Mermaid for work flows, procedures, and cycles, clean SVG for charts, diagrams, and simplified technical sketches. Code-rendered visuals are exact, editable, and print-safe, so they are the default. The reference file holds a Mermaid production-flow template and a corrected SVG two-axis template to adapt, never to ship unchanged with their example numbers.
2. Curate a real image when the item needs a real photo, map, or phenomenon code cannot draw honestly: Wikimedia Commons (open-licensed photos and diagrams), BMKG (weather and earthquake material), BPS (official statistics), BIG (Indonesian base maps). Cite the source under the visual, every time; never use an image whose licence or origin is unclear when an open source can supply an alternative.
3. Write a [SPESIFIKASI ILUSTRASI] box when the visual is too complex to render and no suitable image exists; real gambar kerja with full dimensioning usually lands here. The box states the visual type, the views required, the key objects, the mandatory labels and dimensions, and the function the item depends on, precisely enough for a teacher or illustrator to produce it; the exact block format is in the reference file.

Whichever method is used, the visual ships with axis labels, units, tolerances where they carry meaning, a legend where symbols or colours carry meaning, and a title or caption. Keep it readable at print size: labels large enough, contrast clear, no meaning carried by colour alone.

Visual types per field cluster:

- Teknik (mesin, elektro, otomotif, bangunan): simplified work drawings and sections, wiring and circuit diagrams, measurement readouts (caliper, micrometer, multimeter scales), fault tables, assembly sequences.
- Teknologi informasi: network topologies, flowcharts and pseudocode blocks, interface screenshots described or redrawn, log excerpts, database tables.
- Bisnis dan perkantoran: invoices and receipts, stock and price tables, organisational charts, business letters and memos, sales charts.
- Agribisnis dan perikanan: growth and feed tables, pond or plot layouts, production cycles, quality grading charts.
- Pariwisata, kuliner, dan layanan: menus and costing tables, reservation documents, service flow diagrams, hygiene checklists.
- Mapel umum: supply and demand curves (Ekonomi), force and circuit diagrams (Fisika), geometric figures and function graphs (Matematika), thematic maps and cross-sections (Geografi), system diagrams (Biologi).

Data honesty: never present invented numbers as real statistics or real specifications. Label plausible numbers created for the exercise as simulated ("Data simulasi untuk latihan") in the caption or source line; when real figures are used, name the real source (for example BPS with the table and year). A stimulus that teaches a wrong fact, a wrong tolerance, or a wrong safety limit fails even when the item built on it is well formed.
Length calibration: the figures in the reference file are practical defaults, not official rules, with one precisely scoped exception: 250-300 words per passage and 8-12 words per sentence are the verified text characteristics for the Bahasa Indonesia test subject in TKA SMA/MA/Sederajat and SMK/MAK (Buletin Asesmen Vol-1 2025, p. 12), for that subject and test only. Current official documents set no word limits for other subjects, and vocational documents are calibrated by workplace realism, not by word counts.
Two more gotchas: never leak the tested formula or procedure into the stimulus (a practice rule of this skill; no such prohibition appears in the Desain Pengembangan Soal AKM 2020, so never cite it as an official rule), and a stock photo of a workshop beside a recall question measures nothing: cut it or rebuild the item so the answer lives in the document.

## 3. Asesmen

This role designs the assessment package: identity, kisi-kisi, stimulus and items, answer key and scoring guide, performance rubric, KKTP, remedial and enrichment follow-up, and a quality audit. It covers written items and practical performance assessment as two halves of the same package.

Step 1, clarification gate: if the request is brief (a subject and a topic, nothing more), stop and ask before writing any item:

1. Fase, kelas, mata pelajaran, and whether the subject is a general subject or a vocational subject (and if vocational, the konsentrasi keahlian and the competency element).
2. Jenis asesmen: diagnostik, formatif, or sumatif, and whether the result feeds a report card.
3. Composition: how much of the package is written items and how much is practical or performance assessment, or confirmation to use the defaults below.
4. Cognitive target: the default LOTS:MOTS:HOTS split for Fase E-F, or a custom split.
5. KKTP approach: Deskripsi Kriteria, Rubrik, Skala atau Interval Nilai, or Persentase (the four approaches named in PPA Edisi Revisi 2025, p. 48; the PPA list is open, so another approach is allowed).
6. Whether a JSON or CSV export is needed.

Skip the gate when the request already specifies these points, or when the user says to proceed with standard settings. In that case state the defaults you used at the top of the package.

Step 2, defaults for Fase E-F:

- PG always has 5 options (A-E) in this jenjang. The AKM design ladder sets Kelas 10-12 at 5 options (Desain Pengembangan Soal AKM 2020, printed p. 4), and PG in TKA for SMK/MAK also uses 5 options (Buletin Asesmen Vol-1 2025, p. 12).
- Written items: LOTS:MOTS:HOTS = 20:50:30. This split is derived from the verified AKM Numerasi cognitive distribution for Kelas 11 (Knowing/Applying/Reasoning = 20/50/30; Desain Pengembangan Soal AKM 2020, printed p. 87); it is a school package design default, not an AKM or TKA quota.
- Practical packages: apply the 20:50:30 split to the supporting-knowledge dimension (the written or oral questions around the task). The main score comes from the performance rubric in Step 3, never from the written split.
- Write in standard Indonesian (EYD V), communicative and unambiguous. In the kisi-kisi, each multiple-choice item measures one operational verb (KKO); an essay item may measure more than one.

Step 3, the vocational half: practical and performance assessment. What makes an SMK/MAK package different from a general-school package is this half; design it with the same rigour as the written half:

- The task is a real work task: produce, repair, assemble, configure, serve, or document something against a job specification, a work order, or a client brief, in the workshop, laboratory, studio, kitchen, or Teaching Factory unit.
- The rubric scores observable work criteria, at minimum: keselamatan kerja (K3) and correct use of protective equipment; urutan prosedur (the work steps in the right order, with the right tools); ketepatan hasil (the product or service meets the specification, tolerance, or standard given); waktu (completion inside the allocated time); and sikap kerja (orderliness, tool care, honesty in reporting results).
- Each rubric aspect carries descriptors for tuntas and belum tuntas, so two assessors watching the same performance reach the same judgement. State any critical rule the school applies, for example that a serious safety violation closes the attempt, as a rule of the package, not as a regulation quote.
- Support competency readiness: align task difficulty with the competency elements of the konsentrasi keahlian, keep a product portfolio (photos, job reports, logbooks) as assessment evidence, and let Teaching Factory orders serve as authentic task contexts. Frame certification-style language as school assessment practice; do not present specific LSP or BNSP rules, because no such rules are in this skill's sources.

Step 4, stimulus and visuals: every item that carries a stimulus must need it, under the functionality test of section 2, which holds the full production guidance for this jenjang. Group items under a stimulus in small sets (the TKA pattern is 2-6 items per stimulus, Buletin Asesmen Vol-1 2025, p. 11), with cognitive levels graded inside the set. Prefer visuals rendered in code when the data is structured; use a real internet image only when the context needs a real photo or phenomenon; when a visual is too complex to render and no suitable image exists, write a [SPESIFIKASI ILUSTRASI] box instead. As a writing-practice rule, never leak the formula or the work procedure an item is testing into its stimulus; the item then measures copying instead of reasoning. This is a practice consideration, not an AKM regulation.

Step 5, item formats and scoring. Supported written formats: PG (single answer), PGK MCMA (multiple correct answers, checkbox), PGK Kategori (several statements, each judged in a binary category), Benar/Salah, Menjodohkan, Isian or Jawaban Singkat, and Uraian. The non-test family is Unjuk Kerja (practical performance, Step 3), product assessment, and portfolio. Whichever format is chosen, the technique and instrument must stay aligned with the tujuan pembelajaran (Permendikdasmen No. 1 Tahun 2026, Pasal 8). Scoring rules that must not be improvised:

- PG: 1 for correct, 0 for wrong.
- PGK MCMA is dynamic (a practice rule carried from earlier item-writing guidance; full detail in the second reference file). For sumatif and exams it is binary: 1 only when every correct option is chosen and no wrong option is chosen, otherwise 0. For formatif and diagnostik it is partial 2-1-0: 2 for a fully correct selection, 1 when some correct options are chosen with no wrong option, 0 when any wrong option is chosen. Never use free fractions such as 1/3 or 2/3.
- PGK Kategori: 1 point per statement judged correctly.
- Uraian Objektif (URO): list every keyword or step in the expected answer, 1 point per element present.
- Uraian Non-Objektif (URN): graded rubric built on SOLO levels, and the lowest rubric score is 0, never 1.
- Unjuk Kerja: score per rubric aspect from the observed performance; never convert a rubric judgement into a guessed percentage without the descriptors.

Full construction rules per format are in the first reference file; the scoring and follow-up detail is in the second.

Step 6, cognitive levels, KKTP, and follow-up. Tag every written item twice: a Bloom level (C1-C6, grouped as LOTS = C1-C2, MOTS = C3, HOTS = C4-C6) and, for essays and KKTP descriptions, a SOLO level (Prastruktural, Unistruktural, Multistruktural, Relasional, Berpikir Abstrak yang Mendalam). Berpikir Abstrak yang Mendalam is the term the Naskah Akademik Pembelajaran Mendalam uses for the fifth SOLO level (pp. 44-45); "Extended Abstract" is Biggs & Collis's original English term for the same level.
KKTP is descriptive, not one uniform passing number like the old KKM (PPA Edisi Revisi 2025, p. 64). Use the approach chosen at the gate: Deskripsi Kriteria (Perlu bimbingan, Cukup, Baik, Sangat baik, the PPA's labels, p. 64), Rubrik, Skala atau Interval Nilai, or Persentase of TP indicators mastered.
For practical assessment, state KKTP as performance descriptors: per rubric aspect, what tuntas work looks like and what belum tuntas work looks like, so the pass decision rests on observed criteria, not on a bare number.
Post-remedial grades follow Prinsip 1, Mastery Learning, the principle this skill adopts: the recorded grade is the highest score the student achieves after remedial. Fairness condition: students who already passed must get an equal chance to improve their score too.
The PPA sets no post-remedial grade formula at all: the word "remedial" appears only five times in the whole PPA, and its stated aim for remedial is raising achievement through guided relearning of the unmet criteria, not merely repairing the grade (p. 54). Prinsip 1 is therefore school policy, not a regulation quote, and the package must label it as such.
For practical remedial, the student repeats the failed aspects of the task under guidance, not necessarily the whole job. Hard rule: diagnostik and formatif results never determine report grades, promotion, or graduation (PPA Edisi Revisi 2025, p. 44).

Step 7, output package. Deliver these parts in order, plus the export when requested:

1. Identitas Asesmen: school (placeholder when unknown), fase and kelas, subject and konsentrasi keahlian where relevant, assessment type, time allocation, item and task count.
2. Matriks Kisi-Kisi: item or task number, Elemen or CP, TP, core material or competency element, indicator with its KKO, cognitive level, format.
3. Naskah Stimulus dan Butir Soal, grouped by format, each group with its work instructions; for practical tasks, the work order, specification, tools and materials list, time limit, and safety notes.
4. Kunci Jawaban dan Pedoman Penskoran, including URO keyword lists, the SOLO rubric for URN, and the full performance rubric for Unjuk Kerja.
5. Rubrik KKTP dan Pengolahan Nilai for the chosen approach, including the per-aspect performance descriptors for practical work.
6. Matriks Tindak Lanjut: remedial and enrichment actions per achievement band, differentiated by content, process, or product; for practical work, which task aspects are repeated or extended.
7. Catatan Telaah Mutu: the self-audit report from Step 8.
8. Optional export: JSON or CSV for a CBT or LMS, using the schema in the second reference file; section 5 produces the full delivery set.

Step 8, mandatory self-audit. Run the audit before delivering, and print its result as part 7 of the package:

- Key distribution for PG: compute R = (number of PG items / number of options) + 3. No key letter may appear more than R times. Example: 20 items with 5 options gives R = 7, so a key appearing 9 times must be rebalanced.
- Stimulus function test: remove each visual or document mentally. If the item is still answerable, the stimulus fails.
- Distractor and construction check: options homogeneous and similar in length, no "Semua jawaban di atas benar/salah", no double negatives, no item that depends on another item's answer, no formula or procedure leaked into a stimulus, URN rubric minimum is 0.
- Practical check: every rubric aspect is observable during the performance, safety (K3) is scored rather than assumed, the specification the product is judged against is printed in the package, and the time limit is realistic for the task.
- Language and ethics check: standard Indonesian, no SARA content, no violence, no local or cultural bias that advantages one group of students.

Closing gotchas: do not import rules from other jenjang (in SMK/MAK, PG has 5 options and the written split is 20:50:30, whatever a lower-jenjang package used); do not score practical work with a written-test mindset, because a performance is judged against the rubric's work criteria and the job specification, not against a classmate's result; do not present certification-body rules as if they were in this skill's sources; and never present the practice rules and defaults of this section as regulation.

## 4. Telaah & Validasi

This role reviews assessment material that already exists for SMK/MAK Fase E-F: written items and practical assessment rubrics written by an AI, by a teacher, or by an MGMP team. It does not write new packages; section 3 does that.
It also does not apply to writing items or rubrics from scratch, building a kisi-kisi, or setting KKTP; route those back to section 3.
Read the reference file before reviewing a set: it holds the checklists, formulas, and working standards.

The independence rule: an author reviewing their own items in the same pass will miss their own blind spots, which is why this role exists separately from section 3's self-audit.

- The self-audit is the author's quick check before delivery. This role is the second, deeper pass, run as if the reviewer did not write the items.
- Never let a review under this role silently replace the self-audit, and never present a self-audit as if it were this independent review. Name which one a report is.
- Review the item or rubric as printed, not as intended. If the indicator, the key, the specification, or the scoring guide is missing, that absence is itself a finding; do not reconstruct what the author probably meant and pass the item on that basis.
- When the reviewer and the author disagree, the card decides: cite the code that fails (for example K3, B1, or P2) instead of arguing taste.

Step 1, set up the review: collect what the verdict will be judged against: the items, their keys, the kisi-kisi or indicator for each item, the item format, the fase and subject, and the scoring guide for essays. For a practical task, collect the work order, the job specification the product is judged against, the tools and time allowed, and the rubric.
Items that arrive without a key or an indicator can still be reviewed for construction and language, but their Materi verdict is "cannot be confirmed" until the missing piece is supplied. A rubric that arrives without its job specification cannot be confirmed either. Say so in the report instead of guessing.

Step 2, qualitative review with the card in the reference file, item by item:

- PG and PGK items: the Materi codes (M), Konstruksi codes (K), and Bahasa codes (B). In this jenjang, also confirm the option count is 5 (A-E); a 4-option PG item in an SMK/MAK set is a construction finding, not a style choice.
- Uraian items: the U-M, U-K, and U-B codes, including whether a URO keyword list or a URN SOLO rubric is present and usable.

Record a pass or fail per code, with a short note on any fail that quotes or points at the exact words in the item that cause it. A fail without a location is not actionable.

Step 3, review the practical rubric through the P codes in the reference file:

- Criterion clarity: each aspect (keselamatan kerja/K3, urutan prosedur, ketepatan hasil, waktu, sikap kerja) is defined by observable descriptors, with tuntas and belum tuntas stated per aspect.
- Observability: an assessor can see or measure every scored behaviour during the performance; nothing is scored on impression alone.
- Specification link: ketepatan hasil points at the printed job specification (dimensions, tolerances, service standard), so the judgement is checkable after the fact.
- Safety coverage: K3 is present as a scored aspect, the critical safety rule of the task is stated, and the rubric says what happens when it is violated.
- Fairness of conditions: the tools, materials, and time the rubric assumes match what students actually get.

Give the rubric the same verdict scale as items (Step 4). A rubric whose aspects cannot be observed, or that omits safety on a hazardous task, is Tolak until rebuilt; a rubric with one vague descriptor is Revisi, and the report supplies the sharpened descriptor text.

Step 4, verdict per item and per rubric. Give every item and every rubric exactly one verdict:

- Terima (accept): every applicable code passes. The item or rubric may enter the bank as is.
- Revisi (revise): it measures the right thing but has a fixable defect: a weak distractor, uneven option lengths, a double negative, a missing rubric line, a vague performance descriptor. State the fix, and supply the revised text in Step 5 or in the output.
- Tolak (reject): it cannot be repaired by editing: it does not measure its indicator, it has more than one defensible key or no defensible key, its stimulus leaks the answer or the procedure, its rubric scores what cannot be observed, or (after a trial) its discrimination index is negative. State which defect is fatal.

No set-level verdict replaces the per-item verdicts. A set can be "mostly sound" and still contain two items that must not be used.

Step 5, distractor surgery. Run this on every PG or PGK item whose distractors fail the card or the trial data. This procedure is a working standard of this skill:

1. Diagnose each failing distractor and name the failure: too obvious (no plausible path leads to it), implausible (outside the topic or absurd on its face), cueing the key (longer, more precise, or grammatically matching the stem while others do not), or non-homogeneous (different kind, unit, or category from the key).
2. Name the student misconception the replacement will target: the specific wrong idea a real student holds, such as swapping two procedure steps, reading a measurement scale one division off, applying a formula to the wrong quantity, or confusing two similar components or terms. A distractor without a named misconception behind it is decoration.
3. Rewrite the distractor so it is exactly what a student with that misconception would produce or choose: correct method with one wrong step, right value with the wrong unit, the paired concept swapped in.
4. Re-check the repaired set: options homogeneous in kind and content, similar in length, ordered consistently (numbers ascending or chronological), no option giving away another, and the key not identifiable by form alone.

Show the before and after text for every operated distractor, with the misconception named. Never change the key during surgery without flagging it as a key change and re-running the Materi codes. Surgery touches distractors only; a broken stem or a wrong indicator is a revise or reject verdict with the reason stated.

Step 6, quantitative analysis, when trial data exists. Only run this step when the user supplies response data from a real tryout or class administration of written items. Never invent performance numbers for items that have not been tried, and do not fabricate observation statistics for practical tasks either; rubric quality is judged by the P codes and, where the school ran one, by an inter-assessor agreement check the user supplies.

- Difficulty index P: the share of test takers who answered correctly. Bands and formula are in the reference file.
- Discrimination index D: compare the top 27 percent and the bottom 27 percent of test takers by total score. This 27 percent split is this skill's working standard, taken from classical test theory convention.
- Distractor effectiveness: a distractor is functioning when at least 5 percent of the lower group chose it and the lower group chose it more than the upper group did. A distractor nobody chooses, or one the upper group prefers, is dead weight and goes to surgery.
- Verdicts from numbers: an item with negative D is rejected outright, because strong students fail it more than weak students do, which signals a wrong key or a misleading stem. An item with D in the revise band goes back to Step 2 and Step 5 with the data as evidence.

Interpret P together with D, never alone. A hard item (low P) with strong D is a good HOTS item and stays; an easy item with near-zero D measures nothing and does not earn its place outside a diagnostic set. Do not soften a negative D; it always means reject, however elegant the item looks.

Step 7, key-distribution check: for the PG items in the set, compute R = (number of PG items / number of options) + 3, inherited from section 3's self-audit. With 5 options, 20 PG items give R = 7. No key letter may appear more than R times. If one letter exceeds R, rebalance by reordering options on items where the content allows it, and list every item whose options were reordered. Reordering options is a change to the item: note it in the report.

Output format. Deliver the review in this order:

1. Ringkasan Telaah: how many items and rubrics were reviewed, by format, and the count per verdict (terima, revisi, tolak), plus any set-level problem such as a missing kisi-kisi, a missing job specification, or a failed key distribution.
2. Tabel Putusan per Butir: one row per item or rubric with its number, format, verdict, the card codes that failed, and a one-line reason.
3. Teks Revisi: the full revised text of every item marked revisi, including operated distractors shown before and after with their named misconceptions, the revised scoring guide where an essay guide changed, and the sharpened descriptors where a rubric changed.
4. Hasil Analisis Kuantitatif, only when trial data was supplied: per item, P with its band, D with its band, and the distractor findings, each tied back to the verdict it supports.
5. Catatan Kunci: the R computation and any rebalancing done.

Write reasons in plain language a teacher can act on without opening the reference file. Codes support the reason; they do not replace it.
Closing gotchas: do not run quantitative analysis on invented data (no trial, no P and D); do not pass an item because its intention was good; do not pass a practical rubric that leaves safety unscored on a hazardous task, or whose result aspect names no specification to judge against.

## 5. Konverter Naskah, Praktik & CBT

This role packages a finished package from section 3 into the formats schools and exam systems actually consume: Kartu Soal for administration files, a print-ready exam script, a print-ready practical assessment sheet for performance tasks, and import files for CBT and LMS platforms.
Conversion is a packaging job, not an editing job. Wording, keys, scoring, rubrics, and cognitive tags come from the source package and leave unchanged. If something in the source is broken or missing, this role reports it back instead of repairing it silently; a converter that edits silently destroys the audit trail between the validated set and the delivered file.
Format details, templates, and worked examples live in the two reference files: [references/konverter-spesifikasi-format-ekspor.md](references/konverter-spesifikasi-format-ekspor.md) (Kartu Soal, the print layouts, the Lembar Penilaian Praktik, and GIFT) and [references/konverter-spesifikasi-cbt-xml-csv.md](references/konverter-spesifikasi-cbt-xml-csv.md) (Moodle XML and CSV).
This role does not apply to writing or improving items, tasks, or rubrics. Send that work to section 3 for design and to section 4 for validation; convert only after the set is final.

Inputs required. Do not start converting until the input has:

1. Item set with stable numbering and one entry per item: stem, stimulus reference where used, options where the format has them. In this jenjang PG and MCMA items carry 5 options (A-E).
2. A key for every objectively scored item, and a scoring guide or rubric for every Uraian item.
3. For every practical task: the work order or task brief, the job specification, the tools and materials list, the time limit, and the performance rubric with its aspects and descriptors.
4. The scoring policy per format, above all the assessment type (diagnostik, formatif, or sumatif), because it decides how MCMA is encoded.
5. Identity data for the headers: school, subject, konsentrasi keahlian where relevant, fase and kelas, semester, assessment type, time allocation.
6. Planning data for Kartu Soal: CP, TP, core material or competency element, and the indicator with its cognitive level per item.
7. Pembahasan per item when the target format carries it (JSON and CSV do; the printed student script never does).

If any of these are absent, list exactly what is missing and stop. A converted file with invented keys or guessed scoring is worse than no file.

Outputs. Produce only the formats the user asked for:

- Kartu Soal: one card per item, holding identity, planning fields (CP, TP, material or competency element, indicator, Bloom and SOLO levels), the full item, its key, and its score weight or rubric. For a practical task, the card holds the work order, specification, and rubric instead of options and a key. This is the administration and supervision record.
- Naskah Ujian: the student-facing print script for the written sections. Header (kop) with school and exam identity, general instructions, items grouped by format with a short instruction per group, and a separate answer sheet layout for the objective sections. No keys, no pembahasan, no KKTP data anywhere in this document.
- Lembar Penilaian Praktik: the assessor-facing print sheet for a performance task, one per student per task. Identity fields, the task and specification summary, the time record (start, finish, duration), one row per rubric aspect with its descriptors and a score or judgement column, a notes column for observed events (skipped steps, safety incidents), the critical-rule outcome where the package declares one, and the assessor's name and signature line. The layout spec is in the first reference file.
- GIFT: plain-text import for Moodle and compatible LMS, one block per item.
- Moodle XML: the same set as a well-formed XML quiz file with a category path that names kurikulum, fase, and cognitive grouping.
- CSV: one row per item with the flattened columns defined in the second reference file, including pembahasan and the type-specific key columns.
- JSON: the schema defined in section 8 of [references/asesmen-kktp-solo-dan-tindak-lanjut.md](references/asesmen-kktp-solo-dan-tindak-lanjut.md) (metadata, stimulus, items), including the practical-task entry shape. Do not invent a parallel JSON shape.

Practical tasks do not convert into GIFT, Moodle XML, or CSV question rows; an LMS cannot observe a performance. In a mixed delivery, the written items go to the CBT files and the practical tasks go to the Lembar Penilaian Praktik, and the export notes state that split explicitly.

Scoring conversion rule: the source package's scoring policy governs. Fraction fields in GIFT and Moodle XML are only a transport encoding: they describe how the LMS should add up a response, they are not a new scoring policy, and they never override the policy written in the package.

- PG stays trivial everywhere: full credit for the key, zero for everything else.
- Sumatif MCMA is binary in the package (1 only when every correct option is chosen and no wrong option is chosen, otherwise 0). Encode it all-or-nothing in GIFT and Moodle XML: the correct options share +100 percent in total (each correct option carries 100 divided by the number of correct options), and every wrong option carries -100 percent, so choosing any wrong option cancels the credit from the correct ones. The LMS total for the item is then floored at zero: a response scores the item maximum only when its raw total reaches 100, and 0 otherwise. State this encoding and the floor rule in the export notes that accompany the file.
- Warning that must travel with every sumatif MCMA export: whether the encoding behaves as true all-or-nothing depends on the target LMS. Moodle's multiple-response grading, rounding of repeating fractions such as 33.33333, and negative-total handling differ between versions and question behaviours. Test-import one MCMA item, answer it three ways (fully correct, partially correct with no wrong pick, and correct plus one wrong pick), and confirm the grades are 1, 0, and 0 before importing the whole set.
- Formatif and diagnostik MCMA follow the package's partial 2-1-0 rule. Map it proportionally in the encoding: correct options share the full credit so a fully correct selection earns the maximum, a partial selection with no wrong option earns a proportional share, and any wrong option carries a penalty large enough to bring the total to zero. Say plainly in the export notes that this is a proportional approximation of 2-1-0, because an LMS computes per-option fractions and cannot reproduce the exact three-step scale; the teacher's grade processing still follows the package.
- PGK Kategori keeps its own rule, 1 point per statement judged correctly. Export each statement as its own scorable unit (its own GIFT or XML question, or its own CSV row group) instead of collapsing the item into one all-or-nothing question.
- URO keyword points and URN rubrics do not compress into option fractions. In CBT formats that cannot grade essays automatically, export Uraian as an essay question type with the scoring guide placed in the grader information field, and mark it as manually graded in the export notes.
- Performance rubric scores are never encoded into CBT fractions. They travel only on the Lembar Penilaian Praktik and, when the school records them digitally, as the aspect scores exactly as the assessor entered them.

Pre-export validation checklist. Run this pass before writing any output file, and report the result with the delivery:

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

Format gotchas:

- Never change item content during conversion. A stem that looks wrong, a suspect key, a weak distractor, or a vague rubric descriptor gets flagged back to the author or the review role, not fixed inside the export.
- XML must be well-formed or the LMS rejects the whole file. Escape ampersands, angle brackets, and quotes in text, or wrap question and answer text in CDATA sections; never mix raw HTML into an unescaped text node. Validate the file's structure before delivering it.
- GIFT has its own escaping: characters such as = ~ # { } and : inside answer text must be backslash-escaped, and an unescaped closing brace ends the answer block early.
- CSV quoting is strict. Wrap any field containing a comma, a quote, or a line break in double quotes, and double every quote inside such a field. Write the file as UTF-8 so Indonesian text survives the round trip, and keep one row per item with no line breaks outside quoted fields.
- Keep keys and pembahasan out of student-facing output. The Naskah Ujian and its answer sheet contain no key material; keys live in Kartu Soal, the scoring guide, and the CBT files only. The Lembar Penilaian Praktik is assessor-facing: it may carry the rubric and specification, but it is never handed to students as their task sheet; the student receives the work order without the descriptors.
- One source, many outputs: generate every requested format from the same validated item set in the same pass, so the print script, the cards, the practical sheets, and the CBT file can never drift into different versions of an item.
