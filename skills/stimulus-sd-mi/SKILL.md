---
name: stimulus-sd-mi
description: "Companion skill to the SD/MI assessment skill that designs calibrated stimulus texts and functional visuals for Indonesian Kurikulum Merdeka items at SD/MI only (Fase A-C, Kelas I-VI): oral and picture-based stimulus in Fase A, short paragraphs and labelled pictures in Fase B, simple texts with tables and bar charts in Fase C, AKM contexts (personal, socio-cultural, scientific), Mermaid cycle diagrams and clean SVG charts, curated images from Wikimedia Commons and official Indonesian sources (BMKG, BPS, BIG) with citation, and precise [SPESIFIKASI ILUSTRASI] boxes when a visual cannot be rendered, with every visual passing the functionality test that the item cannot be answered correctly without reading it."
---

# Stimulus & Ilustrasi SD/MI (Fase A-C)

Companion skill to asesmen-sd-mi. That skill assembles the assessment package; this one supplies its raw material for SD/MI (Fase A, B, and C): the short texts, pictures, tables, and simple diagrams that Kelas I-VI students must read and interpret. A weak stimulus caps every item built on it, so stimulus work comes before item writing, not after.

Note on sources: the stimulus lengths in the reference file are practical defaults for calibration at Fase A-C, not official rules. Current official documents set no word limits for these fase. One verified figure exists elsewhere and is deliberately NOT used here: a passage of 250-300 words with sentences of 8-12 words is the text characteristic for the Bahasa Indonesia test subject in a national test at the senior secondary level; it does not belong to SD/MI and must never be quoted as an SD/MI standard. Templates, source lists, and the specification format live in [references/panduan-visual-dan-wacana-sd-mi.md](references/panduan-visual-dan-wacana-sd-mi.md).

Sibling skills for this jenjang: asesmen-sd-mi assembles the package and writes the items; modul-ajar-sd-mi plans the teaching and may request stimulus material for LKPD; telaah-sd-mi reviews finished items, including whether their visuals are functional; konverter-sd-mi converts finished packages into print and CBT formats.

## When this skill applies

- The user asks for a stimulus, wacana, reading passage, picture, data table, or simple diagram for an assessment item at SD/MI, Fase A, B, or C.
- The user has items or a kisi-kisi for Kelas I-VI and needs the stimulus set built or repaired before the items can be finished.
- An existing stimulus fails review: too hard to read for the fase, or a picture that decorates instead of measuring.
- asesmen-sd-mi invokes it during package assembly (see the two modes below).

Indonesia only, same boundary as the parent skill: Kurikulum Merdeka, Fase A-C, AKM Kelas 5 contexts. Not for other jenjang, foreign tests, or general trivia material.

## The functionality test

Every visual and every stimulus must pass one test before it ships: cover it up. If the item can still be answered correctly without reading it, the stimulus fails and gets rebuilt or cut.

- A functional picture holds something the student must observe, compare, count, or order: the objects in a scene, the stages in a picture series, the difference between two simple table rows.
- A functional text carries the facts or events the item reasons about. Background colour that merely restates what the question already says is not a stimulus.
- Name the key objects a student must read (the specific objects, numbers, labels, or arrows the answer depends on) and list them with the stimulus. If you cannot name them, the visual is decoration.

## Two modes of use

Standalone mode: the user asks only for stimulus material. Deliver the calibrated text or visual, its source or data note, and the list of key objects, then stop. Do not invent the items that will use it unless asked.

Invoked mode: asesmen-sd-mi calls this skill after the kisi-kisi exists and before items are written. In this mode the input is the kisi-kisi rows (indicator, KKO, target Bloom and SOLO level, fase) and the output is one stimulus per item group, sized and pitched so the target level is reachable: a Relasional item needs a stimulus with parts that must be connected, such as a picture series whose stages must be ordered, and a simple transfer item needs a familiar situation the child has not been drilled on. Return the stimulus set to the parent workflow; item construction stays there.

## Calibrate the text to the fase

Use the calibration matrix in the reference file as practical house defaults: sentence length, passage length, text types, and visual complexity per fase, from oral and picture-based in Fase A to one simple text with a table in Fase C. Treat the numbers as a starting calibration to adjust for the actual class, never quote them to a user as Kemendikdasmen rules.

Write in standard Indonesian (EYD V) with short sentences and familiar words. Contexts follow the AKM frame: personal (the child's own life, family, play, pocket money), socio-cultural (school, village or neighbourhood events, local traditions, markets), and scientific (simple natural phenomena, plants and animals, weather, simple experiments). One stimulus serves one item or a small graded set; do not stretch one passage across a whole exam.

Fase anchors:

- Fase A (Kelas I-II): the stimulus is oral or a picture. No reading passage is required of the child; any words are read aloud by the teacher.
- Fase B (Kelas III-IV): a short paragraph, a labelled picture, or a table of two or three columns.
- Fase C (Kelas V-VI): one simple text, a bar chart or simple diagram, or a short text paired with a table.

## Produce visuals in this order

Try the methods in order and stop at the first one that produces a functional, readable visual:

1. Render in code. Markdown tables for simple multi-variable data, Mermaid for simple cycles and flows, and clean SVG for simple charts and diagrams. Code-rendered visuals are exact, editable, and print-safe, so they are the default. The reference file holds a Mermaid cycle template to adapt, not to ship unchanged.
2. Curate a real image when the item needs a real photo or phenomenon that code cannot draw honestly: an animal in its habitat, a landform, a market scene. Search the curated sources in the reference file (Wikimedia Commons for open-licensed photos and diagrams, BMKG for weather material, BPS for official statistics, BIG for Indonesian base maps). Cite the source under the visual, every time.
3. Write a [SPESIFIKASI ILUSTRASI] box when the visual is too complex to render and no suitable image exists. The box states the visual type, the reference source or search query, the key objects, the mandatory labels, and the function the item depends on, precisely enough for a teacher or illustrator to produce it. The exact block format is in the reference file.

Whichever method is used, the visual ships with labels and units where the data needs them, and a short title or caption that tells the student what they are looking at. Keep print readability strict at this jenjang: large lettering, few objects per picture, no meaning carried by colour alone.

## Visual types per subject at SD/MI

- Matematika: pictures of grouped objects to count or compare, number lines, simple geometric figures with the given lengths marked, picture graphs and bar charts built from the item's own small data table, nets of simple solids at Fase C.
- IPA: picture series of life cycles and growth stages, simple food chains, experiment setups where the steps must be read from the drawing, weather and season pictures.
- Bahasa Indonesia: a short story or information text with one supporting picture, a picture series to order into a story, labelled scenes for vocabulary and description items.
- IPS: simple maps of the school or neighbourhood, timelines of a child's day or a local event, pictures of occupations, markets, and cultural activities.
- Pendidikan Pancasila and Agama: scenes of daily behaviour and cooperation that the item asks the student to judge or continue.

## Data honesty

Never present invented numbers as real statistics. When a chart or table uses plausible numbers created for the exercise, label it as simulated or example data ("Data simulasi untuk latihan") in the caption or source line. When real figures are used, name the real source (for example BPS with the table and year) so a teacher can check them. A stimulus that teaches a wrong fact fails even when the item built on it is well formed.

## Gotchas

- Decoration fails. A stock photo of a volcano next to a recall question about volcano parts adds nothing the item measures; cut it or rebuild the item so the answer lives in the image.
- Do not leak the tested formula into the stimulus. A numeracy item whose stimulus prints the formula it tests measures copying, not reasoning. This is a practice rule of this skill; no such prohibition appears in the Desain Pengembangan Soal AKM 2020, so never cite it as an official rule.
- Do not import senior-level text lengths into SD/MI. Long passages belong to other jenjang; at Fase A-C the calibration matrix in the reference file governs, as a practical default.
- Do not ship the templates from the reference file unchanged with their example numbers. Adapt the data to the item, then re-check that the key objects and the answer still agree.
- Do not use an internet image without its source line, and do not use one whose licence or origin is unclear when an open source (Wikimedia Commons, BMKG, BPS, BIG) can supply an alternative.
- Do not build a written reading stimulus for Fase A items. Fase A stimulus is spoken or pictured; the reading load itself would measure the wrong thing.
