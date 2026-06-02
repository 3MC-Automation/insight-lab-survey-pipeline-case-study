# PTTC Insight Lab Acceptance Criteria

## Overview

These acceptance criteria define expected MVP behavior for the PTTC Insight Lab public-safe prototype implementation and case study. They focus on the user journey from welcome screen through survey creation, survey generation, results upload, CSV interpretation, analysis output, and DOCX export.

This public repository contains a portfolio-safe prototype implementation and case study documentation. It does not include private client data, credentials, production secrets, or proprietary records.

## 1. Welcome and Path Selection

- Given a user opens the application, when the welcome experience loads, then the user can identify the primary workflow options.
- Given the user wants to create a survey, when they select the survey creation path, then they are taken to the guided survey creation workflow.
- Given the user wants to analyze results, when they select the analysis path, then they are taken toward upload or analysis functionality.
- Given this is a public-safe prototype, when introductory copy appears, then it must not imply that private client records or production data are included in the repository.

## 2. Guided Survey Creation

- Given the user enters survey context, when they proceed through the guided workflow, then the system captures enough information to support a draft survey.
- Given required context is missing, when the user attempts to generate or continue, then the UI should indicate what information is needed.
- Given survey items are generated, when they are displayed, then they are presented as draft content for review.
- Given the workflow is part of the MVP, when users review generated items, then the experience should support clear human review rather than presenting output as final evaluation content.

## 3. Survey Generation API Behavior

- Given valid survey context is submitted, when the OpenAI-backed generation route is available and configured, then the API may return draft survey items.
- Given API credentials are not configured locally, when a generation request is attempted, then the app should fail safely rather than exposing secrets or requiring committed credentials.
- Given AI-generated content is returned, when it appears in the UI, then it should be framed as a draft.
- Given this is a public repository, when environment setup is documented, then credentials and API keys must be described as local or deployment configuration only.

## 4. Survey Results Upload

- Given the user has survey results in CSV format, when they upload a supported file, then the system attempts to parse the survey result structure.
- Given a file is not a supported CSV, when it is uploaded, then the system should communicate that the file cannot be analyzed safely.
- Given a supported aggregate export is uploaded, when parsing succeeds, then the system extracts available question, response, count, and participant-base metadata.
- Given an upload contains private or sensitive data, when used in this public-safe context, then documentation should direct users not to commit or expose that data.

## 5. CSV Participant-Count Logic

- Given a CSV includes a safely detectable participant base, when the data is parsed, then the UI may display that value as “Participants Represented.”
- Given participant base is known, when the DOCX report is exported, then the export should use “Participants Represented” or equivalent participant-base terminology.
- Given participant base is unknown, when the UI or export describes the data, then it must not imply a participant total.
- Given a CSV contains response-category rows, when parsing completes, then the row count must not be treated as participant count.
- Given the CSV has five response-category rows for one question, when participant base is not otherwise detected, then the system must not report five participants.
- Given a wider CSV file is ambiguous, when helper logic cannot safely validate it as a simple PTTC-style aggregate export, then the file must not be handled as that simple aggregate format.
- Given the parser cannot distinguish participant counts from response rows, when analysis is requested, then the system should present a limitation or safe fallback rather than misleading metrics.

## 6. Analysis Output

- Given supported survey results are parsed, when analysis is generated, then the output includes a concise summary.
- Given sufficient result content is available, when analysis is generated, then the output includes themes, gaps, and recommendations.
- Given analysis is generated with AI assistance, when users review the output, then the content is presented as draft support for human review.
- Given the data is aggregate or limited, when the system writes analysis, then it must avoid unsupported causal claims, overstated certainty, or inflated participant counts.

## 7. DOCX Report Export

- Given analysis output is available, when the user chooses export, then the system generates a DOCX report.
- Given the participant base is known, when the DOCX report is generated, then the report includes accurate participant-base terminology such as “Participants Represented.”
- Given only response-category row counts are available, when the DOCX report is generated, then those rows must not be labeled as participants.
- Given themes, gaps, and recommendations are available, when the DOCX report is generated, then they should be included in a structured report format.
- Given the report is a prototype output, when it is exported, then it should remain suitable for human review before stakeholder distribution.

## 8. Terminology Accuracy

- Given documentation describes the repository, when public-facing copy is reviewed, then it must state that the repository contains a portfolio-safe prototype implementation and case study documentation.
- Given documentation describes repository safety, when public-facing copy is reviewed, then it must state that the repository does not include private client data, credentials, production secrets, or proprietary records.
- Given documentation describes implementation, when public-facing copy is reviewed, then it must not describe the repo as static documentation only.
- Given documentation describes implementation, when public-facing copy is reviewed, then it must not say the repository does not include production code.
- Given UI or export labels refer to counts, when participant base is known, then “Participants Represented” should be used where appropriate.
- Given UI or export labels refer to response-category rows, when participant base is unknown, then those rows must be labeled distinctly and not as participant totals.

## 9. MVP Scope Boundaries

- Given the prototype supports guided survey creation, when users need a final validated evaluation instrument, then the product should still require human review.
- Given the prototype supports AI-assisted analysis, when users need formal statistical analysis, then the product should not claim to replace dedicated statistical tools or evaluation expertise.
- Given the prototype supports CSV parsing, when unsupported survey platform formats are uploaded, then the product should fail safely or request a supported format.
- Given the prototype supports DOCX export, when reports are generated, then the product should not imply that exported content is approved or final without review.
- Given this is a public-facing portfolio repository, when examples or documentation are added, then they must remain synthetic, generic, or non-sensitive.
