# Legacy Systems Cloud Migration – Project Plan

ITSU2006 IT Project Management – Assessment 3 (group project plan report).
Topic: Migration of Legacy Systems to a Cloud Infrastructure in a Financial Institution (fictional Wattlebrook Bank, AWS).

## Who does what

| Member | Files in `sections/` | Report sections |
|---|---|---|
| Dasula Bandara | `01-introduction.md`, `03-project-charter.md` | 1 Introduction, 3 Project Charter |
| Daham Warnakulasuriya | `04-wbs-schedule-resources.md` (and `gantt/project-schedule.xlsx`) | 4 WBS, 5 Schedule and Gantt Chart, 6 Resources and RASCI |
| Malmika Sandagomi | `02-literature-review.md`, `05-risk-issue-quality.md` | 2 Literature Review, 7 Risk, 8 Issues, 9 Quality |
| Md Sahadat Hossain Shikdar | `06-change-config-communication.md`, `07-conclusion.md`, `10-appendix-b-evidence.md` | 10–13 Change, GitHub, Communication, Jira; 14 Conclusion; Appendix B |

Everyone uses the shared facts in `sections/00-project-brief.md` (dates, budget, names). If a fact changes, change it there first and tell the group.

## How we work

1. Pick up your task on the Jira board and move it to **In Progress**.
2. Edit your section file on a branch named `section/<topic>`, for example `section/risk-register`.
3. Commit in small steps. Start each message with the section number, for example "Section 7: add EMV analysis for top five risks".
4. Open a pull request and move the Jira task to **In Review**.
5. Another member reviews and approves it. Nobody merges their own pull request.
6. Merge, and move the Jira task to **Done**.

Change requests to the plan use the **Change request** Issue template (see Section 10 of the report).

## Folder contents

| Path | What it is |
|---|---|
| `sections/` | The project brief and the report sections, in report order (`00-` to `10-`) |
| `references/` | Reference list (`refs-official.json`, `refs-papers.json`) and the IEEE citation style |
| `figures/` | Gantt charts and diagrams used in the report |
| `gantt/` | Schedule (Gantt chart) workbook in Excel |
| `screenshots/` | Jira and GitHub screenshots for Appendix B (file names listed in its README) |
| `.github/` | Change request Issue template and pull request template |
| `CHANGELOG.md` | One entry per version (v0.1, v0.5, v0.9, v1.0) |

## Citing sources

Cite in the text with the source's id in square brackets, e.g. `[@apra234]` or `[@aws7rs; @gartner5rs]`. In the final report they become IEEE numbers [1], [2] …, and the reference list is made from the files in `references/`. To add a new source, copy an entry in a refs file and change its fields.
