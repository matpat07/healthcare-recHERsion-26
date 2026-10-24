# Backend

## Existing, verified functionality

No server, database, API handlers, validation, authentication or environment configuration exists.

## Proposed functionality

Start with modular services inside the proposed Next.js server: identity, consent, records, journal, education, summaries, observations and privacy requests. Use PostgreSQL and reviewed migrations; select an ORM later. One deployable service is sufficient initially.

Flow: authenticate -> validate purpose/input -> authorize ownership -> transaction -> minimal typed response. Derive owner identity from the server session, never a client-supplied user ID. Managed authentication should own credentials and session lifecycle.

Validate lengths, vocabulary, severity, timestamps, timezone, pagination and request size on the server. Use parameterized access. Return safe errors with stable codes and request IDs, without SQL exceptions or health text. Use optimistic versions for edit conflicts. Invalidate derived outputs after changes. Rate-limit sensitive operations. Initial rule-based observations require no AI vendor.

## Decisions still needed

Runtime, ORM, managed providers/regions, session model, export/deletion job mechanism, backup objectives, retention and operational owner.
