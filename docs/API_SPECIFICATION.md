# API specification

## Existing, verified functionality

No endpoints, server, authentication contracts or validators exist. Every endpoint below is a draft proposal.

## Proposed functionality

Draft same-origin JSON API `/api/v1`; private requests require server session verification and owner-scoped authorization.

| Method | Draft path | Purpose |
| --- | --- | --- |
| GET, PATCH | /me | Minimal profile/preferences |
| GET, POST | /symptoms | Paginated list/create |
| GET, PATCH, DELETE | /symptoms/{id} | Owner-scoped detail/edit/delete |
| GET, POST | /bleeding-entries | Optional daily records |
| PATCH, DELETE | /bleeding-entries/{id} | Edit/delete |
| GET, POST | /journal-entries | List/create |
| GET, PATCH, DELETE | /journal-entries/{id} | Detail/edit/delete |
| GET | /resources and /resources/{slug} | Public reviewed education |
| GET | /observations | Bounded range and provenance |
| POST | /appointment-summaries/preview | Selected records and questions |
| POST | /exports | Request scoped export |
| GET | /exports/{id} | Owner-scoped status/download |
| GET, POST | /consents | Status/purpose-specific action |
| POST | /privacy-requests | Account export/deletion request |
| GET | /privacy-requests/{id} | Lifecycle status |

Draft symptom payload: symptomCode, severity (scale pending), occurredAt (ISO instant), timezone (IANA), optional bounded note. Reject client userId; derive identity from session. Return server ID, timestamps and version. Updates supply expected version.

Lists use bounded from/to/limit and opaque cursor with stable date/ID ordering. Draft status codes: 201 create, 200 read/update, 204 immediate delete, 202 asynchronous job, 400 invalid request, 401 session required, 404 missing/inaccessible object, 409 edit conflict, 422 semantic validation, 429 rate limit, 500 safe generic failure.

Error shape: `{error: {code, message, fieldErrors?, requestId}}`. Never expose health text, SQL or another user's object existence. Health responses use private/no-store caching. Define CSRF/origin handling, request limits and idempotency before implementation.

## Decisions still needed

OpenAPI schemas, exact enums/limits, authentication callback routes, consent categories, export format/expiry, idempotency retention and synchronous versus queued processing.
