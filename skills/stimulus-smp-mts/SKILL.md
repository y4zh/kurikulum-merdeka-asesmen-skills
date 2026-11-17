---
name: stimulus-smp-mts
description: "Companion skill to asesmen-smp-mts that designs calibrated stimulus texts and functional visuals for Indonesian Kurikulum Merdeka assessment items at SMP/MTs (Fase D, Kelas VII-IX): phase-calibrated reading passages in personal, socio-cultural, and scientific contexts, data tables, Mermaid diagrams, clean SVG charts and subject diagrams, curated images from Wikimedia Commons and official Indonesian sources (BMKG, BPS, BIG) with citation, and precise [SPESIFIKASI ILUSTRASI] boxes when a visual cannot be rendered, with every visual passing the functionality test that the item cannot be answered correctly without reading it."
---

# Stimulus & Ilustrasi SMP/MTs (Fase D)

Companion skill to asesmen-smp-mts. That skill assembles the assessment package; this one supplies its raw material for Fase D (Kelas VII-IX): the stimulus texts students read and the visuals they must interpret. A weak stimulus caps every item built on it, so stimulus work comes before item writing, not after.

This skill is one of five for this jenjang. Its siblings are asesmen-smp-mts, modul-ajar-smp-mts, telaah-smp-mts, and konverter-smp-mts. Other jenjang have their own stimulus skills with their own calibration; do not borrow their length figures.

Note on sources: the Fase D stimulus lengths in the reference file are practical defaults for calibration, not official rules. The one verified passage figure in current documents, 250-300 words with sentences of 8-12 words, belongs to the Bahasa Indonesia test subject in TKA at SMA level (Buletin Asesmen Vol-1 2025, p. 12); it is not a rule for this jenjang and must not be applied here. Current official documents set no word limits for Fase D. Templates, source lists, and the specification format live in [references/panduan-visual-dan-wacana.md](references/panduan-visual-dan-wacana.md).

## When this skill applies

- The user asks for a stimulus, wacana, reading passage, data table, chart, diagram, map, or illustration for an assessment item at SMP/MTs (Fase D).
- The user has items or a kisi-kisi and needs the stimulus set built or repaired before the items can be finished.
- An existing stimulus fails review: too shallow to support the target cognitive level, or a visual that decorates instead of measuring.
- asesmen-smp-mts invokes it during package assembly (see the two modes below).

Indonesia only, same boundary as the parent skill: Kurikulum Merdeka, Fase D, AKM Kelas 8 contexts, Ujian Sekolah. Not for other phases, foreign tests, or general trivia material.

## The functionality test

Every visual and every stimulus must pass one test before it ships: cover it up. If the item can still be answered correctly without reading it, the stimulus fails and gets rebuilt or cut.

- A functional visual holds data the student must extract, compare, or transform: a value on a curve, a stage in a cycle, a difference between two table rows.
- A functional text carries the facts, tension, or evidence the item reasons about. Background colour that merely restates what the question already says is not a stimulus.
- Name the key objects a student must read (the specific numbers, labels, arrows, or legend entries the answer depends on) and list them with the stimulus. If you cannot name them, the visual is decoration.

## Two modes of use

Standalone mode: the user asks only for stimulus material. Deliver the calibrated text or visual, its source or data note, and the list of key objects, then stop. Do not invent the items that will use it unless asked.

Invoked mode: asesmen-smp-mts calls this skill after the kisi-kisi exists and before items are written. In this mode the input is the kisi-kisi rows (indicator, KKO, target Bloom and SOLO level, kelas) and the output is one stimulus per item group, sized and pitched so the target level is reachable: a Relasional item needs a stimulus with parts that must be connected, and a Berpikir Abstrak yang Mendalam item needs one that supports transfer to a new case. Return the stimulus set to the parent workflow; item construction stays there.

## Calibrate the text to Fase D

Use the calibration in the reference file as practical house defaults: sentences of about 7-11 words, passages of about 150-250 words, mixed informational texts (procedure, concept, fact) and mid-level fiction, with bar and line charts, data tables, and cycle diagrams. Treat the numbers as a starting calibration to adjust for the actual class, never quote them to a user as Kemendikdasmen rules.

Use the AKM context families: personal, sosial-budaya, and saintifik. Contexts should be realistic and Indonesian: local markets and prices, weather and seasons, school and village or neighbourhood life, simple national statistics, everyday technology. Write in standard Indonesian (EYD V). One stimulus serves one item or a small graded set (in TKA, one stimulus serves 2-6 items, Buletin Asesmen Vol-1 2025, p. 11); do not stretch one passage across a whole exam.

## Produce visuals in this order

Try the methods in order and stop at the first one that produces a functional, readable visual:

1. Render in code. Markdown tables for multi-variable data, Mermaid for flows and cycles, and clean SVG for charts and subject diagrams. Code-rendered visuals are exact, editable, and print-safe, so they are the default. The reference file holds a Mermaid cycle template and a corrected SVG curve template to adapt, not to ship unchanged.
2. Curate a real image when the item needs a real photo, map, or phenomenon that code cannot draw honestly: a satellite weather image, a landform photograph, a historical artefact. Search the curated sources in the reference file (Wikimedia Commons for open-licensed photos and diagrams, BMKG for weather and earthquake material, BPS for official statistics, BIG for Indonesian base maps). Cite the source under the visual, every time.
3. Write a [SPESIFIKASI ILUSTRASI] box when the visual is too complex to render and no suitable image exists. The box states the visual type, the reference source or search query, the key objects, the mandatory labels, and the function the item depends on, precisely enough for a teacher or illustrator to produce it. The exact block format is in the reference file.

Whichever method is used, the visual ships with axis labels, units, a legend where symbols or colours carry meaning, and a title or caption that tells the student what they are looking at.

## Visual types per subject at Fase D

- Matematika: geometric figures with the given lengths and angles marked, coordinate grids, function graphs, nets of solids, statistical charts built from the item's own data table.
- IPA: food webs, system diagrams (digestive, respiratory, plant transport), experiment setups where the variables must be read from the drawing, simple circuit sketches, motion graphs with labelled axes and units.
- IPS: timelines, historical maps, artefact photographs from open collections, source excerpts paired with a visual record, simple supply and demand curves with a marked equilibrium.
- Geografi content within IPS: soil and rock layer cross-sections, plate movement diagrams with arrows, thematic maps, climate and population charts, hydrological cycle diagrams.
- Bahasa Indonesia and Bahasa Inggris: information texts and fiction excerpts whose details, structure, or language features the items interrogate; the text itself is the visual's counterpart and must carry the answers.

## Data honesty

Never present invented numbers as real statistics. When a chart or table uses plausible numbers created for the exercise, label it as simulated or example data ("Data simulasi untuk latihan") in the caption or source line. When real figures are used, name the real source (for example BPS with the table and year) so a teacher can check them. A stimulus that teaches a wrong fact fails even when the item built on it is well formed.

## Gotchas

- Decoration fails. A stock photo of a volcano next to a recall question about volcano parts adds nothing the item measures; cut it or rebuild the item so the answer lives in the image.
- Do not leak the tested formula into the stimulus. A numeracy or science item whose stimulus prints the formula it tests measures copying, not reasoning. This is a practice rule of this skill; no such prohibition appears in the Desain Pengembangan Soal AKM 2020, so never cite it as an official rule.
- Do not ship the templates from the reference file unchanged with their example numbers. Adapt the data to the item, then re-check that the key objects and the answer still agree.
- Do not stretch calibration defaults into fake authority. If a teacher asks where a word limit comes from, the honest answer is that it is this skill's practical default, not a regulation. In particular, never present the 250-300 word figure here: it is verified only for the Bahasa Indonesia TKA subject at SMA level.
- Do not use an internet image without its source line, and do not use one whose licence or origin is unclear when an open source (Wikimedia Commons, BMKG, BPS, BIG) can supply an alternative.
- Keep the visual readable at print size: labels large enough, contrast clear, no meaning carried by colour alone.
