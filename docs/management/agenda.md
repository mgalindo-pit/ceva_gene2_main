# Day1  

| Workshop                                  | Duration | Participants                                                    | Objective                                                                                                                                                                                         | Deliverables                                                                                                 |
| ----------------------------------------- | -------- | --------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| **Kick-off & Vision Alignment**           | 1h       | CIO (Fabien Tertois), Product Owners, CEVA leads, PALO IT leads | Align on vision, explain methodology, objectives and governance                                                                                                                                   | Kick-off presentation, communication plan                                                                    |
| **Roles & Communication Setup**           | 1h     | CEVA core team, PALO IT core team                               | Define RACI, communication channels, collaboration tools and Agile ceremonies cadence                                                                                                             | Roles map, RACI, communication & ceremonies plan                                                             |
| **Recording & Environment Setup Session** | 1h       | CEVA core team, PALO IT team                                    | Confirm meeting recording policies, explain that sessions will be recorded for transcript analysis, validate technical setup (Teams/Zoom/recording tools), test environment access for both teams | Recording agreement, confirmed setup for transcription and analysis, environment access validation checklist |
| **Use Cases Overview**             | 2h       | Product Owners Renault2MoveECAR, Business Analysts, Dev leads   | Gain a high-level view of the process (purpose, main inputs/outputs, expected value)                                                                                                              | Preliminary “functional vision” document                                                                     |

# Day 2
| Workshop                                                 | Duration | Participants                                         | Objective                                                                                                  | Deliverables                                                     |
| -------------------------------------------------------- | -------- | ---------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------- |
| **Legacy Process Walkthrough – Functional**              | 2.5h     | Product Owners, Business Analysts, Key Users         | Understand process objectives, business use cases, business rules                                          | Functional “as-is” document                                      |
| **Legacy Process Walkthrough – Technical (Static View)** | 2.5h     | CEVA Dev Leads, IBM IIB Architects, PALO IT engineer | Architecture, Review triggers, inputs, outputs, dependencies, **integration endpoints**, mapping of ESQL transformations | Technical flow map (inputs, outputs, dependencies, integrations) |
| **Project Documentation Setup**                          | 1.5h     | PALO IT engineer(s) only                             | Consolidate the first information gathered and structure it in a central documentation repository          | Central documentation repository initialized                     |

# Day 3
| Workshop                                                             | Duration | Participants                                    | Objective                                                                                   | Deliverables                                  |
| -------------------------------------------------------------------- | -------- | ----------------------------------------------- | ------------------------------------------------------------------------------------------- | --------------------------------------------- |
| **Legacy Process Walkthrough – Operations & Support**                | 2h       | CEVA Operations, QA, L2/L3 Support              | Understand how the flow is operated/monitored, common incidents, SLAs                       | Operations & support document, incidents list |
| **Infrastructure & DevOps Assessment**                               | 2.5h     | CEVA DevOps, Cloud/Infra team, PALO IT engineer | Evaluate current environments, CI/CD pipelines, SAST/DAST, tools                            | Infra & DevOps current state report           |
| **Security & Compliance Guidelines (incl. Data Sensitivity Review)** | 2h       | CEVA Security Officer, DevOps, PALO IT engineer | Define security guidelines for code (PII, PCI, encryption, scanning, vulnerabilities, GDPR) | Security & compliance guidelines document     |

# Day 4
| Workshop                                       | Duration | Participants                             | Objective                                                                                                                               | Deliverables                                                 |
| ---------------------------------------------- | -------- | ---------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------ |
| **ESQL Local Development & Testing Workshop**  | 3h       | CEVA Dev Leads, PALO IT engineer(s)      | Hands-on: install, run, and validate ESQL flows locally to replicate outputs for migration testing                                      | Local setup guide, validation checklist, test results        |
| **Testing & Quality Standards Workshop (NEW)** | 2.5h     | QA leads, Dev leads, PALO IT engineer(s) | Define testing strategy (manual vs automated, Karate, Jest), coding standards, linting rules, PR reviews, AI-assisted coding guidelines | Test strategy document, coding standards guide, PR checklist |




# Roles and Responsibilities (RACI)
## Team
- Senior Gen-e2 Engineer
- Senior AI Coach
 
## Definitions
R = Responsible → la(s) persona(s) que ejecutan la tarea. Hacen el trabajo.
A = Accountable → el dueño último de la tarea, quien responde por el resultado (solo puede haber uno).
C = Consulted → expertos o stakeholders que deben ser consultados antes/durante la ejecución. Su feedback es necesario.
I = Informed → personas que solo necesitan ser informadas del progreso o resultado, pero no participan activamente.

## Matrix
| Activity                             | Engineer | AI Coach        |
| ------------------------------------ | -------- | --------------- |
| Code migration (ESQL → TS)           | **R**    | I               |
| CI/CD pipeline setup                 | **R**    | I               |
| Testing automation                   | **R**    | C               |
| Security guidelines implementation   | **R**    | C               |
| Agile ceremonies (daily/retro)       | I        | **R**           |
| AI tooling training (prompts, usage) | C        | **R**           |
| Business alignment workshops         | C        | **R**           |
| AI-augmented playbook                | I        | **R**           |
| Final showcase demo                  | **R**        | **R**  |
