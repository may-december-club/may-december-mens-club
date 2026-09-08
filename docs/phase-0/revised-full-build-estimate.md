# Revised Full-Build Estimate — Phase 0 Informed

Date: 2026-09-08
Status: **PLANNING ESTIMATE — NOT IMPLEMENTATION AUTHORIZATION**

## Purpose

This estimate recalculates the approved controlling-PRD full-build planning baseline using evidence obtained during Phase 0. It does not change the controlling PRD, authorize Production development, staffing, provider purchases, or external commitments.

The comparison baseline is Full-PRD Estimate v1.2 dated 2026-08-19:

- Scenario A — Primary Developer: **5,180h / BRL 1,010,100 / 141 weeks**.
- Scenario B — Lean Brazil Team: **6,590h / BRL 942,700 / 71 weeks**.
- Scenario C — BRL 120k: reduced scope and not approved; it is not used as the full-PRD baseline.

## Phase 0 evidence applied

Phase 0 established reusable Rails foundations, CI/Staging practices, registration, account-state authorization, authentication, password recovery, canonical URL handling and tested Pending/Active/Suspended behavior. Technical Lead UAT completed **19/19 PASS** on 2026-09-08.

Phase 0 human-effort evidence totals **59–69h**, with a **64h planning midpoint**. AI materially assisted the work, but Phase 0 did not reliably measure a numeric percentage of hours saved. Therefore this recalculation does **not** apply a blanket AI discount. Each workstream is adjusted as a planning judgment based on concrete reuse, established implementation patterns, reduced discovery uncertainty, and continued human review/testing requirements.

## Revised Scenario A — Primary Developer

| ID | Workstream | Original h | Revised h | Change | Revised labor BRL* | Phase 0-informed rationale |
|---|---|---:|---:|---:|---:|---|
| A | Accounts, Registration & Authentication | 360 | 230 | -130 | 44,100 | Highest direct reuse: registration, auth, recovery, account states and authorization already exercised. Remaining ID/OTP/exceptions and production hardening retained. |
| B | Profiles & Verification | 390 | 345 | -45 | 67,700 | Account-state patterns reusable; identity/liveness/private-media provider work remains substantial. |
| C | Search & Discovery | 240 | 215 | -25 | 40,000 | Rails authorization/data patterns reusable; PostGIS/search behavior and performance still require implementation and validation. |
| D | Messaging & Member Interaction | 410 | 365 | -45 | 67,600 | Authentication/authorization foundation reused; lifecycle, realtime/concurrency and safety behavior remain. |
| E | Community Circles & Event Listings | 460 | 410 | -50 | 76,300 | Shared account/policy patterns help; community domain and launch content remain largely new. |
| F | Knowledge Center & Help | 270 | 245 | -25 | 46,000 | Platform patterns reused; grounded retrieval/evaluation and controlled content remain. |
| G | Premium, Billing & Payments | 290 | 265 | -25 | 50,300 | Authentication/entitlement foundation helps; production billing/reconciliation remains provider-dependent. |
| H | Notifications & Communications | 190 | 170 | -20 | Staging email/canonical URL experience reduces setup uncertainty; production deliverability and async resilience remain. |
| I | Trust & Safety, Moderation & Admin | 540 | 495 | -45 | Account-state/authorization model provides a base; moderation, appeals, evidence and operations remain high-risk/new. |
| J | Privacy, Security & Compliance | 480 | 430 | -50 | Security review and secrets/configuration boundaries provide reusable decisions; independent/privacy/security launch work remains mandatory. |
| K | Accessibility, UX & Responsive Web | 440 | 395 | -45 | Established Rails flow patterns help implementation; full UX/accessibility work and independent review remain. |
| L | Platform Architecture, Cloud & DevOps | 400 | 345 | -55 | Repository, CI and Staging foundation are directly reusable; Production IaC, observability, backup/recovery and security remain. |
| M | Analytics, Reporting & Re-engagement | 250 | 225 | -25 | Shared application patterns reduce setup; KPI/event model remains largely new. |
| N | Launch, Support & Operational Readiness | 460 | 405 | -55 | Phase 0 evidence/acceptance discipline is reusable; Beta, runbooks, provider certification, launch and hypercare remain. |
| **Total** |  | **5,180** | **4,540** | **-640 (-12.4%)** | **885,600** | |

\*Revised labor uses the v1.2 workstream labor basis proportionally to revised hours and is rounded for planning. A final commercial contract should rebuild the task/role WBS rather than treat these rounded values as invoices.

Planning calendar for Scenario A: **approximately 120–128 weeks**, compared with 141 weeks originally. Calendar reduction is smaller than pure implementation-hour acceleration because provider decisions, independent reviews, Beta, security/accessibility gates and launch activities retain elapsed-time dependencies.

## Revised Scenario B — Lean Brazil Team

The same workstream scope/reuse logic is applied to the team model while preserving the additional QA, UX, backend, frontend and DevOps participation that made the original Scenario B person-hour total larger but calendar duration shorter.

| ID | Workstream | Original h | Revised h | Revised labor BRL* |
|---|---|---:|---:|---:|
| A | Accounts, Registration & Authentication | 510 | 325 | 46,400 |
| B | Profiles & Verification | 520 | 460 | 64,800 |
| C | Search & Discovery | 350 | 315 | 44,900 |
| D | Messaging & Member Interaction | 610 | 545 | 76,000 |
| E | Community Circles & Event Listings | 630 | 560 | 77,000 |
| F | Knowledge Center & Help | 360 | 325 | 45,900 |
| G | Premium, Billing & Payments | 360 | 330 | 46,800 |
| H | Notifications & Communications | 250 | 225 | 32,500 |
| I | Trust & Safety, Moderation & Admin | 710 | 650 | 91,600 |
| J | Privacy, Security & Compliance | 430 | 385 | 60,700 |
| K | Accessibility, UX & Responsive Web | 550 | 495 | 64,300 |
| L | Platform Architecture, Cloud & DevOps | 480 | 415 | 67,400 |
| M | Analytics, Reporting & Re-engagement | 320 | 290 | 41,800 |
| N | Launch, Support & Operational Readiness | 510 | 450 | 65,200 |
| **Total** |  | **6,590** | **5,770** | **825,300** |

This is an **820h / 12.4%** planning reduction from the original Scenario B person-hour estimate. Planning calendar: **approximately 60–64 weeks**, compared with 71 weeks originally, subject to staffing availability and external gates.

## Commercial comparison

| Model | Original | Revised after Phase 0 | Difference |
|---|---:|---:|---:|
| Scenario A hours | 5,180h | 4,540h | -640h / -12.4% |
| Scenario A labor | BRL 1,010,100 | BRL 885,600 | -BRL 124,500 / -12.3% |
| Scenario A calendar | 141 weeks | 120–128 weeks | planning reduction |
| Scenario B hours | 6,590h | 5,770h | -820h / -12.4% |
| Scenario B labor | BRL 942,700 | BRL 825,300 | -BRL 117,400 / -12.5% |
| Scenario B calendar | 71 weeks | 60–64 weeks | planning reduction |

## Why the estimate changed

1. Phase 0 produced accepted/reusable code and engineering foundations rather than only theoretical planning.
2. Registration/authentication/account-state authorization and password recovery were implemented and independently exercised in Staging.
3. CI, Staging, review and acceptance patterns are now known and reusable.
4. Architecture/security/code-quality review reduced uncertainty around the Rails approach and identified specific future conditions rather than requiring a platform restart.
5. AI-assisted development is now demonstrated as workable under Technical Lead supervision, but no unsupported numeric AI-efficiency percentage is applied.
6. Human QA, security, accessibility, provider integration, Trust & Safety and launch-readiness work is deliberately retained; Phase 0 does not justify removing those controls.

## External costs

The original v1.2 reconciled one-time external planning allowance was **BRL 184,000**, separate from labor. Phase 0 did not obtain sufficient provider quotes or approvals to responsibly replace that allowance with a new committed amount. It therefore remains a **planning placeholder pending current provider quotes and written Product Owner approval**, not a committed cost.

Operating costs and payment-processing assumptions likewise remain subject to provider, launch-market, usage and business decisions and are not silently reduced by Phase 0.

## Confidence and contingency

Confidence improves from the original low-medium baseline for the validated Rails/account/auth foundation, but remains **medium overall** because identity verification, messaging concurrency, Trust & Safety operations, billing, AI Help, Production infrastructure, provider certification and launch operations remain unbuilt or provider-dependent.

The revised hours already retain human review/testing effort. A commercial commitment should additionally retain **10–15% management contingency** against the revised labor plan until the major provider/launch decisions and remaining technical spikes are closed. Contingency should be visible and not hidden inside implementation hours.

## Recommendation for commercial planning

Use **Scenario B — revised 5,770h / approximately BRL 825,300 labor / 60–64 weeks** as the preferred full-build planning model because it preserves specialist/QA/UX participation while materially reducing calendar risk. Scenario A remains viable where cash-flow or staffing constraints favor a primary-builder model, but its 120–128 week planning duration creates materially greater key-person and schedule risk.

Neither revised scenario is authorization to start the full build. A final contract should freeze the controlling PRD, provider decisions, milestone acceptance evidence, task/role WBS and external-cost approvals before commitment.
