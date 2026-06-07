# Insight Lab Survey Pipeline Case Study

## Overview

The Insight Lab Survey Pipeline is a product case study for a survey planning, CSV validation, insight drafting, human review, and report export workflow. It helps teams turn survey feedback into clearer insights and stakeholder-ready reporting through a consistent, reviewable process.

## Portfolio Note

This repository is a public portfolio case study and does not include raw survey data, participant-level details, private client materials, proprietary documentation, credentials, or production secrets.

## Problem

Survey reporting often happens across disconnected tools and manual steps. Teams may need to define survey goals, organize questions, interpret exported results, identify useful findings, and prepare reports without one consistent workflow.

This makes it easier to misread survey exports, confuse participant counts with response-category rows, or struggle to turn feedback into clear findings and recommendations.

## Product Goal

The product goal is to provide a repeatable workflow for survey setup, CSV validation, participant-count safeguards, insight drafting, human review, and report export.

## Users

- Program teams
- Evaluation and reporting staff
- Prevention and public health professionals
- Internal teams responsible for survey synthesis and recommendations
- Stakeholders reviewing survey findings

## My Role

- Product operations
- Workflow design
- Requirements definition
- Survey process mapping
- Data interpretation safeguards
- Documentation and implementation planning

## MVP Scope

- Guided survey setup
- CSV survey-result upload
- CSV structure validation
- Participant-count detection and labeling
- Insight drafting
- Human review
- Stakeholder-ready report export

## Product Logic

Survey context is captured first, including the survey purpose, audience, topic areas, and reporting goals. CSV results are then uploaded and validated before analysis begins.

The workflow distinguishes respondent-level records from aggregate response-category rows, separates participant count from CSV row count, and uses “Participants Represented” when the participant base is supported by validated data. It then prepares findings, themes, gaps, recommendations, and methodology notes for human review before export.

## Human-Guided Analysis Process

Automation or AI may support grouping, summarization, drafting, and recommendation development after survey results pass validation. Human review remains central to confirming participant-count language, interpreting findings, revising recommendations, and approving report content.

The workflow does not claim causal, predictive, or fully automated decision-making.

## Key Product Decisions

- Lead with workflow clarity before AI support
- Validate survey exports before drafting analysis
- Separate participant counts from CSV row counts
- Keep findings reviewable and traceable
- Require human review before report export
- Keep public documentation limited to product design and workflow logic

## Repository Contents

```text
README.md
docs/
  requirements.md
  acceptance-criteria.md
```

- [`docs/requirements.md`](docs/requirements.md) documents the MVP workflow, product requirements, constraints, and success criteria.
- [`docs/acceptance-criteria.md`](docs/acceptance-criteria.md) defines expected behavior for survey setup, CSV validation, participant-count handling, insight drafting, review, and report export.

## Outcome

This case study demonstrates how product operations and workflow design can create a more consistent path from survey feedback to reviewable insights, reporting outputs, and decision support.

## Future Iterations

- Add visual workflow diagrams
- Add sanitized example output formats
- Expand reusable reporting templates
- Create implementation checklists
- Develop reusable prompt or review guides for structured synthesis

## Skills Demonstrated

- Product Operations
- Workflow Design
- Requirements Definition
- Survey Operations
- Data Interpretation Safeguards
- Reporting Systems
- AI-Assisted Workflow Design
- Documentation
- Stakeholder-Centered Process Design
