---
okf: 1
type: "pilot-workplan"
title: "ETH Front Desk Pilot — Workplan"
status: "draft"
visibility: "collaborator-shared"
updated: "2026-09-10"
---

# Pilot Workplan

The ETH Front Desk pilot runs for three weeks, with one phase per week. 

## Before Week 1 — Joint allocation decision

Tim and QZ jointly decide:

- time each person is allocating;
- the cases and models in scope;
- the output expected at the end of each week;
- what is explicitly out of scope;
- any data, attribution, or external-cost conditions.

Record the agreement in [decision-log](decision-log.md).

## Week 1 — Create the dataset

**Question:** Can Tim Clancy’s version of the Ethereum-alignment judgment be converted into a small, reviewable dataset?

- Agree the initial principles and case schema.
- Use provider-neutral JSON records as the authoring source.
- Select representative material Tim agrees to use and extract recurring dilemmas.
- Create architecture-review cases with user constraints, evidence, trade-offs, alternatives, and uncertainty.
- Have Tim review the substantive judgments; preserve disagreement and record consent/reuse status.
- Keep Week 1 to Tim’s version: do not recruit a wider reviewer pool or board reviewers yet.
- Produce a JSONL-ready release plus generated Markdown review views.
- Include the synthetic worked sample `EFD-0001` only as a schema demonstration, plus a small Tim-specific calibration set and held-out cases.

**Output:** Tim-specific versioned dataset v0.1, schema, sample, and annotation guide.

**Decision:** jointly decide whether Tim’s version works well enough to baseline; only after the pilot, decide whether to invite additional Ethereum-aligned reviewers, potentially including board members.

## Week 2 — Establish the baseline

**Question:** How do major practical models respond to the same Ethereum-alignment cases?

- Select the major hosted/open models that are practical to test.
- Use the same cases, instructions, evidence package, and output budget.
- Compare ordinary prompting against the principles/evidence framing.
- Blind-review correctness, principle application, evidence support, alternatives, uncertainty, tone, and dogmatism.
- Record latency, cost, failures, and model-specific constraints.

**Output:** baseline comparison and recommendation on which model(s) are worth adapting.

**Decision:** jointly decide whether fine-tuning is justified and which model(s), if any, proceed to Week 3.

## Week 3 — Fine-tune, retest, and report

**Question:** Does fine-tuning improve the chosen model beyond the matched baseline, and was the pilot feasible?

- Select one or two viable open models rather than fine-tuning everything.
- Run a controlled SFT/DPO or adapter experiment using the agreed dataset, if justified.
- Retest against the same held-out cases and baseline conditions.
- Check general capability, brand bias, fabricated evidence, overconfidence, and excessive refusal.
- Report what QZ learned technically, what Tim learned about feasibility, quality, cost, limitations, and the next decision.

**Output:** pilot report and train-versus-don’t-train recommendation
