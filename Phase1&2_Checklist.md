## Phase 1 checklist: Data & API Foundations (Week 2-4)

| Task                           | Status   | Notes                                                                     | Date       |
| ------------------------------ | -------- | ------------------------------------------------------------------------- | ---------- |
| Define preliminary ERD schema  | Pending  | Entities: Candidate, Client, Job, Recruiter, Hiring Manager, Survey, Chat | 03/10/2025 |
| Decide licence (MIT)           | Complete | Attach to repos                                                           | 18/08/2025 |
| Finalise ERD diagrams                                         | Pending | ATS entities + CRM entities                       |      |
| Identify dummy dataset sources | Pending  | GDPR-compliant: Mockaroo, Faker, Kaggle                                   | 06/10/2025 |
| Tools & environment setup      | Pending  | Python, Postgres, FastAPI, Streamlit, Power BI                            | 06/10/2025 |
| Create SeedData.md             | Pending  | Document dummy dataset usage                                              | 06/10/2025 |
| Initial API design             | Pending  | CRUD for candidates, clients, surveys, chats                              | Week 3     |
| Set up Postgres database                                      | Pending | Schema includes ATS & CRM tables                  |      |
| Write initial migration scripts                               | Pending | Use SQLAlchemy/Alembic                            |      |
| Generate seed data scripts                                    | Pending | Candidates, Jobs, Applications, Clients, Contacts |      |
| Create API endpoints – Candidates & Jobs (ATS)                | Pending | Basic CRUD                                        |      |
| Create API endpoints – Applications, Stages, Interviews (ATS) | Pending | Include status transitions                        |      |
| Create API endpoints – Offers, Pipeline Analytics (ATS)       | Pending | Include drop-off analysis                         |      |
| Create API endpoints – Clients (CRM)                          | Pending | Client profile CRUD                               |      |
| Create API endpoints – Contacts (CRM)                         | Pending | Contacts linked to clients                        |      |
| Create API endpoints – Activities / Communications (CRM)      | Pending | Calls, emails, meetings log                       |      |
| Unit tests for database & API                                 | Pending | Pytest + GitHub Actions                           |      |
| Document API (Swagger/OpenAPI)                                | Pending | Auto-generated docs                               |      |
| Connect initial Power BI dashboard                            | Pending | ATS funnel + CRM client activity summary          |      |

**Extend schema & ERD to include**:
messages table (sender_id, receiver_id, role, message, timestamp).
surveys table (stakeholder_type, score, comment, timestamp).
Implement FastAPI endpoints:
POST /message, GET /messages/{conversation_id}.
POST /survey, GET /surveys/{type}.
Seed dummy data:
Candidate-job applications.
Client-hiring manager relationships.
Candidate ↔ Recruiter ↔ Hiring Manager ↔ Client message logs.
Survey responses (Likert scale, free text).
Create Power BI connectors for candidate, CRM, message, and survey tables.
Test retrieval of dummy chat logs and survey results.

## Phase 2 - Core Feaures Implementation (Week 5-8)

| Task                    | Status  | Notes                                            |
| ----------------------- | ------- | ------------------------------------------------ |
| Implement ATS modules   | Pending | Candidate pipeline, job tracking                 |
| Implement CRM modules   | Pending | Client profiles, relationship notes              |
| Implement survey module | Pending | Store satisfaction + Diversity & Inclusion metrics                |
| Build messaging module  | Pending | Secure chat UI: client, recruiter, candidate, HM |
| Unit tests              | Pending | Validate endpoints and DB                        |
| Documentation update    | Pending | API reference, ERD v2                            |
