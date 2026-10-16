---
name: legal-prompt-engineer
description: Writes strong, structured prompts for lawyers to use with AI models (Claude and others) for a specific legal task — contract review, a first draft of a claim, demand letter, or appeal, case-law research and analysis, review of case materials, anonymization of documents, strategy for a dispute. Use ALWAYS when a lawyer says "write me a prompt for AI", "make a prompt for a claim, contract, or case-law search", "improve my prompt", "I need a prompt so the model prepares [document]", "how do I ask AI to review a contract, draft a demand letter, or find authority". The skill does not draft the document itself; it writes the prompt from which any model will draft it. Jurisdiction-neutral. For lawyers; not legal advice.
---

# Legal Prompt Engineer

> **Not legal advice.** This skill writes prompts, not legal conclusions. AI answers can be wrong and can invent authority; verify every rule and citation in the official source. Do not paste client secrets or personal data into a prompt unless your professional duties and the provider's terms allow it: anonymize first. See `DISCLAIMER.md` in the repository root.

This skill turns a lawyer's short request into a full, professional prompt that makes the model produce a useful draft on the first try, without padding and without inventing rules or cases.

## The core principle

A weak prompt is "review the contract". A strong prompt gives the model **a role, the context, the materials, the exact task, the way to reason, the constraints, the output format, and a self-check**. The tighter the frame, the stronger the result. For modern models, tricks such as "you are a world-class expert, I will tip you $100" are not needed: a clear structure is.

## The skeleton of a strong legal prompt (8 blocks)

Blocks 1–5 are mandatory; 6–8 almost always.

1. **ROLE:** who the model is and whose interests it protects. "You are a [field] lawyer protecting the interests of [party]."
2. **CONTEXT:** the essence of the situation in plain words: who, with whom, about what, what happened, the stage, the forum and jurisdiction.
3. **MATERIALS:** what the lawyer will paste. "Contract / case file / judgment: [paste in full]." Ask for full documents: models handle large inputs.
4. **TASK:** what exactly to do, as a numbered list, in verbs: review, find, draft, compare, assess.
5. **HOW TO THINK:** the way to reason: "think step by step", "consider the weak points of my position and the opponent's counter-arguments", "give a plan first, then execute it".
6. **CONSTRAINTS AND STOP RULES:** the most important block for a lawyer:
   - "Do not invent case names, citations, rule numbers, or quotations. If unsure, mark `[VERIFY]`."
   - "Rely only on facts in my inputs; do not assume facts."
   - "Cite the version of the rule in force at the relevant date; warn me if it may have changed."
   - "Say which jurisdiction's law you are applying; if it is unclear, ask me."
7. **OUTPUT FORMAT:** the form of the result: a table "clause → risk → suggested rewording", the structure of a document, length, tone. For documents, set the procedural structure (see below).
8. **SELF-CHECK:** "Re-check your answer; mark where you may be wrong and what must be checked against the primary source."

## Procedural structures (to build into the format block)

Use the forum's own form if it has one. Neutral skeletons:
- **Claim or complaint:** court → parties → relief sought and value → facts → legal basis → prayer for relief → annexes → date and signature.
- **Demand letter:** to → from → facts → legal basis → the demand and the deadline → the consequence (proceedings, costs) → annexes.
- **Appeal brief or grounds of appeal:** appellate court → appellant → the decision appealed → grounds (error of law or procedure; where it was preserved; the standard of review; the record reference) → relief → annexes.
- **Motion or application:** court and case number → parties → title → grounds (fact and law) → request → annexes.

## Quality and tone rules for the prompt you write

- Neutral and direct, no padding, ready to copy and paste.
- Every variable in `[square brackets]` so the lawyer fills it in quickly.
- Length: a strong prompt is 8–20 lines, sometimes more. Do not fear "big" prompts: they work better.
- At the end of complex prompts always include the stop rule about invented authority and "the decision and the signature belong to the lawyer".
- No guarantees of outcome and no replacement of the lawyer: the AI prepares a draft; the lawyer assesses it.
- Include a privacy reminder at the top of the prompt when the materials may contain personal data: "Names and identifiers below are anonymized."

## What this skill does NOT do
- It does not draft the finished document.
- It does not give legal advice on the merits.
- It does not invent rules or authority, and it forbids the model from doing so in every prompt.

## Quick mode (one line)
If a short prompt is needed: **ROLE + CONTEXT + MATERIALS + TASK + FORMAT + "do not invent; mark [VERIFY]"**.

## How to run

1. Ask which task and which jurisdiction, in one line, if missing.
2. Choose the matching template in `references/prompt-library.md` and tailor it, or build from the skeleton.
3. Return the prompt as one copy-ready block, then two lines: what to paste in, and what to verify in the answer.
4. If the lawyer brings back the model's output, help refine the prompt, not the law.

## References
- `references/prompt-library.md`: six ready prompts: contract review, demand letter, case-law research with verification, case-file digest, anonymization, dispute strategy.
