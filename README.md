# web-clean

A Claude Code skill that runs a twenty-point cleanup pass over web UI. It strips AI-slop decoration and fixes the craft details that make an interface feel finished.

| Remove noise | Structure | Craft | Behaviour |
|---|---|---|---|
| Filler badges · redundant labels · random italics · needless mono · embellishments | Design system · real product · enlarged main feature · grouping by spacing · specific headlines · emphasized CTA · one accent colour | Consistent icons · inner radius = outer − padding · text contrast · headline wrapping · optical alignment · tabular numbers | Loading states · useful feedback motion |

The full checklist is in [`SKILL.md`](plugins/web-clean/skills/web-clean/SKILL.md).

## Install

### Claude Code plugin (recommended)

```text
/plugin marketplace add hawk227/web-clean
/plugin install web-clean@web-clean
```

Updates: `/plugin marketplace update web-clean`.

### Any agent that supports skills (skills CLI)

```bash
npx skills add hawk227/web-clean
```

### Manual

```bash
mkdir -p ~/.claude/skills/web-clean
curl -fsSL https://raw.githubusercontent.com/hawk227/web-clean/main/plugins/web-clean/skills/web-clean/SKILL.md -o ~/.claude/skills/web-clean/SKILL.md
```

## Use

Type `/web-clean`, or ask Claude to "clean up", "polish" or "de-slop" a page or component. It reads the code, looks at the rendered page on desktop and mobile, fixes what breaks a rule, and reports a pass/fixed table.

## Contributing

Issues and pull requests welcome. Keep rules short, concrete and checkable.

## License

MIT
