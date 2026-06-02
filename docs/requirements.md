# 📋 Requirements: PTTC Insight Lab

## 🎯 Purpose

PTTC Insight Lab defines a product workflow for AI-assisted survey analysis and report drafting for prevention program insights. The requirements focus on guided survey creation, safe interpretation of uploaded results, participant-count validation, and clear report export expectations.

## 🧭 Product Context

Prevention teams may need to summarize survey results for planning, evaluation, and stakeholder reporting. Survey exports can contain aggregate rows, response categories, percentages, totals, and labels that require careful interpretation before summary drafting.

This case study documents public-safe product requirements only. It does not include private client data, credentials, production secrets, proprietary records, application code, or runtime setup instructions.

## 🛠️ MVP Requirements

### Guided Survey Creation

- Provide a structured workflow for defining survey purpose, audience, topic areas, and intended reporting use.
- Capture question types and expected response formats before analysis assumptions are made.
- Support clear labeling for demographic, program feedback, open-ended, and outcome-oriented questions.
- Preserve enough survey context to guide accurate summary drafting and recommendations.

### Survey Results Upload

- Define an upload step for survey result files, with CSV as the primary MVP format.
- Validate that uploaded files contain recognizable survey result structures before analysis.
- Flag ambiguous files that cannot be safely interpreted as aggregate survey exports.
- Avoid treating unsupported or unclear files as valid inputs without validation.

### CSV Parsing

- Parse headers, labels, response categories, percentages, totals, and available participant-base indicators.
- Identify whether rows represent respondents, response categories, aggregate values, or summary metadata.
- Detect files where row count reflects response-category rows rather than participant records.
- Preserve parsed context for downstream analysis and report export language.

### Participant-Count Detection

- Identify participant count only when supported by validated file content, metadata, totals, or recognizable survey export conventions.
- Separate participant count from CSV row count in all analysis and export language.
- Use “Participants Represented” when the participant base is known.
- Flag unknown or ambiguous participant base values rather than inferring unsupported counts.

### Analysis Drafting

- Generate AI-assisted summary drafts from validated survey results and provided survey context.
- Produce themes, gaps, and recommendations in plain, stakeholder-ready language.
- Indicate when findings are directional because the participant base or export structure is limited.
- Avoid overstating certainty when data quality, sample size, or participant-count information is incomplete.

### Report Export Requirements

- Define report output requirements suitable for DOCX or report-style export.
- Include sections for overview, participants represented, key themes, gaps, recommendations, and methodology notes.
- Ensure exported language distinguishes participants from response categories and aggregate rows.
- Include validation notes when participant count or CSV structure is ambiguous.

## ⚙️ Non-Functional Requirements

- Documentation must remain public-safe and portfolio-facing.
- Requirements must avoid references to private client data, credentials, production secrets, or proprietary records.
- Product language must be concise, professional, and understandable to non-technical stakeholders.
- Any future workflow should prioritize interpretability, auditability, and clear terminology over unsupported automation claims.
- This repository must remain documentation-only and must not include application code or runtime configuration files.

## 👤 User Stories

- As prevention program staff, I want guided survey setup so that analysis reflects the purpose and audience of the survey.
- As an evaluator, I want CSV parsing rules so that aggregate exports are interpreted consistently.
- As a reporting lead, I want participant-count validation so that reports do not confuse response-category rows with participants.
- As a program leader, I want themes, gaps, and recommendations so that survey findings can inform planning decisions.
- As a stakeholder reviewer, I want clear export language so that report outputs are understandable and defensible.

## 🚧 Product Constraints

- CSV row count must not be used as participant count unless the file is validated as respondent-level data.
- Aggregate survey exports must be validated before analysis language treats them as reliable.
- Ambiguous participant counts must be labeled as unknown or not available.
- AI-assisted summaries must be grounded in validated survey context and parsed results.
- Public documentation must not expose private client data, credentials, production secrets, proprietary records, or implementation-specific runtime setup.

## ✅ Success Criteria

- The MVP workflow clearly documents guided survey creation, results upload, CSV parsing, analysis drafting, and report export expectations.
- Participant count is separated from response-category row count throughout the requirements.
- “Participants Represented” is used when the participant base is known.
- Ambiguous CSV exports are flagged instead of being treated as valid aggregate results.
- Report requirements support clear themes, gaps, recommendations, and methodology notes.
- The repository remains a documentation-only public portfolio case study.
