# Automation Plan

Goal: prepare, fill, verify, and execute the RAISE application workflow through
Dealum when the package is ready.

## Surfaces

- Official RAISE page: https://www.raisesummit.com/startup-competition
- Partner listing: https://vc4a.com/raise/raise-summit-2026-startup-competition/
- Application portal: https://app.dealum.com/
- Demo panel: `C:\git\websites\raise_the_stakes_ai_startup_competition`
- Evidence package: this subrepo.

## WAIBAv Playbooks

- `automation/waiba/dealum_draft_prepare.playbook.yml`
  - ensures output folders;
  - checks payload, field map, generated manifest, and application answers;
  - writes a JSONL trace receipt.
- `automation/waiba/dealum_live_form.playbook.yml`
  - opens Dealum or VC4A application route;
  - detects authenticated session state through operator-visible review;
  - maps payload fields to visible controls;
  - saves draft when available;
  - submits final application when `RAISE_FINAL_PACKAGE_READY=1`;
  - captures receipt paths.

## Payload Sources

- `submission/dealum_payload.json`
- `submission/dealum_form_map.yml`
- `docs/APPLICATION_PACKET.md`
- `docs/ELIGIBILITY_CHECKLIST.md`
- `evidence/evidence_ledger.md`
- `evidence/public/manifest.json`

## Receipts

- `automation/output/dealum_draft_prepare_trace.jsonl`
- `automation/output/dealum_live_form_trace.jsonl`
- `automation/output/dealum_form_snapshot.json`
- `automation/output/dealum_confirmation.png`
- `automation/output/submission_receipt.json`

## Execution Cadence

- Daily until submit: refresh source pages and deadline notes.
- Before first draft: validate payload and field map.
- First authenticated Dealum session: learn exact field labels/selectors.
- Before final submit: run checklist against payload and evidence ledger.
- Final submit: execute live form playbook with receipt capture.
