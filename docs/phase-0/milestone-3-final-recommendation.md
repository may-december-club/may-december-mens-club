# Phase 0 Milestone 3 — Final Technical Lead Recommendation

Date: 2026-09-08
Technical Lead: Matheus Moura

## Decision

# **GO WITH CONDITIONS**

Phase 0 evidence supports proceeding from pilot validation into controlled full-build commercial/technical planning. It does **not** support an unconditional Production build or launch without the conditions below.

## Evidence basis

- Milestone 1 established the Rails/repository/CI/Staging foundation.
- Milestone 2 was accepted by Product Owner Michael Fitzgerald on 2026-09-04, merged to `main` in PR #4, and payment was confirmed received.
- Milestone 3 architecture, security and code-quality reviews found no Phase 0 submission blocker.
- Technical Lead Staging UAT completed on 2026-09-08 with **19/19 PASS, 0 FAIL and 0 new submission-blocking defects**.
- Phase 0 human-effort evidence totals **59–69h**, with a **64h planning midpoint**; M3 is a retrospective approximate range rather than an exact timesheet.
- AI assistance materially supported delivery, but human Technical Lead supervision remained necessary and no defensible blanket numeric AI time-saving percentage was measured.
- The commercial recalibration therefore uses workstream-specific reuse/acceleration judgments rather than a general percentage discount.

## Technical conclusion

The evaluated Rails approach is suitable to continue. The pilot demonstrates viable account-state authorization, registration/authentication/password recovery, server-side restricted-route enforcement, CI and Staging validation without requiring a platform restart.

The Phase 0 result is not evidence that the remaining PRD is low-complexity. Identity verification, private media, messaging lifecycle/concurrency, Trust & Safety, billing, grounded AI Help, Production infrastructure, accessibility/security certification and launch operations remain material workstreams.

## Conditions for full-build authorization

1. **Production email resilience:** move recovery/critical delivery from synchronous request-path SMTP to resilient asynchronous delivery with retries, observability and failure handling; retain enumeration-resistant behavior.
2. **Remove Phase 0 UAT-only controls before Production:** UAT state-transition routes/tooling must not remain exposed as Production product functionality.
3. **Authentication/recovery abuse controls:** implement rate limiting and appropriate abuse protections before Production exposure.
4. **Authorization evolution:** retain server-side authoritative state checks and introduce a clearer policy/domain authorization layer as permission complexity grows.
5. **Provider decisions:** close identity/liveness/OTP, payment, infrastructure and AI/provider decisions with privacy/security/data-flow review and current quotes before commercial commitment to dependent workstreams.
6. **Human QA/security/accessibility remain mandatory:** AI assistance must not replace independent testing, human review, accessibility acceptance, security testing or operational rehearsal.
7. **Trust & Safety capacity:** launch scope and acquisition must remain supportable by actual moderation/support capacity; automation cannot substitute for required human judgment.
8. **Controlled milestone acceptance:** full-build payments/delivery should remain tied to objective accepted evidence rather than elapsed time alone.
9. **Visible contingency:** retain 10–15% management contingency until major provider and launch uncertainties are closed; do not hide contingency as implementation hours.
10. **Business-owned infrastructure/accounts:** repositories, Production provider accounts, infrastructure ownership, credentials governance and handoff artifacts remain business-controlled.
11. **Technical Lead quality accountability:** normal implementation/PRD-conformance correction is included in the agreed milestone/fixed delivery cost; Product Owner acceptance is not intended to be the first substantive QA pass.

## Full-build commercial planning result

Original Full-PRD Estimate v1.2 baseline:

- Scenario A — Primary Developer: **5,180h / BRL 1,010,100 / 141 weeks**.
- Scenario B — Lean Brazil Team: **6,590h / BRL 942,700 / 71 weeks**.

First Phase 0-informed revision submitted in PR #7:

- Scenario A: **4,540h / ~BRL 885,600 / 120–128 weeks**.
- Scenario B: **5,770h / ~BRL 825,300 / 60–64 weeks**.

New Product Owner-requested Phase 0 recalibration — preferred Lean Brazil Team model:

- **5,020h human effort**;
- **BRL 125/h Product Owner planning basis**;
- **BRL 627,500 labor**;
- external one-time planning allowance retained at **BRL 184,000** pending current quotes/approval;
- visible labor management contingency **BRL 62,750–94,125 (10–15%)**;
- Phase 0-informed expected Beta: **32–36 weeks**;
- Phase 0-informed expected Production launch: **40–46 weeks**;
- conservative Production scenario: **52–58 weeks**;
- aggressive but realistically achievable Production scenario: **34–38 weeks**.

The reduction is a workstream-by-workstream output based on direct Phase 0 reuse, AI-assisted construction suitability, required Technical Lead/QA effort, provider constraints and unvalidated risk. It is not a blanket AI-efficiency claim.

Detailed calculation: `docs/phase-0/revised-full-build-estimate.md`.
Single-place commercial comparison: `docs/phase-0/milestone-3-commercial-recalibration.md`.

## Fundraising Visual Prototype planning result

Prior estimate:

- **87–112h**, ~100h midpoint;
- BRL 150/h prior basis;
- BRL 15,000 recommended fixed fee;
- 3–4 weeks.

New Phase 0-recalibrated estimate:

- **57–70h**, approximately **64h midpoint**;
- **BRL 125/h** Product Owner planning basis;
- midpoint labor value **BRL 8,000**;
- recommended **BRL 8,500 fixed fee** for the controlled BRD scope, including normal conformance correction and internal QA;
- expected elapsed **1.5–2 weeks**;
- conservative **2.5–3 weeks**;
- aggressive but realistically achievable **5–7 business days**;
- incremental licensed/design-tool allowance **BRL 0–1,500 only if required and separately approved**.

The prototype requires documented Technical Lead QA before every Product Owner gate, including BRD/PRD traceability, unsupported-feature checks, brand/asset conformity, interaction/navigation consistency, responsive-state review and correction before presentation.

Prototype execution is **NOT AUTHORIZED** by this recommendation. Explicit written Product Owner authorization is required before billable prototype implementation or material third-party commitments.

Detailed estimate: `docs/phase-0/fundraising-visual-prototype-estimate.md`.

## Quality and rework commercial model

The Technical Lead role includes directing AI-generated work, reviewing it against the controlling requirements and architecture, testing, identifying deficiencies, correcting those deficiencies, and deciding the deliverable is genuinely ready for acceptance.

Normal in-scope correction required to bring an authorized deliverable into conformance with approved requirements is **included in the agreed milestone/fixed price**. Product Owner identification of an implementation or PRD/BRD-conformance defect does not itself make that correction separately billable. Separate billing requires a written scope change, newly introduced requirement, changed external assumption or other explicitly authorized out-of-scope work.

For the full-build team, independent QA participation is assumed in addition to Technical Lead review. Mandatory pre-acceptance gates include requirements traceability, Technical Lead review, automated test/lint/security checks, browser/system UAT with negative paths, responsive/accessibility review, independent QA where staffed, defect correction/retest, and evidence/status reconciliation.

Repeated Product Owner discovery of issues that should reasonably have been identified in Technical Lead review would require corrective action to the delivery/QA process and, if persistent, reassessment of role/accountability or staffing — not automatic incremental defect-correction billing.

## AI-assisted productivity conclusion

Phase 0 supports continued AI-assisted engineering/design as an acceleration mechanism under accountable human leadership. It does not support unsupervised AI delivery or a contractual assumption that AI removes a fixed percentage of engineering hours.

The practical evidence is mixed in the useful sense: AI supported fast implementation/review/documentation, while M2 still required material correction/rework and M3 still required independent human browser UAT and Product Owner documentation reconciliation despite green automated CI. The appropriate planning model is therefore **AI-assisted + human-reviewed + acceptance-tested**.

## Gate E conclusion

**Gate E — COMPLETE. Final recommendation: GO WITH CONDITIONS.**

The Phase 0 technical/evidence work is substantively complete. PR #7 remains the formal Milestone 3 submission, now updated with the Product Owner-requested commercial recalibration.

The remaining closeout action is **Product Owner review and acceptance**, subject to the current submission head remaining green in CI.

No full-build or fundraising-prototype implementation is authorized by completion of Gate E or submission of PR #7.
