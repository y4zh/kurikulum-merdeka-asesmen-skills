---
name: kurikulum-merdeka-sma-ma
description: "Complete Indonesian Kurikulum Merdeka skill for SMA/MA Fase E-F (Kelas 10-12) only, combining five roles in one level-locked skill: modul ajar planning that derives TP and ATP from CP with deep-learning experiences (Memahami, Mengaplikasi, Merefleksi) mapped to SOLO and differentiated LKPD; calibrated stimulus and functional visual design, including the verified Bahasa Indonesia TKA text characteristics of 250-300 words and 8-12 word sentences; complete assessment packages with the full TKA format set, 5-option PG, the 20:50:30 LOTS:MOTS:HOTS split, dynamic MCMA scoring, KKTP rubrics, and Mastery Learning remedial follow-up; independent item review with the Pusmendik card, HOTS authenticity checks, distractor surgery, and quantitative item analysis; and conversion into Kartu Soal, print-ready exam scripts, and GIFT, Moodle XML, CSV, or JSON exports for CBT/LMS platforms."
---

# Kurikulum Merdeka SMA/MA (Fase E-F)

One single skill for Indonesian SMA/MA under Kurikulum Merdeka (Kemendikdasmen), Fase E (Kelas 10) and Fase F (Kelas 11-12) only. It carries five roles in one skill, so the work stays inside this level's rules from planning to export: (1) Modul Ajar, teaching modules and TP lists; (2) Stimulus & Ilustrasi, stimulus texts and visuals; (3) Asesmen, complete assessment packages and items; (4) Telaah & Validasi Butir Soal, independent item review; (5) Konverter Naskah & CBT, Kartu Soal, print scripts, and CBT exports. Do not import rules from other levels (PAUD & TK/RA, SD/MI, SMP/MTs, SMK/MAK); each level has its own merged skill with its own option counts, splits, and calibration.

Indonesia only, SMA/MA only. The skill is locked to Kurikulum Merdeka Fase E-F, AKM Kelas 11, TKA SMA, and Ujian Sekolah at this level. It does not apply to foreign tests such as SAT, IELTS, or TOEFL, or to general trivia quizzes. School packages at this level mirror the TKA formats; TKA scoring itself is centralized and uses IRT, so a school package imitates the formats, never the IRT scoring.

## Cara memakai skill ini

Route each task to one part of this skill, and read that part's reference file before doing detailed work:

| Tugas | Bagian | Berkas referensi |
| --- | --- | --- |
| Modul ajar, menurunkan CP menjadi TP dan ATP, LKPD, skenario intervensi dari hasil asesmen, instrumen refleksi | 1. Modul Ajar | [references/modul-ajar-kerangka-pembelajaran-mendalam.md](references/modul-ajar-kerangka-pembelajaran-mendalam.md) |
| Stimulus, wacana, tabel data, grafik, diagram, peta, ilustrasi untuk butir soal | 2. Stimulus & Ilustrasi | [references/stimulus-panduan-visual-dan-wacana.md](references/stimulus-panduan-visual-dan-wacana.md) |
| Paket asesmen, kisi-kisi CP-TP, butir soal, kunci dan penskoran, KKTP, tindak lanjut remedial dan pengayaan | 3. Asesmen | [references/asesmen-regulasi-dan-format-soal.md](references/asesmen-regulasi-dan-format-soal.md), [references/asesmen-kktp-solo-dan-tindak-lanjut.md](references/asesmen-kktp-solo-dan-tindak-lanjut.md) |
| Telaah butir soal yang sudah ada, bedah pengecoh, cek keaslian HOTS, analisis butir kuantitatif dari data uji coba | 4. Telaah & Validasi Butir Soal | [references/telaah-kartu-telaah-pusmendik.md](references/telaah-kartu-telaah-pusmendik.md) |
| Kartu Soal, Naskah Ujian siap cetak, berkas impor GIFT, Moodle XML, CSV, JSON untuk CBT/LMS | 5. Konverter Naskah & CBT | [references/konverter-spesifikasi-format-ekspor.md](references/konverter-spesifikasi-format-ekspor.md) |

The normal chain runs in order: Bagian 1 produces the TP list, Bagian 2 builds the stimulus set, Bagian 3 assembles the package, Bagian 4 reviews it independently, and Bagian 5 converts the final set. Each part can also be used on its own; when a task belongs to another part, say so and switch parts instead of improvising.

## Catatan status verifikasi sumber

The core framework claims in this skill have been checked against the primary documents: PPA Edisi Revisi 2025, Desain Pengembangan Soal AKM 2020, Buletin Asesmen Vol-1 2025, Permendikdasmen No. 1 Tahun 2026, and Naskah Akademik Pembelajaran Mendalam. The per-claim status and page citations live in the reference files. Three cautions apply across all five parts. First, the CP citation (SK Kepala BSKAP No. 046/H/KR/2025) has not been independently verified, and the telaah card content has not been independently checked against the official Pusmendik documents; the 27 percent group split and the 5 percent distractor criterion in Bagian 4 are classical test theory conventions used as working standards. Second, some rules are deliberately not regulation quotes: the dynamic MCMA scoring rule, the package defaults, and the formula-leak rule are practice rules or school-package design defaults, labelled as such wherever they appear. Third, before using any output for a high-stakes exam or a formal school document, check any rule you rely on in the official document.

## 1. Modul Ajar

This part works upstream of assessment: it turns a Capaian Pembelajaran (CP) into Tujuan Pembelajaran (TP), orders the TP into an Alur Tujuan Pembelajaran (ATP), and builds the learning experiences, worksheets, and formative checkpoints that make those TP reachable in class. Assessment results then flow back into this part as concrete intervention plans for the next meetings. It does not write test items, kisi-kisi, answer keys, or KKTP rubrics; those belong to Bagian 3. The 8 Dimensi Profil Lulusan, the stage model detail, and the reflection instruments live in [references/modul-ajar-kerangka-pembelajaran-mendalam.md](references/modul-ajar-kerangka-pembelajaran-mendalam.md).

Kapan bagian ini dipakai:

- The user asks for a modul ajar, a lesson plan, or a teaching scenario for an SMA/MA class (Fase E or Fase F).
- The user needs a Fase E or Fase F CP broken down into TP, or TP ordered into an ATP for a semester or a phase.
- The user wants learning activities built on Pembelajaran Mendalam (Memahami, Mengaplikasi, Merefleksi) and asks which of the 8 Dimensi Profil Lulusan a unit develops.
- The user needs an LKPD for Kelas 10-12 with differentiation by readiness level, for example a simplified version and a challenge version of the same task.
- The user has assessment results grouped by KKTP band and needs them turned into actual classroom activities for the next meetings, or asks for teacher or student reflection instruments.

Fase E and Fase F are not interchangeable, and a modul ajar must say which one it serves. Fase E (Kelas 10) states the subject's foundation breadth: TP stay close to the concepts, Mengaplikasi works on guided, well-structured cases, and Merefleksi asks for evaluation of a familiar case, aiming at secure Relasional understanding across the whole element set. Fase F (Kelas 11-12) deepens the same elements toward specialization: more variables, less familiar contexts, open data; TP can target Berpikir Abstrak yang Mendalam directly, Mengaplikasi uses authentic cases and real data sets, and Merefleksi includes defending a conclusion against counter-arguments. Fase F planning also keeps the TKA in view as the final summative context: the TP list should cover the CP elements the TKA samples, without turning lessons into TKA drilling.

Two modes of use. Standalone mode: the user asks only for teaching planning; deliver the modul ajar package and stop, without adding test items. Invoked mode: the workflow needs the upstream half of an assessment package, and the deliverable that matters most is the TP list: each TP as one measurable statement, tagged with its CP element, its position in the ATP, its target SOLO level, and the Dimensi Profil Lulusan it serves. That list feeds Bagian 3, which builds the kisi-kisi from it; if the TP list is vague, the items built on it will be vague too, so this handoff is the quality gate for the whole chain.

Workflow:

1. Read the CP: element, phase (E or F), competencies and content. If the user has not supplied the CP text or at least the subject, fase, and topic, ask first. Never invent CP wording and present it as official text; label a paraphrase as a paraphrase.
2. Derive TP: one verb, one content focus, one TP per statement, observable and checkable; usually two to five TP per meeting sequence.
3. Order the ATP from concrete to abstract and from single-aspect to integrated understanding, so the order itself scaffolds learning across meetings and across the E-to-F boundary when the plan spans both phases.
4. Map each TP to a target SOLO level and to one or two Dimensi Profil Lulusan. Use the Naskah Akademik Pembelajaran Mendalam mapping (Tabel 3.1, pp. 44-45): Memahami covers Unistruktural and Multistruktural together, Mengaplikasi is Relasional, Merefleksi is Berpikir Abstrak yang Mendalam, and Prastruktural is not a stage but the status "Belum Memahami". A TP that maps to no dimension and no SOLO level is probably filler; rewrite or drop it.
5. Design the learning experiences in three stages, stating for each what the teacher does, what the students do, and what product or answer shows the stage worked. Memahami: meet the phenomenon or text, connect prior knowledge, name key facts and concepts (Unistruktural moving to Multistruktural). Mengaplikasi: use the concept on a real case, data set, or problem with the parts working together (Relasional). Merefleksi: evaluate one's own reasoning, defend a conclusion, or transfer the concept to a new situation (Berpikir Abstrak yang Mendalam, the Naskah Akademik's term for the fifth SOLO level; "Extended Abstract" is Biggs & Collis's original English term).
6. Place formative checkpoints between stages: a short check tied to one TP (exit question, observation point, one LKPD section) whose only job is to catch a misconception before the sumatif does. The technique and instrument must stay aligned with the TP (Permendikdasmen No. 1 Tahun 2026, Pasal 8). State what evidence the checkpoint must produce; its item format and scoring belong to Bagian 3.
7. Plan differentiation before it is needed: for each main task, the simplified entry point (fewer variables, worked example, sentence starters) and the extension (extra variable, open data, transfer case). Differentiate content, process, and support; the KKTP expectation for the TP stays the same.
8. Hand off: close with the clean TP list for Bagian 3, plus the misconception list the checkpoints are watching for.

Output structure of a modul ajar, in order:

1. Identitas: school (placeholder when unknown), subject, fase and kelas, semester, time allocation, number of meetings.
2. CP and element, quoted or clearly labelled as paraphrased, with the source the user supplied.
3. TP list, numbered, one measurable statement each.
4. ATP diagram or numbered sequence showing the order across meetings and why that order.
5. Dimensi Profil Lulusan targets: which dimensions this unit develops and where each shows up in an activity, not just a list pasted at the top.
6. Learning experiences per meeting, in the three stages, with teacher activity, student activity, and the evidence each stage produces.
7. LKPD plan: the worksheet sections, which TP each section serves, and its simplified and challenge variants.
8. Formative checkpoints: placement, the TP checked, and the evidence expected.
9. Reflection instruments: the teacher reflection set and the student reflection set from the reference file, trimmed to the unit when the user wants a short version. The teacher set serves the process assessment of Permendikdasmen No. 1 Tahun 2026, Pasal 15-19, which includes teacher self-reflection at least once per semester.
10. Handoff block: the TP list and misconception watchlist, formatted so Bagian 3 can consume it directly.

When assessment results come back grouped by KKTP descriptive band, turn each band into a scenario a teacher can run next meeting, naming the activity, the material, the grouping, and the exit evidence. Perlu bimbingan (Prastruktural to Unistruktural): reteach the base concept in a smaller step with the simplified LKPD variant, a worked example completed together, and short guided practice with the teacher or a trained peer tutor; exit evidence is stating the concept and solving one guided case unaided. Cukup (Multistruktural): the parts are known but not connected, so run a connecting task (concept map, compare-two-cases, the standard LKPD with the linking section emphasised); exit evidence is explaining how two parts relate. Baik (Relasional): no reteaching; move to the next TP at full difficulty, with exit evidence from the next unit's first checkpoint. Sangat baik (Berpikir Abstrak yang Mendalam): a transfer or challenge task from the extension variant (new context, open data, small project); this group can also serve as peer tutors for the first group when the tutoring requires explaining and justifying, not just giving answers. Keep the grade rules of Bagian 3 intact while planning: remedial grades follow Prinsip 1, and formatif results never decide report grades or promotion. The scenarios change the teaching, not the grade policy.

Gotchas: do not write exam items inside a modul ajar; do not list all 8 Dimensi Profil Lulusan as targets for every unit (pick the one to three the activities genuinely develop); do not skip Merefleksi to save time; do not write TP with stacked verbs; do not flatten Fase E and Fase F into one depth.

## 2. Stimulus & Ilustrasi

This part supplies the raw material of Bagian 3 for Fase E-F: the stimulus texts students read and the visuals they must interpret. A weak stimulus caps every item built on it, so stimulus work comes before item writing, not after. Templates, curated source lists, and the specification format live in [references/stimulus-panduan-visual-dan-wacana.md](references/stimulus-panduan-visual-dan-wacana.md).

Kapan bagian ini dipakai:

- The user asks for a stimulus, wacana, reading passage, data table, chart, diagram, map, or illustration for an SMA/MA assessment item (Fase E or Fase F).
- The user has items or a kisi-kisi for Kelas 10-12 and needs the stimulus set built or repaired before the items can be finished.
- An existing stimulus fails review: too shallow to support the target cognitive level, or a visual that decorates instead of measuring.
- Bagian 3 invokes it during package assembly (see the two modes below).

The functionality test governs everything here: cover the stimulus up. If the item can still be answered correctly without reading it, the stimulus fails and gets rebuilt or cut. A functional visual holds data the student must extract, compare, or transform (a value on a curve, a stage in a cycle, a difference between two table rows); a functional text carries the facts, tension, or evidence the item reasons about. Name the key objects a student must read (the specific numbers, labels, arrows, or legend entries the answer depends on) and list them with the stimulus; if you cannot name them, the visual is decoration.

Two modes of use. Standalone mode: the user asks only for stimulus material; deliver the calibrated text or visual, its source or data note, and the list of key objects, then stop. Invoked mode: Bagian 3 calls this part after the kisi-kisi exists and before items are written; the input is the kisi-kisi rows (indicator, KKO, target Bloom and SOLO level, fase) and the output is one stimulus per item group, sized and pitched so the target level is reachable: a Relasional item needs a stimulus with parts that must be connected, and a Berpikir Abstrak yang Mendalam item needs one that supports transfer to a new case.

Calibrate the text to Fase E-F. Students at this level handle single texts, multi-text sets, and infographics, with complex sentences and contrast or cause-effect conjunctions across paragraphs. Two text families dominate, following the AKM and TKA pattern: teks informasi (exposition, report, procedure, data presentation) and teks fiksi (narrative, poetry, drama excerpt). Contexts follow the AKM frames: personal, sosial-budaya, and saintifik, kept realistic and Indonesian: disaster mitigation, local markets and prices, weather and seasons, public policy, national statistics.

Length calibration, with the scope stated precisely:

- Bahasa Indonesia for TKA: 250-300 words per passage (poetry excepted), sentences of 8-12 words. These figures are the verified text characteristics for the Bahasa Indonesia test subject in TKA SMA/MA/Sederajat and SMK/MAK (Buletin Asesmen Vol-1 2025, p. 12). They bind that subject and that test only; this level holds the one precisely scoped, verified length figure in the whole ecosystem, and current official documents set no word limits for other subjects.
- Other subjects at Fase E-F: use the same 250-300 word range as this skill's practical default for a single passage, adjusted to the item's demand; a data-dense stimulus (table plus short text) can be shorter because the reading load sits in the data. Label this as a practical default, never as an official rule.
- Multi-text sets with an infographic can run longer in total; a combined length of up to 700 words is source-reported from ANBK Kelas XI reporting. Treat it as a ceiling reference, not a target.
- One stimulus serves one item or a small graded set: in TKA, one stimulus serves 2-6 items (Buletin Asesmen Vol-1 2025, p. 11), with cognitive levels graded inside the set. Do not stretch one passage across a whole exam.

Write in standard Indonesian (EYD V). Produce visuals in this order, stopping at the first method that yields a functional, readable visual:

1. Render in code: Markdown tables for multi-variable data, Mermaid for flows and cycles, clean SVG for charts and subject diagrams. Code-rendered visuals are exact, editable, and print-safe, so they are the default. The reference file holds a Mermaid cycle template and a corrected SVG supply-demand template to adapt, not to ship unchanged.
2. Curate a real image when the item needs a real photo, map, or phenomenon that code cannot draw honestly (a satellite weather image, a landform photograph, a historical artefact). Search the curated sources in the reference file: Wikimedia Commons for open-licensed photos and diagrams, BMKG for weather and earthquake material, BPS for official statistics, BIG for Indonesian base maps. Cite the source under the visual, every time.
3. Write a [SPESIFIKASI ILUSTRASI] box when the visual is too complex to render and no suitable image exists: visual type, reference source or search query, key objects, mandatory labels, and the function the item depends on, precise enough for a teacher or illustrator to produce it. The exact block format is in the reference file.

Whichever method is used, the visual ships with axis labels, units, a legend where symbols or colours carry meaning, and a title or caption that tells the student what they are looking at. Visual types per subject:

- Ekonomi: supply and demand curves with a marked equilibrium, shifts drawn as new curves rather than arrows alone, elasticity comparisons, circular flow diagrams.
- Fisika: force and vector diagrams on inclined planes and pulleys, circuit sketches, wave and optics ray diagrams, motion graphs with labelled axes and units.
- Matematika: geometric figures with the given lengths and angles marked, coordinate grids, function graphs, nets of solids, statistical charts built from the item's own data table.
- Geografi: soil and rock layer cross-sections, plate subduction diagrams with movement arrows and depth scale, thematic maps, climate and population charts, hydrological cycle diagrams.
- IPA and Biologi: food webs, system diagrams (digestive, respiratory, plant transport), experiment setups where the variables must be read from the drawing.
- IPS and Sejarah: timelines, historical maps, artefact photographs from open collections, source excerpts paired with a visual record.

Data honesty: never present invented numbers as real statistics. When a chart or table uses plausible numbers created for the exercise, label them as simulated or example data ("Data simulasi untuk latihan") in the caption or source line. When real figures are used, name the real source (for example BPS with the table and year) so a teacher can check them. A stimulus that teaches a wrong fact fails even when the item built on it is well formed.

Gotchas: decoration fails (a stock photo beside a recall question adds nothing the item measures; cut it or rebuild the item so the answer lives in the image). Do not leak the tested formula into the stimulus; that is a practice rule of this skill, and no such prohibition appears in the Desain Pengembangan Soal AKM 2020, so never cite it as an official rule. Do not ship the reference templates unchanged with their example numbers. Do not use an internet image without its source line or with an unclear licence when an open source can supply an alternative. Keep the visual readable at print size: labels large enough, contrast clear, no meaning carried by colour alone.

## 3. Asesmen

This part designs assessment packages and test items for Fase E-F: identity, kisi-kisi, stimulus and items, answer key and scoring guide, KKTP rubric, remedial and enrichment follow-up, and a quality audit. Construction rules per format are in [references/asesmen-regulasi-dan-format-soal.md](references/asesmen-regulasi-dan-format-soal.md); scoring, KKTP, and follow-up detail is in [references/asesmen-kktp-solo-dan-tindak-lanjut.md](references/asesmen-kktp-solo-dan-tindak-lanjut.md).

Kapan bagian ini dipakai:

- The user asks for an assessment package (diagnostik, formatif, or sumatif) for SMA/MA, Fase E or Fase F.
- The user asks for items in TKA or Pusmendik formats, a CP-TP kisi-kisi matrix, KKTP rubrics, scoring guides, or remedial and enrichment plans for Kelas 10-12.
- The user asks for a CBT or LMS item-bank export of an SMA/MA package (the export itself is produced by Bagian 5).
- The user works with LOTS, MOTS, HOTS, Bloom levels, or the SOLO taxonomy for SMA/MA students.

Step 1, clarification gate. If the request is brief (a subject and a topic, nothing more), stop and ask before writing any item: (1) fase (E or F), kelas, and mata pelajaran; (2) jenis asesmen (diagnostik, formatif, or sumatif) and whether the result feeds a report card; (3) composition, how many items of each format, or confirmation to use the defaults below; (4) cognitive target, the default Fase E-F split or a custom split; (5) KKTP approach (Deskripsi Kriteria, Rubrik, Skala atau Interval Nilai, or Persentase); (6) whether a JSON or CSV export is needed. Skip the gate when the request already specifies these points or the user says to proceed with standard settings; in that case state the defaults used at the top of the package.

Step 2, Fase E-F defaults:

- PG always has 5 options (A-E) at this level: the AKM design ladder sets Kelas 10-12 at 5 options (Desain Pengembangan Soal AKM 2020, printed p. 4), and PG in TKA for SMA/MA/Sederajat uses 5 options (Buletin Asesmen Vol-1 2025, p. 12). Never use 3 or 4 options here.
- Default cognitive split LOTS:MOTS:HOTS = 20:50:30, derived from the verified AKM Numerasi distribution for Kelas 11 (Knowing 20 / Applying 50 / Reasoning 30; Desain Pengembangan Soal AKM 2020, printed p. 87). It is a school package design default, not an AKM or TKA quota.
- For Literasi-based packages, the verified Kelas 11 reading distribution is Menemukan Informasi 30%, Memahami 40%, Mengevaluasi dan Merefleksi 30% (Desain Pengembangan Soal AKM 2020, printed p. 20).
- Fase E (Kelas 10) builds the foundation breadth of the subject, so keep its items closer to guided application; Fase F (Kelas 11-12) deepens toward specialization and TKA readiness and carries the full HOTS and multi-text load.
- Write in standard Indonesian (EYD V), communicative and unambiguous. In the kisi-kisi, each PG item measures one operational verb (KKO); an essay item may measure more than one.

Step 3, stimulus. Every item that carries a stimulus must need it, and group items under a stimulus in small sets of 2-6 with cognitive levels graded inside the set (Buletin Asesmen Vol-1 2025, p. 11). Calibration, production order, and templates belong to Bagian 2; as a writing-practice rule, never leak the formula an item is testing into its stimulus, especially in numeracy and science items, and never present that rule as an AKM regulation.

Step 4, item formats and scoring. Supported formats, the full TKA set: PG (single answer, 5 options), PGK MCMA (multiple correct answers, checkbox), PGK Kategori (several statements, each judged in a binary category, 3 statements per item in TKA usage), Benar/Salah, Menjodohkan, Isian or Jawaban Singkat, Uraian, and Observasi or Unjuk Kerja for non-test assessment. Whichever format is chosen, the technique and instrument must stay aligned with the tujuan pembelajaran (Permendikdasmen No. 1 Tahun 2026, Pasal 8). Scoring rules that must not be improvised:

- PG: 1 for correct, 0 for wrong.
- PGK MCMA is dynamic. For sumatif and exams it is binary: 1 only when every correct option is chosen and no wrong option is chosen, otherwise 0. For formatif and diagnostik it is partial 2-1-0: 2 for a fully correct selection, 1 when some correct options are chosen with no wrong option, 0 when any wrong option is chosen. Never use free fractions such as 1/3 or 2/3. This dynamic rule is a practice rule from earlier item-writing guidance, labelled as such, not a PPA or TKA quotation.
- PGK Kategori: 1 point per statement judged correctly.
- Uraian Objektif (URO): list every keyword or step in the expected answer, 1 point per element present.
- Uraian Non-Objektif (URN): graded rubric built on SOLO levels, and the lowest rubric score is 0, never 1.

Step 5, cognitive levels, KKTP, and follow-up. Tag every item twice: a Bloom level (C1-C6, grouped as LOTS = C1-C2, MOTS = C3, HOTS = C4-C6) and, for essays and KKTP descriptions, a SOLO level (Prastruktural, Unistruktural, Multistruktural, Relasional, Berpikir Abstrak yang Mendalam). Berpikir Abstrak yang Mendalam is the term the Naskah Akademik Pembelajaran Mendalam uses for the fifth SOLO level (pp. 44-45); "Extended Abstract" is Biggs & Collis's original English term for the same level. The experience-stage map is: Memahami covers Unistruktural and Multistruktural, Mengaplikasi is Relasional, Merefleksi is Berpikir Abstrak yang Mendalam, and Prastruktural is the status "Belum Memahami" with no stage.

KKTP is descriptive, not one uniform passing number like the old KKM (PPA Edisi Revisi 2025, p. 64). Use the approach chosen at the gate: Deskripsi Kriteria (with the PPA's labels Perlu bimbingan, Cukup, Baik, Sangat baik, p. 64), Rubrik, Skala atau Interval Nilai, or Persentase of TP indicators mastered. The four approaches are named in PPA Edisi Revisi 2025, p. 48, and the PPA list is open, so another approach is allowed.

Post-remedial grades follow Prinsip 1, Mastery Learning, the principle this skill adopts: the recorded grade is the highest score the student achieves after remedial, and students who already passed must get an equal chance to improve their score too. The PPA sets no post-remedial grade formula at all: the word "remedial" appears only five times in the whole PPA, and its stated aim for remedial is raising achievement through guided relearning of the unmet criteria, not merely repairing the grade (p. 54). Prinsip 1 is therefore school policy, not a regulation quote, and the package must label it as such. Hard rule: diagnostik and formatif results never determine report grades, promotion, or graduation (formatif is not high-stakes, PPA Edisi Revisi 2025, p. 44).

Step 6, output package. Deliver these seven parts in order, plus the export when requested:

1. Identitas Asesmen: school (placeholder when unknown), fase and kelas, subject, assessment type, time allocation, item count.
2. Matriks Kisi-Kisi: item number, Elemen or CP, TP, core material, indicator with its KKO, cognitive level, item format.
3. Naskah Stimulus dan Butir Soal, grouped by format, each group with its work instructions.
4. Kunci Jawaban dan Pedoman Penskoran, including URO keyword lists and the SOLO rubric for URN.
5. Rubrik KKTP dan Pengolahan Nilai for the chosen approach.
6. Matriks Tindak Lanjut: remedial and enrichment actions per achievement band, differentiated by content, process, or product.
7. Catatan Telaah Mutu: the self-audit report from Step 7.
8. Optional export: JSON or CSV for a CBT or LMS, using the schema in the second reference file of this part. For Kartu Soal, print scripts, or GIFT and Moodle XML, hand the finished package to Bagian 5.

Step 7, mandatory self-audit. Run it before delivering, and print its result as part 7 of the package:

- Key distribution for PG: compute R = (number of PG items / 5 options) + 3. No key letter may appear more than R times. Example: 20 items with 5 options gives R = 7, so a key appearing 9 times must be rebalanced.
- Stimulus function test: remove each visual mentally. If the item is still answerable, the visual fails.
- Distractor and construction check: options homogeneous and similar in length, no "Semua jawaban di atas benar/salah", no double negatives, no item that depends on another item's answer, no formula leaked into a stimulus, URN rubric minimum is 0.
- Language and ethics check: standard Indonesian, no SARA content, no violence, no local or cultural bias that advantages one group of students.

The self-audit is the author's quick check; the independent second pass is Bagian 4, and the two must never be presented as each other.

Gotchas: do not use 3 or 4 options for PG at this level, in school packages or in TKA alike; do not use formatif or diagnostik results for report grades or promotion decisions; do not place the tested formula inside a numeracy or science stimulus; do not start a URN rubric at 1; do not present the MCMA dynamic rule or the package defaults as regulation; do not claim a school package reproduces TKA scoring (TKA is scored centrally with IRT; the package borrows its formats only).

## 4. Telaah & Validasi Butir Soal

This part reviews test items that already exist for Fase E-F. It does not write new packages; it acts as the independent reviewer: it checks items written by an AI, by a teacher, or by an MGMP team against the Pusmendik qualitative review card, gives every item a verdict with reasons, repairs weak distractors, checks that claimed HOTS items are genuinely HOTS, and, when trial results are available, runs the numbers on how each item actually performed. The checklists, formulas, and working standards live in [references/telaah-kartu-telaah-pusmendik.md](references/telaah-kartu-telaah-pusmendik.md); read that file before reviewing a set.

Kapan bagian ini dipakai:

- The user hands over existing SMA/MA items, a draft exam, or a question bank and asks for a review, a telaah, a validation, or a quality check.
- The user supplies trial or class score data (who answered what, or per-item correct counts) and asks for item analysis: difficulty, discrimination, or distractor performance.
- A package produced with Bagian 3 needs its second pass before it is used in class or uploaded to a CBT item bank.
- A teacher wants a second opinion on items from another source before adopting them for Kelas 10-12.

It does not apply to writing items from scratch, building a kisi-kisi, or setting KKTP; route those back to Bagian 3.

The independence rule. An author reviewing their own items in the same pass will miss their own blind spots, which is why this part exists separately from the Bagian 3 self-audit. Run the review as if the reviewer did not write the items; never let a review under this part silently replace the self-audit, and never present a self-audit as if it were this independent review; name which one a report is. Review the item as printed, not as intended: if the indicator, the key, or the scoring guide is missing, that absence is itself a finding; do not reconstruct what the author probably meant and pass the item on that basis. When reviewer and author disagree, the card decides: cite the code that fails (for example K3 or B1) instead of arguing taste.

Step 1, set up the review. Collect what the verdict will be judged against: the items, their keys, the kisi-kisi or indicator for each item, the item format, the fase and subject, and the scoring guide for essays. Items that arrive without a key or an indicator can still be reviewed for construction and language, but their Materi verdict is "cannot be confirmed" until the missing piece is supplied; say so in the report instead of guessing. Confirm the basic shape before anything else: PG items at this level carry 5 options (A-E); a 4-option PG item in an SMA/MA set is a construction finding on its own.

Step 2, qualitative review with the card. Work item by item through the review card in the reference file: for PG and PGK items, the Materi codes (M), Konstruksi codes (K), and Bahasa codes (B); for Uraian items, the U-M, U-K, and U-B codes, including whether a URO keyword list or a URN SOLO rubric is present and usable. Record a pass or fail per code, with a short note on any fail that quotes or points at the exact words in the item that cause it; a fail without a location is not actionable.

Step 3, HOTS authenticity check. At Fase E-F a large share of a set claims HOTS, and the most common fraud is a hard recall item wearing a HOTS label; sulit bukan berarti HOTS. For every item tagged C4-C6, run three questions. Novelty: is the stimulus or situation new to the student, or is it the worked example from the textbook with the numbers changed? A rehearsed procedure is C3 however heavy the arithmetic. Reasoning load: must the student select, connect, or judge information, or only execute one known procedure accurately? Difficulty from long computation, rare vocabulary, or an obscure fact is not HOTS. Answer path: could a student answer correctly by remembering a memorised pattern without reading the stimulus? If yes, the item is LOTS or MOTS in disguise. An item that fails the check keeps its verdict path through the card, but its cognitive tag is corrected in the report and the set's LOTS:MOTS:HOTS balance is recomputed against the Fase E-F default of 20:50:30; a set whose HOTS share collapses after the check is a set-level finding, not a footnote.

Step 4, verdict per item. Give every item exactly one verdict:

- Terima (accept): every applicable code passes. The item may enter the bank as is.
- Revisi (revise): the item measures the right thing but has a fixable defect: a weak distractor, uneven option lengths, a double negative, a missing rubric line, a wrong cognitive tag. State the fix, and supply the revised text in Step 5 or in the output.
- Tolak (reject): the item cannot be repaired by editing: it does not measure its indicator, it has more than one defensible key or no defensible key, its stimulus leaks the answer or the formula, or (after a trial) its discrimination index is negative. State which defect is fatal.

No set-level verdict replaces the per-item verdicts. A set can be "mostly sound" and still contain two items that must not be used.

Step 5, distractor surgery. Run this on every PG or PGK item whose distractors fail the card or the trial data, following this working standard: (1) diagnose each failing distractor and name the failure: too obvious, implausible, cueing the key (longer, more precise, or grammatically matching the stem while others do not), or non-homogeneous; (2) name the student misconception the replacement will target, the specific wrong idea a real Fase E-F student holds, such as reversing a cause and its effect, applying a formula to the wrong quantity, swapping two similar terms, stopping at the intermediate result of a multi-step problem, or reading a graph's axis in the wrong direction; a distractor without a named misconception behind it is decoration; (3) rewrite the distractor so it is exactly what a student with that misconception would produce or choose: correct method with one wrong step, right value with the wrong unit, the paired concept swapped in; (4) re-check the repaired set: five options homogeneous in kind and content, similar in length, ordered consistently (numbers ascending or chronological), no option giving away another, and the key not identifiable by form alone. Show the before and after text for every operated distractor, with the misconception named. Never change the key during surgery without flagging it as a key change and re-running the Materi codes; surgery touches distractors, and a broken stem or a wrong indicator is a revise or reject verdict, not a rewrite.

Step 6, quantitative analysis, when trial data exists. Only run this step when the user supplies response data from a real tryout or class administration; never invent performance numbers for items that have not been tried. Difficulty index P: the share of test takers who answered correctly, with bands and formula in the reference file. Discrimination index D: compare the top 27 percent and the bottom 27 percent of test takers by total score; this 27 percent split is a working standard of this part, taken from classical test theory convention. Distractor effectiveness: a distractor is functioning when at least 5 percent of the lower group chose it and the lower group chose it more than the upper group did; a distractor nobody chooses, or one the upper group prefers, is dead weight and goes to surgery. Verdicts from numbers: an item with negative D is rejected outright, because strong students fail it more than weak students do, which signals a wrong key or a misleading stem; an item with D in the revise band goes back to Step 2 and Step 5 with the data as evidence. Interpret P together with D, never alone: a hard item (low P) with strong D is a good HOTS item and stays; an easy item with near-zero D measures nothing and does not earn its place outside a diagnostic set.

Step 7, key-distribution check. For the PG items in the set, compute R = (number of PG items / 5 options) + 3, inherited from the Bagian 3 self-audit. No key letter may appear more than R times across A-E. If one letter exceeds R, rebalance by reordering options on items where the content allows it, and list every item whose options were reordered; reordering options is a change to the item, so note it in the report.

Output format, in this order:

1. Ringkasan Telaah: how many items were reviewed, by format, and the count per verdict (terima, revisi, tolak), plus any set-level problem such as a missing kisi-kisi, a failed key distribution, or a HOTS share that collapsed under the authenticity check.
2. Tabel Putusan per Butir: one row per item with its number, format, verdict, the card codes that failed, and a one-line reason.
3. Teks Revisi: the full revised text of every item marked revisi, including operated distractors shown before and after with their named misconceptions, corrected cognitive tags, and the revised scoring guide where an essay guide changed.
4. Hasil Analisis Kuantitatif, only when trial data was supplied: per item, P with its band, D with its band, and the distractor findings, each tied back to the verdict it supports.
5. Catatan Kunci: the R computation and any rebalancing done.

Write reasons in plain language a teacher can act on without opening the reference file. Codes support the reason; they do not replace it.

Gotchas: do not run quantitative analysis on invented data (no trial, no P and D); do not pass an item because its intention was good; do not soften a negative D; do not let a difficult item pass as HOTS on difficulty alone.

## 5. Konverter Naskah & CBT

This part packages a finished Fase E-F package into the formats schools and exam systems actually consume: Kartu Soal for administration files, a print-ready exam script, and import files for CBT and LMS platforms. Conversion is a packaging job, not an editing job: wording, keys, scoring, and cognitive tags come from the source package and leave unchanged. If something in the source is broken or missing, this part reports it back instead of repairing it silently. Format details, templates, and worked examples live in [references/konverter-spesifikasi-format-ekspor.md](references/konverter-spesifikasi-format-ekspor.md). It does not apply to writing or improving items; send that work to Bagian 3 for design and Bagian 4 for validation, and convert only after the set is final.

Kapan bagian ini dipakai:

- The user has a finished SMA/MA package from Bagian 3 (or an equivalent item set) and asks for Kartu Soal, a printable exam script, or an import file.
- The user asks for a bank soal in GIFT, Moodle XML, CSV, or JSON form, for example for a Moodle-based CBT or another LMS.
- The user wants the same Fase E-F item set in more than one delivery format at once.

Inputs required. Do not start converting until the input has:

1. Item set with stable numbering and one entry per item: stem, stimulus reference where used, options where the format has them.
2. A key for every objectively scored item, and a scoring guide or rubric for every Uraian item.
3. The scoring policy per format, above all the assessment type (diagnostik, formatif, or sumatif), because it decides how MCMA is encoded.
4. Identity data for the headers: school, subject, fase and kelas, semester, assessment type, time allocation.
5. Planning data for Kartu Soal: CP, TP, core material, and the indicator with its cognitive level per item.
6. Pembahasan per item when the target format carries it (JSON and CSV do; the printed student script never does).

If any of these are absent, list exactly what is missing and stop. A converted file with invented keys or guessed scoring is worse than no file.

Outputs, producing only the formats the user asked for:

- Kartu Soal: one card per item, holding identity, planning fields (CP, TP, material, indicator, Bloom and SOLO levels), the full item, its key, and its score weight or rubric. This is the administration and supervision record.
- Naskah Ujian: the student-facing print script. Header (kop) with school and exam identity, general instructions, items grouped by format with a short instruction per group, and a separate answer sheet layout for the objective sections, with five answer cells (A-E) per PG row. No keys, no pembahasan, no KKTP data anywhere in this document.
- GIFT: plain-text import for Moodle and compatible LMS, one block per item.
- Moodle XML: the same set as a well-formed XML quiz file with a category path that names kurikulum, fase, and cognitive grouping.
- CSV: one row per item with the flattened columns defined in the reference file, including pembahasan and the type-specific key columns.
- JSON: the Bagian 3 schema (metadata, stimulus, items) exactly as defined in [references/asesmen-kktp-solo-dan-tindak-lanjut.md](references/asesmen-kktp-solo-dan-tindak-lanjut.md), section 8. Do not invent a parallel JSON shape.

Scoring conversion rule. The source package's scoring policy governs. Fraction fields in GIFT and Moodle XML are only a transport encoding: they describe how the LMS should add up a response, they are not a new scoring policy, and they never override the policy written in the package.

- PG stays trivial everywhere: full credit for the key, zero for everything else.
- Sumatif MCMA is binary in the package (1 only when every correct option is chosen and no wrong option is chosen, otherwise 0). Encode it all-or-nothing in GIFT and Moodle XML: the correct options share +100 percent in total (each correct option carries 100 divided by the number of correct options), and every wrong option carries -100 percent, so choosing any wrong option cancels the credit from the correct ones. The LMS total for the item is then floored at zero: a response scores the item maximum only when its raw total reaches 100, and 0 otherwise. State this encoding and the floor rule in the export notes that accompany the file.
- Warning that must travel with every sumatif MCMA export: whether the encoding behaves as true all-or-nothing depends on the target LMS. Moodle's multiple-response grading, rounding of repeating fractions such as 33.33333, and negative-total handling differ between versions and question behaviours. Test-import one MCMA item, answer it three ways (fully correct, partially correct with no wrong pick, and correct plus one wrong pick), and confirm the grades are 1, 0, and 0 before importing the whole set.
- Formatif and diagnostik MCMA follow the package's partial 2-1-0 rule. Map it proportionally in the encoding: correct options share the full credit so a fully correct selection earns the maximum, a partial selection with no wrong option earns a proportional share, and any wrong option carries a penalty large enough to bring the total to zero. Say plainly in the export notes that this is a proportional approximation of 2-1-0, because an LMS computes per-option fractions and cannot reproduce the exact three-step scale; the teacher's grade processing still follows the package.
- PGK Kategori keeps its own rule, 1 point per statement judged correctly. Export each statement as its own scorable unit (its own GIFT or XML question, or its own CSV row group) instead of collapsing the item into one all-or-nothing question.
- URO keyword points and URN rubrics do not compress into option fractions. In CBT formats that cannot grade essays automatically, export Uraian as an essay question type with the scoring guide placed in the grader information field, and mark it as manually graded in the export notes.

Pre-export validation checklist. Run this pass before writing any output file, and report the result with the delivery:

- Every objectively scored item has exactly the key its format requires: one key for PG, a defined key set for MCMA, a category key per statement for PGK Kategori.
- Every Uraian item has its scoring guide or rubric attached; a URN rubric starts at 0.
- Option counts match this level: every PG item has exactly 5 options (A-E). A 3- or 4-option item in an SMA/MA package fails validation unless the source package states a deliberate, documented deviation.
- Every stimulus_id or stimulus reference in an item resolves to a stimulus that exists in the set, and every stimulus is used by at least one item.
- Item numbering is continuous, and the item count matches the identity data and the kisi-kisi.
- No leftover placeholders anywhere: no bracketed tokens such as [Nama Sekolah] in a file meant for direct use, no empty option, stem, or pembahasan fields. Placeholders are acceptable only in a template the user explicitly asked for.
- Bloom and SOLO tags are present on every row or record that carries those columns.
- The assessment type is recorded, so the MCMA encoding choice can be checked against it.

Any failure stops the export for the affected items. List the failures by item number and hand them back; do not guess a key, drop an item quietly, or fill a placeholder with invented data.

Gotchas: never change item content during conversion (a stem that looks wrong, a suspect key, or a weak distractor gets flagged back to the author or to Bagian 4, not fixed inside the export; a converter that edits silently destroys the audit trail). XML must be well-formed or the LMS rejects the whole file: escape ampersands, angle brackets, and quotes in text, or wrap question and answer text in CDATA sections, and never mix raw HTML into an unescaped text node; validate the file's structure before delivering it. GIFT has its own escaping: characters such as = ~ # { } and : inside answer text must be backslash-escaped, and an unescaped closing brace ends the answer block early. CSV quoting is strict: wrap any field containing a comma, a quote, or a line break in double quotes, double every quote inside such a field, write the file as UTF-8 so Indonesian text survives the round trip, and keep one row per item with no line breaks outside quoted fields. Keep keys and pembahasan out of student-facing output. One source, many outputs: generate every requested format from the same validated item set in the same pass, so the print script, the cards, and the CBT file can never drift into different versions of an item.
