# RAISE the STAKES AI Startup Competition 2026

Tag: `worth_it`

Track: `ai_startup_pitch`

Product candidate: `ContestOps AI`

Application portal: https://app.dealum.com/

Official page: https://www.raisesummit.com/startup-competition

Expected remote: https://github.com/jechaviz/raise_the_stakes_ai_startup_competition_contest

## Production Target

Goal: application-ready package for RAISE the STAKES 2026.

Operational deadline: 2026-06-10. The official page also shows a lower-page
copy conflict saying "Application closes 1st of July"; VC4A and the official
milestone section show June 10, so June 10 is treated as the hard date.

Event: 2026-07-08 and 2026-07-09 at Le Carrousel du Louvre, Paris.

## Deliverables

- `docs/ELIGIBILITY_CHECKLIST.md`: source-backed eligibility and secure inputs.
- `docs/PRODUCT_AI_PROPOSED.md`: AI startup product proposal.
- `docs/LANDING_DECK_VIDEO_OUTLINE.md`: landing, deck, and demo video outline.
- `docs/TRACTION_PROOF_MINIMUM.md`: minimum validation pack.
- `docs/APPLICATION_PACKET.md`: Dealum-ready answers and field prep.
- `docs/COMPETITIVE_BATTLECARD.md`: competitive landscape, moat, wedge, and
  objection handling.
- `docs/JUDGING_SCORECARD.md`: RAISE judging narrative and score targets.
- `docs/STRATEGIC_BRIEF.generated.md`: generated strategic brief from the
  shared V core.
- `docs/RISKS.md`: risk register and mitigations.
- `docs/AUTOMATION_PLAN.md`: WAIBAv-driven external form workflow.
- `submission/dealum_payload.json`: structured application payload.
- `submission/dealum_form_map.yml`: external form field map.
- `evidence/evidence_ledger.md`: public/private evidence index.
- `evidence/public/manifest.json`: generated V manifest for the RAISE profile.

## Reusable Core

Shared V package generator:

`C:\git\v_projects\contestops_ai`

Commands:

```powershell
v run C:\git\v_projects\contestops_ai -- manifest --profile raise evidence\public\manifest.json
v run C:\git\v_projects\contestops_ai -- checklist --profile raise docs\RULES_CHECKLIST.generated.md
v run C:\git\v_projects\contestops_ai -- evidence --profile raise docs\EVIDENCE.generated.md
v run C:\git\v_projects\contestops_ai -- application-packet --profile raise docs\APPLICATION_PACKET.generated.md
```

Web demo workspace:

`C:\git\websites\raise_the_stakes_ai_startup_competition`

## Production Gate

- Eligibility packet complete.
- Product narrative and AI core evidence complete.
- Demo panel reachable locally and ready for deploy.
- Deck and video script ready.
- Minimum traction proof ledger prepared.
- Dealum payload mapped and automation playbooks validated.
- Final external submit runs only from an authenticated Dealum session with the
  final package flag set.
