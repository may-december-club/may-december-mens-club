# Milestone 3 Commercial Recalibration — Phase 0 Evidence Applied

Date: 2026-09-08
Status: **PLANNING PACKAGE — NO EXECUTION AUTHORIZED**

## Purpose

This document provides the single-place comparison requested by the Product Owner after review of PR #7. It distinguishes the original full-build baseline, the first Phase 0-informed revision, the newly recalibrated Phase 0-informed full-build estimate, the prior fundraising prototype estimate, and the newly recalibrated prototype estimate.

The recalibration uses **BRL 125/hour** as the Product Owner planning basis for internal Technical Lead/development/QA effort. This is a planning convention only and does not establish future contract terms.

## Commercial comparison

| Estimate | Human effort | Rate basis | Labor / fixed fee | External / third-party | Contingency | Expected elapsed | Status |
|---|---:|---:|---:|---:|---:|---:|---|
| Original Full Build — Scenario B | 6,590h | Original mixed-role basis | BRL 942,700 | BRL 184,000 one-time planning allowance | Original planning assumptions | 71 weeks | Historical baseline |
| First Phase 0-informed Full Build — Scenario B | 5,770h | Prior workstream basis | ~BRL 825,300 | BRL 184,000 placeholder | 10–15% management contingency recommended | 60–64 weeks | Superseded by recalibration for current PO evaluation |
| **New Phase 0-recalibrated Full Build — preferred** | **5,020h** | **BRL 125/h** | **BRL 627,500** | **BRL 184,000 placeholder pending current quotes** | **BRL 62,750–94,125 (10–15% labor)** | **40–46 weeks expected** | **Current planning recommendation; not authorized** |
| Prior Fundraising Visual Prototype | 87–112h (~100h midpoint) | BRL 150/h | BRL 15,000 recommended fixed fee | BRL 0–1,500 assets/tools | Normal corrections included | 3–4 weeks | Superseded for current PO evaluation |
| **New Phase 0-recalibrated Prototype** | **57–70h (~64h midpoint)** | **BRL 125/h** | **BRL 8,500 recommended fixed fee** | **BRL 0–1,500 only if approved** | **Normal conformance rework included in range/fixed fee** | **1.5–2 weeks expected** | **Current planning recommendation; not authorized** |

## Full-build elapsed-time scenarios

| Scenario | Beta | Beta to Production | Production launch | Key assumption |
|---|---:|---:|---:|---|
| Conservative | 42–46 weeks | 10–12 weeks | **52–58 weeks** | Slower provider/PO decisions, more sequential work, higher stabilization burden |
| **Phase 0-informed expected** | **32–36 weeks** | **8–10 weeks** | **40–46 weeks** | 3.5–4.0 productive FTE equivalent, AI-assisted parallel construction, timely review gates |
| Aggressive but realistically achievable | 26–30 weeks | ~8 weeks | **34–38 weeks** | Stable 4+ FTE, early provider decisions, low scope ambiguity, rapid PO review |

## Prototype elapsed-time scenarios

| Scenario | Active construction | TL QA/correction | PO review/wait | Total elapsed |
|---|---:|---:|---:|---:|
| Conservative | 7–9 business days | 3–4 days overlapping/final | 4–6 days cumulative | **2.5–3 weeks** |
| **Phase 0-informed expected** | **5–7 business days** | **2–3 days overlapping/final** | **2–4 days cumulative** | **1.5–2 weeks** |
| Aggressive but realistically achievable | 4–5 business days | 1–2 days overlapping | same/next-day decisions | **5–7 business days** |

## Phase 0-informed effort logic

The recalibrated estimates do not apply a general percentage reduction. Workstreams are treated according to evidence:

- **Direct reuse / strongest acceleration:** Rails foundation, CI/Staging patterns, account-state authorization, registration/authentication/recovery patterns, canonical URL/configuration practices, test/evidence structure.
- **Material AI-assisted acceleration with human validation retained:** standard controllers/views/components, common CRUD/domain scaffolding, tests, responsive component construction, documentation, prototype screen generation and iteration.
- **Human Technical Lead / QA remains substantial:** architecture, authorization/security-sensitive behavior, browser/system UAT, negative-path testing, accessibility review, acceptance evidence, requirements traceability and final submission readiness.
- **Largely unchanged or lightly reduced:** live identity/liveness, payment operations, messaging concurrency, Trust & Safety operations, privacy/security certification, provider certification and Production launch dependencies.
- **External dependency:** provider selection/contracting, live third-party behavior, independent certification and business-side policy/operations cannot reasonably be accelerated simply because AI-assisted implementation is faster.
- **Contingency retained:** unknown provider behavior, Production scaling/recovery, certification, launch/Beta findings and unvalidated full-PRD complexity.

## Technical Lead quality accountability

The planning model assumes the Technical Lead is responsible for directing AI output, reviewing against the controlling requirements and architecture, testing, correcting deficiencies, and deciding that work is ready before Product Owner acceptance.

Normal implementation/conformance correction required to satisfy an authorized milestone is **included in the agreed milestone/fixed delivery cost**. Product Owner identification of an in-scope implementation or PRD-conformance defect does not create incremental billable hours. Separate billing applies only to written scope changes, new requirements, changed external assumptions, or other explicitly authorized out-of-scope work.

The full-build team model includes independent QA participation in addition to Technical Lead review. The prototype uses a mandatory documented Technical Lead internal QA checklist before each Product Owner gate; a separate full-time QA role is not assumed for the prototype.

Repeated Product Owner discovery of issues that reasonably should have been identified during Technical Lead review would require corrective action to the Technical Lead/QA process and, if persistent, reassessment of role/accountability or staffing — not automatic additional defect-correction billing.

## Mandatory pre-acceptance quality gates

1. requirements/PRD or Prototype-BRD traceability;
2. Technical Lead architecture/code/design review as applicable;
3. automated test/lint/security gates for software work;
4. browser/system UAT with relevant negative scenarios;
5. responsive/accessibility review for user-facing work;
6. independent QA pass where assumed by the full-build staffing model;
7. conformance correction and retest;
8. evidence/status reconciliation before Product Owner presentation.

For the prototype specifically, the internal gate also verifies that no unsupported feature, Premium benefit, verification claim, member capability or workflow has been invented and that brand/assets/navigation/responsive states conform to the approved BRD.

## Staffing assumptions — preferred full build

- Technical Lead / senior builder: ~0.8–1.0 FTE.
- Two software engineers: ~1.6–2.0 FTE combined.
- QA/test engineer: ~0.4 FTE early, ramping to ~0.8–1.0 FTE for integration/Beta.
- UX/accessibility specialist: ~0.3–0.6 FTE during relevant workstreams.
- DevOps/security specialist: ~0.2–0.5 FTE, higher around infrastructure and launch gates.
- Average main-build productive capacity: ~3.5–4.0 FTE equivalent.

## Recommendation

For Product Owner planning, use:

- **Full build:** 5,020h, BRL 627,500 labor at BRL 125/h, BRL 184,000 external allowance placeholder, 10–15% visible labor contingency, **40–46 weeks expected to Production**, Beta at approximately 32–36 weeks.
- **Fundraising Visual Prototype:** 57–70h, approximately 64h midpoint, **BRL 8,500 fixed fee**, BRL 0–1,500 separately approved asset/tool allowance, **1.5–2 weeks expected**.

Neither estimate authorizes execution, staffing, purchases, provider commitments or scope changes.
