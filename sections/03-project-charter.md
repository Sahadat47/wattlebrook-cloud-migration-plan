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

## 3.5 Success and Acceptance Criteria

## 3.6 Stakeholders, Roles and Responsibilities

## 3.7 Stakeholder Management Strategy

## 3.8 High-Level Risks and Dependencies

## 3.9 Budget Summary and Milestones

## 3.10 Approval
