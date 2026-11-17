# Spesifikasi Format Ekspor SMA/MA (Fase E-F)

Scope: the Kartu Soal template, GIFT, Moodle XML, and CSV formats for Fase E-F packages, where every PG item has 5 options (A-E). One encoding choice is deliberate: the MCMA GIFT encoding below follows the scoring policy of Bagian 3 (Asesmen) (sumatif MCMA binary 1-0, formatif MCMA 2-1-0), so the LMS fraction fields act only as transport encoding. See Bagian 5 of SKILL.md, "Scoring conversion rule", before using any example here.

## 1. Kartu Soal: field structure

One card per item. A card holds everything a supervisor or reviewer needs to judge the item without opening another document.

Identity block:

- Satuan Pendidikan
- Mata Pelajaran
- Kurikulum or reference basis (for example Kurikulum Merdeka, CP per SK Kepala BSKAP 046/H/KR/2025, as named in the source package)
- Fase, Kelas, Semester
- Bentuk Soal
- Nomor Soal

Planning block:

- Capaian Pembelajaran (CP): the relevant element text from the package
- Tujuan Pembelajaran (TP)
- Materi Pokok
- Indikator Soal: the indicator sentence with its operational verb (KKO)
- Level Kognitif: Bloom level with its LOTS, MOTS, or HOTS group, plus the SOLO level where the package assigns one

Item and scoring block:

- Stimulus: full text or visual reference, exactly as the student sees it
- Rumusan Butir Soal: stem and options
- Kunci Jawaban: the key, or the key set for MCMA, or the per-statement keys for PGK Kategori
- Bobot Skor and Pedoman Penskoran: the item weight, the URO keyword list, or the URN rubric, copied from the package unchanged

## 2. Naskah Cetak: layout spec

The printed script is student-facing. Build it in this order:

1. Kop (header): school name and address line as given in the identity data, exam name and assessment type, subject, fase and kelas, semester and academic year, day and date, and time allocation. A horizontal rule separates the kop from the body.
2. Petunjuk Umum: how many items per section, how to record answers, whether corrections are allowed, and that rough work is not collected. Keep it short and in plain Indonesian.
3. Sections by format, in the package's order. Each section opens with its own short instruction line (for example, choose one answer, choose all correct statements, or answer in your own sentences), then its stimulus blocks and items, numbered continuously across the whole script.
4. Stimulus placement: print each stimulus once, directly above the first item that uses it, with the items that share it following in order.
5. Lembar Jawaban: a separate sheet for the objective sections, with student identity fields (name, class, attendance number), one answer grid row per item with five lettered cells (A-E) matching the 5-option items, and a separate lined space or separate sheet for Uraian answers.

Never print keys, pembahasan, KKTP bands, or scoring notes in the script or the answer sheet.

## 3. GIFT examples

GIFT is plain text. Each question opens with a ::name:: line, the stem follows (prefix it with [html] when the stem carries markup), and the answer block sits in braces. In the answer block, = marks full credit in single-answer questions, ~ marks an option in multiple-response encoding, and %n% sets that option's fraction. Escape = ~ # { } : inside answer text with a backslash.

### PG, single answer (Fase F, 5 options)

```text
::GEO-F-01-PG::[html]<p>Perhatikan data curah hujan wilayah X berikut. Faktor utama penyebab tingginya limpasan permukaan di wilayah tersebut adalah...</p>{
=Alih fungsi lahan resapan di hulu menjadi kawasan terbangun
~Tingginya laju evaporasi harian di kawasan pesisir
~Dominasi batuan gamping berpori tinggi di lereng tengah
~Rendahnya kemiringan lereng di sekitar muara sungai
~Tingginya kerapatan vegetasi hutan hujan tropis primer
}
```

### PGK MCMA, sumatif, harmonized all-or-nothing encoding

The item below has two correct options out of five. Per the conversion rule: the correct options share +100 in total, so each carries %50%; every wrong option carries %-100%, so any wrong pick cancels the credit; the LMS total is floored at zero and only a total of 100 earns the item score. This is not partial credit: the %50% figures are how the encoding splits the single binary point across the two correct options, nothing more. Verify the behaviour in the target LMS with a three-way test import before using it on a full set (see Bagian 5 in SKILL.md).

```text
::GEO-F-02-MCMA::[html]<p>Pilihlah DUA pernyataan yang tepat mengenai mitigasi struktural bencana gempa bumi!</p>{
~%50%Penerapan standar bangunan tahan gempa berbasis isolasi seismik
~%50%Pembangunan jalur evakuasi vertikal dan rambu titik kumpul aman
~%-100%Pembentukan kelompok siaga bencana berbasis kearifan lokal
~%-100%Simulasi evakuasi mandiri secara berkala di sekolah
~%-100%Penyusunan peta risiko bencana oleh warga kelurahan
}
```

For a formatif MCMA export, keep the same shape but state in the export notes that the encoding approximates the package's 2-1-0 scale proportionally, as Bagian 5 in SKILL.md describes.

## 4. Moodle XML example

Well-formed XML, UTF-8. Question and answer text sit inside CDATA sections so HTML markup needs no escaping; text outside CDATA must escape ampersands, angle brackets, and quotes. The category question comes first and sets the bank path for the questions after it.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<quiz>
  <question type="category">
    <category>
      <text>$course$/top/Kurikulum-Merdeka/Fase-F/Geografi/HOTS-Relasional</text>
    </category>
  </question>
  <question type="multichoice">
    <name>
      <text>GEO-F-01-PG</text>
    </name>
    <questiontext format="html">
      <text><![CDATA[<p>Perhatikan data curah hujan wilayah X berikut. Faktor utama penyebab tingginya limpasan permukaan di wilayah tersebut adalah...</p>]]></text>
    </questiontext>
    <defaultgrade>1.0000000</defaultgrade>
    <single>true</single>
    <shuffleanswers>true</shuffleanswers>
    <answernumbering>ABC</answernumbering>
    <answer fraction="100" format="html">
      <text><![CDATA[<p>Alih fungsi lahan resapan di hulu menjadi kawasan terbangun</p>]]></text>
    </answer>
    <answer fraction="0" format="html">
      <text><![CDATA[<p>Tingginya laju evaporasi harian di kawasan pesisir</p>]]></text>
    </answer>
    <answer fraction="0" format="html">
      <text><![CDATA[<p>Dominasi batuan gamping berpori tinggi di lereng tengah</p>]]></text>
    </answer>
    <answer fraction="0" format="html">
      <text><![CDATA[<p>Rendahnya kemiringan lereng di sekitar muara sungai</p>]]></text>
    </answer>
    <answer fraction="0" format="html">
      <text><![CDATA[<p>Tingginya kerapatan vegetasi hutan hujan tropis primer</p>]]></text>
    </answer>
  </question>
</quiz>
```

For an MCMA question, set single to false and apply the same fraction rule as GIFT: correct answers share fraction 100 in total, each wrong answer carries fraction -100.

## 5. CSV: improved column list and example

One row per item, UTF-8, header row first. Quote any field containing a comma, a quote, or a line break in double quotes, and double quotes inside it. The column set extends the source template with pembahasan and with separate key columns per item type, so no format has to squeeze its key into a shape that loses information.

Columns, in order:

1. nomor: item number in the set.
2. bentuk_soal: PG, PGK_MCMA, PGK_KATEGORI, BENAR_SALAH, MENJODOHKAN, ISIAN, URAIAN_URO, or URAIAN_URN.
3. id_stimulus: stimulus identifier, empty when the item has none.
4. teks_stimulus: full stimulus text, empty when none.
5. pokok_soal: the stem or instruction for the item.
6. opsi_a to opsi_e: option texts. A Fase E-F PG item fills all five; leave trailing cells empty only for formats with fewer options, rather than deleting columns, so every row has the same shape.
7. kunci_jawaban: the single key for PG (one letter) and Benar/Salah (Benar or Salah). Empty for multi-key formats.
8. kunci_multi: for PGK MCMA, every correct letter separated by semicolons, for example A;C. Empty otherwise.
9. pernyataan_kunci: for PGK Kategori, the statements with their category keys as statement=key pairs separated by semicolons, for example Gempa tektonik disebabkan pergerakan lempeng=Benar;Tsunami selalu mengikuti gempa darat=Salah. Empty otherwise.
10. kunci_teks: for ISIAN, the accepted short answer; for MENJODOHKAN, the stem-to-option pairs; for URO, the keyword list. Empty otherwise.
11. pedoman_penskoran: the URN rubric or any scoring note the format needs, copied from the package.
12. pembahasan: the explanation of the key, for teacher-facing and LMS use. Never exported into the printed student script.
13. bobot_skor: the item's weight in the set's total.
14. skor_maksimal: the maximum score the item itself can earn (1 for PG, 2 for a formatif MCMA, the keyword count for URO, the rubric top for URN).
15. level_bloom: for example C4 (HOTS).
16. level_solo: for example Relasional; empty only when the package assigns none.
17. jenis_asesmen: diagnostik, formatif, or sumatif. Carried on every row so any later re-import can check the MCMA encoding against the policy.

Example row (PG, Fase F, with a stimulus and a pembahasan that contains a comma, hence the quoting):

```csv
nomor,bentuk_soal,id_stimulus,teks_stimulus,pokok_soal,opsi_a,opsi_b,opsi_c,opsi_d,opsi_e,kunci_jawaban,kunci_multi,pernyataan_kunci,kunci_teks,pedoman_penskoran,pembahasan,bobot_skor,skor_maksimal,level_bloom,level_solo,jenis_asesmen
1,PG,STIM-01,"Data curah hujan wilayah X menunjukkan intensitas tinggi selama tiga bulan terakhir, dengan limpasan permukaan meningkat di kawasan hulu.","Faktor utama penyebab tingginya limpasan permukaan di wilayah tersebut adalah...","Alih fungsi lahan resapan di hulu menjadi kawasan terbangun","Tingginya laju evaporasi harian di kawasan pesisir","Dominasi batuan gamping berpori tinggi di lereng tengah","Rendahnya kemiringan lereng di sekitar muara sungai","Tingginya kerapatan vegetasi hutan hujan tropis primer",A,,,,,"Lahan resapan yang beralih fungsi mengurangi infiltrasi, sehingga air hujan lebih banyak mengalir di permukaan.",1,1,"C4 (HOTS)",Relasional,sumatif
```
