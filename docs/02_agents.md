# 🤖 Agent Architecture

This system uses a **multi-agent pipeline** with clearly defined roles and constraints.

---

## Agent 0 — News Scout

**Purpose**
Selects relevant AI governance and safety news from RSS input.

**Responsibilities**
- filter irrelevant / promotional content
- prioritize governance-related topics
- select top 3–5 stories
- define editorial direction

**Output**
- ranked items
- why_it_matters
- newsletter_angle
- primary_story
- article_thesis

---

## Agent 1 — Draft Writer

**Purpose**
Generates the newsletter article draft.

**Constraints**
- non-hype tone
- no exaggerated compliance claims
- clear separation of fact vs interpretation

**Output**
- title
- summary
- article
- key_takeaways
- linkedin_teaser

---

## Agent 2 — Governance Reviewer

**Purpose**
Evaluates content against:
- internal policy
- governance standards
- risk & compliance requirements

**Decision Output**
- approve
- revise
- escalate
- reject

**Scoring Model**
- 8–10 → approve
- 5–7 → revise
- 3–4 → escalate
- 0–2 → reject

---

## Agent 3 — Revision Agent

**Purpose**
Improves draft based on reviewer findings.

**Constraints**
- must preserve original score & status
- must address reviewer issues
- must not introduce new risk

**Output**
- revised article
- revision notes