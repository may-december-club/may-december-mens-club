# Phase 0 Milestone 3 — Technical Lead Staging UAT

## Status

**COMPLETE — 19/19 REQUIRED SCENARIOS PASSED ON 2026-09-08.**

This checklist records the mandatory Technical Lead end-to-end UAT requested for Milestone 3. Matheus Moura executed the scenarios directly against the business-controlled non-Production Staging environment and reported the actual observations recorded below.

Staging target: `https://may-december-staging.onrender.com`

Pre-UAT CI evidence: **CI #173 passed** for head `ff1789396e48b090f510b500f6b683038455b10b` (run `34160861428`). Test, lint and security jobs all completed successfully.

## Execution controls

- Synthetic/test accounts only; no Production member data used.
- Passwords, SMTP credentials and reset tokens are intentionally omitted.
- Browser-observed results were recorded as PASS/FAIL rather than inferred from automated tests.
- The same browser session was retained for the Active -> Suspended stale-session authorization scenario.

## Successful workflows

| ID | Scenario | Actual result | Evidence / notes |
|---|---|---|---|
| M3-UAT-01 | Registration Step 1 with valid unique email and >=12-character password | **PASS** | Browser advanced to Step 2; membership state displayed as Pending. |
| M3-UAT-02 | Save/resume registration across sign-out/sign-in | **PASS** | After save/sign-out/sign-in, browser returned to Step 2 with Pending state preserved. |
| M3-UAT-03 | Complete registration while Pending | **PASS** | Completion succeeded; membership remained Pending and inactive. |
| M3-UAT-04 | Sign in with valid credentials | **PASS** | Authentication succeeded after sign-out; completed registration did not restart; Pending state preserved. |
| M3-UAT-05 | Request password recovery for existing synthetic account | **PASS** | Generic confirmation shown and recovery email was received through configured Staging mail path. |
| M3-UAT-06 | Open valid recovery link | **PASS** | Technical Lead confirmed the valid link opened correctly on the canonical Staging host. |
| M3-UAT-07 | Change password with valid reset token | **PASS** | Password update succeeded and authentication with the new password succeeded. |
| M3-UAT-08 | Active member accesses `/members/dashboard` | **PASS** | Technical Lead confirmed Active member restricted-dashboard access succeeded. |

## Failure / negative workflows

| ID | Scenario | Actual result | Evidence / notes |
|---|---|---|---|
| M3-UAT-09 | Registration with password shorter than 12 characters | **PASS** | Registration remained at Step 1 and displayed minimum-12-character validation feedback. |
| M3-UAT-10 | Register normalized duplicate email | **PASS** | Case-varied duplicate normalized to the existing address and was rejected as already taken. |
| M3-UAT-11 | Sign in with wrong password | **PASS** | Authentication denied with generic `Invalid email or password.` response. |
| M3-UAT-12 | Sign in with nonexistent email | **PASS** | Authentication denied with the same generic `Invalid email or password.` response. |
| M3-UAT-13 | Request password recovery for nonexistent email | **PASS** | Generic `If that email exists...` confirmation displayed without account-existence disclosure. |
| M3-UAT-14 | Use fabricated/invalid reset token | **PASS** | Technical Lead confirmed invalid token was rejected and password was not changed. |
| M3-UAT-15 | Reuse a previously consumed reset token | **PASS** | Technical Lead confirmed consumed token could not be reused. |
| M3-UAT-16 | Anonymous user accesses `/members/dashboard` | **PASS** | Technical Lead confirmed restricted access was denied. |
| M3-UAT-17 | Pending member accesses `/members/dashboard` | **PASS** | Technical Lead confirmed restricted access was denied. |
| M3-UAT-18 | Suspended member accesses `/members/dashboard` | **PASS** | Technical Lead confirmed restricted access was denied. |
| M3-UAT-19 | Same authenticated session: Active -> Suspended, then request `/members/dashboard` again | **PASS** | Initial Active access succeeded; after authoritative transition to Suspended, the same browser session was denied on the next request without sign-out/sign-in. |

## Additional Technical Lead observations

No submission-blocking defect was reported during this Milestone 3 Technical Lead UAT cycle. The browser-observed registration, authentication and non-enumeration results matched the reviewed implementation. Password-recovery delivery and token lifecycle were also confirmed end-to-end. Authorization checks passed for anonymous, Pending, Active and Suspended states, including the required same-session stale-state transition proof.

The technical-review future-MVP hardening conditions remain recommendations rather than Phase 0 UAT defects and are tracked separately in the architecture, security and code-quality reviews.

## Completion statement

Technical Lead: **Matheus Moura**

Execution date: **2026-09-08**

Required scenarios: **19**

Passed: **19**

Failed: **0**

Final result: **PASS**

Gate C decision: **COMPLETE. Milestone 3 may proceed to Gate D scorecard/commercial analysis.**
