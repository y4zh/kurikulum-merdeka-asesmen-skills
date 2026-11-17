---
name: stimulus-sma-ma
description: "Design calibrated stimulus texts and functional visuals for Indonesian Kurikulum Merdeka assessment items at SMA/MA Fase E-F (Kelas 10-12): multi-text passages and infographics pitched to TKA reading loads, including the verified 250-300 word and 8-12 word sentence characteristics of the Bahasa Indonesia TKA text, teks informasi and teks fiksi in AKM contexts, data tables, Mermaid diagrams, clean SVG charts and subject diagrams, curated images from Wikimedia Commons and official Indonesian sources (BMKG, BPS, BIG) with citation, and precise [SPESIFIKASI ILUSTRASI] boxes when a visual cannot be rendered, with every visual passing the functionality test that the item cannot be answered correctly without reading it."
---

# Stimulus & Ilustrasi SMA/MA (Fase E-F)

Companion skill to asesmen-sma-ma. That skill assembles the assessment package; this one supplies its raw material for SMA/MA, Fase E (Kelas 10) and Fase F (Kelas 11-12): the stimulus texts students read and the visuals they must interpret. A weak stimulus caps every item built on it, so stimulus work comes before item writing, not after.

This is one of five SMA/MA skills. Its siblings at this level: asesmen-sma-ma (assessment packages and items), modul-ajar-sma-ma (teaching modules and TP lists), telaah-sma-ma (independent item review), konverter-sma-ma (Kartu Soal, print scripts, and CBT exports). Other levels have their own skill sets; do not import their calibration here.

Note on sources: this level holds the one precisely scoped, verified length figure in the whole ecosystem: a passage of 250-300 words and sentences of 8-12 words are the verified text characteristics for the Bahasa Indonesia test subject in TKA SMA/MA/Sederajat and SMK/MAK (Buletin Asesmen Vol-1 2025, p. 12), and for that subject and test only. Every other length figure in this skill and its reference file is a practical calibration default, not an official rule; current official documents set no word limits for other subjects. Templates, source lists, and the specification format live in [references/panduan-visual-dan-wacana.md](references/panduan-visual-dan-wacana.md).

## When this skill applies

- The user asks for a stimulus, wacana, reading passage, data table, chart, diagram, map, or illustration for an SMA/MA assessment item (Fase E or Fase F).
- The user has items or a kisi-kisi for Kelas 10-12 and needs the stimulus set built or repaired before the items can be finished.
- An existing stimulus fails review: too shallow to support the target cognitive level, or a visual that decorates instead of measuring.
- asesmen-sma-ma invokes it during package assembly (see the two modes below).

Indonesia only, SMA/MA only, same boundary as the parent skill: Kurikulum Merdeka, Fase E-F, AKM Kelas 11, TKA SMA, Ujian Sekolah. Not for other levels, foreign tests, or general trivia material.

## The functionality test

Every visual and every stimulus must pass one test before it ships: cover it up. If the item can still be answered correctly without reading it, the stimulus fails and gets rebuilt or cut.

- A functional visual holds data the student must extract, compare, or transform: a value on a curve, a stage in a cycle, a difference between two table rows.
- A functional text carries the facts, tension, or evidence the item reasons about. Background colour that merely restates what the question already says is not a stimulus.
- Name the key objects a student must read (the specific numbers, labels, arrows, or legend entries the answer depends on) and list them with the stimulus. If you cannot name them, the visual is decoration.

## Two modes of use

Standalone mode: the user asks only for stimulus material. Deliver the calibrated text or visual, its source or data note, and the list of key objects, then stop. Do not invent the items that will use it unless asked.

Invoked mode: asesmen-sma-ma calls this skill after the kisi-kisi exists and before items are written. In this mode the input is the kisi-kisi rows (indicator, KKO, target Bloom and SOLO level, fase) and the output is one stimulus per item group, sized and pitched so the target level is reachable: a Relasional item needs a stimulus with parts that must be connected, and a Berpikir Abstrak yang Mendalam item needs one that supports transfer to a new case. Return the stimulus set to the parent workflow; item construction stays there.

## Calibrate the text to Fase E-F

At this level students handle single texts, multi-text sets, and infographics, with complex sentences and contrast or cause-effect conjunctions across paragraphs. Two text families dominate, following the AKM and TKA pattern: teks informasi (exposition, report, procedure, data presentation) and teks fiksi (narrative, poetry, drama excerpt). Contexts follow the AKM frames: personal, sosial-budaya, and saintifik, kept realistic and Indonesian: disaster mitigation, local markets and prices, weather and seasons, public policy, national statistics.

Length calibration:

- Bahasa Indonesia for TKA: 250-300 words per passage (poetry excepted), sentences of 8-12 words. This is the verified Buletin figure (Buletin Asesmen Vol-1 2025, p. 12) and it binds this subject and test only.
- Other subjects at Fase E-F: use the same 250-300 word range as this skill's practical default for a single passage, adjusted to the item's demand; a data-dense stimulus (table plus short text) can be shorter because the reading load sits in the data.
- Multi-text sets with an infographic can run longer in total; a combined length of up to 700 words is source-reported from ANBK Kelas XI reporting. Treat it as a ceiling reference, not a target.
- One stimulus serves one item or a small graded set (in TKA, one stimulus serves 2-6 items, Buletin Asesmen Vol-1 2025, p. 11); do not stretch one passage across a whole exam.

Write in standard Indonesian (EYD V).

## Produce visuals in this order

Try the methods in order and stop at the first one that produces a functional, readable visual:

1. Render in code. Markdown tables for multi-variable data, Mermaid for flows and cycles, and clean SVG for charts and subject diagrams. Code-rendered visuals are exact, editable, and print-safe, so they are the default. The reference file holds a Mermaid cycle template and a corrected SVG supply-demand template to adapt, not to ship unchanged.
2. Curate a real image when the item needs a real photo, map, or phenomenon that code cannot draw honestly: a satellite weather image, a landform photograph, a historical artefact. Search the curated sources in the reference file (Wikimedia Commons for open-licensed photos and diagrams, BMKG for weather and earthquake material, BPS for official statistics, BIG for Indonesian base maps). Cite the source under the visual, every time.
3. Write a [SPESIFIKASI ILUSTRASI] box when the visual is too complex to render and no suitable image exists. The box states the visual type, the reference source or search query, the key objects, the mandatory labels, and the function the item depends on, precisely enough for a teacher or illustrator to produce it. The exact block format is in the reference file.

Whichever method is used, the visual ships with axis labels, units, a legend where symbols or colours carry meaning, and a title or caption that tells the student what they are looking at.

## Visual types per subject

- Ekonomi: supply and demand curves with a marked equilibrium, shifts drawn as new curves rather than arrows alone, elasticity comparisons, circular flow diagrams.
- Fisika: force and vector diagrams on inclined planes and pulleys, circuit sketches, wave and optics ray diagrams, motion graphs with labelled axes and units.
- Matematika: geometric figures with the given lengths and angles marked, coordinate grids, function graphs, nets of solids, statistical charts built from the item's own data table.
- Geografi: soil and rock layer cross-sections, plate subduction diagrams with movement arrows and depth scale, thematic maps, climate and population charts, hydrological cycle diagrams.
- IPA and Biologi: food webs, system diagrams (digestive, respiratory, plant transport), experiment setups where the variables must be read from the drawing.
- IPS and Sejarah: timelines, historical maps, artefact photographs from open collections, source excerpts paired with a visual record.

## Data honesty

Never present invented numbers as real statistics. When a chart or table uses plausible numbers created for the exercise, label it as simulated or example data ("Data simulasi untuk latihan") in the caption or source line. When real figures are used, name the real source (for example BPS with the table and year) so a teacher can check them. A stimulus that teaches a wrong fact fails even when the item built on it is well formed.

## Gotchas

- Decoration fails. A stock photo of a volcano next to a recall question about volcano parts adds nothing the item measures; cut it or rebuild the item so the answer lives in the image.
- Do not leak the tested formula into the stimulus. A numeracy or physics item whose stimulus prints the formula it tests measures copying, not reasoning. This is a practice rule of this skill; no such prohibition appears in the Desain Pengembangan Soal AKM 2020, so never cite it as an official rule.
- Do not ship the templates from the reference file unchanged with their example numbers. Adapt the data to the item, then re-check that the key objects and the answer still agree.
- Do not stretch the verified figure beyond its scope. The 250-300 word and 8-12 word figures belong to the Bahasa Indonesia test subject in TKA; if a teacher asks where a word limit for another subject comes from, the honest answer is that it is this skill's practical default, not a regulation.
- Do not use an internet image without its source line, and do not use one whose licence or origin is unclear when an open source (Wikimedia Commons, BMKG, BPS, BIG) can supply an alternative.
- Keep the visual readable at print size: labels large enough, contrast clear, no meaning carried by colour alone.
