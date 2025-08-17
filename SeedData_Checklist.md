## Purpose
To provide a realistic, GDPR-compliant dummy dataset for ATS + CRM development and testing.

## Sources
**Mockaroo**: for quick CSV schema generation.
**Faker (Python)**: to generate data programmatically and directly seed Postgres.
**Open datasets**: HR analytics, employee attrition (public / anonymised).
Entities
Candidates – ID, Name, Email, Phone, Skills, GDPR flag
Jobs – ID, Title, Department, Client, Posted Date
Applications – CandidateID, JobID, Applied Date, Stage, Status
Stages – Applied → Screening → Interview → Offer → Hired/Rejected
Interviews – ApplicationID, Scheduled Date, Interviewer, Feedback
Offers – ApplicationID, Salary, Status
CRM – Clients, Contacts, Open roles, Notes
Generation Method
Seed 1,000 candidates across 50 jobs.
Stage progression includes drop-offs: e.g., 20% fail screening, 15% receive offers.
Time delays are incorporated (10–20 days interview → offer).

## Seed Data checklist

| Task                                      | Status  | Notes                                                                                                  | Date |
| ----------------------------------------- | ------- | ------------------------------------------------------------------------------------------------------ | ---- |
| Define schema for dummy data              | Pending | ATS (Candidates, Jobs, Applications, Stages, Interviews, Offers) + CRM (Clients, Contacts, Activities) |      |
| Generate Candidates data (ATS)            | Pending | 1,000 sample profiles                                                                                  |      |
| Generate Jobs data (ATS)                  | Pending | 50 sample jobs                                                                                         |      |
| Generate Applications & Stages data (ATS) | Pending | Simulate funnel with drop-offs                                                                         |      |
| Generate Interviews data (ATS)            | Pending | Include schedules & feedback                                                                           |      |
| Generate Offers data (ATS)                | Pending | With acceptance/rejection                                                                              |      |
| Generate Clients data (CRM)               | Pending | 100 sample companies                                                                                   |      |
| Generate Contacts data (CRM)              | Pending | 2–5 per client                                                                                         |      |
| Generate Activities/Comms data (CRM)      | Pending | Emails, calls, meetings linked to clients/contacts                                                     |      |
| Validate dataset integrity                | Pending | Check FK links: candidate↔application, client↔contact↔activity                                         |      |
| Save sample CSV/SQL export                | Pending | Provide reproducible example                                                                           |      |
| Document seed data generation             | Pending | Scripts, schema, random seed for reproducibility                                                       |      |
