---
name: stimulus-smk-mak
description: "Companion skill to the SMK/MAK assessment skill that designs calibrated stimulus texts and functional visuals for Indonesian Kurikulum Merdeka vocational assessment items in Fase E-F (Kelas X-XII): authentic workplace documents such as SOP excerpts, work drawings (gambar kerja), equipment manuals, nameplates, specification tables, work orders, and industry case studies, safety (K3) as an accurate working context, code-rendered tables, diagrams, and charts, curated images from Wikimedia Commons and official Indonesian sources (BMKG, BPS, BIG) with citation, and precise [SPESIFIKASI ILUSTRASI] boxes when a visual cannot be rendered, where every stimulus must pass the functionality test that the item cannot be answered correctly without reading it."
---

# Stimulus & Ilustrasi SMK/MAK (Fase E-F)

Companion skill to asesmen-smk-mak. That skill assembles the assessment package; this one supplies its raw material: the stimulus texts and workplace documents students read and the visuals they must interpret, for SMK/MAK Fase E (Kelas X) and Fase F (Kelas XI-XII), in general subjects and vocational subjects alike. A weak stimulus caps every item built on it, so stimulus work comes before item writing, not after.

Note on sources: the stimulus lengths in the reference file are practical defaults for calibration, not official rules, with one precisely scoped exception: a passage of 250-300 words and sentences of 8-12 words are the verified text characteristics for the Bahasa Indonesia test subject in TKA SMA/MA/Sederajat and SMK/MAK (Buletin Asesmen Vol-1 2025, p. 12), and for that subject and test only. Current official documents set no word limits for other subjects, and vocational documents are calibrated by workplace realism, not by word counts. Templates, source lists, and the specification format live in [references/panduan-visual-dan-wacana.md](references/panduan-visual-dan-wacana.md).

This skill is one of five for SMK/MAK. Its siblings are asesmen-smk-mak (assessment packages, written and practical), modul-ajar-smk-mak (teaching modules and TP lists), telaah-smk-mak (independent item and rubric review), and konverter-smk-mak (print and CBT conversion). Stay inside this jenjang: stimulus calibration for Fase A-D lives in other jenjang skills.

## When this skill applies

- The user asks for a stimulus, wacana, reading passage, workplace document, data table, chart, diagram, work drawing, or illustration for an assessment item in an SMK/MAK Fase E-F context.
- The user has items or a kisi-kisi and needs the stimulus set built or repaired before the items can be finished.
- An existing stimulus fails review: too shallow to support the target cognitive level, a document that looks industrial but carries no readable data, or a visual that decorates instead of measuring.
- asesmen-smk-mak invokes it during package assembly (see the two modes below).

Indonesia only, same boundary as the parent skill: Kurikulum Merdeka, Fase E-F, AKM, TKA, Ujian Sekolah. Not for foreign tests or general trivia material.

## The functionality test

Every visual and every stimulus must pass one test before it ships: cover it up. If the item can still be answered correctly without reading it, the stimulus fails and gets rebuilt or cut.

- A functional visual holds data the student must extract, compare, or transform: a dimension on a work drawing, a value on a curve, a stage in a work flow, a difference between two specification rows.
- A functional document carries the facts, limits, or evidence the item reasons about: a tolerance in the SOP, a rating on the nameplate, a stock figure in the table. A realistic-looking document whose numbers are never used is set dressing, not a stimulus.
- Name the key objects a student must read (the specific numbers, labels, dimensions, arrows, or legend entries the answer depends on) and list them with the stimulus. If you cannot name them, the visual is decoration.

## Two modes of use

Standalone mode: the user asks only for stimulus material. Deliver the calibrated text, document, or visual, its source or data note, and the list of key objects, then stop. Do not invent the items that will use it unless asked.

Invoked mode: asesmen-smk-mak calls this skill after the kisi-kisi exists and before items are written. In this mode the input is the kisi-kisi rows (indicator, KKO, target Bloom and SOLO level, subject and competency element) and the output is one stimulus per item group, sized and pitched so the target level is reachable: a Relasional item needs a stimulus with parts that must be connected, and a Berpikir Abstrak yang Mendalam item needs one that supports transfer to a new case or a fault not shown directly. Return the stimulus set to the parent workflow; item construction stays there.

## Workplace stimulus: the vocational core

For vocational subjects, the default stimulus is an authentic document of the world of work, trimmed to what the item needs but never falsified:

- SOP and work instruction excerpts: numbered steps, warnings, and the one step or limit the item turns on.
- Gambar kerja (work drawings): orthographic views, sections, dimensions, and tolerances the student must read to choose, compute, or judge.
- Equipment manuals and nameplates: operating limits, maintenance intervals, ratings, and fault tables.
- Specification and data tables: material specifications, price and stock lists, measurement results, service schedules.
- Industry case studies: a short account of a real-shaped workplace problem (a rejected product batch, a recurring machine fault, a customer complaint) with the data needed to analyse it.

Safety is a working context, not decoration: where a document carries K3 warnings, protective-equipment requirements, or prohibition signs, keep them accurate and let items test them when the kisi-kisi targets safety. Never invent a safety limit; use the standard value the subject teaches or label the document as simulated.

For general subjects in this jenjang, use the Fase E-F pattern: single and multi-text stimuli, informational and literary texts, inter-paragraph conjunctions, contrast between texts. Calibrate with the matrix in the reference file as a practical house default; the only verified figures are the Bahasa Indonesia TKA ones named above. One stimulus serves one item or a small graded set (in TKA, one stimulus serves 2-6 items, Buletin Asesmen Vol-1 2025, p. 11); do not stretch one document across a whole exam.

Write in standard Indonesian (EYD V), keeping the trade's technical terms as the subject uses them. Contexts should be realistic and Indonesian: workshops and small industries, workshops' customer orders, local markets and prices, weather and seasons, national statistics.

## Produce visuals in this order

Try the methods in order and stop at the first one that produces a functional, readable visual:

1. Render in code. Markdown tables for specification and multi-variable data, Mermaid for work flows, procedures, and cycles, and clean SVG for charts, diagrams, and simplified technical sketches. Code-rendered visuals are exact, editable, and print-safe, so they are the default. The reference file holds a Mermaid production-flow template and a corrected SVG two-axis template to adapt, not to ship unchanged.
2. Curate a real image when the item needs a real photo, map, or phenomenon that code cannot draw honestly: a machine component, a landform photograph, a satellite weather image. Search the curated sources in the reference file (Wikimedia Commons for open-licensed photos and diagrams, BMKG for weather and earthquake material, BPS for official statistics, BIG for Indonesian base maps). Cite the source under the visual, every time.
3. Write a [SPESIFIKASI ILUSTRASI] box when the visual is too complex to render and no suitable image exists. Real gambar kerja with full dimensioning usually lands here: the box states the visual type, the views required, the key objects, the mandatory labels and dimensions, and the function the item depends on, precisely enough for a teacher or illustrator to produce it. The exact block format is in the reference file.

Whichever method is used, the visual ships with axis labels, units, tolerances where they carry meaning, a legend where symbols or colours carry meaning, and a title or caption that tells the student what they are looking at.

## Visual types per field cluster

- Teknik (mesin, elektro, otomotif, bangunan): simplified work drawings and sections, wiring and circuit diagrams, measurement readouts (caliper, micrometer, multimeter scales), fault tables, assembly sequences.
- Teknologi informasi: network topologies, flowcharts and pseudocode blocks, interface screenshots described or redrawn, log excerpts, database tables.
- Bisnis dan perkantoran: invoices and receipts, stock and price tables, organisational charts, business letters and memos, sales charts.
- Agribisnis dan perikanan: growth and feed tables, pond or plot layouts, production cycles, quality grading charts.
- Pariwisata, kuliner, dan layanan: menus and costing tables, reservation documents, service flow diagrams, hygiene checklists.
- Mapel umum: supply and demand curves (Ekonomi), force and circuit diagrams (Fisika), geometric figures and function graphs (Matematika), thematic maps and cross-sections (Geografi), system diagrams (Biologi).

## Data honesty

Never present invented numbers as real statistics or real specifications. When a chart, table, or document uses plausible numbers created for the exercise, label it as simulated or example data ("Data simulasi untuk latihan") in the caption or source line. When real figures are used, name the real source (for example BPS with the table and year) so a teacher can check them. A stimulus that teaches a wrong fact, a wrong tolerance, or a wrong safety limit fails even when the item built on it is well formed.

## Gotchas

- Decoration fails. A stock photo of a workshop next to a recall question about tool names adds nothing the item measures; cut it or rebuild the item so the answer lives in the image or document.
- Do not leak the tested formula or procedure into the stimulus. A numeracy item or a fault-diagnosis item whose stimulus prints the solution steps measures copying, not reasoning. This is a practice rule of this skill; no such prohibition appears in the Desain Pengembangan Soal AKM 2020, so never cite it as an official rule.
- Do not ship the templates from the reference file unchanged with their example numbers. Adapt the data to the item, then re-check that the key objects and the answer still agree.
- Do not stretch calibration defaults into fake authority. The 250-300 word figure binds the Bahasa Indonesia TKA subject only; if a teacher asks where a length for another subject comes from, the honest answer is that it is this skill's practical default or a workplace-realism judgement, not a regulation.
- Do not use an internet image without its source line, and do not use one whose licence or origin is unclear when an open source (Wikimedia Commons, BMKG, BPS, BIG) can supply an alternative.
- Keep the visual readable at print size: labels and dimensions large enough, contrast clear, no meaning carried by colour alone; a work drawing that cannot be read on paper cannot be assessed fairly.
