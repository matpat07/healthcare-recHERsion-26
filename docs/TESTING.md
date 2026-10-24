# Testing

## Existing, verified functionality

No executable suite, test scripts, compiler configuration or app exists. No runtime/build/accessibility/performance tests have passed. Audit checks were inventory, tracked files, status/history, .gitattributes and README/AGENTS presence. See README for scope.

## Proposed functionality

- Domain: timestamp/local-date interpretation, missing versus zero, validation, duplicates, rule boundaries/denominators and recomputation.
- API/database: cross-user list/read/edit/delete/export denial, expired sessions, CSRF where applicable, transactions, pagination, optimistic conflicts and idempotency.
- Browser: onboarding, consent, log/save/reload/edit/delete, journal, optional cycle, summary/export and deletion progress.
- Accessibility: automated checks plus keyboard, screen reader, zoom, dialogs, chart/table equivalence, mobile and reduced motion.
- Safety: descriptive wording, sparse-data behavior, source provenance, reviewed content and fact/observation separation.
- Operations: migrations, backup restore, export expiry, deletion propagation and log redaction.
- Performance: measure proposed FRONTEND targets on representative mobile hardware/networks.

Use synthetic fixtures only. A real-user release requires persistence across reload and owner isolation demonstrated end to end. Select runners after stack approval.

Documentation validation: required files, internal links, verified/proposed/decision sections, consistent claims and whitespace. These checks do not prove product functionality.

## Decisions still needed

Test tooling, browser matrix, CI environment, clinical/accessibility reviewers, coverage expectations and launch thresholds.
