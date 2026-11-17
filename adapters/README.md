# Adapters and platform doors

This package installs natively as a plugin on several agent platforms. The manifests
live in the repository root area and all point at the same `skills/` folder:

| Platform | Manifest |
| --- | --- |
| Claude Code | `.claude-plugin/plugin.json` |
| Codex | `.codex-plugin/plugin.json` |
| Cursor | `.cursor-plugin/plugin.json` (also loads `rules/`) |
| Cline | `package.json` + `.cline-plugin/plugin.js` |
| Kimi Code | `.kimi-plugin/plugin.json` (also loads `rules/` as system prompt) |
| Generic agent marketplaces | `.agents/plugins/marketplace.json`, `.omp-plugin/marketplace.json` |

See [../GUIDE.md](../GUIDE.md) for installation routes.

## Manual adapters (chat assistants without skill support)

- `chatgpt/custom-gpt-instructions.md`: paste as a Custom GPT's instructions.
- `gemini/gem-instructions.md`: paste as a Gem's instructions, or better, upload the
  single-file build for your level from `gemini/` (one `.md` per level, complete with
  references; Gemini's uploader rejects extra Markdown attachments, so one file is
  the reliable route).
- `claude/README.md` and `muse/README.md`: how to load the five level skills in
  Claude-based and Muse environments.

The full skills (source of truth) live in [../skills/](../skills/). Do not edit the
single-file Gemini builds by hand; they are generated from the skills.
