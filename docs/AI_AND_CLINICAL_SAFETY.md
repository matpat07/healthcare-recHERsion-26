# AI and clinical safety

## Existing, verified functionality

No AI, rules, medical content, clinical integration or validation exists. No clinical outcome claims are supported.

## Proposed functionality

Start with deterministic descriptive rules. Show range, counts, denominator, missing days, source records, rule version and limitations. Synthetic example: "You recorded headaches on 4 of the 10 days with entries. Days without entries are unknown." Do not convert frequency into diagnosis, causation, treatment advice or unsupported risk scores.

Each rule needs reviewed minimum-data criteria, exclusions and quality checks. Sparse/contradictory/duplicate/future-dated inputs produce insufficient-data or quality messages. Missing entries never mean no symptoms. Comparisons show coverage for both windows. Cycle views tolerate irregularity and do not promise ovulation or contraceptive reliability.

Maintain a rule registry: owner, purpose, inputs, thresholds, exclusions, template, references where relevant, reviewer, version and regression fixtures. Recompute after edits/deletion. Exports distinguish reported facts from derived observations.

Education requires authoritative sources, review responsibility/date, revision history and error reporting. Review is a future release requirement, not an existing credential. Explain scope beside observations: supports records and healthcare conversations; does not diagnose or monitor emergencies.

Direct concerns toward qualified healthcare professionals. Clinician review and source verification are required before publishing urgent-care wording or local resources. Do not invent automated triage or reassurance from missing data.

Any future generative AI requires a separate purpose, data/vendor review, evaluation for unsupported diagnoses and harmful reassurance, and user control. Do not send journals to AI providers by default.

## Decisions still needed

Clinical owner, approved sources, rule thresholds, escalation wording/geography, review cadence, safety incident workflow and regulatory classification. Do not advertise clinical validation or certification without evidence.
