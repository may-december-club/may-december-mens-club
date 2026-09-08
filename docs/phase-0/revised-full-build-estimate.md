# Revised Full-Build Estimate — Phase 0 Recalibrated

Date: 2026-09-08
Status: **PLANNING ESTIMATE — NOT IMPLEMENTATION AUTHORIZATION**

## Purpose

This document preserves the original full-build baseline and the first Phase 0-informed revision, then provides a newly recalibrated estimate using the Product Owner-requested **BRL 125/hour planning basis** and a fresh workstream-by-workstream assessment of the actual AI-assisted Phase 0 operating model.

No blanket AI-savings percentage is applied. Each workstream is reconsidered individually for direct Phase 0 reuse, AI-assisted construction opportunity, Technical Lead review/QA burden, specialist work, provider dependencies, and remaining uncertainty.

## Comparison baselines

Original Full-PRD Estimate v1.2:

- Scenario A — Primary Developer: **5,180h / BRL 1,010,100 / 141 weeks**.
- Scenario B — Lean Brazil Team: **6,590h / BRL 942,700 / 71 weeks**.

Prior Phase 0-informed revision submitted in PR #7:

- Scenario A: **4,540h / ~BRL 885,600 / 120–128 weeks**.
- Scenario B: **5,770h / ~BRL 825,300 / 60–64 weeks**.

The prior revision was intentionally conservative and retained the original workstream cost basis proportionally. The Product Owner requested a second pass based more directly on demonstrated Phase 0 velocity and the AI-assisted construction/review model.

## Product Owner planning-rate basis

For this recalibration, internal human Technical Lead/development/QA effort is presented at **BRL 125/hour** as the Product Owner planning basis. This is a commercial planning convention for comparison and does not itself establish future contract terms or individual specialist rates.

Independent provider fees, certification, licensed services and other third-party costs remain separate external allowances.

## Phase 0 operating evidence applied

Phase 0 demonstrated that AI can perform a meaningful portion of implementation and documentation while the Technical Lead remains accountable for directing work, architecture, review, security judgment, testing, correction and acceptance readiness. The active technical execution of individual Phase 0 milestones occurred materially faster than the original one-week-per-milestone planning assumption, while still requiring human review and correction.

The same evidence also limits how far acceleration can be projected. M2 recorded **6.0h identifiable correction/rework out of 24.0h total**, and M3 required Product Owner reconciliation of documentation/status inconsistencies even though Technical Lead UAT found no new technical defect. Therefore the recalibrated model includes explicit review/QA and normal conformance correction rather than assuming AI output is accepted without human validation.

## Newly recalibrated preferred model — Lean Brazil Team

| ID | Workstream | Original B h | Prior revised h | Recalibrated h | Labor @ BRL 125/h | Phase 0-informed treatment |
|---|---|---:|---:|---:|---:|---|
| A | Accounts, Registration & Authentication | 510 | 325 | **250** | **31,250** | Highest direct reuse. Existing Rails structure, auth, recovery, account states, tests and UAT patterns are reusable. AI should materially accelerate remaining CRUD/policy work. Human hardening, abuse controls, MFA/OTP and Production-readiness review remain. |
| B | Profiles & Verification | 520 | 460 | **430** | **53,750** | Profile implementation can use established Rails patterns and AI-assisted construction, but live ID/liveness/private-media integration and exception handling remain provider-dependent and specialist-heavy. |
| C | Search & Discovery | 350 | 315 | **260** | **32,500** | AI should accelerate query/UI scaffolding and test construction. Search quality, PostGIS/indexing, ranking behavior and performance still require substantial human validation. |
| D | Messaging & Member Interaction | 610 | 545 | **470** | **58,750** | Shared auth/policy patterns are reusable and AI can accelerate standard flows. Concurrency, lifecycle, delivery state, abuse/safety and browser/system validation remain substantial. |
| E | Community Circles & Event Listings | 630 | 560 | **480** | **60,000** | Domain screens/controllers/tests are strong AI-construction candidates. Membership rules, moderation, event edge cases and launch content require human review. |
| F | Knowledge Center & Help | 360 | 325 | **250** | **31,250** | Standard content/admin surfaces should accelerate materially. Grounded retrieval, evaluation and controlled AI behavior remain specialist/review intensive. |
| G | Premium, Billing & Payments | 360 | 330 | **310** | **38,750** | Standard entitlement/UI work can accelerate, but payment-provider integration, reconciliation, failure handling and financial acceptance remain largely unchanged. |
| H | Notifications & Communications | 250 | 225 | **170** | **21,250** | Phase 0 email/canonical URL experience and Rails patterns are directly reusable. Async jobs, retries, deliverability and provider failure handling still require Production hardening. |
| I | Trust & Safety, Moderation & Admin | 710 | 650 | **610** | **76,250** | Admin CRUD can accelerate, but policy, appeals, evidence handling, operational workflows and human moderation responsibilities are insufficiently comparable to Phase 0; estimate remains largely retained. |
| J | Privacy, Security & Compliance | 430 | 385 | **390** | **48,750** | Phase 0 security patterns reduce some discovery, but independent privacy/security review, threat modeling, provider/data-flow review and launch validation cannot reasonably be AI-discounted heavily. |
| K | Accessibility, UX & Responsive Web | 550 | 495 | **410** | **51,250** | AI-assisted component construction and responsive implementation should reduce build time. Human UX review, accessibility testing and independent acceptance remain mandatory. |
| L | Platform Architecture, Cloud & DevOps | 480 | 415 | **330** | **41,250** | Repo, CI and Staging patterns are directly reusable; AI can accelerate IaC/config scaffolding. Production observability, backups, recovery, secrets, scaling and security review remain human-controlled. |
| M | Analytics, Reporting & Re-engagement | 320 | 290 | **230** | **28,750** | Event/report scaffolding is AI-suitable. KPI definitions, consent/privacy and business validation remain human-led. |
| N | Launch, Support & Operational Readiness | 510 | 450 | **430** | **53,750** | Documentation/runbook drafting can accelerate, but Beta, support rehearsal, provider certification, operational acceptance and launch dependencies remain substantially elapsed-time driven. |
| **Total** |  | **6,590** | **5,770** | **5,020** | **627,500** | |

The recalibrated total is **5,020h**, a reduction of **1,570h / 23.8%** from the original Scenario B and **750h / 13.0%** from the prior Phase 0-informed revision. This percentage is an output of the workstream analysis, not an input assumption.

## Quality and rework accountability included in the hours

The recalibrated hours include Technical Lead responsibility for directing AI-generated work, reviewing it against the controlling PRD/architecture, testing it, correcting implementation/conformance defects, and determining that work is ready before Product Owner acceptance.

Normal correction required to bring an authorized deliverable into conformance with approved requirements is **included in the agreed milestone/fixed delivery cost**. Implementation defects or PRD-conformance defects identified during Product Owner acceptance are not separately billable when they are within approved scope. Additional billing applies only to approved scope changes, newly introduced requirements, third-party changes outside the controlled assumptions, or explicitly authorized out-of-scope work.

Mandatory internal gates before Product Owner presentation are:

1. requirement/PRD traceability check;
2. Technical Lead architecture/code review;
3. automated tests/lint/security gates where applicable;
4. browser/system UAT including relevant negative paths;
5. accessibility/responsive review for user-facing work;
6. independent QA pass for full-build milestones where the team model assigns QA;
7. defect/conformance correction and retest;
8. evidence/status reconciliation before submission.

Repeated Product Owner discovery of issues that should reasonably have been caught in Technical Lead review would be treated as a delivery-process failure requiring corrective action to the QA/TL process, not as a basis for additional billable defect-correction hours.

## Staffing assumptions — preferred full-build model

Expected operating team by active workstream:

- Technical Lead / senior builder: approximately **0.8–1.0 FTE** throughout active construction and acceptance preparation;
- 2 software engineers: approximately **1.6–2.0 FTE combined** during main construction;
- independent QA/test engineer: approximately **0.4 FTE early**, ramping to **0.8–1.0 FTE** during integration/Beta;
- UX/accessibility specialist: approximately **0.3–0.6 FTE** during user-facing workstreams and acceptance preparation;
- DevOps/security specialist: approximately **0.2–0.5 FTE**, higher around infrastructure/security/launch gates;
- provider/business specialists engaged as dependencies rather than assumed full-time staff.

Average productive capacity is expected to be approximately **3.5–4.0 FTE equivalent** during the main build, with concurrency across frontend/backend/QA/UX/DevOps where dependencies permit.

## Critical-path schedule — Phase 0-informed expected model

| Phase / workstream cluster | Active construction | TL review / QA | PO review / wait | External dependency | Concurrency / sequencing |
|---|---:|---:|---:|---|---|
| Platform baseline + Production architecture | 2–3 w | 1 w overlapping | 0.5–1 w | Cloud/provider decisions | Starts first; enables all later work |
| Accounts + Profiles + Verification foundation | 4–6 w | 1–2 w overlapping | 0.5–1 w | ID/liveness/OTP provider | Accounts can begin immediately; verification provider can run in parallel |
| Search + Messaging + Circles + Knowledge Center | 10–14 w | continuous + 2 w integration | 1–2 w total gate time | Search/realtime/provider decisions where applicable | Major streams can run concurrently after common domain/auth foundation |
| Billing + Notifications + Analytics | 5–8 w | continuous + 1 w integration | ~1 w | Payment/email providers | Can overlap late community/messaging work |
| Trust & Safety + Admin | 7–10 w | 2 w review/UAT | 1 w | policy/ops input | Can begin before feature-complete and mature alongside Beta preparation |
| Security + Accessibility hardening | 4–6 w concentrated, plus continuous review | 2–3 w | 0.5–1 w | independent review/certification | Continuous during build; final gate is sequential before Production |
| Integrated Beta preparation/stabilization | 4–6 w | intensive QA/UAT | 1–2 w | Beta users/provider readiness | Sequential after core feature set reaches integrated acceptance baseline |
| Beta operation to Production launch | 6–10 w | ongoing QA + launch rehearsal | 1–2 w | provider approval, support readiness, security/accessibility closure | Production launch waits on Beta evidence and external gates |

## Elapsed-time scenarios — preferred model

| Scenario | Beta timing | Beta-to-Production | Production launch | Assumptions |
|---|---:|---:|---:|---|
| **Conservative** | **42–46 weeks** | **10–12 weeks** | **52–58 weeks** | Slower provider decisions, more sequential work, normal PO review queues, higher stabilization burden. |
| **Phase 0-informed expected** | **32–36 weeks** | **8–10 weeks** | **40–46 weeks** | 3.5–4.0 productive FTE equivalent, active AI-assisted construction, timely PO gates, workstream concurrency, normal rework included. |
| **Aggressive but realistically achievable** | **26–30 weeks** | **8 weeks** | **34–38 weeks** | Stable 4+ productive FTE equivalent, same/next-day PO decisions, providers selected early, limited scope ambiguity, no major external certification delay. |

The schedule is rebuilt from expected concurrency and Phase 0-observed active execution velocity rather than proportionally reducing the original 71-week calendar. It does not assume every Production workstream can move at Phase 0 pilot speed.

## Cost summary at Product Owner planning basis

- Recalibrated preferred human effort: **5,020h**.
- Product Owner planning basis: **BRL 125/h**.
- Recalibrated labor: **BRL 627,500**.
- Prior revised Scenario B labor: **~BRL 825,300**.
- Original Scenario B labor: **BRL 942,700**.
- External one-time planning allowance retained: **BRL 184,000**, pending current quotes/approval.
- Management contingency: **10–15% of labor = BRL 62,750–94,125**, visible and not hidden as implementation hours.
- Indicative labor + external + contingency planning envelope: **BRL 874,250–905,625**.

Operating costs and payment-processing fees remain separate and dependent on usage/provider decisions.

## Why some areas are not reduced more

Phase 0 did not validate live identity/liveness, realtime messaging under load, Production payment operations, Trust & Safety operations, independent accessibility/security certification, Production scaling/recovery or launch operations. Those areas therefore retain substantial human/specialist effort and contingency despite the demonstrated AI-assisted delivery model.

## Recommendation

Use the **5,020h / BRL 627,500 labor / 40–46 week Phase 0-informed expected launch** model as the preferred commercial planning baseline, with the conservative and aggressive schedule scenarios retained for decision-making. Keep the BRL 184,000 external allowance and 10–15% labor contingency visible until provider and launch uncertainties are closed.

This estimate does not authorize the full build. Final authorization should freeze scope, milestone acceptance evidence, provider decisions, staffing commitments and external-cost approvals in writing.
