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

| Task                                         | Status | Notes                                                                          | Date |
| -------------------------------------------- | ------ | ------------------------------------------------------------------------------ | ---- |
| Generate Candidate Profiles                  |        | Name, contact info, resume link, skills, diversity attributes                  |      |
| Generate Client Profiles                     |        | Company info, contact person, industry, engagement score                       |      |
| Generate Job/Role Listings                   |        | Job title, department, status (open/closed), assigned recruiter                |      |
| Generate Recruiter / Talent Acquisition Data |        | Name, team, region, assigned candidates/jobs                                   |      |
| Generate Hiring Manager Profiles             |        | Name, department, assigned jobs, feedback history                              |      |
| Generate ATS Pipeline Stages                 |        | Applied, Screening, Interview, Offer, Hired/Rejected                           |      |
| Generate Application Events                  |        | Timestamps for stage transitions, duration per stage                           |      |
| Generate Messaging Records                   |        | Sample chats between Candidate ↔ Recruiter, Client ↔ Recruiter, HM ↔ Recruiter |      |
| Generate Email Notifications (Optional)      |        | Simulated email triggers for stage changes or messaging                        |      |
| Generate Satisfaction Survey Responses       |        | Client, Candidate, Recruiter, HM scores, feedback text                         |      |
| Generate Diversity & Inclusion Metrics       |        | Derived from candidate profiles and survey responses                           |      |
| Generate CRM Engagement Events               |        | Notes, follow-ups, calls, meetings, response status                            |      |
| Generate Dummy Analytics Metrics             |        | Funnel counts, conversion rates, engagement scores, average time per stage     |      |
| Tools / Scripts Setup                        |        | Use Python scripts (Faker/Mockaroo), PostgreSQL seed scripts                   |      |
