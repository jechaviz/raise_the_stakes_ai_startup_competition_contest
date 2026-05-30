# Local Ecosystem Evidence

## Purpose

Map the reusable local ecosystem into application proof for RAISE without
publishing secrets or private customer data.

## Evidence Map

| Asset | Role in RAISE packet | Current status | Next action |
|---|---|---|---|
| `contestops_ai` | Generates manifests, eligibility, evidence, application packets, strategy briefs, and scorecards. | Active and tested. | Keep as shared V core. |
| Product wrapper | Provides RAISE-specific CLI commands over the shared core. | Active and tested. | Keep thin and generic. |
| Web demo | Shows judge-facing war room, evidence, ROI, and competition narrative. | Active at local preview. | Replace `TBD` public URLs once deployed. |
| WAIBAv | Validates playbooks and prepares external Dealum/form workflows. | Active with RAISE playbooks. | Use visible authenticated session for final submit. |
| VImport | Provides extraction, redaction, local vault refs, contracts, and evidence-friendly source handling. | Active with `profile-manifest`, `shape`, and jobapply contracts. | Use redacted manifests before any AI shaping. |
| Veloclaw | Provides policy-gated agent/capsule governance and ecosystem scan logic. | Read-only this slice; capability snapshot saved in `evidence/public/veloclaw_vimport_capabilities.json`. | Re-run isolated once pending local work is reconciled. |
| `C:\git\customers\yo` | Private founder/product proof source. | Scanned by redacted manifest only. | Keep public summary only; store raw proof privately. |

## VImport Commands Used

```powershell
v run . -- profile-manifest C:\git\customers\yo evidence\public\redacted_source_manifest.json --label raise_profile
v run . -- shape evidence\public\redacted_source_manifest.json "RAISE startup application packet schema only; no raw PII" --out evidence\public\vimport_profile_shape.json
v run . -- shape-loop evidence\public\redacted_source_manifest.json "resume refs, answer packet, evidence receipts, secure fields" --out evidence\public\vimport_profile_shape_loop.json
v run . -- ready-api jobapply evidence\public\vimport_jobapply_ready_api.yml
v run . -- jobapply-contract evidence\public\vimport_jobapply_contract.yml
v run . -- waiba-plan automation\waiba\dealum_live_form.playbook.yml evidence\public\vimport_waiba_plan.yml
```

Policy: commit only redacted receipts and public source summaries. Do not
commit `.env`, vault material, personal documents, credentials, tax IDs, or
private customer artifacts.

## Veloclaw Use

Veloclaw was used as a read-only governance reference. Its useful commands for
the next pass are:

```powershell
C:\git\v\v.exe run . vimport-capabilities --path C:\git\v_projects\vimport --json
C:\git\v\v.exe run . vimport-common-plan --path C:\git\v_projects --json
C:\git\v\v.exe run . policy-check --capability "inspect:shape@vimport[source=yo_redacted]"
```

This slice did not modify Veloclaw because the repository already had unrelated
local edits and commits ahead of origin. The executed command used a temporary
binary output to avoid writing `veloclaw.exe` inside that dirty repo.

## WAIBAv Commands Used

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File C:\Users\jecha\.codex\skills\waiba\scripts\invoke-waiba.ps1 validate C:\git\v_projects\contests\worth_it\raise_the_stakes_ai_startup_competition\automation\waiba\profile_private_scan.playbook.yml debug
powershell -NoProfile -ExecutionPolicy Bypass -File C:\Users\jecha\.codex\skills\waiba\scripts\invoke-waiba.ps1 run C:\git\v_projects\contests\worth_it\raise_the_stakes_ai_startup_competition\automation\waiba\profile_private_scan.playbook.yml prod
```

The profile scan checks existence and boundaries only. It does not extract or
publish private document content.
