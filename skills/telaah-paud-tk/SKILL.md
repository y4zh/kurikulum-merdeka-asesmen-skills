---
name: telaah-paud-tk
description: "Independently review Indonesian Kurikulum Merdeka PAUD and TK/RA assessment instruments only (Kelompok Bermain, Taman Kanak-Kanak, Raudhatul Athfal): check observation checklists, anecdotal record formats, developmental rating scales, and performance rubrics for alignment of indicators with the PAUD CP elements, clarity of observable behaviour, positive non-labelling language, real-time usability, and activity safety, repair weak indicators through indicator surgery, and give each instrument an accept, revise, or reject verdict with reasons, with no quantitative item analysis because this level has no test items."
---

# Telaah Instrumen PAUD & TK/RA

This skill reviews early-childhood assessment instruments that already exist: observation checklists, anecdotal record formats, developmental rating scales, and performance rubrics for Indonesian PAUD and TK/RA (Kelompok Bermain, Taman Kanak-Kanak, Raudhatul Athfal) under Kurikulum Merdeka. It does not design new instruments; asesmen-paud-tk does that. This skill acts as the independent reviewer: it checks each instrument against the review card in the reference file and gives it a verdict with reasons a teacher can act on.

There is no quantitative item analysis in this skill, deliberately. This level has no test items and no answer data, so difficulty and discrimination indices have nothing to attach to. Quality here is judged qualitatively: alignment, observability, language, usability, and safety. Anyone offering statistical validation for an observation checklist is selling a number without a basis.

This skill is one level of a per-level family. Its same-level siblings are asesmen-paud-tk, modul-ajar-paud-tk, stimulus-paud-tk, and konverter-paud-tk. Other education levels have their own review skills, including quantitative ones where test items exist; do not import their parameters into this one.

The card, checklists, and verdict rules live in [references/kartu-telaah-instrumen-paud.md](references/kartu-telaah-instrumen-paud.md). Read that file before reviewing a set.

## When this skill applies

- The user hands over existing PAUD or TK/RA observation instruments and asks for a review, a telaah, a validation, or a quality check.
- An instrument set produced with asesmen-paud-tk needs its second pass before it is used in class or adopted by a school or a teacher working group.
- A teacher wants a second opinion on observation formats from another source before adopting them.

It does not apply to designing instruments from scratch or setting developmental goals. Route those to asesmen-paud-tk and modul-ajar-paud-tk.

## The independence rule

An author reviewing their own instruments in the same pass will miss their own blind spots. That is why this skill exists separately from the asesmen-paud-tk self-audit.

- The self-audit in asesmen-paud-tk is the author's quick check before delivery. This skill is the second, deeper pass, run as if the reviewer did not write the instruments.
- Never present a self-audit as if it were this independent review. Name which one a report is.
- Review the instrument as printed, not as intended. If the goal, the CP element, or the interpretation guide is missing, that absence is itself a finding; do not reconstruct what the author probably meant and pass the instrument on that basis.
- When reviewer and author disagree, the card decides: cite the code that fails (for example O2 or K1) instead of arguing taste.

## Workflow

### Step 1: Set up the review

Collect what the verdict will be judged against: the instruments, the goal and CP element each indicator serves, the age group, the play context, and the interpretation guide (the BB, MB, BSH, BSB descriptors) where one exists. An instrument that arrives without its goal can still be reviewed for language, usability, and safety, but its alignment verdict is "cannot be confirmed" until the goal is supplied. Say so in the report instead of guessing.

### Step 2: Qualitative review with the card

Work instrument by instrument, indicator by indicator, through the card in the reference file:

- Materi codes (M): alignment with the CP element and goal, developmental fit for the age group.
- Observasi codes (O): whether each indicator names behaviour a teacher can actually see or hear during play, one behaviour per indicator.
- Konstruksi codes (K): whether the format is usable in real time while supervising play, and whether its categories and scales are defined.
- Bahasa codes (B): positive, non-labelling language, standard Indonesian.
- Keamanan dan Etika codes (A): physical and emotional safety of the observed activities, and confidentiality of the records.

Record a pass or fail per code, with a short note on any fail that points at the exact indicator or line that causes it. A fail without a location is not actionable.

### Step 3: Verdict per instrument

Give every instrument exactly one verdict:

- Terima (accept): every applicable code passes. The instrument may be used as is.
- Revisi (revise): the instrument targets the right goal but has a fixable defect: an indicator naming an inner state instead of behaviour, two behaviours fused in one row, an undefined scale step, a checklist too long to use while supervising. State the fix and supply the revised text in Step 4 or in the output.
- Tolak (reject): the instrument cannot be repaired by editing: it targets no identifiable goal or element, it requires children to read or write, it grades children numerically or ranks them, or its activity is unsafe. State which defect is fatal.

No set-level verdict replaces the per-instrument verdicts. A set can be mostly sound and still contain one instrument that must not be used.

### Step 4: Indicator surgery

Run this on every indicator that fails the Observasi codes. This procedure is a working standard of this skill:

1. Diagnose the failure and name it: inner state ("anak memahami...", "anak menyukai..."), fused behaviours (two or three actions in one row), trait language ("anak rajin"), or context-free wording that could mean anything in any activity.
2. Name the observable behaviour the indicator was reaching for: what the child does, says, builds, chooses, or shows, in the stated play context.
3. Rewrite the indicator as that behaviour, in positive wording, one behaviour per row, with the play context named where the behaviour only makes sense in one.
4. Re-check the repaired set: every indicator observable, the set still covers the goal, and the interpretation guide's category descriptors still match the rewritten indicators.

Show the before and after text for every operated indicator. Never change the goal an indicator serves during surgery without flagging it as a goal change and re-running the Materi codes.

## Output format

Deliver the review in this order:

1. Ringkasan Telaah: how many instruments were reviewed, by type, and the count per verdict (terima, revisi, tolak), plus any set-level problem such as a missing interpretation guide.
2. Tabel Putusan per Instrumen: one row per instrument with its name, type, verdict, the card codes that failed, and a one-line reason.
3. Teks Revisi: the full revised text of every instrument marked revisi, including operated indicators shown before and after.
4. Catatan Kategori: whether the BB, MB, BSH, BSB descriptors are defined per indicator and usable, since an instrument without them cannot feed a development report.

Write reasons in plain language a teacher can act on without opening the reference file. Codes support the reason; they do not replace it.

## Gotchas

- Do not invent observation data to "validate" an instrument statistically. No items, no indices; the card is the instrument of judgement here.
- Do not pass an instrument because its intention was good. Review what is printed.
- Do not rewrite a whole instrument during indicator surgery. Surgery touches indicators; a wrong goal or an unsafe activity is a revise or reject verdict with the reason stated.
- Do not let numeric scoring slip back in through the review: a checklist that totals ticks into a grade fails the level's basis, however tidy the format looks.
- Do not treat the review card as verified law. Its content has not been independently checked against official Pusmendik documents; it is this skill's working review instrument, built for this level's instrument types.
