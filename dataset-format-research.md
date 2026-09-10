---
okf: 1
type: "research-note"
title: "ETH Front Desk AI — Week 1 Dataset Format Research"
status: "accepted"
visibility: "collaborator-shared"
updated: "2026-09-10"
---

# ETH Front Desk AI — Week 1 Dataset Format Research

## Decision

Use a **provider-neutral architecture-and-decision case record** as the master format.

- Author and version individual cases as JSON.
- Freeze releases and experiment exports as JSONL.
- Generate Markdown review views for human discussion.
- Keep model input, reviewer assessment, and research metadata separate.

The master record must not be reduced to `question → ideal answer`. It needs to preserve evidence, acceptable alternatives, uncertainty, disagreement, and dataset splits.

This is the approved starting template for Week 1. It is a project format, not an existing Ethereum or provider standard.

## Initial scope

Week 1 is intentionally **Tim Clancy’s version**: a bounded case set based on source material Tim agrees to use and substantive judgments Tim reviews. It is not yet a multi-reviewer or board dataset. If the pilot works, the next scope decision can invite additional Ethereum-aligned reviewers, potentially including board members.

The synthetic sample `EFD-0001` demonstrates the format only; it is not Tim’s judgment and must not be presented as his answer.

## Week 1 output

- `dataset/schema/case.schema.json`
- `dataset/cases/EFD-0001.json` as a synthetic worked sample
- a bounded Tim-specific calibration set and held-out cases;
- family-based train/dev/test assignments before Week 2;
- generated review views and experiment-ready exports only after review.

## Case structure

| Part | Contents | Model access |
|---|---|---|
| Model input | Scenario, question, date, and explicitly selected evidence | Shown to the tested model |
| Assessment | Reference answer, criteria, acceptable alternatives, failure modes | Reviewer/evaluator only |
| Research metadata | Provenance, split, versions, judgments, disagreement, optional preferences | Project tooling and reviewers |

## Required principles

- `case_id` identifies a case; `revision` changes when its content changes.
- `family_id` groups related scenarios and counterfactuals; assign whole families to one split.
- Only evidence named in `input.evidence_ids` is shown to the model.
- Reference answers are examples, not the only valid wording or conclusion.
- AI-drafted cases start as `draft`; human review is required before `approved`.
- Keep model outputs, latency, cost, and scores in run-result files, not in the canonical case.
- Preserve ties, abstentions, both-bad judgments, and real disagreement.
- Do not use a single Ethereum-alignment score or hidden chain-of-thought field.
- Do not treat tone, harshness, branding, or an AI-generated ranking as evidence of alignment.

## Evaluation scale

Use a simple criterion scale:

- **0** — missing, materially incorrect, or contradicts the expectation;
- **1** — partly correct but misses a material part;
- **2** — accurate and specific for the case.

A zero on a critical criterion is reported separately as a critical failure; it must not disappear inside an aggregate score.

## Export rules

- **Baseline:** send only the experiment system prompt, `input.as_of`, selected evidence, and `input.messages`.
- **SFT:** export approved training cases with the rendered input and `assessment.reference_answer`.
- **DPO:** export only clear human-reviewed `a`/`b` preferences; preserve ties, abstentions, and both-bad judgments in the master record.
- **Evaluation:** keep reference answers, criteria, failure modes, and reviewer comments out of model input.

## Worked sample

`dataset/cases/EFD-0001.json` is synthetic and currently unreviewed. It demonstrates the intended case shape; it is not a real company assessment and does not create a human or institutional endorsement.

## Research sources to verify before external circulation

- [Hugging Face TRL dataset formats](https://huggingface.co/docs/trl/dataset_formats)
- [Hugging Face TRL DPO trainer](https://huggingface.co/docs/trl/dpo_trainer)
- [OpenAI fine-tuning data preparation](https://platform.openai.com/docs/guides/fine-tuning)

These sources inform export compatibility; they do not determine the project’s normative judgments.
