# Prod 100 Task

Goal: take `raise_the_stakes_ai_startup_competition` to application-ready
production for RAISE the STAKES 2026.

Track: `ai_startup_pitch`

Product: `ContestOps AI`

## Version Path

| Version | Milestone | Completion Gate |
|---|---|---|
| v0.1.0 | Source lock | Official and partner pages captured with deadline conflict noted. |
| v0.2.0 | V generator | `contestops_ai` emits RAISE manifest, checklist, evidence, and packet. |
| v0.3.0 | Worth-it package | Eligibility, product, traction, risks, and application docs exist. |
| v0.4.0 | Demo panel | Vue3 CDN + SFC + UnoCSS panel exists under `C:\git\websites`. |
| v0.6.0 | Automation | Dealum prep and live-form playbooks validate with receipts. |
| v0.8.0 | Submission QA | Payload, field map, docs, links, and evidence pass local QA. |
| v1.0.0 | Application ready | Dealum packet is ready for authenticated final submission. |

## Acceptance

- [x] Track is declared as `ai_startup_pitch`.
- [x] Eligibility checklist exists.
- [x] AI product proposal exists.
- [x] Landing, deck, and video outline exist.
- [x] Minimum traction proof plan exists.
- [x] Application packet and structured payload exist.
- [x] Risk register exists.
- [x] Competitive battlecard exists.
- [x] RAISE judging scorecard exists.
- [x] Competitive intelligence war-room exists.
- [x] Judge objection Q&A exists.
- [x] 72-hour pilot sprint playbook exists.
- [x] Demo choreography exists.
- [x] WAIBAv automation plan and playbooks exist.
- [x] Generated V manifest exists.
- [ ] Authenticated Dealum session submits final packet and captures receipt.

## Current Technical Debt

Technical debt target is `0%`.

Controls:

- Shared data stays in `contestops_ai`.
- Opportunity-specific evidence stays in this subrepo.
- Web demo stays in `C:\git\websites\raise_the_stakes_ai_startup_competition`.
- Files are kept well under 600 lines.
- External credentials and private legal documents are never committed.
