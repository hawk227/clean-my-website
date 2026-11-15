# Clean My Website

A Claude Code skill that runs a twenty-point cleanup pass over web UI. It strips AI-slop decoration and fixes the craft details that make an interface feel finished.

| Remove noise | Structure | Craft | Behaviour |
|---|---|---|---|
| Filler badges · redundant labels · random italics · needless mono · embellishments | Design system · real product · enlarged main feature · grouping by spacing · specific headlines · emphasized CTA · one accent colour | Consistent icons · inner radius = outer − padding · text contrast · headline wrapping · optical alignment · tabular numbers | Loading states · useful feedback motion |

The full checklist is in [`SKILL.md`](plugins/clean-my-website/skills/clean-my-website/SKILL.md).

## Install

### Claude Code plugin (recommended)

```text
/plugin marketplace add hawk227/clean-my-website
/plugin install clean-my-website@clean-my-website
```

Updates: `/plugin marketplace update clean-my-website`.

### Any agent that supports skills (skills CLI)

```bash
npx skills add hawk227/clean-my-website
```

### Manual

```bash
mkdir -p ~/.claude/skills/clean-my-website
curl -fsSL https://raw.githubusercontent.com/hawk227/clean-my-website/main/plugins/clean-my-website/skills/clean-my-website/SKILL.md -o ~/.claude/skills/clean-my-website/SKILL.md
```

## Use

Type `/clean-my-website`, or ask Claude to "clean up", "polish" or "de-slop" a page or component. It reads the code, looks at the rendered page on desktop and mobile, fixes what breaks a rule, and reports a pass/fixed table.

## Contributing

Issues and pull requests welcome. Keep rules short, concrete and checkable.

## License

MIT
