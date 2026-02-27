---
name: documentation
description: Review and rewrite documents under flow/ using a 5-point quality checklist. document quality, rewrite, documentation
---

# Document Quality Check

Check notes under `flow/` against 5 quality criteria before finalizing it.

## When to Use

- Reviewing an existing flow note
- Cleaning up a draft before sharing
- Improving quality before a review

## Checklist (5 items)

### 1. Hierarchical structure proportional to content
- Flat list with **4+ items** → consider splitting into `###` sub-headings by theme
- Ask: "Are multiple themes mixed together?" or "Are there chunks the reader might skip?"

### 2. Consistent formatting for same-type information
- Same category of data (IDs, URLs, dates, citations) → use a **single consistent format**
- Common duplication: arXiv ID as plain text + full URL on a separate line → consolidate to `[arXiv:XXXX](URL)`

### 3. Self-contained terminology
- Scan the full body for abbreviations and domain terms
- Any term that appears in the body but is missing from the terminology section → add it

### 4. Single responsibility per section
- Can each section's role be described in **one sentence**? If not, split or rename it
- If the same content appears in two sections → merge into the more appropriate one and remove the duplicate
- Example: "Comparison" = factual differences between papers; "Gaps" = unaddressed areas in the field

### 5. Use tables for N×M comparisons
- When comparing N items across M evaluation axes, a table is clearer than bullet lists
- Rule of thumb: N ≥ 3 and M ≥ 2
