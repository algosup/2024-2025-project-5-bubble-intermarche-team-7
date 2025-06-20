# 2024-2025 Project-5 Bubble Intermarché Team-7 — Management Artifacts

This document aims to centralize all the management artifact links and resources listed below:

- [Tasks & schedule](#tasks--schedule)
- [RACI Matrix](#raci-matrix)
- [Risks & Assumptions](#risks--assumptions)
- [Key Performance Indicators](#key-performance-indicators)
  - [Definition of our KPIs](#definition-of-our-kpis)
    - [Documents](#documents)
    - [Design](#design)
    - [Development](#development)
    - [Mood](#mood)
  - [Link to the project's KPIs](#link-to-the-projects-kpis)
- [Weekly reports](#weekly-reports)
- [Post Mortem Analysis](#post-mortem-analysis)
- [Addendum](#addendum)
  - [Differences Between Gantt Chart and Actual Schedule](#differences-between-gantt-chart-and-actual-schedule)

---

## Tasks & schedule

You can view the breakdown of all the tasks we've identified for the duration of the project, the Gantt chart, and the KPIs in the following Excel document:

[**Bubble Project Tasks, KPIs & Gantt Chart** (Excel)](Bubble_Project_Team7.xlsx)

All project deadlines, progress tracking, and completion rates are centralized in this file for easy client review and internal follow-up.

---

## RACI Matrix

The RACI matrix of this project is as follows considering the Project Charter:

| Name          | Project Manager | Program Manager | Technical Lead | Developer | QA/Test | Technical Writer |
|---------------|----------------|----------------|---------------|-----------|---------|-----------------|
| Project kick-off         | I | I | I | I | I | I |
| Project charter          | R | A | C | C | C | C |
| Schedule creation        | R | C | C | C | C | C |
| Functional specification | A | R | C |   | C |   |
| Technical specification  | A | C | R/A | I | C |   |
| Coding process           | A | I | R | R/A | C |   |
| Testing planification    | A |   | C | C | R/A | I |
| Usage instructions       | A | C | C | C | I | R/A |

Legend:

| Letter | Full name   | Description                                     |
| ------ | ----------- | ----------------------------------------------- |
| R      | Responsible | Executes the task or activity                   |
| A      | Accountant  | Ultimately answerable for the task's completion |
| C      | Consulted   | Provides input and/or advice on the task        |
| I      | Informed    | Kept updated on progress and decisions          |
| /      | /           | No interaction with this role for this task     |

---

## Risks & Assumptions

| ID  | Description                                                     | Consequence                                      | Impact   | Likelihood | Mitigation/Avoidance                                          |
|-----|-----------------------------------------------------------------|--------------------------------------------------|----------|------------|---------------------------------------------------------------|
| 1   | Bubble learning curve & new features                            | Delays and/or bugs                               | High     | Medium     | Plan extra time, collaborative troubleshooting                |
| 2   | Database/image import limits (Bubble plan)                      | Blocked features if trial runs out               | Medium   | High       | Activate trial close to submission date                       |
| 3   | Uneven workload near deadlines                                  | Burnout, loss of motivation                      | High     | Medium     | Weekly status updates, task sharing                           |
| 4   | Holidays and assignment overlaps                                | Reduced productivity                             | Medium   | High       | Adjust timeline, reschedule non-critical tasks                |
| 5   | Unexpected design or translation complexity                     | Extra design/translation work, missed deadline   | Medium   | Medium     | Freeze scope, distribute review tasks across team             |

---

## Key Performance Indicators

### Definition of our KPIs

#### Documents

The following KPIs are included in this section:

- **Functional specifications**
- **Technical specifications**
- **Test Plan**
- **User Manual**

The progress of these documents is measured using the following formula:

percentage = (current number of sections / total number of sections) x 100

Where:

- **current_number_of_sections**: The number of sections that are completely done.
- **total_number_of_sections**: The number of predefined sections in the document's outline, which may evolve.

#### Design

The KPIs in this section include:

- **Mock-ups**
- **User journey roadmap**

The percentage progress for these KPIs is calculated using this formula:

percentage = (current number of designed pages / total number of pages to design) x 100

#### Development

- **UI features**
- **Database**
- **Filtering, tags, product pages, search, onboarding, etc.**

Progress is calculated by:

percentage = (current number of fully coded pages + sum percentages unfinished pages) / total designed pages x 100

## Weekly reports

Weekly reports can be found in [Management/weekly_reports](Documents/Management/weekly_reports) and summarize all progress and challenges for each week.

- [Access Report for Week 1](weekly_reports/week1_report.md)
- [Access Report for Week 2](weekly_reports/week2_report.md)
- [Access Report for Week 3](weekly_reports/week3_report.md)
- [Access Report for Week 4](weekly_reports/week4_report.md)
- [Access Report for Week 5](weekly_reports/week5_report.md)
- [Access Report for Week 6](weekly_reports/week6_report.md)
- [Access Report for Week 7](weekly_reports/week7_report.md)
- [Access Report for Week 8](weekly_reports/week8_report.md)
- [Access Report for Week 9](weekly_reports/week9_report.md)
- [Access Cumulative report (Weeks 1–9)](weekly_reports/cumulative_report.md)

## Post Mortem Analysis

A complete retrospective will be produced after final delivery and stored in `/documents/Management/PostMortem.md`.

---

## Addendum

### Differences Between Gantt Chart and Actual Schedule

The project schedule deviated from the original Gantt Chart in several ways:

- Unexpected delays were caused by holidays, Bubble technical limitations (CSV import/paywall), and learning curve.
- Some features (translations, full database import, and image optimization) took longer and had to be completed in focused work bursts near the deadline.
- Most management and tracking (tasks, KPIs, Gantt) were centralized in one Excel file, making progress and bottlenecks easy to spot.
- Future projects should better anticipate tool limits, plan for more design/translation review time, and distribute workloads evenly.

**Despite challenges, the team delivered a fully functional product on time and gained valuable skills in Bubble app development, collaboration, and time management.**
