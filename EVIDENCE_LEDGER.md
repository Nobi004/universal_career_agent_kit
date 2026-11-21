# Evidence Ledger

Use this ledger as the boundary between persuasive storytelling and unsupported claims. Add one row for every material claim used in a resume, profile, cover letter, screening answer, or recruiter message.

| Claim ID | Claim | Current status | Evidence required | Permitted use now |
|---|---|---|---|---|
| EMP-01 | Team Lead (Q-Bit Coders) & AI Developer, JVAI under Betopia Group, May 2025–Apr 2026 | Candidate-confirmed title/period; legal employer naming needs check | Appointment/experience letter, payslip, HR record, manager reference | Use with cautious employer naming; don't claim current employment |
| EMP-02 | Permanent employee | Previously candidate-described | Employment letter / HR confirmation | Omit employment type until verified if form is legally consequential |
| LEAD-01 | Led 30+ developers | Candidate-reported; scope and direct-report count unclear | Org chart, team roster, manager confirmation; distinguish direct reports from broader team | Use only as “coordinated/led a 30+ developer group” after scope confirmation |
| LEAD-02 | Handled two additional teams / night-shift leadership | Candidate-reported | Role description, roster, manager confirmation | Narrative only after exact scope/timing clarified |
| IMP-01 | 20+ projects delivered | Candidate-reported; team vs personal attribution | Project list, delivery records | “Contributed to a team that delivered…” only after confirmation |
| IMP-02 | USD 250K total project value | Candidate-reported; not equivalent to revenue personally generated | Contract/invoice or employer-approved aggregate | Do not use until attribution, period, and definition are confirmed |
| VM-01 | Voice Mind achieved 1,000+ installs in 7 days | Candidate-reported | Play Store listing, analytics export, date range, ownership/contribution | Can say “reported 1,000+ installs…” only in internal drafts; verify before public use |
| AI-01 | LangGraph business-data agent | Candidate-reported | Architecture, sanitized demo, repo, deployment evidence | Describe project and personal contribution; avoid unsupported production claims |
| DOC-01 | ACORD 25/101 pipeline using PaddleOCR + LayoutLMv3 + graph model | Candidate-reported; GraphSAGE vs Graph Attention conflict | Code/config, model card, pipeline diagram, demo, technical explanation | Describe only verified components; resolve graph model terminology |
| PUB-01 | IEEE power-line insulator fault detection paper | Publication record previously identified | IEEE author page / DOI metadata / PDF | Cite exact official publication record after checking author and date |
| PUB-02 | WBFVD UNet paper, NCIM-2025 | Candidate-reported | Official proceedings / publisher record | Omit until publication status and metadata verified |
| RES-01 | EEG/Parkinson's thesis work | Candidate-reported | Thesis, supervisor confirmation, university status | Describe as academic research only; don't imply completed degree |
| EDU-01 | B.Sc. EEE, Faridpur Engineering College | Institution/program/session known; award status unresolved | Transcript, provisional certificate, degree certificate | Say “B.Sc. in EEE studies” only if needed; never say graduated yet |
| CAREEROS-01 | CareerOS deployed product | Candidate project; deployment state can change | Current live app, repository, release notes | Describe as a personal product and list verified features |
| PORT-01 | Portfolio site | Public URL known; publication gating was previously implemented | Current live pages and repo | Link portfolio; only cite currently published pages |

## Evidence quality levels

- **A — Primary verified:** official records, employer letters, publisher pages, product analytics, production telemetry.
- **B — Direct artifact:** repository, deployed demo, code, screenshots with provenance, technical documentation.
- **C — Candidate attestation:** credible self-report, but not independently corroborated.
- **D — Inference:** derived or assumed; prohibited from external claims.

## Claim lifecycle

`DRAFT → CANDIDATE_CONFIRMED → EVIDENCE_ATTACHED → VERIFIED → APPROVED_FOR_PUBLIC_USE`

A claim may be approved for limited use without being independently verified, but the status must remain visible internally. Never silently upgrade confidence.
