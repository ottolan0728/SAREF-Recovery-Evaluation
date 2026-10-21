# Reliable-Agent R1-A Closure Report

**Closed gate: STOP. Closure date: 2026-09-29.**

R1-A is closed without advancement to full R1 or R2. **The current formulation does
not justify a learned recovery controller.** This closure records existing evidence;
no further experiments were run and no benchmark, failure, or recovery scope was added.

## Attempt history

| Attempt | Preserved classification |
|---|---|
| 1 — 2026-09-20 | ENVIRONMENT BLOCKED / NO SCIENTIFIC DECISION |
| 2 — 2026-09-22 | CHECKER GATE REVISE / NO SCIENTIFIC DECISION |
| 3 — 2026-09-22 | First completed empirical R1-A execution; bounded STOP |

## Validated checker and completed execution

The evaluator-only strict checker passed C1's 12 controls twice, including wrong
content, permissions, and output order. Final C2 established reproducible positive
and task-specific negative controls for **13 official InterCode Bash tasks**;
tasks 31 and 39 were excluded for checker-quality reasons before fault injection.
Contracts cover relevant path/type/mode/link/content state, normalized stdout,
stderr, exit status, and task invariants. Expected data remained evaluator-only.
Official InterCode source/reward remained unchanged and was reported separately.
These controls establish bounded validation, not an exhaustive correctness proof.

Attempt 3 completed **39 episodes and 117 branches**, limited to F1 transient
unavailability, F3 missing prerequisites, F5 contaminated persistent state, and
A1 retry, A2 local replay, A3 suffix restart. Branches shared identical frozen
failure prefixes. The saved independent implementation audit recomputed all 117
branch outcomes and metrics. Checker source, contracts, task selection and eligibility
evidence were archived before the first recovery episode.

## Fixed strategies and oracle

| Fixed strategy | Recovery successes | Mean cost | Mean regret | Oracle selections |
|---|---:|---:|---:|---:|
| A1 retry | 13/39 | 0.250 | 1.500 | 13 |
| A2 local replay | 39/39 | 0.583 | 0.111 | 26 |
| A3 suffix restart | 39/39 | 0.833 | 0.361 | 0 |

The oracle was defined in all 39 episodes: retry for F1 and local replay for F3/F5.
Cost was frozen as `(tool calls + replayed steps + rollback steps) / 12`.
Successful regret subtracts oracle cost; failed regret is `2 + incurred cost`.
Latency is recorded but has zero cost weight; no LLM was used. Recovery success
requires task correctness, valid persistent working state, and valid recovery calls.
Some F5 retries returned correct task results but left invalid scratch state.
Successful nominal workflows received official reward 0.72 because the unchanged
checker penalized their extra scratch directory; this was not hidden or corrected.

## Propagation limits and literal hard stop

Mean retry propagation radius was F1: 0, F3: 1, F5: 0.538. Only one node followed
the injection point, bounding radius at 1. Workflows were constructed four-step
decompositions with persistent scratch files; some stages merely copied artifacts.
Near-duplicate task variants, fixed checkpoint placement, and complete local rollback
limit diversity and generalization. This is not evidence about open-ended agents,
concurrent external databases, or inevitable harm from residual auxiliary artifacts.

The handoff's literal hard-stop trigger—**one universal strategy solves nearly
everything**—is satisfied by A2 (and A3), each successful in 39/39 episodes.
Suffix restart was never the minimum-cost action. Cost separability is preserved
as a finding, but does not override the closed STOP or justify learned recovery.

## Preservation

All prior artifacts, reports, frozen archives and image packages remain unchanged.
The closure manifest inventories their SHA256 hashes and links the three existing
audit ZIPs. This additive closure supersedes any earlier pending-gate language
without rewriting historical records. No further execution or expansion is authorized.
