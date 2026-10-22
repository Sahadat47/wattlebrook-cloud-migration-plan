# Project Brief – shared facts (whole group)

Every section must use these facts. If something needs to change, change it here first and tell the group.

## Key facts

| Item | Value |
|---|---|
| Project name | Legacy Systems Cloud Migration Project |
| Organisation | Wattlebrook Bank – a fictional, customer-owned Australian bank headquartered in Melbourne |
| Size | About 1,200 staff and 400,000 customers |
| Project sponsor | Chief Information Officer (CIO) |
| Cloud provider | Amazon Web Services (AWS) |
| Cloud regions | AWS Asia Pacific (Sydney) as the main region; AWS Asia Pacific (Melbourne) for disaster recovery – all data stays in Australia |
| Duration | 12 months: Monday 1 February 2027 to Friday 28 January 2028 |
| Budget | AUD 4.5 million (AUD 4.1M planned costs + AUD 0.4M contingency reserve, about 10%) |
| Approach | Phased migration in 3 waves – least critical systems first, customer-facing systems last |

## Why the bank is doing this

- Data centre hardware is reaching end of support – the support contract ends on 31 March 2028.
- High maintenance costs, and it can't scale for peak periods such as end of month.
- Weak disaster recovery and resilience, which regulators (APRA) expect banks to manage.
- Slow to deliver new digital services.

## Systems in scope

| Wave | System | Migration strategy ("7 Rs") |
|---|---|---|
| 1 | HR and payroll | Repurchase – move to a SaaS product |
| 1 | Internal document management | Rehost – lift-and-shift |
| 2 | Customer CRM | Replatform |
| 2 | Data warehouse and reporting | Replatform |
| 2 | Old reporting server | Retire – replaced by the new data warehouse |
| 3 | Loan origination system | Replatform |
| 3 | Internet banking portal | Refactor – redesign for the cloud |

## Out of scope

- Core banking ledger – stays on-premises (Retain); a separate future project.
- ATM network and branch hardware.
- New features – systems move as they are, except changes needed to run in the cloud.

## Budget breakdown

| Category | AUD |
|---|---|
| Internal staff (project team labour) | 1,900,000 |
| AWS partner consultants and contractors | 1,000,000 |
| AWS cloud running costs during the project (incl. running old and new in parallel) | 500,000 |
| Software licences and migration tools (incl. SaaS payroll) | 350,000 |
| Training and change management | 200,000 |
| Testing and external security audit (penetration testing) | 150,000 |
| **Planned costs** | **4,100,000** |
| Contingency reserve (justified by Malmika's EMV analysis) | 400,000 |
| **Total budget** | **4,500,000** |

## Governance

- **Steering committee:** CEO, CIO (chair), Chief Financial Officer, Chief Risk Officer. Meets monthly; final escalation point.
- **Change Control Board (CCB):** CIO, project manager, cloud architect, security and compliance lead.

## Project team (fictional bank staff – not the four of us)

Used in the charter, Gantt chart and RASCI.

| Role | Name |
|---|---|
| Project Sponsor (CIO) | Helen Fraser |
| Project Manager | Arjun Mehta |
| Cloud Architect | Sarah Kim |
| Security and Compliance Lead | Thomas Walker |
| Data Migration Specialist | Mei Ling Tan |
| Network Engineer | Lucas Silva |
| Test Lead | Olivia Brown |
| Change and Training Manager | Ahmed Hassan |
| Cloud vendor | AWS account team, supported by an AWS partner consultancy |
| Business system owners | Heads of HR, Lending, Digital Banking and Finance – accept their systems and supply UAT testers |

## Key milestones

Taken from the schedule in `gantt/project-schedule.xlsx`.

| ID | Milestone | Date |
|---|---|---|
| M1 | Project charter approved | Fri 19 Feb 2027 |
| M2 | AWS landing zone ready | Wed 19 May 2027 |
| M3 | Wave 1 live (cutover weekend 17–18 Jul) | Fri 16 Jul 2027 |
| M4 | Wave 2 live (cutover weekend 18–19 Sep) | Fri 17 Sep 2027 |
| M5 | Wave 3 live (cutover weekend 20–21 Nov) | Fri 19 Nov 2027 |
| M6 | Old servers decommissioned, project closed | Fri 28 Jan 2028 |

## Scheduling rules

- 250 working days, Monday to Friday, excluding Victorian public holidays.
- Cutovers happen over weekends: go/no-go decision on Friday, cutover Friday night to Sunday, live on Monday.
- HR and payroll move after end-of-financial-year processing (30 June), so year-end payroll isn't split across two systems.
- Each wave's lessons learned must be finished before the next wave's trial migration starts.
- Change freeze from Mon 13 Dec 2027 to Fri 7 Jan 2028 – no changes to live systems over the holidays.
- Old servers are switched off only after at least 30 days of stable running and after the freeze, so decommissioning happens in January 2028.
- Wave 3 has three spare cutover weekends (26 Nov, 3 Dec, 10 Dec) before the freeze. If all are missed, the next window is 14–16 Jan 2028 and closure moves to early March 2028 – still before the data centre hardware support contract ends on 31 March 2028.
