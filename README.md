# 🧪 PTTC Insight Lab Case Study

## Overview

PTTC Insight Lab is a portfolio-safe prototype implementation and product case study for an AI-assisted survey workflow. It explores how prevention training and technical assistance teams could move from survey design to aggregate results review, insight generation, and report export in a clearer, more repeatable way.

This public repository contains a portfolio-safe prototype implementation and case study documentation. It does not include private client data, credentials, production secrets, or proprietary records.

The prototype is intended to demonstrate product thinking, implementation approach, and documentation discipline for a public audience while accurately representing that the repository includes runnable application concepts such as:

- Next.js application screens for survey creation and analysis workflows
- OpenAI-backed API route patterns for assisted survey generation and analysis
- Survey results upload and CSV interpretation logic
- Participant-count detection separate from response-category row counts
- DOCX report export behavior for shareable summaries

## 🧩 Problem

Prevention and public health teams often collect feedback through surveys, but the path from survey design to useful findings can be fragmented. Staff may need to draft survey items, export data from survey tools, interpret aggregate CSV files, summarize themes, and prepare reports for stakeholders.

This creates several product risks:

- Survey questions may be inconsistent across programs or regions.
- Aggregate exports can be misread when response-category rows are confused with participant counts.
- Teams may spend significant time manually turning survey results into narrative summaries.
- Reports may lack consistent terminology, scope boundaries, or recommendations.
- Public-facing examples must avoid exposing private client data or proprietary records.

## 💡 Why This Matters

Reliable interpretation of survey data is essential when program teams use findings to improve training, technical assistance, and prevention services. A tool that separates participant base from response-category rows helps reduce misleading summaries and supports more trustworthy decisions.

The case study matters because it demonstrates how a product can combine AI assistance with clear constraints, transparent terminology, and export-ready reporting without presenting prototype output as production evidence.

## 👥 Users

Primary users considered in this case study include:

- Program evaluators reviewing survey feedback and aggregate results
- Prevention training and technical assistance staff preparing reports
- Project leads who need concise summaries, themes, gaps, and recommendations
- Internal teams exploring responsible AI support for survey workflows
- Portfolio reviewers evaluating product strategy, UX, and implementation decisions

## 🎯 My Role

My role covered product strategy, workflow design, documentation, and prototype implementation planning. Key responsibilities included:

- Defining MVP boundaries for a public-safe prototype
- Translating survey workflow needs into requirements and acceptance criteria
- Designing guided survey creation and analysis flows
- Documenting participant-count terminology and CSV interpretation rules
- Framing AI-assisted generation as a bounded support feature rather than an autonomous decision-maker
- Maintaining a portfolio-safe repository posture with no private data, credentials, production secrets, or proprietary records

## 🚀 Product Goals

The prototype and case study are organized around the following goals:

1. Help users create structured survey drafts through a guided workflow.
2. Support OpenAI-assisted generation of survey items based on user-provided context.
3. Allow users to upload survey results for aggregate analysis.
4. Detect participant counts separately from response-category row counts when CSV structure allows safe interpretation.
5. Generate useful analysis summaries, themes, gaps, and recommendations.
6. Export a DOCX report that uses accurate terminology and avoids overstating the data.
7. Keep the public repository safe for portfolio review while still showing runnable prototype implementation direction.

## 🛠️ MVP Scope

The MVP scope focuses on the end-to-end survey insight workflow:

- Welcome and path selection for survey creation or results analysis
- Guided survey creation screens
- AI-assisted survey item generation
- Survey results upload
- CSV parsing and metadata extraction
- Participant-count detection for supported aggregate export patterns
- Separation of participant base from response-category row counts
- Analysis summary generation
- Themes, gaps, and recommendations
- DOCX report export
- Public-safe documentation and sample-oriented framing

The MVP does not claim to replace formal evaluation methods, statistical analysis tools, human review, or production data governance processes.

## 🧪 Prototype Implementation

This repository should be understood as both a case study and a runnable prototype implementation. The implementation is designed to demonstrate how the workflow could operate in practice, including application screens, API route patterns, CSV handling, analysis output, and report export behavior.

Brief local setup:

```bash
npm install
npm run dev
```

Recommended checks:

```bash
npm run lint
npx tsc --noEmit
```

If using OpenAI-backed routes locally, provide required environment variables through a local environment file or deployment configuration. Do not commit credentials, API keys, private client files, production secrets, or proprietary records.

## 🔮 Future Scope

Future scope could include:

- Additional CSV format validators for more survey platforms
- More explicit confidence states for ambiguous uploads
- Role-based review workflows for program teams
- Richer report templates and branding controls
- Stronger audit trails for generated summaries
- Human-in-the-loop approval states before export
- Expanded accessibility and usability testing
- Deployment hardening, observability, and production security review

## 🧠 Key Product Decisions

- **Use precise participant terminology.** The product distinguishes known participant base from response-category rows and uses labels such as “Participants Represented” when the participant base is known.
- **Reject unsafe assumptions.** Ambiguous wider CSV files should not be treated as simple PTTC-style aggregate exports unless helper logic can safely validate the structure.
- **Keep AI bounded.** AI-assisted survey and analysis features support drafting and summarization, but the user remains responsible for review and interpretation.
- **Design for public safety.** The repository is written for portfolio review and excludes private client data, credentials, production secrets, and proprietary records.
- **Preserve runnable prototype value.** The case study documentation does not describe the repository as documentation-only; it reflects that prototype implementation patterns are included.

## 📁 Repository Contents

Key public-facing contents include:

- `README.md` — case study overview, product framing, MVP scope, and prototype setup notes
- `docs/requirements.md` — product context, MVP requirements, non-functional requirements, user stories, constraints, and success criteria
- `docs/acceptance-criteria.md` — acceptance criteria for survey creation, generation, upload, CSV handling, analysis, export, terminology, and MVP boundaries

Depending on the branch or deployment package being reviewed, the repository may also include runnable Next.js application code, OpenAI-backed API routes, survey creation screens, analysis screens, CSV participant-count logic, and DOCX export logic.

## ✅ Outcome

The case study documents a public-safe AI-assisted survey workflow that demonstrates:

- A practical path from survey creation to analysis and report export
- Product safeguards around participant-count interpretation
- Clear MVP boundaries and terminology requirements
- A portfolio-ready explanation of prototype implementation decisions
- Documentation that supports reviewers without exposing private or proprietary material

## 🔁 Future Iterations

Potential future iterations include:

- Add supported sample CSV fixtures with synthetic data only
- Expand validation states for unsupported or ambiguous files
- Add clearer analyst review checkpoints before generated content is exported
- Improve setup documentation as implementation details evolve
- Add screenshots or diagrams only when public-safe assets are committed to the repository
- Create deployment guidance for safe demo environments

## 🧰 Skills Demonstrated

This case study demonstrates skills in:

- Product discovery and MVP scoping
- AI-assisted workflow design
- Requirements writing and acceptance criteria definition
- Survey data interpretation and terminology design
- CSV parsing requirements and edge-case documentation
- Next.js prototype implementation framing
- API route and environment-variable awareness
- DOCX export product behavior definition
- Public-safe portfolio documentation
- Responsible AI product communication
