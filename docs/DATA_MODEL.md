# Data model

## Existing, verified functionality

No schema, migrations, tables or stored product data exist. The following is conceptual, not an implemented database schema.

## Proposed functionality

| Entity | Candidate fields and constraints |
| --- | --- |
| User | id, unique external identity subject, timezone, createdAt; minimal profile |
| ConsentEvent | userId, purpose, policyVersion, action, occurredAt; consent/withdrawal history |
| SymptomEntry | id, userId, symptomCode, severity, occurredAt, localDate, timezone, optional note, version, timestamps |
| BleedingEntry | id, userId, localDate, timezone, flow, optional note, version; optional domain |
| JournalEntry | id, userId, entryDate, timezone, body, version, timestamps; bounded private text |
| Resource | slug, title, body, references, reviewer, reviewedAt, publication status |
| Observation | userId, ruleVersion, window, sourceIds, coverage, output, generatedAt; recomputable |
| AppointmentSummary | userId, selectedIds, range, userNotes, snapshotVersion; persist only if needed |
| PrivacyRequest | userId, type, state, requestedAt, completedAt; no copied health text |

Use foreign keys, owner-scoped queries, indexes on owner/date, server IDs and optimistic version checks. Store instants in UTC and preserve IANA timezone/local dates where relevant. Bleeding days are date records. Missing days are unknown, not symptom-free. Edits/deletion must invalidate observations and summary artifacts.

Avoid collecting name, address, birth date, pregnancy status or anatomy details without a reviewed purpose. Separate identity from optional health profile.

## Decisions still needed

Exact types, required fields, symptom/severity vocabulary, note limits, duplicate-day policy, deletion cascades, retention, observation storage versus computation and key management.
