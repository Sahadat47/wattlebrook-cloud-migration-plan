<!-- Owner: Daham Warnakulasuriya. Matches the schedule in gantt/project-schedule.xlsx. -->

# Appendix A: Detailed Schedule

Durations are in working days (Monday to Friday, excluding Victorian public holidays). All dependencies are finish-to-start. Tasks with zero total float are on the critical path and are shown in bold.

| WBS | Task | Days | Start | Finish | Predecessors | Responsible | Float |
|------|--------------------------|------|----------|----------|------------|-----------|-----|
| **1.0** | **Project management** | | **01 Feb 2027** | **28 Jan 2028** | | | |
| 1.1.1 | **Develop project charter** | 10 | 01 Feb 2027 | 12 Feb 2027 | — | Arjun Mehta | 0 |
| 1.1.2 | **Charter review and sponsor sign-off** | 5 | 15 Feb 2027 | 19 Feb 2027 | 1.1.1 | Helen Fraser | 0 |
| M1 | **Project charter approved** | 0 | 19 Feb 2027 | 19 Feb 2027 | 1.1.2 | Helen Fraser | 0 |
| 1.2.1 | Project management plan and baselines | 15 | 22 Feb 2027 | 15 Mar 2027 | M1 | Arjun Mehta | 45 |
| 1.3.1 | Risk, quality and communication plans | 10 | 22 Feb 2027 | 05 Mar 2027 | M1 | Arjun Mehta | 50 |
| 1.4.1 | Monitoring, control and reporting | Ongoing | 22 Feb 2027 | 28 Jan 2028 | — | Arjun Mehta | — |
| **2.0** | **Discovery and assessment** | | **22 Feb 2027** | **07 Apr 2027** | | | |
| 2.1.1 | **Application and infrastructure inventory** | 10 | 22 Feb 2027 | 05 Mar 2027 | M1 | Mei Ling Tan | 0 |
| 2.2.1 | **Map dependencies between systems** | 10 | 09 Mar 2027 | 22 Mar 2027 | 2.1.1 | Sarah Kim | 0 |
| 2.3.1 | **Select 7R strategies and wave plan** | 5 | 23 Mar 2027 | 31 Mar 2027 | 2.2.1 | Sarah Kim | 0 |
| 2.4.1 | Validate business case and budget | 5 | 01 Apr 2027 | 07 Apr 2027 | 2.3.1 | Arjun Mehta | 30 |
| **3.0** | **Cloud foundation (AWS landing zone)** | | **01 Apr 2027** | **19 May 2027** | | | |
| 3.1.1 | **Design AWS landing zone** | 10 | 01 Apr 2027 | 14 Apr 2027 | 2.3.1 | Sarah Kim | 0 |
| 3.2.1 | Network connectivity to AWS | 15 | 15 Apr 2027 | 05 May 2027 | 3.1.1 | Lucas Silva | 5 |
| 3.3.1 | **Identity and access management** | 10 | 15 Apr 2027 | 28 Apr 2027 | 3.1.1 | Thomas Walker | 0 |
| 3.4.1 | **Security controls, logging, monitoring** | 10 | 29 Apr 2027 | 12 May 2027 | 3.3.1 | Thomas Walker | 0 |
| 3.5.1 | **Landing zone review and sign-off** | 5 | 13 May 2027 | 19 May 2027 | 3.2.1, 3.4.1 | Thomas Walker | 0 |
| M2 | **AWS landing zone ready** | 0 | 19 May 2027 | 19 May 2027 | 3.5.1 | Sarah Kim | 0 |
| **4.0** | **Migration Wave 1** | | **20 May 2027** | **03 Aug 2027** | | | |
| 4.1.1 | **Wave 1 migration design** | 5 | 20 May 2027 | 26 May 2027 | M2, 1.2.1, 1.3.1, 2.4.1 | Sarah Kim | 0 |
| 4.2.1 | **Configure SaaS payroll and rehost DMS** | 15 | 27 May 2027 | 17 Jun 2027 | 4.1.1 | AWS partner team | 0 |
| 4.3.1 | **Wave 1 data migration trial** | 5 | 18 Jun 2027 | 24 Jun 2027 | 4.2.1 | Mei Ling Tan | 0 |
| 4.4.1 | **Wave 1 functional/integration testing** | 10 | 25 Jun 2027 | 08 Jul 2027 | 4.3.1 | Olivia Brown | 0 |
| 4.4.2 | Wave 1 security testing | 5 | 18 Jun 2027 | 24 Jun 2027 | 4.2.1 | Thomas Walker | 10 |
| 4.4.3 | **Wave 1 user acceptance testing** | 5 | 09 Jul 2027 | 15 Jul 2027 | 4.4.1, 4.4.2 | Olivia Brown | 0 |
| 4.5.1 | **Wave 1 go/no-go and cutover** | 1 | 16 Jul 2027 | 16 Jul 2027 | 4.4.3, 8.3.1, 7.2.1 | Arjun Mehta | 0 |
| M3 | **Wave 1 live** | 0 | 16 Jul 2027 | 16 Jul 2027 | 4.5.1 | Arjun Mehta | 0 |
| 4.6.1 | **Wave 1 hypercare support** | 10 | 19 Jul 2027 | 30 Jul 2027 | M3 | Sarah Kim | 0 |
| 4.6.2 | **Wave 1 lessons learned** | 2 | 02 Aug 2027 | 03 Aug 2027 | 4.6.1 | Arjun Mehta | 0 |
| **5.0** | **Migration Wave 2** | | **27 May 2027** | **11 Oct 2027** | | | |
| 5.1.1 | Wave 2 migration design | 10 | 27 May 2027 | 09 Jun 2027 | 4.1.1 | Sarah Kim | 18 |
| 5.2.1 | Build CRM and data warehouse on AWS | 20 | 10 Jun 2027 | 08 Jul 2027 | 5.1.1 | AWS partner team | 18 |
| 5.3.1 | **Wave 2 data migration trials** | 10 | 04 Aug 2027 | 17 Aug 2027 | 5.2.1, 4.6.2 | Mei Ling Tan | 0 |
| 5.4.1 | **Wave 2 functional/integration testing** | 15 | 18 Aug 2027 | 07 Sep 2027 | 5.3.1 | Olivia Brown | 0 |
| 5.4.2 | Wave 2 security testing | 5 | 09 Jul 2027 | 15 Jul 2027 | 5.2.1 | Thomas Walker | 38 |
| 5.4.3 | Wave 2 performance testing | 5 | 18 Aug 2027 | 24 Aug 2027 | 5.3.1 | Olivia Brown | 10 |
| 5.4.4 | **Wave 2 user acceptance testing** | 7 | 08 Sep 2027 | 16 Sep 2027 | 5.4.1, 5.4.2, 5.4.3 | Olivia Brown | 0 |
| 5.5.1 | **Wave 2 go/no-go and cutover** | 1 | 17 Sep 2027 | 17 Sep 2027 | 5.4.4, 8.3.2 | Arjun Mehta | 0 |
| M4 | **Wave 2 live** | 0 | 17 Sep 2027 | 17 Sep 2027 | 5.5.1 | Arjun Mehta | 0 |
| 5.6.1 | **Wave 2 hypercare support** | 10 | 20 Sep 2027 | 04 Oct 2027 | M4 | Sarah Kim | 0 |
| 5.6.2 | Retire old reporting server | 5 | 05 Oct 2027 | 11 Oct 2027 | 5.6.1 | Lucas Silva | 65 |
| 5.6.3 | **Wave 2 lessons learned** | 2 | 05 Oct 2027 | 06 Oct 2027 | 5.6.1 | Arjun Mehta | 0 |
| **6.0** | **Migration Wave 3** | | **10 Jun 2027** | **07 Dec 2027** | | | |
| 6.1.1 | Wave 3 migration design | 15 | 10 Jun 2027 | 01 Jul 2027 | 5.1.1 | Sarah Kim | 18 |
| 6.2.1 | Refactor internet banking portal | 50 | 02 Jul 2027 | 09 Sep 2027 | 6.1.1 | AWS partner team | 18 |
| 6.3.1 | Replatform loan origination system | 25 | 02 Jul 2027 | 05 Aug 2027 | 6.1.1 | AWS partner team | 43 |
| 6.4.1 | **Wave 3 data migration trials** | 10 | 07 Oct 2027 | 20 Oct 2027 | 6.2.1, 6.3.1, 5.6.3 | Mei Ling Tan | 0 |
| 6.5.1 | **Wave 3 functional/integration testing** | 15 | 21 Oct 2027 | 11 Nov 2027 | 6.4.1 | Olivia Brown | 0 |
| 6.5.2 | Wave 3 security and penetration testing | 10 | 10 Sep 2027 | 23 Sep 2027 | 6.2.1, 6.3.1 | Thomas Walker | 33 |
| 6.5.3 | Wave 3 performance and load testing | 5 | 21 Oct 2027 | 27 Oct 2027 | 6.4.1 | Olivia Brown | 10 |
| 6.5.4 | **Wave 3 user acceptance testing** | 5 | 12 Nov 2027 | 18 Nov 2027 | 6.5.1, 6.5.2, 6.5.3 | Olivia Brown | 0 |
| 6.6.1 | **Wave 3 go/no-go and cutover** | 1 | 19 Nov 2027 | 19 Nov 2027 | 6.5.4, 8.3.3, 8.4.1, 7.3.1 | Arjun Mehta | 0 |
| M5 | **Wave 3 live** | 0 | 19 Nov 2027 | 19 Nov 2027 | 6.6.1 | Arjun Mehta | 0 |
| 6.7.1 | Wave 3 hypercare support | 10 | 22 Nov 2027 | 03 Dec 2027 | M5 | Sarah Kim | 20 |
| 6.7.2 | Wave 3 lessons learned | 2 | 06 Dec 2027 | 07 Dec 2027 | 6.7.1 | Arjun Mehta | 20 |
| **7.0** | **Compliance and security assurance** | | **01 Apr 2027** | **24 Nov 2027** | | | |
| 7.1.1 | APRA compliance assessment | 10 | 01 Apr 2027 | 14 Apr 2027 | 2.3.1 | Thomas Walker | 60 |
| 7.2.1 | Regulator notification | 5 | 15 Apr 2027 | 21 Apr 2027 | 7.1.1 | Thomas Walker | 60 |
| 7.3.1 | Independent security audit | 10 | 19 Jul 2027 | 30 Jul 2027 | M3 | Thomas Walker | 77 |
| 7.4.1 | Final compliance sign-off | 3 | 22 Nov 2027 | 24 Nov 2027 | M5, 7.3.1 | Thomas Walker | 39 |
| **8.0** | **Training and change management** | | **01 Apr 2027** | **18 Nov 2027** | | | |
| 8.1.1 | Change impact and training needs | 10 | 01 Apr 2027 | 14 Apr 2027 | 2.3.1 | Ahmed Hassan | 45 |
| 8.2.1 | Develop training materials | 15 | 15 Apr 2027 | 05 May 2027 | 8.1.1 | Ahmed Hassan | 45 |
| 8.3.1 | **Wave 1 staff training** | 5 | 09 Jul 2027 | 15 Jul 2027 | 8.2.1, 4.4.1 | Ahmed Hassan | 0 |
| 8.3.2 | Wave 2 staff training | 5 | 08 Sep 2027 | 14 Sep 2027 | 5.4.1 | Ahmed Hassan | 2 |
| 8.3.3 | **Wave 3 staff training** | 5 | 12 Nov 2027 | 18 Nov 2027 | 6.5.1 | Ahmed Hassan | 0 |
| 8.4.1 | Customer communications (Wave 3) | 10 | 21 Oct 2027 | 04 Nov 2027 | 6.4.1 | Ahmed Hassan | 10 |
| **9.0** | **Decommission and closure** | | **22 Nov 2027** | **28 Jan 2028** | | | |
| 9.1.1 | **Stability period (to end of freeze)** | 32 | 22 Nov 2027 | 07 Jan 2028 | M5 | Sarah Kim | 0 |
| 9.2.1 | **Archive legacy data** | 5 | 10 Jan 2028 | 14 Jan 2028 | 9.1.1, 6.7.2 | Mei Ling Tan | 0 |
| 9.3.1 | **Decommission on-premises servers** | 5 | 17 Jan 2028 | 21 Jan 2028 | 9.2.1, 5.6.2 | Lucas Silva | 0 |
| 9.4.1 | **Final project report** | 3 | 24 Jan 2028 | 27 Jan 2028 | 9.3.1, 7.4.1 | Arjun Mehta | 0 |
| 9.5.1 | **Closure and sponsor sign-off** | 1 | 28 Jan 2028 | 28 Jan 2028 | 9.4.1 | Helen Fraser | 0 |
| M6 | **Project closed** | 0 | 28 Jan 2028 | 28 Jan 2028 | 9.5.1 | Helen Fraser | 0 |
