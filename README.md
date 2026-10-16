# Legal skills for Claude Code

AI skills and plugins for **licensed lawyers**: drafting, stress-testing, and strategy. Jurisdiction-neutral frameworks; country packs may follow.

> Not legal advice. Read [DISCLAIMER.md](DISCLAIMER.md) before use.

## Plugins

| Plugin | What it does |
|---|---|
| [`devils-advocate`](plugins/devils-advocate) | Ruthless opposing-counsel mode: finds the holes in your position before the other side does. Legal mode (procedure, merits, evidence, case-law audit) and general mode. |
| [`red-team-brief`](plugins/red-team-brief) | Strengthen your own draft in five layers, or audit an adverse judgment for appeal (attack lines ranked by cost of concession for the court). |

## Install (Claude Code)

```
/plugin marketplace add arsenyajurist-sudo/legal-skills
/plugin install red-team-brief@legal-skills
/plugin install devils-advocate@legal-skills
```

Then ask: *"Red-team this draft"* and paste an anonymized document.

## License

MIT. Copyright (c) 2026 Arsenia Razumovskaya.
