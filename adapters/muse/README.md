# Muse adapter

In Muse, custom skills live in `~/workspace/custom-skills/` with snake_case folder
names. Copy or install the five level skills with the hyphen-to-underscore mapping:

| Repository folder (skills/) | Muse custom skill name |
| --- | --- |
| `kurikulum-merdeka-paud-tk` | `kurikulum_merdeka_paud_tk` |
| `kurikulum-merdeka-sd-mi` | `kurikulum_merdeka_sd_mi` |
| `kurikulum-merdeka-smp-mts` | `kurikulum_merdeka_smp_mts` |
| `kurikulum-merdeka-sma-ma` | `kurikulum_merdeka_sma_ma` |
| `kurikulum-merdeka-smk-mak` | `kurikulum_merdeka_smk_mak` |

Each Muse skill folder contains the same `SKILL.md` body as the repository version
(without the Agent Skills frontmatter), the `skill.yaml` manifest, and the
`references/` folder.
