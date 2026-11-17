---
name: modul-ajar-sd-mi
description: "Design Indonesian Kurikulum Merdeka teaching modules (modul ajar) for SD/MI only (Fase A-C, Kelas I-VI): derive Tujuan Pembelajaran (TP) and Alur Tujuan Pembelajaran (ATP) from Capaian Pembelajaran (CP) per fase, plan deep learning experiences in the Memahami, Mengaplikasi, and Merefleksi stages mapped to SOLO levels with concrete, play-based design in Fase A, target the 8 Dimensi Profil Lulusan, build differentiated LKPD per fase (picture-based and hands-on in Fase A, short written sections in Fase B, fuller worksheets in Fase C), place observation-based formative checkpoints that hand over to the SD/MI assessment skill, and turn assessment follow-up bands into concrete classroom intervention scenarios."
---

# Modul Ajar SD/MI (Fase A-C)

Skill for planning teaching under Kurikulum Merdeka (Kemendikdasmen) for SD/MI only: Fase A (Kelas I-II), Fase B (Kelas III-IV), and Fase C (Kelas V-VI). It works upstream of assessment: it turns a Capaian Pembelajaran (CP) into Tujuan Pembelajaran (TP), orders the TP into an Alur Tujuan Pembelajaran (ATP), and builds the learning experiences, worksheets, and formative checkpoints that make those TP reachable in a primary classroom. Assessment results then flow back into this skill as concrete intervention plans for the next meetings.

Verification status: the deep-learning stage model and its SOLO mapping below follow the Naskah Akademik Pembelajaran Mendalam (Tabel 3.1, pp. 44-45), and the process-assessment provisions follow Permendikdasmen No. 1 Tahun 2026, Pasal 8 and Pasal 15-19; both have been checked against the primary documents. The CP citation (SK Kepala BSKAP No. 046/H/KR/2025) has not been independently verified. Check a cited rule in the official document before relying on it for a formal school document. Background detail lives in [references/kerangka-pembelajaran-mendalam-sd-mi.md](references/kerangka-pembelajaran-mendalam-sd-mi.md).

Sibling skills for this jenjang: asesmen-sd-mi designs the assessment packages and KKTP from the TP list this skill hands over; stimulus-sd-mi builds reading passages and visuals pitched at Fase A-C; telaah-sd-mi reviews finished items; konverter-sd-mi converts finished packages into Kartu Soal, print scripts, and CBT files.

## When this skill applies

- The user asks for a modul ajar, a lesson plan, or a teaching scenario for an SD/MI class.
- The user needs a CP for Fase A, B, or C broken down into TP, or TP ordered into an ATP for a semester or a phase.
- The user wants learning activities built on Pembelajaran Mendalam: the three experience stages Memahami, Mengaplikasi, and Merefleksi, pitched at primary-school children.
- The user asks which of the 8 Dimensi Profil Lulusan a unit develops, and how to show that in the plan.
- The user needs an LKPD with differentiation by readiness level, for example a picture-heavy guided version and a challenge version of the same task.
- The user has assessment results grouped by KKTP band and needs them turned into actual classroom activities for the next meetings.
- The user asks for teacher or student reflection instruments for a lesson or a semester.

Indonesia only, same boundary as the assessment skill: Kurikulum Merdeka, Fase A-C, CP from SK Kepala BSKAP No. 046/H/KR/2025 (citation not independently verified). It does not plan lessons for other jenjang or foreign curricula.

## When this skill does not apply

- Writing test items, kisi-kisi, answer keys, scoring guides, or KKTP rubrics belongs to asesmen-sd-mi. This skill ends at the TP list and the formative checkpoints; it does not write the exam.
- Auditing finished items belongs to telaah-sd-mi. Converting a finished package into print or CBT formats belongs to konverter-sd-mi. Building a stimulus text or a visual belongs to stimulus-sd-mi, although this skill may request one.
- General timetable, staffing, or school administration planning is out of scope.

## Two modes of use

Standalone mode: the user asks only for teaching planning. Deliver the modul ajar package described below and stop. Do not add test items the user did not ask for.

Invoked mode: the user (or the assessment workflow) needs the upstream half of an assessment package. In this mode the deliverable that matters most is the TP list: each TP written as one measurable statement, tagged with its CP element, its position in the ATP, its target SOLO level, and the Dimensi Profil Lulusan it serves. Hand that list to asesmen-sd-mi, which builds the kisi-kisi from it. If the TP list is vague, the items built on it will be vague too, so this handoff is the quality gate for the whole chain.

## Workflow

1. Read the CP. Identify the element, the fase (A, B, or C), and the competencies and content named in it. If the user has not supplied the CP text or at least the subject, fase, and topic, ask for them before planning. Do not invent CP wording and present it as official text; if you draft a paraphrase, label it as a paraphrase.
2. Derive TP. Break the CP into TP that a teacher can observe and check: one verb, one content focus, one TP per statement. Keep the count teachable, usually two to five TP per meeting sequence.
3. Order the ATP. Sequence the TP from concrete to abstract and from single-aspect to integrated understanding, so the order itself scaffolds learning across meetings. At SD/MI the concrete end matters most: start from objects, pictures, and direct experience before symbols and text.
4. Map each TP to a target SOLO level and to one or two Dimensi Profil Lulusan. A TP that maps to no dimension and no SOLO level is probably filler; rewrite or drop it. Use the Naskah Akademik Pembelajaran Mendalam mapping (Tabel 3.1, pp. 44-45): Memahami covers Unistruktural and Multistruktural together, Mengaplikasi is Relasional, Merefleksi is Berpikir Abstrak yang Mendalam, and Prastruktural is not a stage but the status "Belum Memahami".
5. Design the learning experiences in three stages. Memahami: students meet the phenomenon, picture, story, or object, connect prior knowledge, and name the key facts and concepts (SOLO target: Unistruktural moving to Multistruktural). Mengaplikasi: students use the concept on a real case, a simple data set, or a hands-on problem, working with the parts together (SOLO target: Relasional). Merefleksi: students say or show how they reasoned, check their conclusion against a new example, or apply the concept to a situation at home or school (SOLO target: Berpikir Abstrak yang Mendalam, the Naskah Akademik's term for the fifth SOLO level; "Extended Abstract" is Biggs & Collis's original English term). State for each stage what the teacher does, what the students do, and what product or answer shows the stage worked.
6. Place formative checkpoints between stages. Each checkpoint is a short check tied to one TP: an exit question, a quick observation point, or one LKPD section. Its only job is to catch a misconception before the sumatif assessment does. The technique and instrument chosen must stay aligned with the TP (Permendikdasmen No. 1 Tahun 2026, Pasal 8). At Fase A every checkpoint is observation, performance, or play, never a written test (PPA Edisi Revisi 2025, p. 45). Deciding the item format and scoring for a checkpoint belongs to asesmen-sd-mi; here, state what evidence the checkpoint must produce.
7. Plan differentiation before it is needed. For each main task, note the simplified entry point (fewer variables, worked example, picture support, sentence starters) and the extension (extra variable, open data, transfer case), so the follow-up scenarios below can reuse them.
8. Hand off. Close the plan with the clean TP list for asesmen-sd-mi, plus the misconception list the checkpoints are watching for.

## Output structure of a modul ajar

Deliver these parts in order:

1. Identitas: school (placeholder when unknown), subject, fase and kelas, semester, time allocation, number of meetings.
2. CP and element, quoted or clearly labelled as paraphrased, with the source the user supplied.
3. TP list: numbered, one measurable statement each.
4. ATP diagram or numbered sequence showing the order across meetings and why that order.
5. Dimensi Profil Lulusan targets: which dimensions this unit develops and where each one shows up in an activity, not just a list pasted at the top.
6. Learning experiences per meeting, in the three stages, with teacher activity, student activity, and the evidence each stage produces.
7. LKPD plan: the worksheet sections, which TP each section serves, and its simplified and challenge variants (see the fase notes below).
8. Formative checkpoints: placement, the TP checked, and the evidence expected.
9. Reflection instruments: the teacher reflection set and the student reflection set from the reference file, trimmed to the unit when the user wants a short version. The teacher set serves the process assessment of Permendikdasmen No. 1 Tahun 2026, Pasal 15-19, which includes teacher self-reflection at least once per semester.
10. Handoff block: the TP list and misconception watchlist, formatted so asesmen-sd-mi can consume it directly.

## LKPD per fase

- Fase A: the worksheet is mostly pictures and concrete activity. Large images to observe, match, sort, or colour with a purpose; tracing and copying short words; tasks the child completes by doing (arranging objects, pointing, demonstrating) while the teacher observes. Written answers are minimal: a word, a tick, a drawing. Instructions are read aloud by the teacher.
- Fase B: short written sections appear. One short paragraph or picture series per task, sentence starters for written answers, tables with two or three columns to complete, and simple worked examples before independent items.
- Fase C: fuller worksheets. A medium text or data table as the working material, multi-step tasks, space for a short written explanation, and a challenge section that asks for transfer to a new situation.

## From assessment bands to classroom scenarios

When assessment results come back grouped by the KKTP descriptive bands, do not deliver a table that only repeats the bands. Turn each band into a scenario a teacher can run next meeting, naming the activity, the material, the grouping, and the exit evidence:

- Perlu bimbingan (Prastruktural to Unistruktural): reteach the base concept in a smaller step. Use the simplified LKPD variant, a worked example the group completes together, and short guided practice with the teacher or a trained peer tutor at the table. At Fase A this is guided play and hands-on repetition, not extra worksheets. Exit evidence: the student can state the concept and solve one guided case without help.
- Cukup (Multistruktural): the parts are known but not yet connected. Run a connecting task: a concept map, a compare-two-cases exercise, or the standard LKPD with the linking section emphasised. Exit evidence: the student explains how two parts of the material relate.
- Baik (Relasional): no reteaching. The group moves to the next TP in the ATP and gets the standard task at full difficulty. Exit evidence comes from the next unit's first checkpoint.
- Sangat baik (Berpikir Abstrak yang Mendalam): give a transfer or challenge task from the extension variant: new context, open data, or a small project. This group can also serve as peer tutors for the first group, which counts as their enrichment when the tutoring task requires them to explain and justify, not just to give answers.

Keep the grade rules from asesmen-sd-mi intact while planning these scenarios: remedial grades follow Prinsip 1 (Mastery Learning, highest score after remedial, with an equal improvement chance for students who already passed), and formatif results never decide report grades or promotion. The scenarios change the teaching, not the grade policy.

## Gotchas

- Do not write exam items inside a modul ajar. A plan that quietly contains the sumatif questions teaches to the test and breaks the handoff.
- Do not copy a CP from memory and present it as the official SK text. Quote what the user supplied or label your version a paraphrase.
- Do not list all 8 Dimensi Profil Lulusan as targets for every unit. Pick the one to three the activities genuinely develop; a unit that claims all eight usually develops none on paper that a supervisor can trace.
- Do not skip the Merefleksi stage to save time. Without it the sequence stops at Relasional and the Berpikir Abstrak yang Mendalam TP in the ATP has no activity that reaches it.
- Do not write TP with stacked verbs ("memahami dan menganalisis dan mengevaluasi"). One TP, one verb, one focus; split it if it needs two.
- Do not plan differentiation as different final grades. Differentiate the content, the process, and the support; the KKTP expectation for the TP stays the same.
- Do not design a written formative test for Fase A, in the plan or in a checkpoint. Observation, performance, and play are the Fase A instruments.
- Do not present citations beyond their verified status. The SOLO stage mapping and the Permendikdasmen No. 1/2026 provisions (Pasal 8, Pasal 15-19) are verified against the primary documents; the CP citation (SK BSKAP 046/2025) is not, so flag it as unverified wherever a formal document relies on it.
