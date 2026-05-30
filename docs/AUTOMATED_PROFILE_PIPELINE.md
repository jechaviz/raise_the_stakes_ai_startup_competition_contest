# Automated Profile Pipeline

Purpose: turn `C:\git\customers\yo` into application evidence without copying
private profile content into the public RAISE repository.

## Pipeline

1. Generate a role-level redacted manifest:

```powershell
C:\git\v\v.exe -o $env:TEMP\vimport_raise_profile.exe run C:\git\v_projects\vimport -- profile-manifest C:\git\customers\yo evidence\public\redacted_source_manifest.json --label raise_profile
```

2. Generate an application-fit packet from the redacted manifest:

```powershell
C:\git\v\v.exe -o $env:TEMP\vimport_raise_profile.exe run C:\git\v_projects\vimport -- profile-application-packet evidence\public\redacted_source_manifest.json evidence\public\vimport_profile_application_packet.json --opportunity raise_the_stakes
```

3. Generate a public schema and private fill template for secure Dealum fields:

```powershell
C:\git\v\v.exe -o $env:TEMP\vimport_raise_profile.exe run C:\git\v_projects\vimport -- profile-secure-inputs evidence\public\secure_inputs.public_schema.json --opportunity raise_the_stakes
C:\git\v\v.exe -o $env:TEMP\vimport_raise_profile.exe run C:\git\v_projects\vimport -- profile-secure-inputs evidence\private\profile\secure_inputs.template.json --opportunity raise_the_stakes
```

4. Capture Veloclaw policy posture:

```powershell
C:\git\v\v.exe -o $env:TEMP\veloclaw_raise.exe run C:\git\v_projects\veloclaw policy-check --capability "inspect:shape@vimport[source=yo_redacted]"
```

5. Validate the RAISE profile packet with WAIBAv:

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File C:\Users\jecha\.codex\skills\waiba\scripts\invoke-waiba.ps1 run C:\git\v_projects\contests\worth_it\raise_the_stakes_ai_startup_competition\automation\waiba\profile_application_packet.playbook.yml prod
```

## Current Result

- `evidence/public/vimport_profile_application_packet.json` reports readiness
  score `100` from redacted role-level evidence.
- `evidence/public/secure_inputs.public_schema.json` names the secure Dealum
  fields without values.
- `evidence/private/profile/secure_inputs.template.json` exists locally and is
  ignored by git.
- Veloclaw policy marks direct `inspect:shape@vimport[source=yo_redacted]` as
  medium risk requiring operator approval.
- WAIBAv verifies the public packet, private template existence, policy receipt,
  and redacted manifest boundary.

## Guardrails

- Do not feed raw OCR/profile documents to `shape`, LLM, or browser automation.
- Use only `redacted_source_manifest.json` for public AI/application shaping.
- Fill secure inputs locally, then transfer them in the authenticated Dealum
  session after human review.
- Commit receipts and public schemas, never private values.
