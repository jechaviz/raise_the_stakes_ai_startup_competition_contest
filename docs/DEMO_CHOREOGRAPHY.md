# Demo Choreography

Prepared: 2026-05-29

Goal: make judges feel that ContestOps AI is a live application-ops product,
not a static writing assistant.

## Demo Principle

The hero is the workflow:

source -> rules -> evidence gaps -> application assets -> field map -> form prep
-> receipt.

Every beat should answer one judging criterion: team, distinctive product,
traction/validation, and market scale.

## 3:30 Core Demo

| Time | Screen | Say | Proof |
|---:|---|---|---|
| 0:00 | RAISE page or source snapshot | "RAISE is the live test: AI startup, real deadline, judges care about team, distinctiveness, traction, and market scale." | RAISE source URL and `evidence/source_snapshot.md` |
| 0:20 | Risk/deadline note | "The system flags operational risk. VC4A shows June 10; RAISE FAQ shows July 1, so we operate to the earliest deadline." | `docs/RISKS.md` |
| 0:40 | Generated checklist | "The first output is not prose. It is eligibility, requirements, and missing proof." | `docs/RULES_CHECKLIST.generated.md` |
| 1:05 | Application packet | "Then it turns the opportunity into a submit-ready narrative and structured answers." | `docs/APPLICATION_PACKET.md`, `submission/application_answers.md` |
| 1:30 | Evidence ledger | "Claims are gated by evidence. Public artifacts stay public; sensitive founder proof stays private." | `evidence/evidence_ledger.md` |
| 1:55 | Competitive intelligence | "This is not a portal, grant writer, or generic browser agent. It is founder application ops." | `docs/COMPETITIVE_INTELLIGENCE.md` |
| 2:20 | Dealum payload and field map | "The workflow moves from strategy to execution: payloads and field maps for the external portal." | `submission/dealum_payload.json`, `submission/dealum_form_map.yml` |
| 2:45 | WAIBAv playbook or trace | "Automation is receipt-backed and human-approved for authenticated actions." | `automation/waiba`, `automation/output` |
| 3:10 | Pilot sprint playbook | "The next proof gate is user validation: five conversations, two validations, one live run, one paid or pilot-intent signal." | `docs/PILOT_SPRINT_PLAYBOOK.md` |
| 3:25 | Close | "ContestOps AI turns AI build speed into real-world startup outcomes." | Judging scorecard |

## 90-Second Version

1. Open with RAISE: "This competition is the live demo."
2. Show generated checklist: "The product reads the opportunity and extracts
   what must be true."
3. Show evidence ledger: "It blocks unsupported claims instead of inventing
   them."
4. Show Dealum payload/field map: "It prepares the external submission."
5. Show pilot sprint: "Now we validate with real founder opportunities."
6. Close: "Portals collect applications; ContestOps AI makes founders ready."

## 5-Minute Version

Add two deeper beats:

- Competitive map: compare against portals, grant/RFP systems, proposal tools,
  generic agents, and consultants.
- QA gate: show one missing item and explain how the system routes it to secure
  private evidence instead of placing it in public docs.

## Talk Track

Use this exact spine:

"Founders are building faster with AI, but opportunity execution is still
manual. A competition or grant is not just a form. It is rules, proof, pitch,
media, attachments, portal fields, deadlines, and receipts. ContestOps AI turns
that mess into an operating workflow. The RAISE packet you are seeing was
generated, checked, mapped, and prepared by that workflow."

## Visual Rules

- Show real files and generated artifacts, not abstract slides first.
- Keep terminal output minimal; use docs and structured JSON/YAML as proof.
- Never show credentials, private founder data, private customer proof, or live
  authenticated portals unless the user explicitly controls the session.
- If the web demo is unstable, use the repo package as the demo. The audit trail
  is stronger than a fragile UI walkthrough.
- End on the judge scorecard, not the technical architecture.

## Objection Triggers During Demo

| If judge asks | Jump to | One-line response |
|---|---|---|
| "Is this just writing?" | Rules checklist and evidence ledger | "Writing is one artifact; the product runs the application workflow." |
| "Can agents do this?" | Field map and WAIBAv playbook | "Agents can operate; this product knows what to operate and what evidence gates matter." |
| "Where is traction?" | Pilot sprint playbook | "The sprint is designed to convert this from product proof into user proof before final submit." |
| "What about privacy?" | Evidence ledger | "Public docs are summaries; sensitive proof remains private and redacted." |
| "What is the moat?" | Competitive intelligence | "Repeated opportunity rubrics, field maps, evidence patterns, and receipts." |

## Pre-Demo Checklist

- Confirm no private data is visible in open tabs.
- Open the repo at this package, not the broader workspace.
- Open these files in order:
  - `docs/RULES_CHECKLIST.generated.md`
  - `docs/APPLICATION_PACKET.md`
  - `evidence/evidence_ledger.md`
  - `docs/COMPETITIVE_INTELLIGENCE.md`
  - `submission/dealum_payload.json`
  - `submission/dealum_form_map.yml`
  - `docs/PILOT_SPRINT_PLAYBOOK.md`
- Have the RAISE and VC4A source URLs ready for deadline questions.
- Keep the final line memorized.

## Fallback Plan

If internet, portal login, or live automation fails:

1. Say: "The product is designed for deadline-safe operations, so I will show
   the receipt-backed prepared package instead of risking a live portal action."
2. Show the local source snapshot, checklist, payload, field map, and playbook.
3. Explain that final authenticated submission requires human confirmation.
4. Return to the judge scorecard and market wedge.

## Sources

- RAISE Startup Competition: https://www.raisesummit.com/startup-competition
- VC4A RAISE listing: https://vc4a.com/raise/raise-summit-2026-startup-competition/
- Dealum: https://dealum.com/
- OpenAI ChatGPT agent help: https://help.openai.com/en/articles/11752874-chatgpt-agent
- Anthropic computer use tool: https://platform.claude.com/docs/en/agents-and-tools/tool-use/computer-use-tool
