---
name: telaah-validasi-butir-soal
description: "Independent second-pass review of Kurikulum Merdeka test items written by anyone (AI, a teacher, or an MGMP team): qualitative review with the Pusmendik review card (Materi, Konstruksi, Bahasa codes for PG/PGK and Uraian), a verdict per item (accept, revise, or reject with reasons), distractor surgery that rewrites failed options from named student misconceptions, quantitative item analysis when trial scores are supplied (difficulty index P, discrimination index D with top and bottom 27 percent groups, distractor effectiveness), and the key-distribution check inherited from the core asesmen skill."
---

# Telaah dan Validasi Butir Soal

This skill reviews test items that already exist. It does not write new packages; the core skill asesmen_kurikulum_merdeka does that. This one acts as the independent reviewer: it checks items written by an AI, by a teacher, or by an MGMP team against the Pusmendik qualitative review card, gives every item a verdict with reasons, repairs weak distractors, and, when trial results are available, runs the numbers on how each item actually performed.

The checklists, formulas, and working standards live in [references/kartu-telaah-pusmendik.md](references/kartu-telaah-pusmendik.md). Read that file before reviewing a set.

## When this skill applies

- The user hands over existing items, a draft exam, or a question bank and asks for a review, a telaah, a validation, or a quality check.
- The user supplies trial or class score data (who answered what, or per-item correct counts) and asks for item analysis: difficulty, discrimination, or distractor performance.
- A package produced with the core asesmen skill needs its second pass before it is used in class or uploaded to a bank soal such as NINEXAM.
- A teacher wants a second opinion on items from another source before adopting them.

It does not apply to writing items from scratch, building a kisi-kisi, or setting KKTP. Route those back to asesmen_kurikulum_merdeka.

## The independence rule

An author reviewing their own items in the same pass will miss their own blind spots. That is why this skill exists separately from the core skill's Step 7 self-audit.

- The core skill's self-audit is the author's quick check before delivery. This skill is the second, deeper pass, run as if the reviewer did not write the items.
- Never let a review under this skill silently replace the self-audit, and never present a self-audit as if it were this independent review. Name which one a report is.
- Review the item as printed, not as intended. If the indicator, the key, or the scoring guide is missing, that absence is itself a finding; do not reconstruct what the author probably meant and pass the item on that basis.
- When the reviewer and the author disagree, the card decides: cite the code that fails (for example K3 or B1) instead of arguing taste.

## Workflow

### Step 1: Set up the review

Collect what the verdict will be judged against: the items, their keys, the kisi-kisi or indicator for each item, the item format, the fase and subject, and the scoring guide for essays. Items that arrive without a key or an indicator can still be reviewed for construction and language, but their Materi verdict is "cannot be confirmed" until the missing piece is supplied. Say so in the report instead of guessing.

### Step 2: Qualitative review with the card

Work item by item through the review card in the reference file:

- PG and PGK items: the Materi codes (M), Konstruksi codes (K), and Bahasa codes (B).
- Uraian items: the U-M, U-K, and U-B codes, including whether a URO keyword list or a URN SOLO rubric is present and usable.

Record a pass or fail per code, with a short note on any fail that quotes or points at the exact words in the item that cause it. A fail without a location is not actionable.

### Step 3: Verdict per item

Give every item exactly one verdict:

- Terima (accept): every applicable code passes. The item may enter the bank as is.
- Revisi (revise): the item measures the right thing but has a fixable defect: a weak distractor, uneven option lengths, a double negative, a missing rubric line. State the fix, and supply the revised text in Step 4 or in the output.
- Tolak (reject): the item cannot be repaired by editing: it does not measure its indicator, it has more than one defensible key or no defensible key, its stimulus leaks the answer or the formula, or (after a trial) its discrimination index is negative. State which defect is fatal.

No set-level verdict replaces the per-item verdicts. A set can be "mostly sound" and still contain two items that must not be used.

### Step 4: Distractor surgery

Run this on every PG or PGK item whose distractors fail the card or the trial data. This procedure is a working standard of this skill:

1. Diagnose each failing distractor and name the failure: too obvious (no plausible path leads to it), implausible (outside the topic or absurd on its face), cueing the key (longer, more precise, or grammatically matching the stem while others do not), or non-homogeneous (different kind, unit, or category from the key).
2. Name the student misconception the replacement will target: the specific wrong idea a real student holds, such as reversing a cause and its effect, applying a formula to the wrong quantity, or confusing two similar terms. A distractor without a named misconception behind it is decoration.
3. Rewrite the distractor so it is exactly what a student with that misconception would produce or choose: correct method with one wrong step, right value with the wrong unit, the paired concept swapped in.
4. Re-check the repaired set: options homogeneous in kind and content, similar in length, ordered consistently (numbers ascending or chronological), no option giving away another, and the key not identifiable by form alone.

Show the before and after text for every operated distractor, with the misconception named. Never change the key during surgery without flagging it as a key change and re-running the Materi codes.

### Step 5: Quantitative analysis, when trial data exists

Only run this step when the user supplies response data from a real tryout or class administration. Never invent performance numbers for items that have not been tried.

- Difficulty index P: the share of test takers who answered correctly. Bands and formula are in the reference file.
- Discrimination index D: compare the top 27 percent and the bottom 27 percent of test takers by total score. This 27 percent split is this skill's working standard, taken from classical test theory convention.
- Distractor effectiveness: a distractor is functioning when at least 5 percent of the lower group chose it and the lower group chose it more than the upper group did. A distractor nobody chooses, or one the upper group prefers, is dead weight and goes to surgery.
- Verdicts from numbers: an item with negative D is rejected outright, because strong students fail it more than weak students do, which signals a wrong key or a misleading stem. An item with D in the revise band goes back to Step 2 and Step 4 with the data as evidence.

Interpret P together with D, never alone. A hard item (low P) with strong D is a good HOTS item and stays; an easy item with near-zero D measures nothing and does not earn its place outside a diagnostic set.

### Step 6: Key-distribution check

For the PG items in the set, compute R = (number of PG items / number of options) + 3, inherited from the core skill's self-audit. No key letter may appear more than R times. If one letter exceeds R, rebalance by reordering options on items where the content allows it, and list every item whose options were reordered. Reordering options is a change to the item: note it in the report.

## Output format

Deliver the review in this order:

1. Ringkasan Telaah: how many items were reviewed, by format, and the count per verdict (terima, revisi, tolak), plus any set-level problem such as a missing kisi-kisi or a failed key distribution.
2. Tabel Putusan per Butir: one row per item with its number, format, verdict, the card codes that failed, and a one-line reason.
3. Teks Revisi: the full revised text of every item marked revisi, including operated distractors shown before and after with their named misconceptions, and the revised scoring guide where an essay guide changed.
4. Hasil Analisis Kuantitatif, only when trial data was supplied: per item, P with its band, D with its band, and the distractor findings, each tied back to the verdict it supports.
5. Catatan Kunci: the R computation and any rebalancing done.

Write reasons in plain language a teacher can act on without opening the reference file. Codes support the reason; they do not replace it.

## Gotchas

- Do not run quantitative analysis on invented data. No trial, no P and D.
- Do not pass an item because its intention was good. Review what is printed.
- Do not rewrite a whole item during distractor surgery. Surgery touches distractors; a broken stem or a wrong indicator is a revise or reject verdict with the reason stated.
- Do not soften a negative D. It always means reject, however elegant the item looks.
- Do not treat the regulatory citations behind the review card as verified law. The card content here was rebuilt from Gemini research shared on 2026-11-17 and has not been independently checked against the official Pusmendik documents; the 27 percent and 5 percent rules are classical test theory conventions, stated as this skill's working standards.
