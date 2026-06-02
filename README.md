# 🧪 PTTC Insight Lab Case Study

## 📌 Overview

PTTC Insight Lab is a product case study for an AI-assisted needs assessment and reporting workflow designed to help prevention organizations move from stakeholder input to structured insights.

The concept combines guided survey creation, AI-assisted analysis, and branded report generation into a single streamlined experience.

This repository documents the product strategy, requirements, acceptance criteria, and key design decisions behind the MVP.

This repository is a public portfolio case study and does not include private client data, credentials, production secrets, or proprietary records.

## 🧩 Problem

Prevention organizations frequently need to collect stakeholder feedback through surveys and needs assessments, then transform that information into reports that support planning, funding, and decision-making.

Today, that process is often fragmented across multiple tools and manual steps:

• Creating survey questions
• Collecting responses
• Exporting raw data
• Analyzing results
• Writing executive summaries
• Creating stakeholder reports

The result is a time-consuming workflow that can delay insights and create inconsistencies across programs.

## 💡 Why This Matters

A streamlined insight workflow allows prevention teams to spend less time formatting reports and more time understanding community needs.

By combining survey generation, AI-assisted analysis, and report creation into a single experience, organizations can move from raw feedback to actionable insights more efficiently while maintaining clear reporting standards.

## 🚀 Product Goals

The MVP was designed to:

• Generate needs-assessment surveys through a guided chat-style intake
• Allow users to upload survey results for analysis
• Produce executive summaries and key findings automatically
• Generate branded stakeholder-ready reports
• Support optional visualizations and charts
• Minimize infrastructure and operational costs
• Reduce the number of manual steps required to move from survey creation to reporting

## 🛠️ MVP Scope

The MVP focuses on two primary workflows:

### Survey Mode

Users complete a guided intake that generates:

• Survey questions
• Needs-assessment content
• Structured survey outputs

### Analyze Mode

Users upload survey data and receive:

• Executive summary
• Key findings
• Themes and observations
• Optional charts
• Branded PDF report export

The MVP intentionally avoids complex databases, heavy backend infrastructure, and long-term storage requirements in order to validate the workflow quickly and cost-effectively.


## 💡 Why This Matters

Accurate survey interpretation supports stronger program planning, clearer reporting, and better stakeholder communication. A workflow that separates participant counts from response-category row counts helps prevent misleading summaries and improves confidence in exported reports.

## 👥 Users

- Prevention program staff preparing survey summaries
- Evaluation and reporting teams reviewing participant feedback
- Program leaders using insights to guide planning decisions
- Stakeholders who need clear, defensible report outputs

## 🎯 My Role

I defined the product structure, MVP workflow, documentation scope, participant-count logic requirements, report export expectations, and public-safe case study boundaries.

## 🚀 Product Goals

- Guide users through survey setup and results interpretation
- Validate aggregate CSV exports before analysis
- Distinguish participants represented from response-category rows
- Support AI-assisted drafting of themes, gaps, and recommendations
- Produce clear report-ready outputs for prevention program insights

## 🛠️ MVP Scope

- Guided survey creation flow
- Survey results upload and CSV parsing requirements
- Participant-count detection and validation rules
- AI-assisted analysis summary requirements
- Themes, gaps, and recommendation outputs
- DOCX/report export requirements
- Public-safe documentation boundaries

## 📊 Product Logic Diagrams

Diagram assets to be added.

## 🔮 Future Scope

- Expanded export format support
- Additional validation patterns for varied survey tools
- Reviewer notes and approval workflow concepts
- More detailed reporting templates by program type
- Accessibility and plain-language review guidance

## 🧠 Key Product Decisions

- Treat participant count as a validated metric, not a raw CSV row count.
- Use “Participants Represented” when the participant base is known.
- Require ambiguity handling before aggregate exports are considered valid.
- Keep this repository documentation-only for public portfolio review.
- Exclude client data, credentials, production secrets, proprietary records, and runtime setup instructions.

## 📁 Repository Contents

```text
README.md
docs/
  requirements.md
  acceptance-criteria.md
```

> Planned diagram assets: `workflow-diagram.png` and `architecture-diagram.png`. Diagram PNGs are not included until finalized.

## ✅ Outcome

This case study documents a focused product concept for improving survey analysis quality, reducing participant-count confusion, and clarifying report export expectations for prevention program teams.

## 🔁 Future Iterations

Future iterations may expand the requirements, add finalized diagram assets, document additional CSV validation scenarios, and refine report language patterns for different prevention program audiences.

## 🧰 Skills Demonstrated

- Product requirements documentation
- MVP scoping and workflow definition
- Data interpretation safeguards
- Acceptance criteria writing
- AI-assisted reporting product strategy
- Public-safe case study documentation
