# ✅ Acceptance Criteria: PTTC Insight Lab

## 🎯 Purpose

These acceptance criteria define the expected behavior and documentation boundaries for the PTTC Insight Lab MVP concept. They focus on survey workflow clarity, CSV participant-count logic, AI-assisted analysis output, and report export terminology.

## 🧪 MVP Workflow

- Given a user needs to analyze survey results, the workflow must describe guided survey creation, results upload, CSV validation, analysis output, and report export.
- Given the repository is public-facing, all documentation must avoid private client data, credentials, production secrets, proprietary records, and runtime setup instructions.
- Given this is a case study repository, it must remain documentation-only and must not present itself as a runnable prototype.

## 1. Guided Survey Creation

- Given a user begins a survey workflow, they must be prompted to define survey purpose, audience, topic areas, and reporting goals.
- Given survey questions are documented, question type and expected response format must be captured or inferable from the survey context.
- Given analysis will later summarize findings, the workflow must preserve enough context to distinguish program feedback, demographic information, outcome signals, and open-ended responses.

## 2. Survey Results Upload

- Given a user uploads survey results, CSV must be treated as the primary MVP file format.
- Given a file is uploaded, the workflow must validate that it resembles a supported survey results structure before analysis.
- Given a file is unsupported, incomplete, or unclear, it must not proceed as a valid input without a safe validation path.

## 3. CSV Participant-Count Logic

- Given a CSV contains aggregate response-category rows, CSV row count must not be treated as participant count.
- Given participant base is known from validated totals, metadata, or recognized export structure, the label “Participants Represented” must be used.
- Given participant base is unknown, the workflow must state that participant count is unavailable or ambiguous rather than inventing a value.
- Given a CSV includes percentages, totals, and response labels, parsing must distinguish those fields from respondent-level records.
- Given an ambiguous CSV file cannot be safely validated, it must not be treated as a valid aggregate export.

## 4. Analysis Output

- Given validated survey results, the analysis output must include concise findings, themes, gaps, and recommendations.
- Given participant-count uncertainty exists, the analysis output must include cautious language and avoid overstating certainty.
- Given the survey data is aggregate or limited, recommendations must be framed as planning guidance rather than definitive causal conclusions.
- Given open-ended responses are included, summary language must synthesize themes without exposing private or identifying information.

## 5. Report Export

- Given a report export is produced, it must include sections for overview, participants represented, key themes, gaps, recommendations, and methodology notes.
- Given participant count is known, report language must use “Participants Represented” rather than unsupported labels.
- Given participant count is unknown or ambiguous, the report must include a validation note instead of a fabricated participant count.
- Given DOCX/report export requirements are documented, exported content must be stakeholder-ready, plain-language, and clear about data limitations.

## 6. Terminology Accuracy

- Given the file contains response-category rows, those rows must be described as categories, options, or aggregate rows rather than individual participants.
- Given the file contains respondent-level records, participant terminology may be used only after the structure is validated.
- Given totals represent responses rather than people, the workflow must avoid labeling those totals as participants.
- Given the participant base is known, “Participants Represented” must be used consistently in analysis and report sections.

## 7. MVP Scope Boundaries

- Given this repository is documentation-only, it must not include app code, package files, TypeScript configuration, API routes, OpenAI setup instructions, or local run commands.
- Given diagram assets are not finalized, fake or broken PNG files must not be created.
- Given diagrams are absent, the README must include the Product Logic Diagrams section with the note “Diagram assets to be added.”
- Given public portfolio boundaries, documentation must not include private client data, credentials, production secrets, or proprietary records.
