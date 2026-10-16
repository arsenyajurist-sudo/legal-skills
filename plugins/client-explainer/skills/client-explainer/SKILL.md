---
name: client-explainer
description: Turns legal analysis into plain-language communications for clients. Use when the user asks to explain a legal situation in simple words, draft a reply to a client, write a short advice email, prepare a client memo or checklist, an FAQ on a legal topic, or an explanation of a court decision. Triggers — "explain this to the client", "plain language", "client memo", "what do I tell the client", "client email", "FAQ for clients", "explain this ruling", "step-by-step instructions for the client". Honest about risks and uncertainty, no promises of outcome. Jurisdiction-neutral: the lawyer supplies the facts, forum, and rules. For lawyers preparing client communications; not legal advice.
---

# Client Explainer

> **Not legal advice.** This skill helps a licensed lawyer, or a person working under their supervision, turn analysis into clear client communications. It does not give legal advice to the public and does not replace the lawyer's judgment. Check every rule, deadline, and sum against the official source before sending anything to a client. Do not upload client secrets or personal data unless your professional duties and the provider's terms allow it. See `DISCLAIMER.md` in the repository root.

## Purpose

Translate complex legal language into explanations the client can understand and act on, while keeping the substance accurate.

## Principles

1. **Plain language.** Avoid jargon where you can. If a term is needed, define it in a few words the first time.
2. **Structure:** situation → what it means → what to do → deadlines → risks.
3. **Specifics, not generalities.** Not "you can go to court", but "a claim must be filed in [the competent court] within [period] of [trigger date]" with the period and the date supplied by the lawyer or marked `[VERIFY]`.
4. **Honesty.** Always state risks and uncertainties. Never promise a result. Never frighten the client into a decision.
5. **The lawyer is the author.** Draft in the lawyer's voice for their review; do not add advice the lawyer has not given.
6. **Do not invent.** Never invent a rule, deadline, fee, authority, or address. Where a fact is missing, ask for it or insert a bracketed placeholder `[date]`, `[fee: VERIFY]`.

## Before you write

If the format is not clear, ask in one line which it is (reply, memo, FAQ, decision explainer). If the facts are thin, ask the 2–4 questions without which the explanation could mislead: the forum and jurisdiction, the client's status in the matter, the key dates, what has already happened, and what the client wants. If the lawyer says "just draft it", draft with placeholders and list the assumptions.

## Formats

### Short reply to a client (message or email)
- 3–5 short paragraphs.
- Situation in one sentence → the conclusion → what we recommend doing → the next step and who does it.
- Tone: respectful, confident, calm, no scare tactics.

### Memo or step-by-step instructions
- Numbered steps.
- Which documents to gather and where to get each.
- **Deadlines** in bold or in a separate block.
- Costs (court fees, notary or other fees, our fees if the lawyer provides them).
- Where to go: the office, the website, or the contact: supplied by the lawyer or marked `[VERIFY]`.

### FAQ for the client
- Question and answer format.
- The 5–10 most common questions on the topic.
- Short answers (2–4 sentences), each with the one thing the client must not miss.

### Explanation of a court decision
- What the court decided (one or two sentences, plain words).
- What it means for the client.
- The options now (appeal, comply, settle, enforce) with the main risk of each.
- Deadlines for action, with the date the clock started `[VERIFY]`.

## Workflow

1. The lawyer describes the situation or pastes the analysis.
2. Confirm the format and the audience (a private client, a business, a vulnerable client).
3. If the format is obvious, draft at once.
4. Offer the output as a chat reply, or as a document if the lawyer wants a file.
5. After the draft, list in one or two lines what the lawyer must verify before sending.

## Tone and style

- Address the client directly ("you").
- Empathetic but professional.
- No panic and no pressure, but an honest statement of the risks.
- No stiff phrases such as "the aforementioned", "hereinafter", "the undersigned".
- Short sentences. One idea per paragraph. Active voice. Numbers and dates written out clearly.
- Aim for a reading level the client will understand without a dictionary.

## Readability check (run before delivering)
- Could the client act on this today without calling you?
- Is every deadline named with its date or its trigger?
- Is there any term that needs a definition?
- Does any sentence promise a result? Remove it.
- Is there anything the client could misread as advice for a different situation? Add the limit.

## When not to use this skill
- The client needs a formal legal opinion or a filing: use a drafting skill.
- The user is not a lawyer and asks for personal legal advice: explain that this is a tool for lawyers and suggest consulting a licensed lawyer.

## References
- `references/templates.md`: model structures for the four formats, with neutral wording.
