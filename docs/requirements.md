# Requirements: Insight Lab Survey Pipeline

## Purpose

The Insight Lab Survey Pipeline helps prevention program teams move from survey planning to a clear, reviewable stakeholder report. The workflow guides survey setup, validates uploaded results, supports accurate interpretation, and prepares findings for human review before export.

## Product Context

Prevention teams use surveys and needs assessments to understand stakeholder feedback and guide program planning. Moving from survey results to a useful report often requires several manual steps, and aggregate survey exports can be misread when response-category rows, totals, and participant counts are not clearly distinguished.

The Insight Lab Survey Pipeline provides a consistent workflow for defining survey context, validating CSV results, drafting insights, and preparing plain-language reports. Drafting support may help organize findings after validation, but users remain responsible for reviewing and approving the final content.

This repository is a public portfolio case study and does not include raw survey data, participant-level details, private client materials, proprietary documentation, credentials, or production secrets.

## MVP Requirements

The MVP includes guided survey setup, CSV upload and validation, participant-count handling, insight drafting, human review, and report export.

## 1. Guided Survey Setup

- Allow users to define the survey purpose, intended audience, topic areas, and reporting use.
- Capture question types and expected response formats.
- Support clear labels for demographic, program feedback, open-ended, and outcome-oriented questions.
- Preserve survey context for use during validation, drafting, and review.

## 2. Survey Results Upload

- Accept CSV as the primary MVP upload format.
- Confirm that an uploaded file can be read before validation begins.
- Identify missing, incomplete, or unsupported file content.
- Prevent unsupported or unclear files from proceeding to analysis as validated results.

## 3. CSV Validation

- Validate CSV structure before analysis begins.
- Identify headers, question labels, response categories, percentages, totals, and available participant-base indicators.
- Distinguish respondent-level records from aggregate response-category rows and summary metadata.
- Classify the file as respondent-level data, aggregate survey results, or unsupported or ambiguous data.
- Keep validation findings available for drafting, review, and report export.

## 4. Participant-Count Handling

- Determine participant count only when supported by validated file content, metadata, totals, or a recognized export structure.
- Keep participant count separate from CSV row count.
- Do not treat aggregate response-category rows as individual participants.
- Use “Participants Represented” when the participant base is known.
- Mark participant count as unknown when it cannot be validated.
- Carry participant-count limitations into the analysis draft and exported report.

## 5. Insight Drafting

- Prepare a structured draft after survey results pass validation.
- Include findings, themes, gaps, recommendations, and methodology notes.
- Ground drafted content in the validated survey results and preserved survey context.
- Use drafting support to organize and summarize findings without replacing reviewer judgment.
- Describe limited or aggregate findings carefully and avoid unsupported causal or predictive claims.

## 6. Human Review

- Allow reviewers to inspect and revise findings, themes, gaps, recommendations, and methodology notes before export.
- Keep validation warnings and unresolved data limitations visible during review.
- Allow reviewers to confirm or revise participant-count language.
- Require human review before a report is treated as final.

## 7. Report Export

- Produce a stakeholder-ready report in plain language.
- Include a survey overview, participants represented when known, findings, themes, gaps, recommendations, and methodology notes.
- Distinguish participants from response categories, response totals, and aggregate rows.
- Include clear limitation notes when participant count or CSV structure is unknown or ambiguous.
- Preserve reviewer-approved language in the exported report.

## Non-Functional Requirements

- Use terminology that is clear to non-technical users.
- Make validation results and data limitations visible and reviewable.
- Keep drafted findings traceable to validated survey inputs.
- Avoid unsupported claims about data quality, participant counts, or findings.
- Support a consistent workflow from survey setup through report export.

## User Stories

- As prevention program staff, I want to define survey purpose and reporting goals so that the workflow preserves the context needed for analysis.
- As an evaluator, I want uploaded CSV files validated so that aggregate results and respondent-level records are interpreted correctly.
- As a reporting lead, I want participant counts separated from CSV row counts so that reports do not overstate participation.
- As a program leader, I want clear findings, themes, gaps, and recommendations so that survey results can support planning.
- As a reviewer, I want to revise draft language and confirm limitations before a report is exported.

## Product Constraints

- CSV is the only required upload format for the MVP.
- CSV row count must not be used as participant count unless the file is validated as respondent-level data.
- Unknown or ambiguous participant counts must remain unknown.
- Unsupported or ambiguous files must not proceed as validated results.
- Analysis must remain descriptive and must not claim causal or predictive conclusions.
- Final reports require human review before export.

## Success Criteria

- Users can define survey context and reporting goals through a guided setup.
- The workflow validates CSV structure before analysis begins.
- Respondent-level records are distinguished from aggregate survey rows.
- Participant counts are reported only when supported by validated data.
- Unknown or ambiguous values are clearly labeled.
- Drafts include findings, themes, gaps, recommendations, and methodology notes.
- Reviewers can revise draft content and confirm limitations before export.
- Exported reports communicate findings and limitations in plain language.
