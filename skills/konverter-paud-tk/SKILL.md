---
name: konverter-paud-tk
description: "Convert finished Indonesian Kurikulum Merdeka PAUD and TK/RA assessment instrument sets into ready-to-use documents only (Kelompok Bermain, Taman Kanak-Kanak, Raudhatul Athfal): printable observation sheets, anecdotal record formats, portfolio checklists, and narrative child development report formats written in the BB, MB, BSH, and BSB developmental categories, produced from one validated source set without changing indicator wording, and with no CBT, GIFT, Moodle, or item-bank export because digital test delivery does not apply at this level."
---

# Konverter Dokumen Asesmen PAUD & TK/RA

Companion skill to asesmen-paud-tk. The assessment skill designs the instruments; this skill turns a finished instrument set for Indonesian PAUD and TK/RA (Kelompok Bermain, Taman Kanak-Kanak, Raudhatul Athfal) into the documents teachers actually hold and file: printable observation sheets, anecdotal record formats, portfolio checklists, and the narrative child development report format. Conversion is a packaging job, not an editing job: indicators, categories, and wording come from the source set and leave unchanged. If something in the source is broken or missing, this skill reports it back instead of repairing it silently.

This skill is one level of a per-level family. Its same-level siblings are asesmen-paud-tk, modul-ajar-paud-tk, stimulus-paud-tk, and telaah-paud-tk. Other levels have their own converter skills.

There is no digital test export in this skill, explicitly: no CBT file, no GIFT, no Moodle XML, no CSV item bank. Those formats exist to deliver test items to a computer, and this level has no test items and no computer-delivered assessment. A request to export PAUD instruments "to the LMS" is answered with the print and document formats below, plus this explanation, never with an invented item-bank file.

Format details and templates live in [references/format-dokumen-paud.md](references/format-dokumen-paud.md).

## When this skill applies

- The user has a finished instrument set from asesmen-paud-tk (or an equivalent set) and asks for ready-to-use sheets or report formats.
- The user wants class sets: one observation sheet per meeting, a semester anecdotal record book format, or a portfolio checklist per child.
- The user wants the development report format that turns accumulated BB, MB, BSH, BSB judgements into a parent-readable narrative document.

It does not apply to designing or improving instruments. Send that work to asesmen-paud-tk for design and to telaah-paud-tk for review; convert only after the set is final.

## Inputs required

Do not start converting until the input has:

1. The finished instrument set: checklists, anecdotal formats, rating scales, or rubrics, each with its goal and CP element stated.
2. The interpretation guide: the BB, MB, BSH, BSB descriptors per indicator. Without it, sheets can be produced but the report format cannot, because the report is written in those categories.
3. Identity data for the headers: school, kelompok usia (KB, TK A, or TK B), class name, teacher, semester, and academic year.
4. The class roster when per-child documents are requested (portfolio checklists, report shells). Names come from the user, never invented.
5. For a filled report (not just the format): the accumulated observation records and portfolio notes per child. A report narrative is written from evidence the user supplies; this skill never invents a child's development.

If any of these are absent, list exactly what is missing and stop for the affected documents.

## Outputs

Produce only the documents the user asked for:

- Lembar Observasi Cetak: one sheet per play session or per week, with the identity header, the play context line, the indicator rows, the observation columns, and the notes space, laid out to be filled by hand while supervising play.
- Format Catatan Anekdot: a record format (one per page or a running log) with separated fields for the factual record and the later interpretation, plus the indicator link.
- Ceklist Portofolio: one checklist per child per element, listing the evidence entries to collect across the semester, with date and teacher-note columns.
- Format Laporan Perkembangan Anak: the semester report shell and, when evidence is supplied, the filled narrative: per element, the category reached (BB, MB, BSH, or BSB), the evidence in plain parent-readable language, and the stimulation planned next.

Layout rules for every document are in the reference file: large handwriting space, few items per page, and headers that survive photocopying.

## Conversion rules

- Indicators and descriptors are copied from the source set unchanged. A converter that rewords an indicator breaks the audit trail between the reviewed set and the document in the teacher's hand.
- Categories stay categories. Never convert BB, MB, BSH, BSB into numbers, percentages, letter grades, or a class ranking anywhere in a converted document, including in totals rows or summary tables.
- One source, many documents: generate every requested document from the same source set in the same pass, so the observation sheet, the portfolio checklist, and the report format can never drift into different versions of an indicator.
- A filled narrative reports only supplied evidence. Where evidence for an element is thin, the narrative says the observation is still ongoing; it does not fill the gap with generic praise.

## Pre-conversion validation checklist

Run this pass before writing any output document, and report the result with the delivery:

- Every instrument in the set names its goal and CP element; documents are not produced for instruments that lack them.
- The interpretation guide exists and its category descriptors match the indicators in the set, indicator by indicator.
- Indicator wording is identical across all documents being produced in this pass.
- Identity data is complete for the headers; no placeholder such as [Nama Sekolah] remains in a document meant for direct use. Placeholders are acceptable only in a blank template the user explicitly asked for.
- The roster, when per-child documents are requested, is the roster the user supplied, complete and unaltered.
- No document contains a score column, a total, or a ranking field. Their presence means a higher-level format has leaked into this level's documents; remove and report.

Any failure stops the conversion for the affected documents. List the failures and hand them back; do not guess a descriptor, drop an indicator quietly, or invent identity data.

## Gotchas

- Never invent observation results. An empty report shell is a valid deliverable; a filled report without supplied evidence is fabrication.
- Keep records confidential in form as well as content: per-child documents are produced per child, not as one class sheet that exposes every child's categories to whoever holds the page, unless the user explicitly asks for a teacher-only class overview.
- Handwriting space is a functional requirement, not decoration. A beautiful sheet with rows too small to write in fails in the classroom exactly like a wrong indicator does.
- Do not offer a spreadsheet of categories as a "summary with scores". A teacher-only overview may list categories per child for planning; it still carries no numbers and no ranking.
