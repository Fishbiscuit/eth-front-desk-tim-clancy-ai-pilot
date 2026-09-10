# ETH Front Desk AI — Dataset

This directory contains the Week 1 case format and initial sample.

**Week 1 scope:** the reviewed collection should be Tim Clancy’s version only. The synthetic sample below demonstrates the schema and is not Tim’s judgment. Expansion to additional Ethereum-aligned reviewers, potentially including board members, is a later decision if the pilot works.

## Source of truth

- Authoring source: individual JSON case records under `cases/`.
- Schema: `schema/case.schema.json`.
- Obsidian review companion: `schema/case.schema.md`.
- Frozen releases: JSONL files generated from approved case records.
- Human review: generated Markdown views, not independent source files.

## Current sample

- `cases/EFD-0001.json` — synthetic architecture-review case; draft and unreviewed.
- `cases/EFD-0001.md` — Obsidian review view of the sample case.

## Split rule

Assign complete `family_id` groups to one split before Week 2. Do not use a case or close paraphrase in both training and held-out evaluation.

## Handling rule

Do not add identifying, confidential, or unreleased project material without explicit clearance and consent. Keep assessment fields out of model inputs.
