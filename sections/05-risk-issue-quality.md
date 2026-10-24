<!-- Owner: Malmika Sandagomi -->

# 7 Risk Management

## 7.1 Approach

Risk management follows the process in ISO 31000:2018 [@iso31000]: establish the context and risk criteria, assess risks (identify, analyse and evaluate them), treat them, and monitor and review them, with communication and recording throughout. Risks were identified through workshops with the project team and business system owners, a review of the assumptions and constraints in the charter, the system dependency analysis, and the risks reported in the cloud migration literature (Section 2), such as vendor lock-in and hidden dependencies between systems [@gholami2016; @oparamartins2016].

Two lessons from the literature shaped the approach. First, IT project overruns are not normally distributed. In a study of 1,471 IT projects the average cost overrun was 27%, but one project in six overran its budget by about 200% on average and its schedule by almost 70% [@flyvbjerg]. The plan therefore does not rely on average outcomes and holds an explicit contingency reserve and schedule reserve. Second, a risk with a low probability but a severe and irreversible impact – a data breach or a regulatory breach, for example – needs strong treatment even when its overall score is only moderate.

## 7.2 Risk Criteria

Probability and impact are each rated on a five-point scale (Table 15). The risk score is probability × impact, giving four rating bands: Low (1–4), Medium (5–9), High (10–16) and Extreme (20–25).

Table: Table 15. Probability and impact scales

| Rating | Probability | Impact (cost / schedule / other) |
|--------|--------------------------|--------------------------------------------------------------|
| 1 | Rare (10% or less) | Negligible: under AUD 20,000; under 1 day |
| 2 | Unlikely (11–25%) | Minor: AUD 20,000–50,000; up to 1 week |
| 3 | Possible (26–50%) | Moderate: AUD 50,000–150,000; 2–4 weeks |
| 4 | Likely (51–75%) | Major: AUD 150,000–400,000; 1–2 months; noticeable customer impact |
| 5 | Almost certain (over 75%) | Severe: over AUD 400,000; data loss; regulatory breach; serious reputational damage |

## 7.3 Risk Register

Table 16 lists the 16 risks identified. Each risk statement is made in cause, event, effect format to be able to address the cause.

Table: Table 16. Risk register

| ID | Risk | Category | P | I | Score | Rating | Owner |
|------|----------------------------------------------|-------------|---|---|--------|----------|--------------|
| R01 | Errors in data mapping or transfer cause data loss or corruption during migration, damaging customer records | Technical | 2 | 5 | 10 | High | Mei Ling Tan |
| R02 | A cutover takes longer than the weekend window, causing a customer-facing outage on Monday | Operational | 3 | 4 | 12 | High | Arjun Mehta |
| R03 | A security misconfiguration in AWS exposes customer data | Security | 2 | 5 | 10 | High | Thomas Walker |
| R04 | The cloud arrangement does not meet APRA CPS 234 or CPS 230 obligations, leading to regulatory action | Regulatory | 2 | 5 | 10 | High | Thomas Walker |
| R05 | Data is stored or processed outside Australia, breaching data residency requirements | Regulatory | 1 | 5 | 5 | Medium | Sarah Kim |
| R06 | Undocumented dependencies between legacy systems are found late, forcing redesign and rework | Technical | 4 | 4 | 16 | High | Sarah Kim |
| R07 | Refactoring the internet banking portal needs more effort than estimated, raising partner costs and squeezing Wave 3 testing | Schedule / cost | 3 | 4 | 12 | High | Sarah Kim |
| R08 | AWS running costs are higher than forecast because resources are oversized or left running | Financial | 3 | 3 | 9 | Medium | Arjun Mehta |
| R09 | IT staff lack AWS skills, slowing the work and weakening support after go-live | Resource | 3 | 3 | 9 | Medium | Ahmed Hassan |
| R10 | Heavy use of provider-specific services increases future switching costs (vendor lock-in) | Strategic | 2 | 2 | 4 | Low | Sarah Kim |
| R11 | A key team member leaves during the project, causing loss of knowledge and delays | Resource | 2 | 4 | 8 | Medium | Arjun Mehta |
| R12 | A legacy application cannot run on the target AWS platform as planned | Technical | 2 | 3 | 6 | Medium | Sarah Kim |
| R13 | System performance is worse after migration, frustrating users | Technical | 2 | 3 | 6 | Medium | Olivia Brown |
| R14 | Staff resist the new systems, reducing adoption and increasing support calls | Organisational | 3 | 2 | 6 | Medium | Ahmed Hassan |
| R15 | The partner consultancy or SaaS vendor misses a delivery date | External | 2 | 3 | 6 | Medium | Arjun Mehta |
| R16 | Wave 3 slips past the last cutover weekend before the change freeze, delaying decommissioning and closure | Schedule | 2 | 4 | 8 | Medium | Arjun Mehta |

## 7.4 Qualitative Analysis

Each risk is depicted on a probability–impact heat map in Figure 6. There are nine "Medium" risk and one "Low" risk, and six "High" risk. The greatest risk is R06, undocumented dependencies (score 16), which is typical when migrating legacy applications: point-to-point interfaces are not often documented over the course of several decades [@gholami2016]. The answer is to invest early in discovery (WBS 2.0), and test all interfaces in the various trial migrations.

The heat map also shows a cluster of risks in the Severe impact column (R01, R03, R04 and R05) with low probabilities. Their scores will not do them justice: if a data breach, data loss or regulatory breach happens to the bank, it's not something that can be undone and it could result in the loss of customers' trust. These risks are therefore treated as priorities equal to the High-rated risks, with avoidance or strong mitigation (Table 18), and are reviewed at every steering committee meeting.

![Figure 6. Risk heat map (probability × impact)](../figures/risk-heat-map.png)

## 7.5 Quantitative Analysis

**Expected monetary value (EMV).** EMV multiplies the probability of a risk by its cost impact [@schwalbe]. Table 17 provides the estimated EMV for the five risks where a reasonable estimate of the cost impact can be made. Their total, AUD 400,000, is the basis for the contingency reserve in the budget (Table 8). The contingency reserve is held by the sponsor and released through the change request process.

Table: Table 17. Expected monetary value of the top cost risks

| ID | Risk | Probability | Cost impact (AUD) | EMV (AUD) |
|------|---------------------------------------|-----------:|-----------:|----------:|
| R01 | Data loss or corruption (recovery, rework, remediation) | 20% | 500,000 | 100,000 |
| R02 | Cutover overrun (rollback, repeat cutover, customer compensation) | 30% | 200,000 | 60,000 |
| R06 | Undocumented dependencies (redesign and rework) | 55% | 180,000 | 99,000 |
| R07 | Internet banking refactor overrun (extra partner effort) | 35% | 300,000 | 105,000 |
| R08 | AWS cost overrun during the project | 30% | 120,000 | 36,000 |
| | **Total (contingency reserve)** | | | **400,000** |

**Three-point estimate for the refactor.** The internet banking refactor (6.2.1) is the largest and most uncertain activity. Using an optimistic estimate of 40 days, a most likely estimate of 50 days and a pessimistic estimate of 75 days, the PERT expected duration is (40 + 4 × 50 + 75) / 6 = 52.5 days, with a standard deviation of (75 − 40) / 6 ≈ 5.8 days. The activity has 18 days of float, so it can take up to 68 days without delaying Wave 3. That is about 2.7 standard deviations above the expected duration, which gives roughly a 99% chance that the refactor alone will not delay the go-live. When looking at the main schedule exposure in Wave 3, it is the testing chain on the critical path, not the build. This is the reason that the plan includes three spare cutover weekends for Wave 3 (Section 5.4).

## 7.6 Risk Responses

Table 18 outlines the response strategy (avoid, mitigate, transfer or accept), what will be done in advance to address the risk, the contingency plan if the risk materialises and the trigger that would trigger the contingency plan.

Table: Table 18. Risk response plan

| ID | Strategy | Response actions | Contingency plan | Trigger |
|------|------------|----------------------------------------|--------------------------------|--------------------------|
| R01 | Mitigate | Full backup before every cutover; at least one trial migration per wave; automated reconciliation of record counts and checksums | Roll back to the legacy system, which stays available until the stability period ends; restore from backup | Any reconciliation mismatch on a critical table |
| R02 | Mitigate | Time the cutover steps in trial runs; timed runbook with checkpoints; go/no-go criteria | Roll back at the Sunday 2 pm decision point so the legacy system is ready for Monday | Cutover more than 2 hours behind the runbook |
| R03 | Mitigate | Landing zone guardrails; least-privilege access; automated configuration checks; penetration test before each go-live; independent audit (7.3.1) | Incident response plan: isolate resources, investigate, notify APRA within the required time if the incident is material [@apra234] | Critical alert from security monitoring or audit |
| R04 | Avoid | Early compliance assessment (7.1.1); regulator notification (7.2.1) before the first production workload; compliance lead on the Change Control Board | Pause the affected wave and agree a remediation plan | Compliance gap identified or regulator query received |
| R05 | Avoid | Guardrails that block AWS regions outside Australia; contract clause on data location with the SaaS vendor | Remove the data and report the incident | Monitoring alert for a resource in a non-approved region |
| R06 | Mitigate | Automated discovery plus interviews (2.1.1–2.2.1); dependency map signed off by system owners; interface tests in every trial migration | Move the affected system to a later wave; use contingency | An interface fails in a trial migration |
| R07 | Mitigate and transfer | Partner contract with fixed-price milestones; fortnightly demonstrations; scope locked at design sign-off; 18 days of float | Reduce scope: refactor the critical customer journeys and replatform the rest | Partner delivers under 80% of planned work for two fortnights |
| R08 | Mitigate | AWS budgets and cost alerts; resource tagging; right-sizing after hypercare | Cost optimisation review; use contingency | Monthly cost above 110% of forecast |
| R09 | Mitigate | AWS training for IT operations staff; pairing with partner engineers; knowledge transfer during hypercare | Extend partner support after go-live | Skills gaps found in the training needs analysis (8.1.1) |
| R10 | Accept | Prefer portable technologies (for example, standard databases) where practical; keep a documented exit plan [@oparamartins2016] | Use the exit plan if commercial terms change | Major change to AWS pricing or terms |
| R11 | Mitigate | Documentation standards; a named backup for every key role; partner bench resources | Partner backfills the role | Resignation or long absence |
| R12 | Mitigate | Proof of concept for each system during discovery; choose replatform or repurchase where needed | Keep the system on-premises temporarily and move it to a later wave | Proof of concept fails |
| R13 | Mitigate | Measure performance before migration; performance and load testing in Waves 2 and 3 | Scale up resources; tune the application | Response time more than 10% worse than the baseline |
| R14 | Mitigate | Change impact assessment; change champions in each business unit; training before each go-live | Extra floor support during hypercare | Low training attendance or a spike in help-desk calls |
| R15 | Transfer | Contracts with milestone payments and penalties; weekly vendor meetings | Escalate to vendor management; partner provides substitute resources | Vendor milestone missed |
| R16 | Mitigate | Three spare cutover weekends; weekly critical path tracking | Cut over on 14–16 January 2028; closure moves to early March 2028, before the hardware deadline | Wave 3 UAT not complete by 2 December 2027 |

## 7.7 Risk Monitoring and Control

Each risk has a named owner who monitors its trigger. The project manager reviews the full register fortnightly with the risk owners, and the steering committee reviews the High and Severe-impact risks monthly. New risks can be raised by anyone through Jira and are assessed within one week. The project manager can release up to AUD 50,000 of contingency for a single risk; anything larger needs the sponsor's approval. Each wave's lessons-learned review (4.6.2, 5.6.3, 6.7.2) updates the probabilities and impacts so that the register reflects what the project has actually experienced.

# 8 Issue Management

## 8.1 Risks and Issues

## 8.2 Issue Process and Escalation

## 8.3 Issue Log

# 9 Quality Management

## 9.1 Quality Approach

## 9.2 Quality Standards and Metrics

## 9.3 Quality Assurance

## 9.4 Quality Control

## 9.5 Continuous Improvement
