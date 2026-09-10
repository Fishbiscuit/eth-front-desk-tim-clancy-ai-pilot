---
okf: 1
type: "pilot-brief"
title: "ETH Front Desk Pilot — Brief"
status: "draft"
visibility: "collaborator-shared"
updated: "2026-09-10"
---
 
# ETH Front Desk Pilot — Brief

## Purpose

Test whether an AI assistant can give Ethereum builders more principled, technically grounded architecture advice without collapsing principles into branding or personality.

This is a bounded ETH Front Desk collaboration. It does not represent the Ethereum Foundation, does not imply EF endorsement, and does not assume a universal Ethereum constitution.

## Pilot question

Does a versioned principles framework plus current, cited evidence improve architecture-review quality over ordinary prompting? If yes, is the improvement best delivered through prompting and retrieval, or does fine-tuning add enough value to justify its cost and maintenance?

## First use case

A builder submits a product description, architecture document, or design choice. The assistant produces:

1. assessment;
2. relevant evidence;
3. consequences and trust dependencies;
4. practical alternatives;
5. unresolved questions and uncertainty.

The output should identify what is preserved, compromised, unclear, or not applicable across relevant dimensions. It should not hide a critical failure inside a single composite score.

## Initial review dimensions

- user control and exit;
- censorship resistance;
- openness and replaceability;
- privacy and meaningful choice;
- security and trust dependencies;
- neutrality and capture resistance;
- practical usefulness and fit for the user’s constraints.

## Three-week pilot

One phase per week:

1. **Week 1 — Create Tim Clancy’s version:** produce provider-neutral JSON case records, a JSONL-ready release, and generated Markdown review views from Tim’s agreed source material and judgments, with held-out cases and preserved disagreement. This first version is intentionally Tim-specific; expansion to other Ethereum-aligned reviewers, potentially including board members, is a later decision contingent on the pilot results. Reference and deliverable: [dataset-format-research](dataset-format-research.md).
2. **Week 2 — Establish the baseline:** test major practical models on the same cases, instructions, and evidence conditions.
3. **Week 3 — Fine-tune, retest, and report:** adapt only the most promising viable model(s), compare against the matched baseline, and document the result.

If fine-tuning is not justified, Week 3 reports the train-versus-don’t-train decision instead. The prototype remains read-only. Evidence, costs, configuration, and uncertainty are recorded throughout.

## Boundaries

The pilot will not train from scratch, issue a token, allocate grants, make investment recommendations, sign transactions, take custody, change production configuration, or claim official Ethereum authority.

The assistant should challenge decisions rather than insult people. It should support a clearly stated, accepted compromise by documenting risks and migration options.

## Deliverables

- constitution and annotation guide v0.1;
- [dataset-format-research](dataset-format-research.md) as the Week 1 dataset-format research and deliverable;
- approved case schema and synthetic worked sample;
- a bounded Tim Clancy case set with calibration and held-out cases;
- a post-pilot decision on whether to invite additional Ethereum-aligned reviewers, potentially including board members;
- reproducible baseline evaluation runner;
- controlled source catalog and freshness policy;
- initial architecture-review prototype;
- pilot report covering quality, evidence support, cost, user value, failures, and the train/don’t-train decision.

## Success evidence

The pilot succeeds if it can show, with matched comparisons and reviewer agreement analysis, whether the framework improves technical correctness, evidence support, principle application, useful alternatives, and appropriate uncertainty. A successful result may be a decision not to fine-tune.

## Working horizon

Three weeks, with one phase per week, subject to contributor availability. Scope, roles, weekly time allocation, budget, and experiment dates remain to be confirmed together.

## Allocation decision

Before Week 1 begins, Tim and QZ will jointly decide how much time each person is allocating, what is in scope for each week, and what is explicitly out of scope. The decision will be recorded in the decision log.

## Proposed collaborators

For Week 1, the working pair is Tim Clancy and QZ. The initial dataset should represent Tim’s version only. Additional Ethereum-aligned reviewers, potentially including board members, may be invited after the pilot if the results justify expanding the scope. Final roles and decision rights remain open until agreed.
