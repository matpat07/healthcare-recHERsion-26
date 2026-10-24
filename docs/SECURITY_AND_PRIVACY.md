# Security and privacy

## Existing, verified functionality

No data collection, authentication, consent, encryption configuration, privacy policy or security tests exist. Compliance is not established.

## Proposed functionality

Treat symptom/cycle/journal information as sensitive. Minimize collection and specify purpose per field. No advertising trackers, session replay or health payload analytics in private views.

| Threat | Required control |
| --- | --- |
| Cross-user access | Server-derived identity, owner-scoped queries, denial tests for every operation/export |
| Session theft/CSRF | Managed authentication, secure HttpOnly cookies where appropriate, expiry/revocation and origin/CSRF controls |
| Injection/XSS | Server validation, parameterized queries, safe text rendering and reviewed sanitization |
| Accidental disclosure | Private cache policies; no health details in URLs/logs/errors; synthetic development data |
| Storage/export exposure | TLS, reviewed encryption at rest/key access, private database, expiring protected downloads and cleanup |
| Operational loss | Encrypted backups, restore tests, incident owner and credential rotation |

Separate required service purposes from optional analytics/communications; record purpose and policy version, support withdrawal. User controls cover access, correction, export and deletion. Define propagation to observations, exports, processors and backups, with truthful completion timing and justified retention exceptions. Downloaded copies remain under user control.

Future secret templates contain placeholders only; server secrets never enter browser bundles or Git. Limit administrative access and retain audit metadata without copying health text.

## Decisions still needed

Jurisdiction, legal basis/obligations, age policy, controller/processors, residency, retention, backup expiry, recovery, incident response and reviewed privacy notice. This plan is not a compliance declaration.
