# QA Automation Site · One‑Pager


> Realistic playground for login and contact flows.


| Field | Details |
| --- | --- |
| Goal | Validate end‑to‑end auth and contact flows reliably |
| Scope | Web UI (static) + FastAPI backend, cross‑browser E2E |
| Repo | https://github.com/eduardogallifaochoa/qa-automation-site |


**Stack**
- HTML/CSS/JS, FastAPI, Python, Playwright, Pytest


**CI/CD**
- Workflow: CI
- Status: [![CI](https://github.com/eduardogallifaochoa/qa-automation-site/actions/workflows/ci.yml/badge.svg)](https://github.com/eduardogallifaochoa/qa-automation-site/actions)


## Key Tests
- Login success redirects with valid session
- Rate‑limit blocks after repeated failures
- Contact form validates length and email format
- API returns 2xx and matches JSON schema


## Evidence
- Screenshot: assets/qa-automation-site.png


## Results
- Stable cross‑browser runs on Chromium, Firefox, WebKit with clean HTML reports.


## Next Steps
- Contract tests for status codes and schema
- Client‑side max length guard for contact form