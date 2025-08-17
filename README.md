## Project Plan – CanvasCore

## Overview
This document outlines the 12-week plan for building CanvasCore, a unified ATS + CRM platform. It includes a traceability matrix mapping deliverables to project objectives, a week-by-week timeline, and notes on artefacts including dummy datasets for testing.

## Traceability Matrix
| Deliverable                            | Objective / Purpose                           | Evidence Type / Notes                                   |
| -------------------------------------- | --------------------------------------------- | ------------------------------------------------------- |
| GitHub Repository                      | Central codebase & documentation              | Repo link, commit history                               |
| README.md                              | Vision, tech stack, installation instructions | Public-facing overview                                  |
| ProjectPlan.md                         | Timeline & traceability                       | Internal reference                                      |
| ERD Diagram                            | Data model clarity                            | dbdiagram.io                                            |
| Migration Scripts (SQLAlchemy/Alembic) | Database versioning and reproducibility       | Scripts + version control                               |
| Seed Data Generator/ Dummy datasets    | Generate realistic recruitment data           | Python script, sample synthetic data                    |
| FastAPI Endpoints                      | Core API functionality                        | Swagger/OpenAPI auto-generated docs                     |
| Unit Test Coverage                     | Ensure code reliability                       | GitHub Actions + pytest                                 |
| Power BI Dashboard                     | Analytics & KPI visualization                 | Pipeline metrics, recruiter performance                 |
| Feature Backlog / Issues               | Track development tasks                       | GitHub Issues (labelled: feature, tech, docs)           |

## Dependencies / Tech Stack
Python 3.11+
FastAPI
SQLAlchemy / Alembic
PostgreSQL
Pydantic
pytest / GitHub Actions
Streamlit (frontend prototype)
Power BI (dashboard)
dbdiagram.io (ERD)

## Seed Data Generator / Dummy Datasets
Purpose: To test API endpoints, database migrations, and analytics dashboards without using real personal data.
Source: All datasets are synthetically generated using Python scripts.
Compliance: Fully GDPR-compliant as all data is fictional; suitable for testing and demo purposes.
Contents: Candidates, jobs, applications, stages, interviews, offers—covering common and edge-case scenarios.

## 12-Week timeline
| Week | Focus Area                            | Key Activities & Deliverables                                                    |
| ---- | ------------------------------------- | -------------------------------------------------------------------------------- |
| 1    | Inception                             | Finalise scope, success criteria, initial GitHub repo, README.md, ProjectPlan.md |
| 2    | Data Modelling                        | ERD diagrams, database schema, initial migration scripts                         |
| 3    | Seed Data Generator                   | Build Python scripts, generate sample data with edge cases (dummy datasets)      |
| 4    | API Development (Part 1)              | Implement GET/POST endpoints for Candidates and Jobs                             |
| 5    | API Development (Part 2)              | Implement Applications, Stages, Interviews endpoints                             |
| 6    | API Development (Part 3)              | Implement Offers, PATCH Applications, and pipeline analytics endpoints           |
| 7    | Testing & Validation                  | Unit tests for APIs, database scripts, seed data validation                      |
| 8    | Frontend Setup                        | Streamlit UI prototyping, basic dashboards connected to APIs                     |
| 9    | Analytics Dashboard                   | Power BI dashboard development (pipeline KPIs, recruiter metrics)                |
| 10   | Documentation & Cleanup               | API docs (Swagger/OpenAPI), README updates, code refactoring                     |
| 11   | Integration & Performance Checks      | Connect backend, frontend, and analytics; performance tuning                     |
| 12   | Final Review & Artefact Consolidation | Ensure all deliverables complete, all evidence mapped, repo polished             |


## License
This project is licensed under the [MIT License](./LICENSE).
