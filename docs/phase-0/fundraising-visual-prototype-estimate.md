# Fundraising Visual Prototype — Phase 0 Recalibrated Commercial Estimate

Date: 2026-09-08
Status: **ESTIMATE ONLY — EXECUTION NOT AUTHORIZED**

## Scope basis

This estimate is based on the approved Fundraising Visual Prototype BRD v1.0 dated 2026-09-07. The prototype remains separate scope from Phase 0 and from the future Production build.

The controlled BRD requires 10 core screens, journey/screen inventory, low-fidelity wireframes, visual direction, high-fidelity screens, clickable prototype, responsive anchor states, presentation exports, editable source files, component/design-system guidance, PRD traceability, asset/license inventory, and seven Product Owner approval gates.

Excluded: Production backend/database, live member data, Production authentication, live ID verification/OTP, live search/messaging, payments, moderation queues, admin systems, analytics, live AI, native applications and Production security certification.

## Why the estimate is being recalibrated

The prior PR #7 prototype estimate was **87–112h / ~100h midpoint / BRL 15,000 fixed fee / 3–4 weeks**, using BRL 150/h. That estimate treated many design/production steps conservatively as largely manual.

Phase 0 demonstrated a faster AI-assisted operating model: AI can materially accelerate first-pass construction, documentation and iteration while the Technical Lead remains accountable for requirements traceability, review, QA, correction and acceptance readiness. The prototype is especially suitable for this model because it excludes most live backend/provider/security dependencies.

The new estimate therefore reduces construction hours while increasing the explicitness of the internal quality gate. It does not remove Product Owner approval gates or assume that generated output can bypass Technical Lead review.

## Recalibrated human-effort estimate

| Work item | Prior estimate | Recalibrated estimate | Treatment |
|---|---:|---:|---|
| Scope / PRD traceability / constraints | 5–7h | **4–5h** | Human-led; AI assists extraction/checklists but Technical Lead owns interpretation. |
| Screen inventory + member journey | 3–4h | **2–3h** | Strong AI-assisted drafting opportunity with human conformance check. |
| Low-fidelity wireframes — 10 screens | 8–10h | **5–6h** | AI/design-tool acceleration is material; human structure review retained. |
| Visual direction / brand application | 5–7h | **4–5h** | Brand judgment remains human; AI accelerates variants. |
| High-fidelity anchor screens | 9–12h | **7–8h** | AI-assisted component/layout construction with Technical Lead/design review. |
| Remaining high-fidelity screens | 14–18h | **9–11h** | Reuse of established components and AI-assisted construction materially reduces effort. |
| Clickable interaction/prototype wiring | 6–8h | **4–5h** | Standard interaction wiring is highly automatable; navigation consistency remains reviewed. |
| Responsive/mobile anchor states | 5–7h | **4–5h** | AI/component reuse helps, but manual responsive QA retained. |
| AI/design-tool direction + iteration | 5–7h | **4–5h** | Explicit Technical Lead supervision retained. |
| Internal BRD/PRD/brand review | 6–8h | **5–6h** | Not materially discounted; this is a mandatory accountability function. |
| Interaction/responsive QA + correction | 5–7h | **5–6h** | Normal conformance correction included before PO presentation. |
| Product Owner approval-gate support | 6–8h | **4–5h** | Seven gates retained; faster package preparation assumed, not fewer approvals. |
| Final exports/source/component guide/asset inventory | 5–7h | **4–5h** | AI/documentation templates and reuse accelerate packaging. |
| **Total** | **87–112h** | **57–70h** | |
| **Planning midpoint** | **~100h** | **~64h** | |

The recalibrated range is **57–70h**, with a **64h planning midpoint**.

## Product Owner planning-rate basis

- Planning rate: **BRL 125/hour**.
- Labor range: **BRL 7,125–8,750**.
- Midpoint labor value: **BRL 8,000**.
- Recommended controlled-scope fixed fee: **BRL 8,500**.

The fixed-fee recommendation includes normal Technical Lead review, internal QA, correction of implementation/design/BRD-conformance defects within the approved scope, final packaging, and support through the seven defined approval gates.

The prior BRL 15,000 recommendation at BRL 150/h is retained only as historical comparison; the new commercial planning recommendation is **BRL 8,500 fixed fee** under the requested BRL 125/h basis and Phase 0-informed delivery assumptions.

## Quality-accountability model

Product Owner review is an **acceptance gate, not the first substantive QA pass**.

Before any prototype output is presented at a Product Owner approval gate, the Technical Lead must complete and retain an internal checklist covering:

1. controlling Prototype BRD and relevant PRD traceability;
2. no invented unsupported feature, Premium benefit, verification claim, workflow or member capability;
3. approved brand/asset conformity and asset-license status;
4. navigation and interaction consistency;
5. responsive-state review for required anchor screens;
6. component/design-system consistency;
7. obvious content/visual/accessibility issues appropriate to a fundraising prototype;
8. normal conformance correction and re-review before submission.

Normal correction required to bring the authorized prototype into conformance with the approved BRD/PRD is **included in the fixed fee and is not separately billable**. Separate billing requires written scope change: additional screens/journeys, new deliverable classes, materially changed approved requirements, Production functionality, or other explicitly authorized out-of-scope work.

Repeated Product Owner discovery of issues that should reasonably have been caught during Technical Lead review would be treated as a failure of the Technical Lead QA process and would require process correction rather than additional defect-correction billing.

## Phase 0-informed elapsed-time scenarios

The prototype has substantially fewer external dependencies than the Production build. Its seven Product Owner gates are the main elapsed-time variable.

| Scenario | Active construction | TL QA/correction | PO review/wait | Expected elapsed |
|---|---:|---:|---:|---:|
| **Conservative** | 7–9 business days | 3–4 days overlapping/final | 4–6 days cumulative | **2.5–3 weeks** |
| **Phase 0-informed expected** | 5–7 business days | 2–3 days overlapping/final | 2–4 days cumulative | **1.5–2 weeks** |
| **Aggressive but realistically achievable** | 4–5 business days | 1–2 days overlapping | same-day / next-day gate decisions | **5–7 business days** |

The aggressive scenario requires immediate access to approved assets/content, stable BRD scope, rapid Product Owner decisions, no material visual-direction restart after Gate 3, and concentrated Technical Lead availability.

The expected scenario is the recommended planning assumption: **approximately 1.5–2 weeks**.

## Third-party / asset allowance and contingency

- Incremental licensed asset/design-tool allowance: **BRL 0–1,500**, only if required and approved before purchase.
- No live provider integration is included.
- Normal correction/rework is included in the 57–70h range and BRL 8,500 fixed-fee recommendation.
- The range itself provides an internal effort reserve of approximately 10% around the midpoint; no separate hidden implementation contingency should be added.
- Product Owner-requested scope changes remain separately authorized rather than charged against defect/rework allowance.

## Staffing assumption

Primary delivery is expected to use one Technical Lead/senior builder using AI-assisted design/construction tools, with targeted specialist design input only if needed. No independent full-time QA resource is assumed for this prototype; the mandatory documented Technical Lead QA gate substitutes for a separate QA role at this scope. If independent design/accessibility review is later required, it should be explicitly added and costed rather than assumed silently.

## Commercial comparison

| Model | Human effort | Rate basis | Labor / fixed fee | Elapsed time |
|---|---:|---:|---:|---:|
| Prior prototype estimate | 87–112h (~100h midpoint) | BRL 150/h | BRL 15,000 recommended fixed fee | 3–4 weeks |
| **Phase 0-recalibrated prototype** | **57–70h (~64h midpoint)** | **BRL 125/h** | **BRL 8,500 recommended fixed fee** | **1.5–2 weeks expected** |

## Authorization boundary

This document satisfies the revised estimate request only. It does **not** authorize prototype execution. No billable prototype work, material provider purchase, licensed-asset commitment or third-party engagement should begin without explicit written Product Owner authorization.
