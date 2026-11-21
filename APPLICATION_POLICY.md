# Application Policy — Quality, Truth, and Candidate Control

## North-star metric

Optimize for **qualified interviews per high-quality application**, not applications per day.

Track:
- Qualified roles found
- Roles passing hard gates
- Applications approved
- Applications submitted
- Recruiter responses
- Screening calls
- Technical interviews
- Final rounds
- Offers
- Rejection reasons
- Time spent per qualified opportunity

## Hard rejection gates

Reject or hold a vacancy if any applies:
1. The role is not genuinely relevant to the candidate's skills or trajectory.
2. Location/work authorization requirements exclude Bangladesh and no eligible contractor/EOR arrangement is stated.
3. The employer or vacancy appears fraudulent, impersonates a company, requests payment, or collects suspicious sensitive information.
4. The vacancy is expired, duplicated, or cannot be corroborated.
5. The role requires a mandatory degree/certification/clearance that the candidate cannot truthfully claim.
6. The role's seniority is materially beyond verified experience.
7. The role requires relocation or on-site attendance that has not been approved.
8. Compensation, equity, exclusivity, IP assignment, or contractual terms require a decision not authorized by the candidate.

## Role scoring (0–100)

| Dimension | Weight | Evaluation |
|---|---:|---|
| Core technical fit | 25 | Actual duties vs proven skills and projects |
| Evidence strength | 20 | Can the candidate substantiate the required experience? |
| Seniority fit | 15 | Scope and years required vs verified profile |
| Location / hiring eligibility | 15 | Explicit Bangladesh eligibility, contractor/EOR, timezone |
| Career trajectory | 10 | Moves toward Applied AI / Agentic AI / AI product engineering |
| Compensation / quality | 10 | Salary transparency, contract quality, employer credibility |
| Application feasibility | 5 | Required materials, referral access, deadline, effort |

Suggested decision:
- 80–100: priority; prepare tailored application.
- 65–79: consider; identify gaps and decide.
- 50–64: hold for candidate review.
- Below 50: do not apply.

A score never overrides a hard rejection gate.

## Tailoring rules

For each job:
1. Extract responsibilities, must-haves, nice-to-haves, seniority, location, employment type, salary, visa/work authorization, and application questions.
2. Map each requirement to a claim ID in the evidence ledger.
3. Mark each match: strong evidence / partial evidence / no evidence.
4. Select the best role-specific positioning from `POSITIONING_MATRIX.md`.
5. Tailor the summary, skills order, project selection, and bullet order — not the underlying facts.
6. Preserve exact employer names, titles, dates, and education status.
7. Do not keyword-stuff skills that the candidate cannot discuss in an interview.
8. Include a gap analysis; do not hide mandatory gaps.

## Approval levels

- **Level 0 — Research:** agent may discover, deduplicate, score, and summarize jobs.
- **Level 1 — Draft:** agent may prepare profile text, resume, cover letter, and screening answers.
- **Level 2 — Candidate approval:** required before changing a public profile, sending a message, or submitting an application.
- **Level 3 — Pre-authorized low-risk automation:** allowed only for explicitly approved platforms, exact role filters, approved answers, and no novel legal/financial/eligibility questions.

Never autonomously:
- Accept an offer or reject one.
- Negotiate salary or make compensation commitments.
- Agree to exclusivity, non-compete, IP, or contract terms.
- Answer legal/work-authorization questions by inference.
- Claim a degree, certification, skill, employment date, or metric without evidence.
- Bypass CAPTCHA, MFA, anti-bot measures, rate limits, or platform terms.

## Profile update policy

Before editing a profile:
1. Capture current profile text/fields.
2. Compare against canonical facts.
3. Generate a proposed diff.
4. Flag fields with unresolved facts.
5. Request approval.
6. Apply changes only through supported platform mechanisms.
7. Re-read the profile and record what actually changed.

Do not create duplicate accounts. Do not mass-edit every platform with identical text. Adapt length, keywords, and tone to each platform while preserving facts.
