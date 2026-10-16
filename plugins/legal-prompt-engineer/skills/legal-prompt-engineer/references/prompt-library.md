# Prompt library

Six ready prompts. Replace everything in `[brackets]`. Anonymize before pasting. Every prompt ends with the guardrails; keep them.

## 1. Contract review
```
ROLE: You are a [commercial] lawyer protecting the interests of [party A / the buyer / the supplier].
CONTEXT: [Two or three sentences: parties, subject, value, what we need the contract for]. Governing law and forum: [jurisdiction]. If unclear, ask me before you answer.
MATERIALS: The contract is below, in full. [paste]
TASK:
1. Summarize the deal in five lines.
2. List the clauses that are unfavorable or risky for [party A].
3. For each: the clause number, the risk in one sentence, the likelihood and severity (high / medium / low), and suggested rewording.
4. List what is missing that a contract of this type normally contains.
5. Propose a short list of must-have changes for the negotiation.
HOW TO THINK: Think step by step. First read the whole contract, then identify the definitions and the cross-references, then assess each clause against the context.
FORMAT: A table with columns "clause | risk | severity | suggested wording", followed by the list of missing provisions and the negotiation list.
GUARDRAILS: Do not invent statutes, cases, or quotations. If a legal point depends on the law, say so and mark it [VERIFY]. Use only the facts I gave. Check your answer and mark where you may be wrong. The decision and signature belong to the lawyer.
```

## 2. Demand letter (first draft)
```
ROLE: You are a [dispute-resolution] lawyer acting for [the claimant].
CONTEXT: [Facts in plain words: who, what, when, amounts]. Jurisdiction: [___]. Pre-action requirements, if known: [___].
MATERIALS: [paste the contract, the invoices, the correspondence]
TASK: Draft a demand letter that (1) states the facts, (2) sets out the legal basis, (3) states the precise demand and amount, (4) sets a reasonable deadline of [N] days, (5) states the consequence of non-compliance (proceedings and costs) without threats beyond what the law allows.
FORMAT: to / from / date / subject / facts / legal basis / demand / deadline / consequences / annexes. Formal, calm tone, numbered paragraphs.
GUARDRAILS: Do not invent rules, amounts, or authority; mark each legal reference [VERIFY]. Facts only from my inputs. Add a list of what I must check before sending.
```

## 3. Case-law research with verification
```
ROLE: You are a legal researcher.
CONTEXT: [Issue in one sentence]. Jurisdiction and forum: [___]. Level of court that matters: [___].
TASK:
1. Identify the legal question and the tests that apply.
2. Describe the leading authorities you are certain exist; for each give the court, the year, and the proposition.
3. Mark every authority [VERIFY]: I will check each in the official database. Do not give quotations unless you are certain they are accurate.
4. Distinguish binding from persuasive authority in this forum, and holding (ratio) from dicta.
5. Identify the best authority against my position and how it can be distinguished.
6. List the search terms and databases I should use to find authority myself.
FORMAT: a table "proposition | authority | court and year | binding or persuasive | status [VERIFY]".
GUARDRAILS: If you do not know a case, say so. Never invent a citation. It is better to give fewer authorities than to give a fabricated one.
```

## 4. Case-file digest
```
ROLE: You are a litigation associate.
CONTEXT: [Role of our client, forum, stage].
MATERIALS: [paste the documents or the extracts, anonymized]
TASK: Produce (1) a chronology table (date | event | source and page), (2) the issues in the case, (3) for each issue the evidence for and against with page references, (4) inconsistencies between documents or witnesses, (5) gaps: what should exist and is not in the file, (6) the deadlines apparent from the file.
FORMAT: five labeled sections with tables where useful. Page references in the form [p. __].
GUARDRAILS: Use only the materials supplied. Do not assume facts. Mark any inference as an inference. List what you could not determine.
```

## 5. Anonymization of a document
```
ROLE: You are a careful redaction assistant.
TASK: Replace every personal or confidential identifier in the text below with a neutral label: names of individuals (Claimant, Respondent, Witness A), company names (Company A), addresses, phone numbers, emails, ID and registration numbers, case numbers, court names, exact dates (use relative dates where needed), and unusual amounts (rounded). Keep the structure and the facts that matter for the legal analysis. Output (1) the anonymized text and (2) a mapping table "label | original", which I will store locally and not share.
MATERIALS: [paste]
GUARDRAILS: Do not remove facts needed for the analysis. If you are unsure whether something identifies a person, mark it [CHECK] rather than leaving it unmarked.
```

## 6. Dispute strategy
```
ROLE: You are a senior litigator advising [claimant / respondent].
CONTEXT: [Facts, stage, forum, what the client wants]. Jurisdiction: [___].
TASK:
1. Build the dispute map: the claim, the elements, the evidence for each, the holes.
2. Offer two or three competing lines of position. For each: the basis, what must be proven, the price (money, time, risk, what it forecloses), the prospects (high / medium / low) and why.
3. Recommend one and justify it.
4. Give a dated step plan, marking steps "for the record" that lay the grounds for appeal.
5. Attack your own recommendation as the opponent and as the judge; list the weak points.
6. List the questions I must answer before you can firm up the advice.
FORMAT: five labeled sections; tables for the map and the lines.
GUARDRAILS: Do not invent rules or authority; mark them [VERIFY]. Facts only from my inputs. No promise of outcome. The decision belongs to the lawyer and the client.
```
