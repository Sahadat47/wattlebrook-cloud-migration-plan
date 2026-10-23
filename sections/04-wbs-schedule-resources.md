<!-- Owner: Daham Warnakulasuriya -->

# 4 Work Breakdown Structure

The work breakdown structure (WBS) breaks the whole project scope into smaller, manageable pieces of work organised around deliverables [@schwalbe]. It follows the 100% rule: the WBS contains all of the work in the scope statement (Section 3.4) and nothing outside it. Figure 2 shows the first two levels. Level 1 has nine work packages: six management and enabling packages (1.0–3.0 and 7.0–9.0) and the three migration waves (4.0–6.0). Level 3, which forms the schedule, contains 60 activities and 6 milestones and is listed in full in Appendix A.

All three migration waves deliberately use the same structure – design, build, data migration, testing, cutover, then hypercare and lessons learned. This means the team repeats a proven pattern, estimates improve with each wave, and lessons learned can be applied directly to the matching step of the next wave.

![Figure 2. Work breakdown structure (levels 1 and 2)](../figures/wbs.png)

Table 11 is the WBS dictionary for level 1. It defines what each work package contains, what it delivers and who owns it.

Table: Table 11. WBS dictionary (level 1)

| WBS | Work package | Description | Main deliverable | Owner |
|-------|----------------|------------------------------------------|----------------------|----------------|
| 1.0 | Project management | Initiation, planning, monitoring and control across the whole project | Charter, project management plan, status reports | Arjun Mehta |
| 2.0 | Discovery and assessment | Inventory of applications and infrastructure, dependency mapping, 7R strategy selection, business case validation | Dependency map and wave plan | Sarah Kim |
| 3.0 | Cloud foundation | Design and build of the AWS landing zone: accounts, network, identity and access, security controls and logging | Signed-off landing zone | Sarah Kim |
| 4.0 | Migration Wave 1 | SaaS payroll and rehosted document management, from design to hypercare | Two systems live on AWS/SaaS | Sarah Kim |
| 5.0 | Migration Wave 2 | CRM and data warehouse replatformed; old reporting server retired | Two systems live; one retired | Sarah Kim |
| 6.0 | Migration Wave 3 | Loan origination replatformed and internet banking portal refactored | Two customer-critical systems live | Sarah Kim |
| 7.0 | Compliance and security assurance | APRA compliance assessment, regulator notification, independent audit and sign-off | Compliance sign-off | Thomas Walker |
| 8.0 | Training and change management | Change impact analysis, training materials, staff training per wave, customer communications | Trained staff; informed customers | Ahmed Hassan |
| 9.0 | Decommission and closure | Stability period, data archiving, server decommissioning, final report | Closed project | Arjun Mehta |

# 5 Project Schedule and Gantt Chart

## 5.1 Scheduling Approach

## 5.2 Milestones and Summary Schedule

## 5.3 Detailed Gantt Chart

## 5.4 Critical Path Analysis

## 5.5 Schedule Control

# 6 Resource Allocation and Responsibility Matrix

## 6.1 Resource Plan

## 6.2 Resource Levelling

## 6.3 Responsibility Matrix (RASCI)
