# Guide

This package gives your AI assistant a working knowledge of Indonesian Kurikulum
Merdeka assessment practice: teaching modules (modul ajar), stimulus design,
assessment writing, item review (telaah), and exam/CBT conversion. It is organised as
one self-contained skill per school level, so an assistant never mixes the rules of
one level into another.

## What is inside

- `skills/` holds the five level skills. Each skill is one folder with a `SKILL.md`
  (five sections: Modul Ajar, Stimulus, Asesmen, Telaah, Konverter) and a
  `references/` folder with the detailed rules, checklists, and export schemas.
- `rules/` holds the always-on core rules that route work to the right level skill.
- The dot-folders (`.claude-plugin/`, `.codex-plugin/`, `.cursor-plugin/`,
  `.cline-plugin/`, `.kimi-plugin/`, `.agents/`, `.omp-plugin/`) are plugin manifests
  for each agent platform. They all point at the same `skills/` folder; there is one
  source of truth.

## Choose an installation route

### As a plugin (recommended where supported)

- Claude Code: install from this repository as a plugin; the manifest is
  `.claude-plugin/plugin.json`.
- Codex: the manifest is `.codex-plugin/plugin.json`.
- Cursor: the manifest is `.cursor-plugin/plugin.json`; it also loads `rules/`.
- Cline: `package.json` registers `.cline-plugin/plugin.js`; Cline reads `skills/`.
- Kimi Code: the manifest is `.kimi-plugin/plugin.json`; it also loads the core rules
  as its system prompt file.
- Generic agent marketplaces: `.agents/plugins/marketplace.json` and
  `.omp-plugin/marketplace.json` list this repository as a local plugin.

### As a skills directory

Copy the five folders under `skills/` into your agent's skills directory. Each folder
is a standard Agent Skill (`SKILL.md` with name and description frontmatter).

### In chat assistants (no skill support)

- ChatGPT: create a Custom GPT and paste `adapters/chatgpt/custom-gpt-instructions.md`
  as its instructions.
- Gemini: create one Gem (Keahlian) per level and upload the matching single file
  from `adapters/gemini/` (for example `kurikulum-merdeka-sma-ma.md`). The single file
  contains the whole level skill including its references, because Gemini's uploader
  accepts one Markdown skill file but often rejects additional Markdown attachments.
  Alternatively paste `adapters/gemini/gem-instructions.md` and attach references as
  `.txt` files.

## Working with the skills

1. Tell the assistant the school level (jenjang) and what you need. If the level is
   missing, the assistant is instructed to ask.
2. The assistant loads that level's skill and works in the matching section. A full
   package usually flows: Modul Ajar (TP list) -> Stimulus -> Asesmen (package) ->
   Telaah (independent review) -> Konverter (Kartu Soal, print script, CBT export).
3. Check the labels: rules cited to a Kemendikdasmen document carry page numbers;
   anything labelled a practice rule or school policy is guidance, not regulation.

## Update and removal

Plugin installs update from this repository. Skills-directory installs: replace the
five folders with the new release. To remove, delete the plugin or the folders; the
package writes nothing outside its own directory.
