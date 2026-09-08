# Phase 0 Measurement Scorecard

## Status

**GATE E COMPLETE — Phase 0 evidence scorecard and final Technical Lead recommendation are complete. PR #7 is the formal Milestone 3 submission for Product Owner review and acceptance.**

This scorecard consolidates only metrics supported by the Phase 0 evidence recorded in the repository or explicitly supplied by the Technical Lead. Missing measurements remain explicitly unreported rather than estimated without evidence.

## Commercial baseline

| Milestone | Name | Fixed amount | Delivery status | Payment status |
|---|---|---:|---|---|
| M1 | Foundation | BRL 5,400 | Completed | Not restated here without a specific payment record in the current evidence set |
| M2 | Accepted Pilot Slices | BRL 7,200 | Accepted; PR #4 merged | Paid — confirmed by Matheus Moura on 2026-09-04 |
| M3 | Evidence & Recommendation | BRL 5,400 | Gate E complete; submitted in PR #7 for Product Owner acceptance | Pending Product Owner acceptance |
| **Phase 0** |  | **BRL 18,000** | Formal closeout submission under Product Owner review |  |

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

### Phase 0 through Gate E

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
- M3 closeout also required Product Owner reconciliation of documentation/status inconsistencies before acceptance readiness, reinforcing that acceptance should not substitute for Technical Lead quality control.
- Phase 0 therefore supports continued AI-assisted delivery as an acceleration mechanism under accountable human technical leadership; it does not support unsupervised AI implementation as a planning assumption.

## Cost / effort observations

The Phase 0 fixed commercial amount is **BRL 18,000**. The observed human-effort evidence through Gate E is **59–69 hours**, with a **64-hour planning midpoint**. Dividing fixed milestone price by those hours would describe the commercial Phase 0 package, not an agreed hourly labor rate, so this scorecard does not use that arithmetic as a future pricing basis.

The Product Owner requested a **BRL 125/hour planning basis** for the final commercial recalibration. Applying that basis together with a fresh workstream analysis produces the current preferred full-build planning model of **5,020h / BRL 627,500 labor**, with **40–46 weeks expected to Production** and **32–36 weeks expected to Beta**. The recalibrated Fundraising Visual Prototype is **57–70h (~64h midpoint) / BRL 8,500 recommended fixed fee / 1.5–2 weeks expected**.

These are planning outputs, not factual measurements of a universal AI efficiency rate and not authorization to execute either scope. Detailed rationale and schedule are in `revised-full-build-estimate.md`, `fundraising-visual-prototype-estimate.md`, and `milestone-3-commercial-recalibration.md`.

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

## Gate E conclusion

**Gate E — COMPLETE.**

The scorecard, final Technical Lead recommendation, revised/recalibrated full-build estimate, recalibrated Fundraising Visual Prototype estimate, commercial comparison, and submission evidence have been completed. **PR #7 is the formal Milestone 3 submission.**

The remaining Phase 0 closeout action is **Product Owner review and acceptance of PR #7**, subject to the submission head remaining green in CI. No additional implementation scope is authorized by this submission.
