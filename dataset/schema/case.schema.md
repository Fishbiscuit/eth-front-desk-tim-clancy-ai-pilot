---
okf: 1
type: "schema-reference"
title: "ETH Front Desk AI Case Schema — Review View"
status: "accepted"
visibility: "collaborator-shared"
updated: "2026-09-10"
---

# ETH Front Desk AI Case Schema — Review View

The machine-readable schema is `case.schema.json`. This page is the Obsidian review companion.

## Required top-level fields

`schema_version`, `case_id`, `revision`, `family_id`, `split`, `title`, `tags`, `provenance`, `input`, `evidence`, `assessment`, and `review`.

## Core rules

- `schema_version` is `eth-front-desk.case.v0.1`.
- `case_id` uses the form `EFD-0001`.
- `revision` is a positive integer.
- `family_id` groups related scenarios; a full family belongs to one dataset split.
- `split` is `unassigned`, `train`, `dev`, or `test`.

## Provenance

Required fields: `origin`, `author_id`, `created_on`, and `usage_status`.

- Origin: `human_authored`, `ai_draft`, or `human_edited_ai`.
- Usage status: `internal_only`, `cleared_for_release`, or `pending`.

## Model input

`input` contains:

- `as_of`: date or `null`;
- `messages`: one or more user/assistant messages;
- `evidence_ids`: the only evidence identifiers shown to the tested model.

The final input message must be from the user. Assessment fields are never included in model input.

## Evidence

Each evidence item records:

`evidence_id`, `title`, `source_url`, `source_type`, `retrieved_on`, `content_kind`, and `content`.

Optional provenance fields: `source_version` and `snapshot_sha256`.

## Assessment

Required fields:

- `reference_answer`: string or `null`;
- `criteria`: reviewer criteria with dimension, expectation, critical flag, and evidence IDs;
- `acceptable_variations`;
- `failure_modes`.

Criteria dimensions include censorship resistance, open-source freedom, privacy, security, trust assumptions, trade-offs, evidence/uncertainty, and constructive challenge.

## Review

Required fields:

- `status`: `draft`, `in_review`, `approved`, `contested`, or `retired`;
- `judgments`;
- `decision_by`;
- `decision_note`;
- `open_questions`.

## Optional preferences

Preference records may contain two candidate responses and a label: `a`, `b`, `tie`, `both_bad`, or `abstain`. Only clear human-reviewed `a`/`b` preferences may be exported for DPO training.

## Companion files

- Machine-readable contract: `case.schema.json`
- Synthetic worked sample: `../cases/EFD-0001.json`
- Format research: `../../dataset-format-research.md`
