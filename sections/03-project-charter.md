<!-- Owner: Dasula Bandara -->

# 3 Project Charter

The project charter serves as a formal approval to start the project, identifies the sponsor or key stakeholder and project manager, and defines the objectives, scope, and constraints agreed upon before detailed project planning is started [@schwalbe]. Table 2 summarises the key facts of the charter.

Table: Table 2. Project summary

| Item | Detail |
|-----------------|---------------------------------------------------------------|
| Project title | Legacy Systems Cloud Migration Project |
| Organisation | Wattlebrook Bank, Melbourne |
| Project sponsor | Helen Fraser, Chief Information Officer (CIO) |
| Project manager | Arjun Mehta |
| Duration | 1 February 2027 to 28 January 2028 (250 working days) |
| Budget | AUD 4.5 million (AUD 4.1 million planned costs and AUD 0.4 million contingency reserve) |
| Cloud provider | AWS – Asia Pacific (Sydney) as the main region; Asia Pacific (Melbourne) for disaster recovery |
| Approach | Three migration waves, from least critical to most critical systems |

## 3.1 Project Background

Wattlebrook Bank's core business systems are managed from one data centre, located in their head office in Melbourne. The most recent refresh of the hardware was in 2020 and the support contract for the hardware will run to 31 March 2028. Replacing it with a like-for-like replacement is estimated at AUD 3.2 million and would lock the bank into another 5 year hardware cycle. In the present context, there are also three structural weaknesses. Firstly, it can't scale - the web banking portal gets slower and slower every month when it's time to process the month-end and calculate the interest. Second, disaster recovery involves backups and a small secondary server room, with the restoration of critical services taking days, not hours. Third, every new digital service needs new hardware to be ordered and installed, which slows the bank's response to competitors.

In 2026 the Board approved a cloud-first strategy and asked the CIO to move suitable systems to a public cloud before the hardware support contract ends. AWS was selected because it offers two Australian regions, which allows a disaster recovery design that keeps all data in Australia, and because of its migration guidance and partner network for financial services [@aws7rs]. The core banking ledger is excluded from this project because of its complexity and will be considered in a separate future project.

## 3.2 Business Objectives

Table: Table 3. Business objectives

| ID | Business objective |
|--------|---------------------------------------------------------------------------|
| BO1 | Avoid the AUD 3.2 million hardware refresh and reduce infrastructure running and maintenance costs by 20% within two years of project closure, compared with the 2026 baseline. |
| BO2 | Improve resilience so that critical services can be restored within 4 hours with no more than 15 minutes of data loss, supporting the bank's operational resilience obligations [@apra230]. |
| BO3 | Scale capacity on demand for peak periods such as month end. |
| BO4 | Shorten the time needed to deliver new digital services by removing hardware lead times. |

## 3.3 Project Objectives

The project objectives are specific, measurable, achievable, relevant and time-bound (SMART), and each one contributes to at least one business objective.

Table: Table 4. SMART project objectives

| ID | Objective | Measure | Target date |
|-------|-----------------------------------|-----------------------------------|-------------|
| PO1 | Migrate the six in-scope systems to AWS Australian regions using the strategy selected for each system | All six systems live on AWS; old reporting server retired | 19 Nov 2027 |
| PO2 | Deliver the project within budget | Total spend at or below AUD 4.5 million; contingency use reported monthly | 28 Jan 2028 |
| PO3 | Protect data during migration | 100% of records reconciled; zero data-loss incidents | Each cutover |
| PO4 | Limit disruption to customers and staff | Planned downtime of no more than 4 hours per system, with all cutovers on weekends | Each cutover |
| PO5 | Meet regulatory obligations | Regulator notified before the first production workload moves; final compliance sign-off | 21 Apr 2027 and 24 Nov 2027 |
| PO6 | Exit the on-premises servers | In-scope servers switched off and legacy data archived | 21 Jan 2028 |

## 3.4 Scope Statement

**In scope.** The project migrates six systems and retires one, as shown in Table 5. The migration strategy for each system follows the AWS "7 Rs" [@aws7rs] and was chosen by balancing business value, technical condition and risk.

Table: Table 5. Systems in scope

| Wave | System | Strategy | Reason |
|--------|---------------------------|--------------|-----------------------------------------|
| 1 | HR and payroll | Repurchase | Move to a software-as-a-service (SaaS) payroll product; the current package is near end of life |
| 1 | Internal document management | Rehost | Low complexity; fastest path to AWS |
| 2 | Customer CRM | Replatform | Move to managed AWS database services to reduce maintenance |
| 2 | Data warehouse and reporting | Replatform | Gains elastic capacity for month-end reporting |
| 2 | Old reporting server | Retire | Replaced by the new data warehouse |
| 3 | Loan origination system | Replatform | Business-critical; moved after earlier waves prove the process |
| 3 | Internet banking portal | Refactor | Redesigned for the cloud so it can scale for customer peaks |

The project also includes building the AWS landing zone (accounts, network, identity and security controls), data migration and reconciliation, all testing, staff training, customer communications, compliance activities, and decommissioning the old servers.

**Out of scope.** The core banking ledger (retained on-premises), the ATM network and branch hardware, end-user devices, new features beyond the changes needed to run in the cloud, and changes to business processes.

**Deliverables.**

- Project charter and project management plan with approved scope, schedule and cost baselines
- System inventory, dependency map, migration strategy and wave plan
- Secure AWS landing zone with network connectivity, identity and access management, and logging
- Six systems running on AWS and one server retired, each with test reports and user acceptance sign-off
- APRA compliance assessment, regulator notification and final compliance sign-off
- Training materials, trained staff and customer communications
- Archived legacy data, decommissioned servers, and a final project report with lessons learned

**Assumptions.** The required AWS services are available in the Sydney and Melbourne regions; business units provide user acceptance testers when scheduled; the SaaS payroll vendor can store data in Australia; legacy data quality is good enough after cleansing; and no major regulatory change occurs during the project.

**Constraints.** There's a capped budget of AUD 4.5 million. The project must finish before the hardware support contract ends on 31 March 2028, and the planned finish is 28 January 2028. All data must stay in Australia. Cutovers may only happen on weekends and not during end-of-financial-year processing or the change freeze (13 December 2027 to 7 January 2028). The bank must continue to meet APRA prudential standards and the Privacy Act 1988 (Cth). Note that CPS 230 treats providers of core technology services as material service providers, so the arrangement with AWS will need to be included on the bank's register of material service providers, under a formal arrangement, with notification to APRA within the applicable time periods [@apra230].

## 3.5 Success and Acceptance Criteria

Table: Table 6. Success and acceptance criteria

| Area | Criterion | Accepted by |
|--------------|------------------------------------------------------|------------------------|
| Data integrity | 100% of records reconciled by count and checksum after every migration | Data Migration Specialist and business system owner |
| Availability | At least 99.9% availability for each migrated system in its first three months | CIO |
| Performance | Response times equal to or better than the pre-migration baseline under peak load | Test Lead |
| Security | No open critical or high security findings at go-live; independent audit passed | Security and Compliance Lead |
| User acceptance | All critical UAT test cases passed and signed off by the business system owner | Business system owners |
| Compliance | Final compliance sign-off with no adverse regulator findings | Chief Risk Officer |
| Time and cost | Project closed by 28 January 2028 within AUD 4.5 million | Steering committee |

Each wave is accepted at its go/no-go meeting against these criteria. The whole project is accepted when the sponsor signs the closure report (task 9.5.1). The 20% cost reduction in BO1 is a benefit that the sponsor will measure after the project closes.

## 3.6 Stakeholders, Roles and Responsibilities

Table 7 defines each stakeholder's role and responsibilities. Responsibilities for each deliverable are assigned in more detail in the responsibility matrix in Section 6.3.

Table: Table 7. Stakeholder roles and responsibilities

| Stakeholder | Role | Key responsibilities |
|-------------------------|------------------------|------------------------------------------------------------|
| Helen Fraser, CIO | Project sponsor | Owns the business case; approves the charter, baselines and major changes; chairs the Change Control Board; releases contingency funds; accepts the final product |
| Steering committee (CEO, CIO, CFO, Chief Risk Officer) | Governance | Meets monthly; decides on escalated risks, issues and changes; makes the Wave 3 go/no-go decision |
| Arjun Mehta | Project manager | Plans and controls scope, schedule, cost and quality; runs the risk, issue and change logs; reports status; leads the project team |
| Sarah Kim | Cloud architect | Designs the landing zone and target architecture; technical authority for migration designs; leads hypercare |
| Thomas Walker | Security and compliance lead | Security controls and testing; APRA compliance assessment and regulator notification; coordinates the independent audit |
| Mei Ling Tan | Data migration specialist | System inventory; data mapping, cleansing, trial migrations and reconciliation; data archiving |
| Lucas Silva | Network engineer | Network connectivity to AWS; cutover network changes; server decommissioning |
| Olivia Brown | Test lead | Test strategy; functional, performance and user acceptance testing; defect management |
| Ahmed Hassan | Change and training manager | Change impact assessment; staff training; staff and customer communications |
| AWS account team and partner consultancy | Vendor | Landing zone build support; replatforming and refactoring work under contract |
| Business system owners (HR, Lending, Digital Banking, Finance) | Business representatives | Supply requirements and UAT testers; accept their systems |
| APRA | External regulator | Receives required notifications; may review the bank's arrangements |
| Internal audit | Independent assurance | Reviews controls and project governance |
| Bank staff and customers | System users | Attend training; receive notices of changes and outages |

## 3.7 Stakeholder Management Strategy

Stakeholders were mapped by their power over the project and their interest in it (Figure 1). Each quadrant has its own engagement approach:

- **Manage closely** – the sponsor, the steering committee and AWS with its partner. They are involved in key decisions through fortnightly sponsor meetings, monthly steering committee reviews and weekly vendor meetings.
- **Keep satisfied** – APRA, the Board and internal audit. They receive formal briefings at key points and early notice of anything that affects compliance, so that there are no surprises.
- **Keep informed** – the project team, bank staff, customers and IT operations. They receive regular updates, training and advance notice of outages.
- **Monitor** – the media, the public and the payroll SaaS vendor. The project watches for concerns and has prepared statements ready for any customer-facing incident.

The communication activities for each group are detailed in the communication management plan (Section 12).

![Figure 1. Stakeholder power/interest grid](figures/stakeholder-grid.png){width=88%}

## 3.8 High-Level Risks and Dependencies

## 3.9 Budget Summary and Milestones

## 3.10 Approval
