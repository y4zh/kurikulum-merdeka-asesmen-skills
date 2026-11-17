# Spesifikasi CBT: Moodle XML dan CSV SMK/MAK

Reference for the konverter_smk_mak skill: the Moodle XML and CSV export formats for SMK/MAK Fase E-F (5 options, A-E). Kartu Soal, the print layouts, the Lembar Penilaian Praktik, and GIFT live in the companion reference file, spesifikasi-format-ekspor.md. The MCMA fraction encoding below follows the core skill's scoring policy (sumatif MCMA binary 1-0, formatif MCMA 2-1-0); LMS fraction fields are transport encoding only. See SKILL.md, "Scoring conversion rule", before using any example here.

## 1. Moodle XML example

Well-formed XML, UTF-8. Question and answer text sit inside CDATA sections so HTML markup needs no escaping; text outside CDATA must escape ampersands, angle brackets, and quotes. The category question comes first and sets the bank path for the questions after it.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<quiz>
  <question type="category">
    <category>
      <text>$course$/top/Kurikulum-Merdeka/Fase-F/Teknik/MOTS-Multistruktural</text>
    </category>
  </question>
  <question type="multichoice">
    <name>
      <text>SMK-F-03-PG</text>
    </name>
    <questiontext format="html">
      <text><![CDATA[<p>Hasil pengukuran jangka sorong (ketelitian 0,05 mm) menunjukkan skala utama 24 mm dan garis skala nonius yang berimpit adalah garis ke-7. Hasil pengukuran tersebut adalah...</p>]]></text>
    </questiontext>
    <defaultgrade>1.0000000</defaultgrade>
    <single>true</single>
    <shuffleanswers>true</shuffleanswers>
    <answernumbering>ABC</answernumbering>
    <answer fraction="100" format="html">
      <text><![CDATA[<p>24,35 mm</p>]]></text>
    </answer>
    <answer fraction="0" format="html">
      <text><![CDATA[<p>24,07 mm</p>]]></text>
    </answer>
    <answer fraction="0" format="html">
      <text><![CDATA[<p>24,70 mm</p>]]></text>
    </answer>
    <answer fraction="0" format="html">
      <text><![CDATA[<p>23,35 mm</p>]]></text>
    </answer>
    <answer fraction="0" format="html">
      <text><![CDATA[<p>24,53 mm</p>]]></text>
    </answer>
  </question>
</quiz>
```

For an MCMA question, set single to false and apply the same fraction rule as GIFT: correct answers share fraction 100 in total, each wrong answer carries fraction -100.

## 2. CSV: improved column list and example

One row per item, UTF-8, header row first. Quote any field containing a comma, a quote, or a line break in double quotes, and double quotes inside it. The column set extends the source template with pembahasan and with separate key columns per item type, so no format has to squeeze its key into a shape that loses information. Practical tasks are not CSV question rows; they export through the JSON schema's task shape or stay on the printed Lembar Penilaian Praktik.

Columns, in order:

1. nomor: item number in the set.
2. bentuk_soal: PG, PGK_MCMA, PGK_KATEGORI, BENAR_SALAH, MENJODOHKAN, ISIAN, URAIAN_URO, or URAIAN_URN.
3. id_stimulus: stimulus identifier, empty when the item has none.
4. teks_stimulus: full stimulus text, empty when none.
5. pokok_soal: the stem or instruction for the item.
6. opsi_a to opsi_e: option texts. In this jenjang all five are filled for PG and MCMA items; leave a cell empty only where the item format has no options, rather than deleting columns, so every row has the same shape.
7. kunci_jawaban: the single key for PG (one letter) and Benar/Salah (Benar or Salah). Empty for multi-key formats.
8. kunci_multi: for PGK MCMA, every correct letter separated by semicolons, for example A;C. Empty otherwise.
9. pernyataan_kunci: for PGK Kategori, the statements with their category keys as statement=key pairs separated by semicolons, for example Pintu darurat bengkel harus bebas hambatan=Benar;APAR boleh disimpan di dekat sumber panas=Salah. Empty otherwise.
10. kunci_teks: for ISIAN, the accepted short answer; for MENJODOHKAN, the stem-to-option pairs; for URO, the keyword list. Empty otherwise.
11. pedoman_penskoran: the URN rubric or any scoring note the format needs, copied from the package.
12. pembahasan: the explanation of the key, for teacher-facing and LMS use. Never exported into the printed student script.
13. bobot_skor: the item's weight in the set's total.
14. skor_maksimal: the maximum score the item itself can earn (1 for PG, 2 for a formatif MCMA, the keyword count for URO, the rubric top for URN).
15. level_bloom: for example C3 (MOTS).
16. level_solo: for example Multistruktural; empty only when the package assigns none.
17. jenis_asesmen: diagnostik, formatif, or sumatif. Carried on every row so any later re-import can check the MCMA encoding against the policy.

Example row (PG, SMK/MAK, no stimulus, a pembahasan that contains a comma, hence the quoting):

```csv
nomor,bentuk_soal,id_stimulus,teks_stimulus,pokok_soal,opsi_a,opsi_b,opsi_c,opsi_d,opsi_e,kunci_jawaban,kunci_multi,pernyataan_kunci,kunci_teks,pedoman_penskoran,pembahasan,bobot_skor,skor_maksimal,level_bloom,level_solo,jenis_asesmen
1,PG,,,"Sebelum mengoperasikan mesin bubut untuk pekerjaan pembubutan rata, tindakan keselamatan kerja yang wajib dilakukan operator adalah...","Memeriksa kondisi mesin, memakai kacamata pelindung, dan memastikan benda kerja terjepit kuat pada cekam","Menyalakan mesin terlebih dahulu agar putaran stabil sebelum benda kerja dipasang pada cekam","Memakai sarung tangan kain agar tangan tidak licin saat memegang benda kerja yang berputar","Mengatur putaran spindel setinggi mungkin agar proses pemotongan selesai lebih cepat","Membersihkan tatal dengan tangan saat mesin masih berputar agar area kerja tetap bersih",A,,,,,"Pemeriksaan mesin, alat pelindung diri, dan penjepitan benda kerja adalah urutan keselamatan awal sebelum mesin dijalankan, sedangkan pilihan lain justru melanggar kaidah K3 bengkel.",1,1,"C3 (MOTS)",Multistruktural,sumatif
```
