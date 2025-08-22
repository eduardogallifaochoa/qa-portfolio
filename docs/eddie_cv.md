<!--
File: docs/eddie_cv.md
Export to PDF and upload as docs/eddie_cv.pdf
-->

# **Eduardo Gallifa Ochoa** — QA Engineer
Manual & Automation Testing · Playwright · Selenium · Pytest · CI/CD · Performance · AI-assisted testing

**Location:** Ciudad Madero, Tamaulipas, Mexico · **Phone:** +52 833 121 0691  
**Email:** eduardogallifao@gmail.com  
**GitHub:** https://github.com/eduardogallifaochoa  
**LinkedIn:** https://www.linkedin.com/in/eduardogallifaochoa/  
**Portfolio:** https://eduardogallifaochoa.github.io/qa-portfolio

---

## **Profile**
QA Engineer & AI Automation Consultant. I build practical, production-style quality systems: **Playwright + Pytest** for UI, **FastAPI + TestClient** for API, and **OpenAPI contract + fuzz testing** (Schemathesis/Hypothesis)—all wired into **CI/CD (GitHub Actions + Docker)** with quality gates, HTML reports, and coverage. Comfortable with both automation and manual QA (exploratory, test design, bug triage). I use AI intentionally to speed up test creation, code review, and reporting—always with outcomes that non-technical stakeholders can understand.

---

## **Core Skills**
| Area | Detail |
|---|---|
| **UI** | Playwright (Chromium/Firefox/WebKit), robust selectors, fixtures, parallel runs, HTML reports |
| **API** | FastAPI, Pydantic, HTTPX, Starlette TestClient, OpenAPI 3.1, contract & fuzz (Schemathesis/Hypothesis) |
| **CI/CD & DevOps** | GitHub Actions, Docker/Compose, Uvicorn, Nginx, Codecov |
| **Quality & Security** | Pytest + coverage, Ruff (lint/format), Bandit (SAST), pip-audit (deps) |
| **Scripting & Data** | Python, JavaScript, Bash; SQL for QA queries |
| **Manual QA** | Exploratory testing, boundary/edge cases, test cases, bug reporting (Jira/TestRail) |
| **Practices** | STLC/SDLC, Agile (Scrum/Kanban), requirements-to-tests traceability |
| **Languages** | Spanish (Native), English (B2–C1 Cambridge) |

---

## **Highlight Project — QA Automation Site (2025)**
**Repo:** https://github.com/eduardogallifaochoa/qa-automation-site

- **Stack:** Static Nginx frontend (index/login/contact) + **FastAPI** backend (login/contact), **OpenAPI 3.1** (`/openapi.json`), CORS & security headers.  
- **UI Automation (Playwright + Pytest):** positive/negative/edge flows for login & contact; reusable fixtures; seeded runs; clean HTML reports.  
- **API Tests (Pytest + TestClient):** unit/integration for `/api/*` with input validation and error paths.  
- **Contract & Fuzz:** **Schemathesis** against OpenAPI 3.1 (reproducible seeds) with a Pytest wrapper.  
- **CI/CD:**  
  - `test.yml`: Docker Compose (frontend + backend), readiness checks, UI + API tests, upload `report.html`, push coverage to **Codecov**.  
  - `fuzz.yml`: boot FastAPI (Uvicorn), run Schemathesis (`--checks all`, `--max-examples`), then Pytest wrapper.  
- **Quality Gates:** pipeline blocks merges on failing UI/API/fuzz tests or failing lint/security/coverage thresholds.  
- **Tooling:** browser caching in CI, deterministic fuzzing, fixtures designed for stability, business-friendly reports.

---

## **Experience**
**QA Engineer / AI Automation Consultant — Freelance** · 2024–Present  
- Designed **UI/API test suites** and **CI/CD pipelines** with quality gates for safer releases.  
- Introduced **AI workflows** (structured prompting) to generate/expand cases, scripts, and analyze failures.  
- Reduced **flakiness** with robust locators and stability controls; curated test data and led bug triage/prioritization with product.

---

## **Selected Projects**
- **Analytics REST API** — *FastAPI · Pytest · CI*  
  CRUD with contract tests, coverage, and GitHub Actions.  
  Docs: `docs/projects/analytics-rest-api_one-pager.md`
- **Microservice Deployment Pipeline** — *Docker · GitHub Actions*  
  Build → Test → Publish → Release; reproducible pipelines.  
  Docs: `docs/projects/microservice-deployment-pipeline_one-pager.md`
- **AI Assistant Bot** — *Python · OpenAI*  
  CLI to summarize test results and flag flaky cases.  
  Docs: `docs/projects/ai-assistant-bot_one-pager.md`
- **Price Monitoring Tool** — *Python · SQLite · Docker*  
  Scheduler for BTC/ETH snapshots, logs, and alerts.  
  Docs: `docs/projects/price-monitoring-tool_one-pager.md`
- **AI Trading Bot** — *Python · OpenAI · Binance*  
  Modular services for signals/backtests and summaries.  
  Docs: `docs/projects/ai-trading-bot_one-pager.md`
- **SauceDemo Automation** — *Selenium · Pytest*  
  Login → cart → checkout with clean test reports.

---

## **Education**
**B.Eng., Industrial Engineering** — Universidad Latinoamericana (2020–2024)  
**Certifications:** Cambridge English (B2–C1)

---

## **Toolbox**
Playwright, Pytest, FastAPI, HTTPX, Pydantic, Schemathesis/Hypothesis, Docker, GitHub Actions, Uvicorn, Nginx, Ruff, Bandit, pip-audit, Codecov, Jira, TestRail

---

## **Availability**
Open to **Automation QA**, **Manual QA**, and short-term consulting (quality gates, test architecture, release safety with AI).
