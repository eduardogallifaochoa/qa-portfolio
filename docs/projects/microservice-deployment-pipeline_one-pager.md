# Microservice Deployment Pipeline · One‑Pager


| Field | Details |
| --- | --- |
| Goal | CI/CD with Dockerized FastAPI services and release artifacts |
| Scope | Build, test, image publish, release |
| Repo | https://github.com/eduardogallifaochoa/microservice-deployment-pipeline |


**Stack**
- FastAPI, Docker, GitHub Actions


**CI/CD**
- Build → Test → Publish → Release


## Key Tests
- Unit tests on service layer
- Healthcheck returns 200


## Evidence
- Screenshot: assets/microservice-pipeline.png


## Results
- Reproducible builds and releases with badges.