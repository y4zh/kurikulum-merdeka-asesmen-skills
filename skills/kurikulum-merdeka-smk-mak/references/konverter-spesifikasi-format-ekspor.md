# Spesifikasi Format Ekspor SMK/MAK

Scope: the Kartu Soal template, the Naskah Ujian layout, the Lembar Penilaian Praktik layout, GIFT, Moodle XML, and CSV formats, for SMK/MAK Fase E-F where written items carry 5 options (A-E). One encoding choice is deliberate: the MCMA GIFT encoding below follows the core skill's scoring policy (sumatif MCMA binary 1-0, formatif MCMA 2-1-0), so the LMS fraction fields act only as transport encoding. See SKILL.md, "Scoring conversion rule", before using any example here.

## 1. Kartu Soal: field structure

One card per item. A card holds everything a supervisor or reviewer needs to judge the item without opening another document.

Identity block:

- Satuan Pendidikan
- Mata Pelajaran
- Konsentrasi Keahlian (for vocational subjects)
- Kurikulum or reference basis (for example Kurikulum Merdeka, CP per SK Kepala BSKAP 046/H/KR/2025, as named in the source package)
- Fase, Kelas, Semester
- Bentuk Soal dan Nomor Soal

Planning block:

- Capaian Pembelajaran (CP): the relevant element text from the package
- Tujuan Pembelajaran (TP)
- Materi Pokok or Elemen Kompetensi
- Indikator Soal: the indicator sentence with its operational verb (KKO)
- Level Kognitif: Bloom level with its LOTS, MOTS, or HOTS group, plus the SOLO level where the package assigns one

Item and scoring block:

- Stimulus: full text or visual reference, exactly as the student sees it
- Rumusan Butir Soal: stem and options
- Kunci Jawaban: the key, or the key set for MCMA, or the per-statement keys for PGK Kategori
- Bobot Skor and Pedoman Penskoran: the item weight, the URO keyword list, or the URN rubric, copied from the package unchanged

Practical task card variant: for an Unjuk Kerja task, the item and scoring block is replaced by the work order (perintah kerja), the job specification, the tools and materials list, the time limit, and the full performance rubric with its aspects and descriptors. There is no key on a task card; the specification and rubric are its scoring truth.

## 2. Naskah Cetak: layout spec

The printed script is student-facing and covers the written sections. Build it in this order:

1. Kop (header): school name and address line as given in the identity data, exam name and assessment type, subject, fase and kelas, semester and academic year, day and date, and time allocation. A horizontal rule separates the kop from the body.
2. Petunjuk Umum: how many items per section, how to record answers, whether corrections are allowed, and that rough work is not collected. Keep it short and in plain Indonesian.
3. Sections by format, in the package's order. Each section opens with its own short instruction line (for example, choose one answer, choose all correct statements, or answer in your own sentences), then its stimulus blocks and items, numbered continuously across the whole script.
4. Stimulus placement: print each stimulus once, directly above the first item that uses it, with the items that share it following in order. Workplace documents (SOP excerpts, specification tables, work drawings) print at full readability; a drawing that shrinks below readable size moves to an A3 attachment page, never to a smaller font.
5. Lembar Jawaban: a separate sheet for the objective sections, with student identity fields (name, class, attendance number), one answer grid row per item, five lettered cells (A-E) per row, and a separate lined space or separate sheet for Uraian answers.

Practical tasks are not printed in the Naskah Ujian. The student receives the work order sheet (task, specification, tools, time, safety notes, without rubric descriptors), and the assessor works from the Lembar Penilaian Praktik in section 3.

Never print keys, pembahasan, KKTP bands, or scoring notes in the script or the answer sheet.

## 3. Lembar Penilaian Praktik: layout spec

The practical assessment sheet is assessor-facing, one sheet per student per task. Build it in this order:

1. Kop and identity: school, subject, konsentrasi keahlian, fase and kelas, task name, date; then the student's name, NIS, and class.
2. Task summary: work order number or title, the job specification in brief (the dimensions, tolerances, or service standard the result is judged against), tools and materials issued, and the time limit.
3. Time record: start time, finish time, and duration, filled in during the session.
4. Aspect table, one row per rubric aspect, with columns: Aspek | Deskriptor Tuntas | Deskriptor Belum Tuntas | Skor | Catatan Pengamatan. Default aspect rows, copied from the package's rubric unchanged: Keselamatan Kerja (K3), Urutan Prosedur, Ketepatan Hasil, Waktu, Sikap Kerja. The notes column records observed events as they happen: a skipped step, a measurement repeated, a safety incident.
5. Critical rule line: where the package declares a critical rule (for example, a serious safety violation stops the attempt), print the rule and a met/not-met tick box. Copy the rule from the package; never invent one at conversion time.
6. Judgement and closing: total or per-aspect judgement (tuntas or belum tuntas per aspect, as the package's KKTP states), the follow-up consequence the package prescribes (which aspects are repeated in remedial), and the assessor's name and signature line.

Print the sheet on one or two pages per student; descriptors must stay at readable size, so a long rubric goes to two pages rather than a smaller font.

## 4. GIFT examples

GIFT is plain text. Each question opens with a ::name:: line, the stem follows (prefix it with [html] when the stem carries markup), and the answer block sits in braces. In the answer block, = marks full credit in single-answer questions, ~ marks an option in multiple-response encoding, and %n% sets that option's fraction. Escape = ~ # { } : inside answer text with a backslash.

### PG, single answer (SMK/MAK, 5 options)

```text
::SMK-F-01-PG::[html]<p>Sebelum mengoperasikan mesin bubut untuk pekerjaan pembubutan rata, tindakan keselamatan kerja yang wajib dilakukan operator adalah...</p>{
=Memeriksa kondisi mesin, memakai kacamata pelindung, dan memastikan benda kerja terjepit kuat pada cekam
~Menyalakan mesin terlebih dahulu agar putaran stabil sebelum benda kerja dipasang pada cekam
~Memakai sarung tangan kain agar tangan tidak licin saat memegang benda kerja yang berputar
~Mengatur putaran spindel setinggi mungkin agar proses pemotongan selesai lebih cepat
~Membersihkan tatal dengan tangan saat mesin masih berputar agar area kerja tetap bersih
}
```

### PGK MCMA, sumatif, harmonized all-or-nothing encoding

The item below has two correct options out of five. Per the conversion rule: the correct options share +100 in total, so each carries %50%; every wrong option carries %-100%, so any wrong pick cancels the credit; the LMS total is floored at zero and only a total of 100 earns the item score. This is not partial credit: the %50% figures are how the encoding splits the single binary point across the two correct options, nothing more. Verify the behaviour in the target LMS with a three-way test import before using it on a full set (see SKILL.md).

```text
::SMK-F-02-MCMA::[html]<p>Pilihlah DUA tindakan yang wajib dilakukan pada pemeriksaan awal kendaraan sebelum perawatan berkala dimulai!</p>{
~%50%Memeriksa level oli mesin dan kondisi aki sesuai lembar pemeriksaan
~%50%Memastikan kendaraan terparkir di permukaan rata, rem parkir terpasang, dan roda terganjal
~%-100%Menguras oli mesin sebelum memeriksa riwayat servis kendaraan
~%-100%Memanaskan mesin pada putaran tinggi selama 15 menit sebelum pemeriksaan
~%-100%Melepas terminal aki sebelum memeriksa tekanan angin ban
}
```

For a formatif MCMA export, keep the same shape but state in the export notes that the encoding approximates the package's 2-1-0 scale proportionally, as SKILL.md describes.
