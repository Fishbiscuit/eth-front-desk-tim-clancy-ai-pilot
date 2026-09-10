---
okf: 1
type: "decision-log"
title: "ETH Front Desk Pilot — Decision Log"
status: "active"
visibility: "collaborator-shared"
updated: "2026-09-10"
---

# ETH Front Desk Pilot — Decision Log

## Project setup decision

| Date | Decision | Status | High-level setup |
|---|---|---|---|
| 2026-09-10 | Set up the ETH Front Desk architecture-review POC with Tim Clancy | Accepted | Three weeks: Tim-specific dataset → matched baseline → fine-tune/retest/report if justified. Use principles plus current evidence before training; author cases as provider-neutral JSON, release experiments as JSONL, and use Markdown for review. Keep the prototype read-only, without blockchain components, custody, production changes, or claims of official Ethereum authority. Tim and QZ will agree the POC’s time, scope, outputs, data rights, attribution, and expenses before Week 1. |

## Open decisions for this POC

- What source material may Tim provide or approve for the initial dataset, and what attribution or reuse terms apply?
- Which bounded architecture-review cases should the Tim-specific Week 1 set include?
- What principles, evidence sources, and scoring rubric will Tim and QZ use for the baseline?
- How much time will each person allocate, and who owns each Week 1–3 output and decision?
- Which models, prompts, tools, and evaluation conditions will be used for the baseline?
- What result would justify fine-tuning, and what result would justify stopping at prompting/retrieval?
- What external costs, if any, are approved for this POC?

## Change rule

Material changes to principles, data rights, model scope, public claims, or external release require an entry here with date, owner, rationale, and affected artifacts.
