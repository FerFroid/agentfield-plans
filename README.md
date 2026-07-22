# AgentField Plans

Public, versioned workout plans for the AgentField Connect IQ DataField.

## Published contract

- Runtime alias: [`current.v1.json`](current.v1.json)
- Immutable revision 1: [`plans/agentfield-main/revision-1.json`](plans/agentfield-main/revision-1.json)
- JSON Schema: [`static-plan-v1.schema.json`](static-plan-v1.schema.json)

The v1 profile is deliberately narrow: one timed work step followed by one timed recovery step, both with open targets. The first short acceptance plan is `AgentField 10/10`: `ACELERA` 10 s and `RECUPERA` 10 s.

## Safety boundary

- Static JSON only; no server-side application or custom backend.
- No credentials, personal data, device identifiers, activity history, or health data.
- The watch validates every plan strictly and accepts only a newer revision.
- Published revisions are immutable; updates use a new revision number.
- Changing `current.v1.json` requires publishing the same content under a new immutable revision first.
