# QA Automation Site · Test Plan (short)


## Overview
| Item | Detail |
| --- | --- |
| Objective | Validate login and contact flows with durable selectors |
| In scope | UI, API, cookies/session, email format |
| Out of scope | Email provider delivery, analytics |
| Env | Local FastAPI http://localhost:8000 |


## Approach
- Smoke: happy paths for login and contact
- MAT: all fields, boundaries, cookies and session
- AT: negatives for credentials, invalid emails, long messages, rate‑limit


## Test Types
- Functional E2E, API contract
- Non‑functional: performance baseline (50 VUs)


## Entry Criteria
- [ ] Build available
- [ ] Routes healthy


## Exit Criteria
- [ ] Smoke and MAT pass
- [ ] No Major/Critical open


## Severity
| Level | Meaning |
| --- | --- |
| Critical | Auth bypass, crash, data loss |
| Major | Session not created or broken form submission |
| Average | Wrong validation message or layout shift impacting input |
| Minor | Cosmetic |
| Enhancement | Suggestion |


## Deliverables
- HTML report, bug tickets, short summary


## Risks
- Flaky selectors from dynamic attributes → mitigated with role‑based locators


## Schedule
| Phase | Date |
| --- | --- |
| Smoke | today |
| MAT | today |
| AT | today |