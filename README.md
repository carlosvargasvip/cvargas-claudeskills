# cvargas-claudeskills

Claude Code plugin marketplace by Carlos Vargas.

## Skills

### /human
Rewrites text in English or Spanish so it reads like a person wrote it. Covers sentence-level AI tells (vocabulary, punctuation, phrasing) and structural tells (stated takeaways, somatic emotion language, over-tidy narrative arcs). Spanish output is neutral Latin American with tú/ustedes only.

## Install

In Claude Code:

```
/plugin marketplace add carlosvargasvip/cvargas-claudeskills
/plugin install human@cvargas-claudeskills
```

Updates are picked up automatically when the repo changes.

## Updating (maintainer)

1. Edit `plugins/human/skills/human/SKILL.md`
2. Bump `version` in `plugins/human/.claude-plugin/plugin.json`
3. Commit and push
