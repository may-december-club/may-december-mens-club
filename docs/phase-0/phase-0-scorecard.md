# Phase 0 Measurement Scorecard

## Status

**GATE D COMPLETE — Phase 0 evidence scorecard reconciled through Technical Lead Staging UAT. Final Product Owner submission remains pending Gate E recommendation and final CI/SHA evidence.**

This scorecard consolidates only metrics supported by the Phase 0 evidence recorded in the repository or explicitly supplied by the Technical Lead. Missing measurements remain explicitly unreported rather than estimated without evidence.

## Commercial baseline

| Milestone | Name | Fixed amount | Delivery status | Payment status |
|---|---|---:|---|---|
| M1 | Foundation | BRL 5,400 | Completed | Not restated here without a specific payment record in the current evidence set |
| M2 | Accepted Pilot Slices | BRL 7,200 | Accepted; PR #4 merged | Paid — confirmed by Matheus Moura on 2026-09-04 |
| M3 | Evidence & Recommendation | BRL 5,400 | Gate D complete; final recommendation/submission pending | Not yet due |
| **Phase 0** |  | **BRL 18,000** | Final closeout in progress |  |

## Human-effort evidence

| Metric | Milestone 1 | Milestone 2 | Milestone 3 | Phase 0 |
|---|---:|---:|---:|---:|
| Actual / reconstructed / TL-supplied approximate human effort | 15.0h | 24.0h | 20–30h retrospective range | **59–69h range** |
| Planning midpoint | 15.0h | 24.0h | 25.0h | **64.0h** |
| Specification / clarification | Not separately recorded | 2.0h in confirmed baseline | Not reliably separated | At least 2.0h; not fully comparable |
| Human implementation / documentation | 7.0h | 8.0h in confirmed baseline | Not reliably separated | 15.0h explicitly categorized before M3 |
| AI-assisted work / supervision | 3.5h | 3.0h in confirmed baseline | Present but not reliably separated | 6.5h explicitly categorized before M3; no valid final numeric total |
| Human review | 1.5h | 2.0h in confirmed baseline | Material component but not reliably separated | 3.5h explicitly categorized before M3; no valid final numeric total |
| Rework / correction | 1.0h explicit rework | 6.0h identifiable correction/rework-related effort | No new UAT defect/rework amount separately identified | **At least 7.0h identifiable** |
| Testing / Staging validation | 2.0h | 3.0h in confirmed baseline plus part of 3.0h aggregate | Material M3 UAT component but not reliably separated | Not reliably comparable as a final numeric total |

### Milestone 3 measurement qualification

On 2026-09-08, Technical Lead Matheus Moura supplied a retrospective approximate actual M3 human-effort range of **20–30 hours**. A **25-hour midpoint** is retained solely for planning/comparison. It is not an exact timesheet value.

No reliable category-level split was captured for M3. Therefore this scorecard does not invent allocations among AI supervision, technical review, documentation, Staging UAT, commercial analysis, testing, or correction.

## Rework / correction indicators

### Milestone 1

- Explicit rework recorded: **1.0h / 15.0h = 6.7%**.
- No separate material source-line rewrite percentage was reliably measured.

### Milestone 2

- Identifiable correction/rework-related effort: **6.0h / 24.0h = 25.0%**.
- This consists of the prior confirmed 3.0h aggregate rework + defect correction and the confirmed 3.0h post-baseline correction/UAT cycle.
- This is an effort-based measure, not a literal percentage of source-code lines rewritten.

### Phase 0 through Gate D

- Human effort: **59–69h**, midpoint **64h**.
- Identifiable correction/rework-related effort with explicit support: **at least 7.0h** (M1 1.0h + M2 6.0h).
- Relative to the 64h planning midpoint, 7.0h is **10.9%**, but this must not be presented as a complete Phase 0 rework rate because M3 category-level rework was not separately measured.
- A literal material rewrite percentage remains **not reliably measured**.

## Acceptance and quality evidence

### Milestone 1

- Foundation deliverables completed and retained on `main`.
- Architecture/engineering standards, CI, repository governance and Staging foundation evidence are present in the Phase 0 documentation set.

### Milestone 2

- All Product Owner hands-on acceptance scenarios passed before acceptance.
- Registration/save-resume, password-strength and negative authentication/recovery paths were exercised.
- End-to-end password recovery through business-controlled Staging email infrastructure passed.
- Pending/Active/Suspended authorization passed.
- Same-session Active -> Suspended stale-state authorization denial passed.
- Explicit Product Owner acceptance occurred on 2026-09-04 and PR #4 was merged to `main`.

### Milestone 3 Technical Lead validation

- Technical Lead Staging UAT completed on **2026-09-08**.
- **19/19 required scenarios PASS; 0 FAIL**.
- Registration, save/resume, completed Pending state, authentication, password validation, duplicate-email normalization, generic invalid authentication, recovery non-enumeration, real recovery email delivery, canonical reset link, valid password reset, invalid/consumed token rejection, anonymous/Pending/Suspended authorization denial, Active access and same-session Active -> Suspended immediate denial were exercised.
- No new submission-blocking defect was identified during M3 Technical Lead UAT.
- Architecture, security and code-quality reviews found no Phase 0 submission blocker, while recording future-MVP conditions.

## AI-assisted productivity observations

AI assistance materially supported Phase 0 implementation, review and evidence preparation, but the evidence does **not** support a defensible numeric claim such as a specific percentage of hours saved or an equivalent non-AI delivery duration.

Supported observations are:

- AI-assisted work was explicitly part of the M1 and M2 effort records and continued as part of the M3 workflow.
- Human Technical Lead supervision remained necessary for scope interpretation, review, defect correction, Staging configuration, security/architecture judgment, end-to-end UAT and acceptance evidence.
- M2 demonstrates that AI-assisted implementation did not eliminate correction/review cycles: 6.0h of the final 24.0h were identifiable as correction/rework-related effort.
- M3 demonstrates the value of independent human validation: 19 browser-level scenarios were executed by the Technical Lead even though automated CI was already green.
- Phase 0 therefore supports continued AI-assisted delivery as an acceleration mechanism under accountable human technical leadership; it does not support unsupervised AI implementation as a planning assumption.

## Cost / effort observations

The Phase 0 fixed commercial amount is **BRL 18,000**. The observed human-effort evidence through Gate D is **59–69 hours**, with a **64-hour planning midpoint**. Dividing fixed milestone price by those hours would describe the commercial Phase 0 package, not an agreed hourly labor rate, so this scorecard does not use that arithmetic as a future pricing basis.

Phase 0 has produced reusable technical foundations and evidence around Rails project structure, CI, Staging, account states, registration, authentication, password recovery and authorization. Reuse should reduce some future full-build work, but Phase 0 does not provide enough evidence to apply a single blanket percentage reduction to the original full-build estimate. The revised full-build estimate must be recalculated by workstream and explicitly distinguish reusable Phase 0 work, remaining implementation, human review/testing, expected AI efficiency and contingency.

## Metrics not reliably measured

The following remain **not reliably measured** and must not be presented as factual numeric Phase 0 results:

- literal material source-code rewrite percentage;
- normalized accepted-output-per-hour efficiency;
- comparable defect density across all milestones;
- complete Phase 0 correction/rework percentage including M3;
- exact M3 category-level effort split;
- exact percentage of human effort saved by AI;
- counterfactual non-AI delivery hours;
- full Phase 0 elapsed calendar-cycle efficiency independent of human effort.

## Gate D conclusion

**Gate D — Scorecard and commercial-analysis evidence: COMPLETE.**

The evidence is sufficient to proceed to Gate E and to prepare the requested closeout commercial comparison. Gate E must use this scorecard as the evidence baseline and must not convert approximate or unmeasured values into false precision.

Before final Product Owner submission, the closeout package still requires:

- final Technical Lead Go / Go-with-conditions / No-Go recommendation;
- revised full-build estimate calculated workstream by workstream from the Phase 0 evidence;
- separate Fundraising Visual Prototype estimate, clearly identified as unexecuted separate scope requiring explicit authorization;
- original vs revised full-build vs prototype comparison;
- final submission-head CI/SHA evidence and PR.
