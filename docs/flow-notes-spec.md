# Flow Notes Specification

Purpose
- Provide a consistent, lightweight structure for research and implementation notes under `flow/`.
- Keep files machine-friendly via required YAML front matter, and human-friendly via concise Markdown sections.

Types
- Core types
  - `reading_list`: Curated candidates with scope and selection criteria.
  - `paper_note`: Single-paper distilled notes focused on transfer and application.
  - `mini_survey`: 2–10 papers contrasted with gaps and next steps.
  - `synthesis`: Integrative claim backed by evidence and implications.
  - `critique`: Strengths, weaknesses, assumptions, failure modes, validation plan.
  - `replication`: Reproduction plan with acceptance criteria.
  - `experiment_log`: Hypothesis → design → observation → decision → next.
  - `roadmap`: Objectives, milestones, risks, success metrics, timeline.
- Auxiliary types
  - `dataset_note`, `benchmark_brief`, `concept_primer`, `prompt_recipe`.

Front Matter (YAML)
- Required fields
  - `id`: Unique identifier (see Naming).
  - `title`: Document title.
  - `type`: One of the listed types.
  - `created_at`, `updated_at`: ISO 8601 timestamps.
  - `status`: `draft` | `final`.
  - `tags`: Array of keywords.
  - `topic`: Short topic phrase.
  - `sources`: Array of stable IDs (arXiv/DOI/URL).
- Recommended fields
  - `importance`: `low` | `medium` | `high`.
  - `timebox`: e.g., "45m".
  - `related`: Array of related note IDs.
  - `owners`: Array of owners.
  - `model`: Model used for generation (if applicable).

Naming
- Recommended filename: `YYYYMMDDHHMM.{type}.{slug}.md`
  - Example: `20251029T1030.paper_note.rtc-act.md`
  - `slug` is a short, kebab-case descriptor.

Section Structures
- `reading_list`
  - Purpose/Scope, Selection Criteria, Candidates (title + 1-line reason), Next Actions, References.
- `paper_note`
  - TL;DR, Background/Contributions, Terminology, Method/Setup, Results/Limitations, Insights/Questions, References.
- `mini_survey`
  - Scope/Criteria, Terminology, Per-paper Summaries (1–3 lines), Comparison/Differences, Gaps, Next Actions, References.
- `synthesis`
  - Central Claim, Terminology, Evidence (bullets), Counterexamples/Limits, Implications (design/research), To‑Do, References.
- `critique`
  - Claim Summary, Terminology, Strengths, Weaknesses/Assumptions, Failure Modes, Validation Plan, References.
- `replication`
  - Goal/Scope, Terminology, Env/Assets, Procedure, Metrics/Acceptance, Risks/Mitigation, Next Actions.
- `experiment_log`
  - Hypothesis, Design (variables/conditions), Execution/Observations, Results, Decision, Next Actions.
- `roadmap`
  - Objective/Scope, Milestones, Tasks (priority/effort), Risks, Success Metrics, Timeline.
- `dataset_note`
  - Overview, Terminology, Schema/Labels, Splits/Stats, Quality/Issues, Usage/License, References.
- `benchmark_brief`
  - Task Definition, Terminology, Metrics, Protocol, Baselines, Caveats, References.
- `concept_primer`
  - Concept Summary, Core Ideas, Typical Pitfalls, Canonical Examples, References.
- `prompt_recipe`
  - Intent, Instructions, Parameters, Few-shot Examples, Guardrails, References.

Generation Prompt (for agents)
- Output exactly one Markdown file with YAML front matter as specified above.
- Language: Japanese by default. Use concise bullets (one line per point when possible).
- Use only Markdown headings and bullets; avoid heavy tables/footnotes.
- Cite sources by stable IDs (arXiv/DOI/URL) in the References section.
