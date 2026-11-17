# Roadmap

## Released

- v1.x: five role skills (asesmen, modul ajar, stimulus, telaah, konverter) with
  claims verified against the primary Kemendikdasmen documents.
- v2.0.0: skills split per school level (25 skills) so levels never mix.
- v3.0.0: skills merged back to one self-contained skill per level (5 skills, five
  sections each), plugin manifests for Claude Code, Codex, Cursor, Cline, Kimi, and
  generic agent marketplaces, always-on core rules, and single-file Gemini builds.

## Planned

- Re-verify the Capaian Pembelajaran citations against the current BSKAP decision
  documents and the Pusmendik review card against the official telaah documents, then
  update the verification notes in each skill.
- A distilled HOTS item-writing reference (from official ministry training material),
  mapped to the current framework, as an added reference in the SMA/MA and SMK/MAK
  skills, with a HOTS authenticity check in the Telaah section.
- Validation scripts that check every skill folder for format drift (frontmatter,
  reference links, level parameters) in CI.
- Additional platform manifests as new agent plugin formats stabilise.

## Not planned

- Per-subject skill forks. Subject specifics belong in prompts and kisi-kisi, not in
  separate skills; the level skills are deliberately subject-neutral.
