## Project Plan – CanvasCore

## Overview
This document outlines the 12-week plan for building CanvasCore, a unified ATS + CRM platform. It includes a traceability matrix mapping deliverables to project objectives, a week-by-week timeline, and notes on artefacts including dummy datasets for testing.

## Purpose
The goal of this project is to build an Applicant Tracking System (ATS) and a Customer Relationship Management (CRM) platform that unifies recruitment operations and client relationship management. 
The system will:
-Manage candidate pipelines (ATS) and client relationships (CRM).
-Provide real-time analytics dashboards for recruitment and client engagement.
-Include messaging functionality (chat UI) to streamline communication between clients, candidates, recruiters, and hiring managers.
-Capture satisfaction surveys (client, candidate, recruiter/TA, hiring manager) to measure engagement, experience, and diversity metrics.
-Be open-source, modular, and extensible within 12 weeks.

## Scope
PostgreSQL database with schema covering candidates, jobs, roles, clients, hiring managers, recruiters, messages, surveys. 
REST API (FastAPI) for data operations. 
Basic chat UI (Streamlit or React) for messaging. 
Power BI dashboards for ATS metrics, CRM insights, messaging analytics, and engagement scores. 
GitHub repository with MIT licence, seeded dummy dataset, and documentation. 

## Objectives
Build a modular platform supporting ATS and CRM workflows. 
Enable real-time or near-real-time communication between candidates, recruiters, hiring managers, and clients via a simple chat interface and stored logs. 
Capture satisfaction survey data for candidates, clients, recruiters, and hiring managers. 
Deliver dashboards in Power BI covering: 
Candidate pipeline metrics (ATS). 
Client and hiring manager analytics (CRM). 
Messaging volume, response times, sentiment (Messaging). 
Engagement scores and diversity metrics (Surveys). 
Provide an open-source GitHub repository with reproducible documentation and seeded datasets for testing.  

## Success Criteria
**1. Core ATS Features**: Job requisition, candidate pipeline, CV tracking, interview stages, offer management.Drop-off points and recruiter efficiency can be measured.
**2. Core CRM Features**: Client profiles, account management, contact tracking, relationship notes.Clients and contacts can be stored with full relationship history.
**3. Unified Dashboards**: Candidate pipeline metrics, client pipeline health, recruiter KPIs. Communication/activities (emails, calls, meetings) can be logged and reported.
**4. Engagement Metrics**: Survey dashboards showing client, candidate, recruiter, and hiring manager satisfaction, with breakdowns for diversity & inclusion data.
**5. Messaging System**:
-Secure chat UI (client & recruiter, candidate & recruiter, recruiter & hiring manager).
-Logged conversations for traceability.
-Optionally extensible to email integration.
**6. Data Foundations**: GDPR-compliant dummy datasets from sources like Mockaroo, Faker, Kaggle open datasets.
**7. Tech Delivery**:
-Backend: Postgres + FastAPI
-Frontend: Streamlit (dashboards) + optional lightweight chat UI
-Analytics: Power BI dashboards. Recruiters can view account-level dashboards in Power BI (e.g., active jobs per client, comms volume).
**8. Open Source Standards**: MIT licence, contribution guide, traceability to project goals.
**9. Technical**: System must expose REST APIs (ATS + CRM), seed datasets, and integrate with Power BI.

## Traceability Matrix
| Deliverable                             | Objective / Purpose                             | Notes                                                                   |
| --------------------------------------- | ----------------------------------------------- | ----------------------------------------------------------------------- |
| GitHub Repository                       | Central codebase & documentation                | Repo link, commit history                                               |
| README.md                               | Vision, tech stack, installation instructions   | Public-facing overview                                                  |
| ProjectPlan.md                          | Timeline & traceability                         | Internal reference                                                      |
| ERD Diagram                             | Data model clarity (ATS + CRM entities)         | dbdiagram.io — includes candidates, clients, jobs, recruiters, messages |
| Migration Scripts (SQLAlchemy/Alembic)  | Database versioning and reproducibility         | Scripts + version control                                               |
| Seed Data Generator/ Dummy datasets     | Generate realistic ATS + CRM data               | Python script (Faker/Mockaroo), sample synthetic data for testing       |
| FastAPI Endpoints                       | Core API functionality (ATS + CRM modules)      | Swagger/OpenAPI auto-generated docs                                     |
| Messaging UI                            | Real-time communication between stakeholders    | Secure chat: client ↔ recruiter, candidate ↔ recruiter, HM ↔ recruiter  |
| Email Notifications (Optional fallback) | Non-real-time comms for updates                 | Easier than chat if time runs short; email integration with FastAPI     |
| Unit Test Coverage                      | Ensure code reliability                         | GitHub Actions + pytest                                                 |
| Power BI Dashboard                      | Analytics & KPI visualization (ATS + CRM)       | Funnel metrics, recruiter performance, engagement & satisfaction scores |
| Satisfaction Surveys                    | Engagement, business improvement, D\&I insights | Client, Candidate, Recruiter, HM feedback loop                          |
| Diversity & Inclusion Metrics           | Track representation & fairness                 | Derived from surveys + recruitment data                                 |
| Feature Backlog / Issues                | Track development tasks                         | GitHub Issues (labelled: feature, tech, docs)                           |
| Deployment Docs (README/Docs folder)    | Setup, deployment, and usage guidance           | Instructions for local dev + production (Heroku/Docker optional)        |

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
JSON fields for surveys
React/Streamlit component, no enterprise features for Messaging UI

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


## Deliverables
Build a modular platform supporting ATS and CRM workflows. 
Enable real-time or near-real-time communication between candidates, recruiters, hiring managers, and clients via a simple chat interface and stored logs. 
Capture satisfaction survey data for candidates, clients, recruiters, and hiring managers. 
Deliver dashboards in Power BI covering: 
Candidate pipeline metrics (ATS). 
Client and hiring manager analytics (CRM). 
Messaging volume, response times, sentiment (Messaging). 
Engagement scores and diversity metrics (Surveys). 
Provide an open-source GitHub repository with reproducible documentation and seeded datasets for testing.

## License
This project is licensed under the [MIT License](./LICENSE).
