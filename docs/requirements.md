# PTTC Insight Lab Requirements

## Product Context

PTTC Insight Lab is a portfolio-safe prototype implementation and case study for an AI-assisted survey creation, analysis, and reporting workflow. The product concept helps prevention training and technical assistance teams draft survey instruments, upload aggregate survey results, interpret participant counts safely, and generate narrative reports for review.

This public repository contains a portfolio-safe prototype implementation and case study documentation. It does not include private client data, credentials, production secrets, or proprietary records.

The requirements below describe the intended MVP behavior for the public prototype. They are written to preserve the distinction between a runnable prototype and a production system, and to avoid implying that sample or generated outputs represent private client records.

## MVP Requirements

### 1. Guided Survey Creation

- The system must provide a guided path for creating a survey draft.
- The user must be able to enter context such as audience, purpose, topic, and desired focus areas.
- The workflow should help users move from a broad survey need to a structured set of draft survey items.
- Generated or drafted survey items must remain editable or reviewable by the user.

### 2. OpenAI-Assisted Survey Item Generation

- The system may use OpenAI-backed API routes to generate draft survey items from user-provided context.
- AI-generated content must be treated as a draft for human review.
- The system should avoid presenting generated survey items as final evaluation instruments without user review.
- API behavior must avoid requiring or exposing committed credentials, API keys, or production secrets.

### 3. Survey Results Upload

- The system must support uploading survey results for analysis in CSV format.
- The upload experience should communicate that the prototype is designed for supported aggregate export patterns, not every possible CSV shape.
- The system should extract relevant metadata when it can do so safely.
- The system must avoid making unsupported assumptions when file structure is ambiguous.

### 4. CSV Parsing and Metadata Extraction

- The system must parse supported CSV files to identify survey result structures, question labels, response categories, and counts where available.
- The parser should distinguish between rows that represent response categories and values that represent participant totals.
- The system must preserve enough metadata to support clear analysis and export terminology.
- Unsupported or ambiguous files should produce a clear limitation state rather than misleading analysis.

### 5. Participant-Count Detection

- The system must detect participant count only when the CSV structure provides a safe basis for doing so.
- The system must not treat CSV row count as participant count.
- When participant base is known, the UI and export should use terminology such as “Participants Represented.”
- When participant base is not known, the system should avoid implying that row counts are participant totals.

### 6. Response-Category Row Count Separation

- The system must treat response-category rows separately from participant-count values.
- Analysis should not overstate sample size based on the number of response categories, answer choices, or aggregate rows.
- DOCX exports must preserve this distinction in headings, labels, and narrative summary text.

### 7. Analysis Summary Generation

- The system must generate an analysis summary from supported uploaded results.
- The summary should be concise, reviewable, and tied to the available aggregate data.
- The summary should avoid unsupported causal claims or claims that exceed the uploaded data.
- AI-assisted analysis must be framed as draft support for human review.

### 8. Themes, Gaps, and Recommendations

- The system should identify draft themes based on survey results.
- The system should identify potential gaps, limitations, or areas needing additional follow-up.
- The system should produce practical recommendations that align with the uploaded data and product context.
- Recommendations should be written as reviewable suggestions, not final program decisions.

### 9. DOCX Report Export

- The system must support exporting analysis output to DOCX format.
- The exported report should include clear headings, summary content, themes, gaps, recommendations, and participant terminology where available.
- The export must not convert response-category row count into participant count.
- The export should be suitable for stakeholder review after human validation.

### 10. Public-Safe Prototype Constraints

- The repository must remain public-safe and portfolio-friendly.
- The repository must not include private client data, credentials, production secrets, or proprietary records.
- Documentation must not describe the repository as static documentation only.
- Documentation must not claim the repository excludes production code; instead, it must frame the work as a portfolio-safe prototype implementation and case study.

## Non-Functional Requirements

- **Privacy and safety:** Public materials must use generic, synthetic, or non-sensitive examples only.
- **Clarity:** User-facing terminology must distinguish participants represented from response-category rows.
- **Maintainability:** Requirements and acceptance criteria should be understandable to product, design, and engineering reviewers.
- **Reliability:** CSV parsing should fail safely when structure is unsupported or ambiguous.
- **Reviewability:** AI-generated survey and analysis content should be easy for a human to inspect and revise.
- **Portability:** DOCX export should produce a usable report artifact without requiring proprietary templates.
- **Security posture:** Environment variables and credentials must be kept outside the repository.
- **Accessibility direction:** Interface language and report structure should support clear navigation and plain-language comprehension.

## User Stories

- As a program evaluator, I want guided survey creation so that I can quickly draft a survey aligned to a program or training objective.
- As a prevention staff member, I want AI-assisted survey item suggestions so that I can start from a structured draft instead of a blank page.
- As an analyst, I want to upload aggregate survey results so that I can review patterns without manually rebuilding every summary.
- As a report writer, I want the system to separate participant counts from response-category rows so that I do not misstate the number of participants represented.
- As a project lead, I want themes, gaps, and recommendations so that I can identify practical next steps for stakeholders.
- As a reviewer, I want a DOCX export so that I can share a report draft for edits, approval, or discussion.
- As a portfolio reviewer, I want public-safe documentation so that I can understand the product and implementation approach without accessing private client data.

## Product Constraints

- The MVP supports a constrained set of survey creation and analysis workflows.
- The prototype must not be presented as a fully governed production evaluation platform.
- OpenAI-assisted output must remain subject to human review.
- CSV participant-count logic must not infer participants from row count alone.
- Ambiguous wider CSV files must not be handled as simple PTTC-style aggregate exports unless helper logic can safely validate them.
- DOCX export must preserve accurate terminology and avoid overstating participant base.
- Public repository content must exclude private client data, credentials, production secrets, and proprietary records.

## Success Criteria

The MVP is successful when:

- A user can follow a guided path to draft survey items.
- AI-assisted survey generation produces useful draft content from user-provided context.
- A user can upload supported CSV survey results for analysis.
- The system safely distinguishes participant base from response-category row count.
- Analysis output includes a summary, themes, gaps, and recommendations.
- DOCX export produces a clear report draft with accurate terminology.
- Unsupported or ambiguous CSV structures are not misrepresented as validated aggregate exports.
- Public documentation accurately describes the repository as a portfolio-safe prototype implementation and case study.
