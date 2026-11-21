# Universal Agent Workflow

## Architecture

Use a platform-neutral core with replaceable adapters:

- `candidate-kb/` — canonical profile, evidence, preferences, approved answers.
- `connectors/job_sources/` — job-board/search adapters.
- `connectors/profile_platforms/` — profile read/write adapters.
- `pipeline/` — normalize, deduplicate, qualify, score, tailor, approve, submit.
- `artifacts/` — resumes, cover letters, screening answers, profile diffs.
- `tracker/` — application records, events, outcomes, feedback.
- `audit/` — action logs, source snapshots, approvals, errors.
- `tests/` — truth, privacy, duplicate, permission, and regression tests.

## Pipeline

1. **Discover:** gather vacancies from permitted sources.
2. **Normalize:** canonicalize employer, title, URL, location, remote status, salary, dates, skills, and source.
3. **Verify:** corroborate employer and vacancy; identify scams, stale listings, and duplicates.
4. **Gate:** apply hard eligibility checks.
5. **Analyze:** extract responsibilities and requirements from the JD.
6. **Map evidence:** map each requirement to claim IDs; record gaps.
7. **Score:** calculate role-fit score and explain it.
8. **Select:** choose role positioning and evidence-backed resume variant.
9. **Generate:** produce resume, cover letter, profile answers, and recruiter note if useful.
10. **Validate:** factual consistency, ATS parsing, date consistency, keyword coverage, no unsupported claims.
11. **Approve:** candidate reviews exact final payload and destination.
12. **Submit:** only through permitted mechanisms and only after approval or narrowly configured pre-authorization.
13. **Verify:** confirm submission receipt; never report success merely because a button was clicked.
14. **Track:** save source snapshot, versioned artifacts, submission timestamp, and confirmation.
15. **Learn:** update targeting from responses and rejection reasons, not from unverified assumptions.

## Data model

Every job should have:
- `job_id`, `source`, `source_url`, `canonical_url`, `employer`, `title`
- `location`, `remote_type`, `eligible_countries`, `timezone`
- `employment_type`, `salary_min`, `salary_max`, `currency`
- `posted_at`, `closing_at`, `first_seen_at`, `last_verified_at`
- `requirements[]`, `responsibilities[]`, `application_questions[]`
- `hard_gate_results`, `fit_score`, `fit_explanation`
- `evidence_mapping[]`, `gaps[]`, `decision`
- `artifact_version_ids[]`, `approval_id`, `submission_status`

Every application should have:
- candidate profile version
- resume version and checksum
- cover-letter version
- exact screening answers
- job description snapshot
- approval record
- submission confirmation or failure
- follow-up dates and outcome events

## Learning loop

Do not optimize based on raw rejection counts alone. Classify outcomes:
- no response
- recruiter rejection
- location ineligible
- seniority mismatch
- skills mismatch
- compensation mismatch
- role closed
- interview passed/failed
- offer / declined

After a meaningful sample, analyze conversion by role family, seniority, source, location, resume variant, and evidence strength. Avoid changing strategy based on one or two outcomes.

## Agent portability

The core knowledge base must remain readable without a specific vendor. Store content in Markdown and JSON. Keep prompts in `AGENT_PROMPTS.md`. Use environment-based configuration and documented adapter contracts. No vendor-specific memory should be the only copy of candidate truth.
