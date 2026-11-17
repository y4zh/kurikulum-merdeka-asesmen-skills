# Claude adapter

The five skills in [../../skills/](../../skills/) are standard Agent Skills: each
folder holds a `SKILL.md` with `name` and `description` frontmatter, a `skill.yaml`,
and a `references/` folder. They load as-is in Claude Code (as a plugin via
`../../.claude-plugin/plugin.json`, or by copying the folders into a skills
directory) and in any Agent Skills compatible client.

| Skill folder | Level |
| --- | --- |
| `kurikulum-merdeka-paud-tk` | PAUD & TK/RA |
| `kurikulum-merdeka-sd-mi` | SD/MI (Fase A-C) |
| `kurikulum-merdeka-smp-mts` | SMP/MTs (Fase D) |
| `kurikulum-merdeka-sma-ma` | SMA/MA (Fase E-F) |
| `kurikulum-merdeka-smk-mak` | SMK/MAK (Fase E-F) |

Each skill is self-contained for its level and holds five sections (Modul Ajar,
Stimulus, Asesmen, Telaah, Konverter). Load the one skill for the level you are
working in; do not load two levels at once.
