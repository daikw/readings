# Agent Working Guide

Scope
- This file defines how agents should create and maintain research/implementation notes under `flow/` directory.
- Detailed specifications live in `@docs/flow-notes-spec.md`.

Key Rules
- Use YAML front matter with the required fields before any content.
- Prefer concise Japanese bullets and headings; avoid heavy footnotes.
- File naming: `YYYYMMDDHHMM.{type}.{slug}.md` (see docs for details).
- Sources must include stable IDs (arXiv/DOI/URL) in a References section.

Types and Templates
- Core types: `reading_list`, `paper_note`, `mini_survey`, `synthesis`, `critique`, `replication`, `experiment_log`, `roadmap`.
- Auxiliary: `dataset_note`, `benchmark_brief`, `concept_primer`, `prompt_recipe`.
- Templates are available under `flow/template/` for each type.

