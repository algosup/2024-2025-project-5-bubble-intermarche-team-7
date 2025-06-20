# 2025 Project Intermarché Wine & Cheese Recommendation App - Project Charter

## Project Definition

This project aims to develop an intuitive, fast, and effective suggestion application to enhance customer experience at Intermarché Saint-Rémy-de-Provence by recommending ideal wine and cheese combinations.

The client is Intermarché Saint-Rémy-de-Provence, represented by Célia ([moustier09@hotmail.fr](mailto:moustier09@hotmail.fr)).

## Scope

The application will be developed using Bubble, with a focus on delivering a front-end that is intuitive, multilingual (French, English, optionally Spanish), and capable of operating offline. It will integrate product information (references, images, descriptions) sourced from Intermarché's e-commerce site or data exports. It must include a minimalistic user registration process, personalized recommendations based on customer preferences, and internal positioning of products within the store.

## Stakeholders

| Role               | Representative                                                     | Expectation                                                                        |
| ------------------ | ------------------------------------------------------------------ | ---------------------------------------------------------------------------------- |
| Client             | Célia (Intermarché Saint-Rémy-de-Provence)                         | Fast, intuitive, and effective solution increasing sales and customer satisfaction |
| School director    | Franck JEANNIN (ALGOSUP)                                           | Professional documentation, management skills demonstration                        |
| Apprentice Liaison | Chris ([chryscadeau13@gmail.com](mailto:chryscadeau13@gmail.com))   | Liaison with cheese and wine experts; coordinate questions among the eight teams   |

## Team Members and Responsibilities

| Name              | Role              | Responsibilities                                                                                                            | Performance Criteria                                                                   |
| ----------------- | ----------------- | --------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| Abderrazaq MAKRAN | Project Manager   | Team management (time, resources), workload distribution, stakeholder communication, risk anticipation and mitigation       | On-time delivery, efficient resource use, stakeholder satisfaction                     |
| Quentin CLEMENT   | Program Manager   | Functional specification, client validation, UX/UI design, user journey mapping                                             | Client-approved functional specs, intuitive UX                                        |
| Manech LAGUENS    | Technical Leader  | Technical specification, selection of no-code integrations, technical oversight                                            | Accurate, scalable tech spec delivered punctually                                      |
| Pierre GORIN      | Software Engineer | Application development in Bubble, workflow automation, bug fixes, documentation                                           | Stable, bug-free MVP with core features                                                |
| Evan URHING       | Quality Assurance | Test plan creation, manual testing, offline mode verification, validation of recommendation accuracy                        | Comprehensive test coverage, documented test results                                   |
| David C            | Technical Writer  | User manual creation, help content, release notes                                                                          | Clear, concise, user-friendly documentation                                            |

## Project Plan

On April 23rd, 2025, we held a kick-off meeting. The client, currently busy and on vacation until May 12th, will resume direct feedback thereafter. In the interim, communication will be coordinated via Chris, our apprentice liaison. To streamline inquiries across eight teams, we will consolidate questions and circulate them through lead project managers by email.

Given the tight 50-day schedule, we recommend a hybrid Agile-Waterfall approach: Agile sprints to gather iterative feedback and adjust features rapidly, combined with fixed waterfall milestones to ensure specification and testing deliverables are met predictably. Our goal is to deliver a simple, fully functional MVP without overengineering.

Tasks derived from the project brief and client meetings will be prioritized by impact and complexity, then assigned to team members. We will use GitHub Projects for task tracking; tools such as Jira or Trello can complement our workflow for visual boards and reporting as needed.

Team meetings will occur biweekly (every ten days) to review progress and tackle blockers, supplemented by asynchronous updates via email and shared documentation.

## Milestones

| Date       | Milestone                         |
| ---------- | --------------------------------- |
| 23/04/2025 | Kick-off meeting                  |
| 12/05/2025 | Client availability resumes       |
| 16/05/2025 | Functional Specification delivery |
| 28/05/2025 | Technical Specification delivery  |
| 06/06/2025 | Test Plan delivery                |
| 16/06/2025 | Code & User Manual delivery       |
| 20/06/2025 | Final Project Presentation        |

## Deliverables

- Deployment of the final Bubble application (MVP)
- Interactive mock-ups and prototypes
- Functional Specification document
- Technical Specification document
- Test Plan
- User Manual
- Weekly management planning reports
- 15-minute final presentation pitch

## Allocated Resources

- Budget: €0  
- Team: 6 members  
- Estimated effort: 16 half-days at 3.5 hours each (approx. 336 hours)

## Risks

| Type                          | Description                                                                                                                  | Likelihood | Impact | Mitigation Strategy                                               |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ---------- | ------ | ----------------------------------------------------------------- |
| New Requirements              | Client may request additional features outside initial scope, leading to scope creep and delays                             | Medium     | High   | Maintain strict change control process; assess impact before accepting |
| Requirement Misinterpretation | Ambiguity in requirements may cause rework if stakeholder expectations differ from delivered features                        | Medium     | High   | Frequent clarification meetings; documented sign-offs              |
| Technical Integration Issues  | Challenges in web-scraping product data from Intermarché’s e-commerce website and ensuring reliable offline functionality     | Medium     | Medium | Early development and testing of scraping scripts; implement robust local caching mechanisms |
