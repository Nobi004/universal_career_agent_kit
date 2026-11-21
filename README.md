# Universal Career Agent — Candidate Intelligence Kit

Version: 1.0  
Candidate: MD. Mahmudun Nobi  
Primary use: OpenCode, Codex, Claude Code, Cursor, other coding agents, and human career workflows.

## Mission

Operate a portable, evidence-grounded career system that improves **qualified interview probability**, not raw application count.

The system must:
1. Maintain one canonical candidate knowledge base.
2. Generate platform-specific profiles from that source of truth.
3. Discover and qualify vacancies against role fit, seniority, location eligibility, and evidence.
4. Tailor resumes and application answers without inventing facts.
5. Require approval before consequential external actions by default.
6. Track outcomes and use feedback to improve targeting.

## Start here

1. Read `CAREER_TRUTH.json`.
2. Read `EVIDENCE_LEDGER.md`.
3. Read `POSITIONING_MATRIX.md`.
4. Read `PROFILE_MASTER.md`.
5. Follow `APPLICATION_POLICY.md`.
6. Implement according to `AGENT_WORKFLOW.md` and `PORTAL_ADAPTER_SPEC.md`.
7. Resolve every item in `OPEN_QUESTIONS.md` before publishing claims that depend on it.

## Source-of-truth hierarchy

1. Candidate-confirmed facts in the canonical knowledge base.
2. Primary evidence: signed employment records, official employer pages, deployed products, repositories, DOI/publisher records, certificates, transcripts.
3. Candidate-provided descriptions that have not yet been independently verified.
4. Agent inference — **never publish as fact**.

Every material claim should have a claim ID, evidence pointer, confidence, and permitted use.

## Universal, not OpenCode-specific

This package intentionally uses Markdown, JSON, and implementation-neutral rules. Any agent that can read files can use it. Do not make OpenCode-specific assumptions about paths, tools, memory, or browser automation.

## Privacy

Do not place passwords, session cookies, API keys, recovery codes, government IDs, or private account tokens in this repository. Use environment variables or a secret manager. Do not commit `.env` files or browser profile directories.

## Default operating mode

`ASSISTED`: research and prepare autonomously; ask for approval before profile publication, job submission, recruiter messages, salary commitments, or any action that represents the candidate externally.

An explicitly configured `AUTONOMOUS_LOW_RISK` mode may submit only applications that pass every hard gate in `APPLICATION_POLICY.md` and use pre-approved answers. Never bypass CAPTCHAs, platform restrictions, anti-bot controls, or consent requirements.
