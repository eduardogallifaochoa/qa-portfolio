# <Project> · Test Plan (short)


> Concise plan you can scan fast. Keep it to 1–3 pages.


## Overview
| Item | Detail |
| --- | --- |
| Objective | Validate core flows with realistic data and clear pass/fail criteria |
| Scope (In) | <list of features/areas> |
| Scope (Out) | <list excluded for this iteration> |
| Environments | Dev: <url> · Local: <how to run> |


## Approach
- Smoke Test: general positive flows with valid data
- MAT (Minimal Acceptance Test): all functionalities with valid data
- AT (Acceptance Test): negative coverage of all functionalities


## Test Types
- Functional: E2E UI, API contract
- Non‑functional: Performance baseline, Accessibility quick pass


## Test Data
- Stored in `testdata/` with boundary values defined.


## Entry Criteria
- [ ] Build available
- [ ] Critical blockers resolved
- [ ] Test env accessible


## Exit Criteria
- [ ] Smoke and MAT passed
- [ ] No Major/Critical open
- [ ] Reports published


## Severity
| Level | Meaning |
| --- | --- |
| Critical | Crash, payment failure, data loss |
| Major | Blocks core purpose of the app |
| Average | Non‑blocking defect with workaround |
| Minor | Cosmetic/low impact |
| Enhancement | Improvement suggestion |


## Deliverables
- HTML test report, bug tickets with evidence, summary note


## Risks & Mitigations
- <risk> → <mitigation>


## Schedule
| Phase | Date |
| --- | --- |
| Smoke | <date> |
| MAT | <date> |
| AT | <date> |