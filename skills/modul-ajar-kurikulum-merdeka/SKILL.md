---
name: modul-ajar-kurikulum-merdeka
description: "Design Indonesian Kurikulum Merdeka teaching modules (modul ajar) for PAUD and Fase A-F: derive Tujuan Pembelajaran (TP) and Alur Tujuan Pembelajaran (ATP) from Capaian Pembelajaran (CP), plan deep learning experiences in the Memahami, Mengaplikasi, and Merefleksi stages mapped to SOLO levels, target the 8 Dimensi Profil Lulusan, build differentiated LKPD and formative checkpoints, turn assessment follow-up bands into concrete classroom intervention scenarios, and hand a clean TP list to the asesmen_kurikulum_merdeka skill for item writing."
---

# Modul Ajar Kurikulum Merdeka

Skill for planning teaching under Kurikulum Merdeka (Kemendikdasmen) for PAUD and Fase A-F (SD, SMP, SMA, SMK). It works upstream of assessment: it turns a Capaian Pembelajaran (CP) into Tujuan Pembelajaran (TP), orders the TP into an Alur Tujuan Pembelajaran (ATP), and builds the learning experiences, worksheets, and formative checkpoints that make those TP reachable in class. Assessment results then flow back into this skill as concrete intervention plans for the next meetings.

Verification status: the deep-learning stage model and its SOLO mapping below follow the Naskah Akademik Pembelajaran Mendalam (Tabel 3.1, pp. 44-45), and the process-assessment provisions follow Permendikdasmen No. 1 Tahun 2026, Pasal 8 and Pasal 15-19; both have been checked against the primary documents. The CP citation (SK Kepala BSKAP No. 046/H/KR/2025) has not been independently verified. Check a cited rule in the official document before relying on it for a formal school document. Background detail lives in [references/kerangka-pembelajaran-mendalam.md](references/kerangka-pembelajaran-mendalam.md).

## When this skill applies

- The user asks for a modul ajar, a lesson plan, or a teaching scenario for a Kurikulum Merdeka class.
- The user needs CP broken down into TP, or TP ordered into an ATP for a semester or a phase.
- The user wants learning activities built on Pembelajaran Mendalam: the three experience stages Memahami, Mengaplikasi, and Merefleksi.
- The user asks which of the 8 Dimensi Profil Lulusan a unit develops, and how to show that in the plan.
- The user needs an LKPD (student worksheet) with differentiation by readiness level, for example a simplified version and a challenge version of the same task.
- The user has assessment results grouped by KKTP band and needs them turned into actual classroom activities: what the Perlu bimbingan group does next meeting, what the Sangat baik group does, and so on.
- The user asks for teacher or student reflection instruments for a lesson or a semester.

Indonesia only, same boundary as the assessment skill: Kurikulum Merdeka, Fase A-F, CP from SK Kepala BSKAP No. 046/H/KR/2025 (citation not independently verified). It does not plan lessons for foreign curricula or test systems.

## When this skill does not apply

- Writing test items, kisi-kisi, answer keys, scoring guides, or KKTP rubrics belongs to the asesmen_kurikulum_merdeka skill. This skill ends at the TP list and the formative checkpoints; it does not write the exam.
- Auditing finished items belongs to telaah_validasi_butir_soal. Converting a finished package into print or CBT formats belongs to konverter_naskah_ujian_dan_cbt. Building a stimulus text or a visual belongs to stimulus_dan_ilustrasi_asesmen, although this skill may request one.
- General timetable, staffing, or school administration planning is out of scope.

## Two modes of use

Standalone mode: the user asks only for teaching planning. Deliver the modul ajar package described below and stop. Do not add test items the user did not ask for.

Invoked mode: the user (or the assessment workflow) needs the upstream half of an assessment package. In this mode the deliverable that matters most is the TP list: each TP written as one measurable statement, tagged with its CP element, its position in the ATP, its target SOLO level, and the Dimensi Profil Lulusan it serves. Hand that list to asesmen_kurikulum_merdeka, which builds the kisi-kisi from it. If the TP list is vague, the items built on it will be vague too, so this handoff is the quality gate for the whole chain.

## Workflow

1. Read the CP. Identify the element, the phase, and the competencies and content named in it. If the user has not supplied the CP text or at least the subject, fase, and topic, ask for them before planning. Do not invent CP wording and present it as official text; if you draft a paraphrase, label it as a paraphrase.
2. Derive TP. Break the CP into TP that a teacher can observe and check: one verb, one content focus, one TP per statement. Keep the count teachable, usually two to five TP per meeting sequence.
3. Order the ATP. Sequence the TP from concrete to abstract and from single-aspect to integrated understanding, so the order itself scaffolds learning across meetings.
4. Map each TP to a target SOLO level and to one or two Dimensi Profil Lulusan. A TP that maps to no dimension and no SOLO level is probably filler; rewrite or drop it. Use the Naskah Akademik Pembelajaran Mendalam mapping (Tabel 3.1, pp. 44-45): Memahami covers Unistruktural and Multistruktural together, Mengaplikasi is Relasional, Merefleksi is Berpikir Abstrak yang Mendalam, and Prastruktural is not a stage but the status "Belum Memahami".
5. Design the learning experiences in three stages. Memahami: students meet the phenomenon or text, connect prior knowledge, and name the key facts and concepts (SOLO target: Unistruktural moving to Multistruktural). Mengaplikasi: students use the concept on a real case, data set, or problem, working with the parts together (SOLO target: Relasional). Merefleksi: students evaluate their own reasoning, defend a conclusion, or transfer the concept to a new situation (SOLO target: Berpikir Abstrak yang Mendalam, the Naskah Akademik's term for the fifth SOLO level; "Extended Abstract" is Biggs & Collis's original English term). State for each stage what the teacher does, what the students do, and what product or answer shows the stage worked.
6. Place formative checkpoints between stages. Each checkpoint is a short check tied to one TP: an exit question, a quick observation point, or one LKPD section. Its only job is to catch a misconception before the sumatif assessment does. The technique and instrument chosen must stay aligned with the TP (Permendikdasmen No. 1 Tahun 2026, Pasal 8). Deciding the item format and scoring for a checkpoint belongs to the assessment skill; here, state what evidence the checkpoint must produce.
7. Plan differentiation before it is needed. For each main task, note the simplified entry point (fewer variables, worked example, sentence starters) and the extension (extra variable, open data, transfer case), so the follow-up scenarios below can reuse them.
8. Hand off. Close the plan with the clean TP list for the assessment skill, plus the misconception list the checkpoints are watching for.

## Output structure of a modul ajar

Deliver these parts in order:

1. Identitas: school (placeholder when unknown), subject, fase and kelas, semester, time allocation, number of meetings.
2. CP and element, quoted or clearly labelled as paraphrased, with the source the user supplied.
3. TP list: numbered, one measurable statement each.
4. ATP diagram or numbered sequence showing the order across meetings and why that order.
5. Dimensi Profil Lulusan targets: which dimensions this unit develops and where each one shows up in an activity, not just a list pasted at the top.
6. Learning experiences per meeting, in the three stages, with teacher activity, student activity, and the evidence each stage produces.
7. LKPD plan: the worksheet sections, which TP each section serves, and its simplified and challenge variants.
8. Formative checkpoints: placement, the TP checked, and the evidence expected.
9. Reflection instruments: the teacher reflection set and the student reflection set from the reference file, trimmed to the unit when the user wants a short version. The teacher set serves the process assessment of Permendikdasmen No. 1 Tahun 2026, Pasal 15-19, which includes teacher self-reflection at least once per semester.
10. Handoff block: the TP list and misconception watchlist, formatted so asesmen_kurikulum_merdeka can consume it directly.

## From assessment bands to classroom scenarios

When assessment results come back grouped by the KKTP descriptive bands, do not deliver a table that only repeats the bands. Turn each band into a scenario a teacher can run next meeting, naming the activity, the material, the grouping, and the exit evidence:

- Perlu bimbingan (Prastruktural to Unistruktural): reteach the base concept in a smaller step. Use the simplified LKPD variant, a worked example the group completes together, and short guided practice with the teacher or a trained peer tutor at the table. Exit evidence: the student can state the concept and solve one guided case without help.
- Cukup (Multistruktural): the parts are known but not yet connected. Run a connecting task: a concept map, a compare-two-cases exercise, or the standard LKPD with the linking section emphasised. Exit evidence: the student explains how two parts of the material relate.
- Baik (Relasional): no reteaching. The group moves to the next TP in the ATP and gets the standard task at full difficulty. Exit evidence comes from the next unit's first checkpoint.
- Sangat baik (Berpikir Abstrak yang Mendalam): give a transfer or challenge task from the extension variant: new context, open data, or a small project. This group can also serve as peer tutors for the first group, which counts as their enrichment when the tutoring task requires them to explain and justify, not just to give answers.

Keep the grade rules from the assessment skill intact while planning these scenarios: remedial grades follow Prinsip 1 (Mastery Learning, highest score after remedial, with an equal improvement chance for students who already passed), and formatif results never decide report grades or promotion. The scenarios change the teaching, not the grade policy.

## Gotchas

- Do not write exam items inside a modul ajar. A plan that quietly contains the sumatif questions teaches to the test and breaks the handoff.
- Do not copy a CP from memory and present it as the official SK text. Quote what the user supplied or label your version a paraphrase.
- Do not list all 8 Dimensi Profil Lulusan as targets for every unit. Pick the one to three the activities genuinely develop; a unit that claims all eight usually develops none on paper that a supervisor can trace.
- Do not skip the Merefleksi stage to save time. Without it the sequence stops at Relasional and the Berpikir Abstrak yang Mendalam TP in the ATP has no activity that reaches it.
- Do not write TP with stacked verbs ("memahami dan menganalisis dan mengevaluasi"). One TP, one verb, one focus; split it if it needs two.
- Do not plan differentiation as different final grades. Differentiate the content, the process, and the support; the KKTP expectation for the TP stays the same.
- Do not present citations beyond their verified status. The SOLO stage mapping and the Permendikdasmen No. 1/2026 provisions (Pasal 8, Pasal 15-19) are verified against the primary documents; the CP citation (SK BSKAP 046/2025) is not, so flag it as unverified wherever a formal document relies on it.
