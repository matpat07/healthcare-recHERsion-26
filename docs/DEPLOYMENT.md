# Deployment

## Existing, verified functionality

No host, domain, runtime, CI, container, environment template, database connection or deployment command exists.

## Proposed functionality

Choose managed hosting compatible with the approved framework and private managed PostgreSQL in an approved region. Review identity provider/processors before enabling accounts. Separate local, preview, staging and production secrets, identities and databases. Previews use synthetic data.

Future configuration categories, not existing variable names: database connection, identity issuer/credentials, canonical origin, session secret if needed, export storage and observability. Validate configuration at startup without printing values; document server/client exposure explicitly.

Release: CI -> preview review -> staging migration/flows -> backup/restore readiness -> controlled production migration -> deploy -> synthetic smoke tests -> monitoring. Prefer backward-compatible migrations; roll the application back independently and avoid schema reversal that loses records.

Operations require HTTPS, private caching, security headers, session configuration, least privilege, rate limits, encrypted backups, artifact cleanup, deletion processing, safe logs and uptime/error monitoring. Assign incident, rotation and restoration ownership.

Launch gates: owner isolation, consent/privacy review, clinical wording review, export/deletion checks, accessibility/reduced motion, mobile performance, dependency review and rehearsed restore/rollback. Public claims must match deployed protections.

## Decisions still needed

Host/region, domain, runtime versions, cost, availability and recovery objectives, release owner, monitoring, secret manager and support process.
