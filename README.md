# AgentField Plans

Public, versioned workout plans for the AgentField Connect IQ DataField.

## Published contract

- Runtime alias: [`current.v1.json`](current.v1.json)
- Current immutable revision: [`plans/kaito-fixture-1/revision-7.json`](plans/kaito-fixture-1/revision-7.json)
- Runtime JSON Schema: [`connectiq-runtime-plan-v1.schema.json`](connectiq-runtime-plan-v1.schema.json)
- Archived legacy schema: [`static-plan-v1.schema.json`](static-plan-v1.schema.json)

The active profile is `connectiq-runtime-v1`: a closed, flat and bounded transport generated from validated AgentField IR. Revision 7 exercises four supported stages: warm-up, distance work with pace target, timed recovery with heart-rate target, and cooldown.

## Safety boundary

- Static JSON only; no server-side application or custom backend.
- No credentials, personal data, device identifiers, activity history, or health data.
- The watch strictly validates the complete runtime plan before persisting or loading it.
- Published revisions are immutable; updates use a higher revision number.
- `current.v1.json` must be byte-identical to an immutable revision before publication.
- Starting, cancelling or finishing a session does not consume the current plan; it remains reusable until a validated higher revision replaces it.
