# Acceptance Criteria: Insight Lab Survey Pipeline

## Purpose

These acceptance criteria define the expected behavior of the Insight Lab Survey Pipeline MVP. They focus on a clear survey-to-report workflow, accurate interpretation of CSV results, human review, and plain-language report export.

## MVP Workflow

- User can define survey context before results are analyzed.
- System validates uploaded CSV results before drafting begins.
- System distinguishes participant counts from aggregate rows and response totals.
- System prepares a structured insight draft from validated results.
- Reviewer can inspect and revise the draft before export.
- System exports a plain-language report that communicates findings and limitations.

## 1. Guided Survey Setup

### Business Goal

Preserve the context needed to interpret survey results and prepare useful stakeholder reporting.

### Acceptance Criteria

- User can define survey purpose, intended audience, topic areas, and reporting goals.
- User can identify question types and expected response formats.
- System preserves survey context for validation, drafting, and review.
- Survey setup supports demographic, program feedback, open-ended, and outcome-oriented questions.

## 2. Survey Results Upload

### Business Goal

Provide a clear and controlled starting point for survey-result analysis.

### Acceptance Criteria

- User can upload a CSV file as the MVP survey-results format.
- System confirms that the uploaded file can be read.
- System identifies missing, incomplete, unsupported, or unclear file content.
- Unsupported or unclear files do not proceed as validated survey results.

## 3. CSV Validation and Participant-Count Logic

### Business Goal

Prevent aggregate survey rows and response totals from being misreported as participant counts.

### Acceptance Criteria

- System validates CSV structure before analysis begins.
- System identifies headers, question labels, response categories, percentages, totals, and available participant-base indicators.
- System distinguishes aggregate response-category rows from respondent-level records.
- System classifies the file as respondent-level data, aggregate survey results, or unsupported or ambiguous data.
- System does not treat CSV row count as participant count unless respondent-level data is validated.
- System uses “Participants Represented” when the participant base is known.
- System labels participant count as unknown when it cannot be validated.
- System keeps participant-count limitations available for drafting, review, and export.

## 4. Insight Drafting

### Business Goal

Turn validated survey results into a clear draft that supports program planning and stakeholder communication.

### Acceptance Criteria

- System prepares an insight draft only after survey results pass validation.
- Analysis draft includes findings, themes, gaps, recommendations, and methodology notes.
- Drafted content reflects the validated survey results and preserved survey context.
- Drafting support organizes and summarizes findings without replacing reviewer judgment.
- Draft language identifies important data limitations.
- Draft does not make unsupported causal or predictive claims.

## 5. Human Review

### Business Goal

Keep reviewers responsible for the accuracy, clarity, and final interpretation of survey findings.

### Acceptance Criteria

- Reviewer can inspect and revise findings, themes, gaps, recommendations, and methodology notes before export.
- Reviewer can confirm or revise participant-count language.
- Validation warnings and unresolved limitations remain visible during review.
- Report is not treated as final until human review is complete.

## 6. Report Export

### Business Goal

Produce a clear stakeholder report that communicates findings accurately and makes limitations visible.

### Acceptance Criteria

- Exported report uses plain language.
- Exported report includes a survey overview, participants represented when known, findings, themes, gaps, recommendations, and methodology notes.
- Exported report distinguishes participants from response categories, response totals, and aggregate rows.
- Exported report labels participant count as unknown when it cannot be validated.
- Exported report includes clear limitation notes where needed.
- Exported report preserves reviewer-approved language.

## 7. MVP Scope Boundaries

### Business Goal

Keep the first release focused on a reliable survey-to-report workflow.

### Acceptance Criteria

- MVP supports CSV as the required survey-results upload format.
- MVP requires validation before insight drafting begins.
- MVP requires human review before report export.
- MVP does not claim causal, predictive, or fully automated decision-making.
- MVP does not infer participant counts from unsupported data.
- MVP does not treat unsupported or ambiguous files as validated survey results.
