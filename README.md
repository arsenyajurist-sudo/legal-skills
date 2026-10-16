# Legal skills for Claude Code

AI skills and plugins for **licensed lawyers**: drafting, stress-testing, and strategy. Jurisdiction-neutral frameworks; country packs may follow.

> Not legal advice. Read [DISCLAIMER.md](DISCLAIMER.md) before use.

## Plugins

| Plugin | What it does |
|---|---|
| [`devils-advocate`](plugins/devils-advocate) | Ruthless opposing-counsel mode: finds the holes in your position before the other side does. Legal mode (procedure, merits, evidence, case-law audit) and general mode. |
| [`litigation-strategy`](plugins/litigation-strategy) | Advisor for civil and commercial disputes: dispute map, two or three lines of position with their price, enforceability first, stage tactics, appeal map. Jurisdiction-neutral with a common-law lens. |
| [`criminal-defense-strategy`](plugins/criminal-defense-strategy) | Advisor for defense counsel: case map, two or three lines of defense with their price, attack on evidence, stage tactics from first contact to appeal, appeal map. Jurisdiction-neutral with a common-law lens. |
| [`criminal-defense-drafting`](plugins/criminal-defense-drafting) | Drafting assistant for defense counsel: bail applications, exclusion and dismissal motions, disclosure applications, grounds of appeal, submissions, cross-examination outlines, expert questions. Formal register, no invented authority. |
| [`client-explainer`](plugins/client-explainer) | Turns legal analysis into plain-language client communications: short reply, step-by-step memo, FAQ, explanation of a court decision. Honest about risk, no promises of outcome. |
| [`legal-prompt-engineer`](plugins/legal-prompt-engineer) | Writes strong structured prompts for lawyers (8-block skeleton, guardrails against invented authority) and includes six ready prompts: contract review, demand letter, case-law research, case-file digest, anonymization, dispute strategy. |
| [`legal-design`](plugins/legal-design) | Premium visual design for client-facing legal documents: four style presets, typographic hierarchy, signature block, HTML and print rules. Not for court filings. |
| [`red-team-brief`](plugins/red-team-brief) | Strengthen your own draft in five layers, or audit an adverse judgment for appeal (attack lines ranked by cost of concession for the court). |

## Install (Claude Code)

```
/plugin marketplace add arsenyajurist-sudo/legal-skills
/plugin install red-team-brief@legal-skills
/plugin install devils-advocate@legal-skills
/plugin install litigation-strategy@legal-skills
/plugin install criminal-defense-strategy@legal-skills
/plugin install criminal-defense-drafting@legal-skills
/plugin install client-explainer@legal-skills
/plugin install legal-prompt-engineer@legal-skills
/plugin install legal-design@legal-skills
```

Then ask: *"Red-team this draft"* and paste an anonymized document.

## License

MIT. Copyright (c) 2026 Arsenia Razumovskaya.
