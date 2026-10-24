# Pipeline and roadmap

## Existing, verified functionality

No build/CI/release workflow exists. Audit is complete at repository level; this change supplies documentation only.

## Proposed functionality

| Phase | Deliverable | Exit criteria |
| --- | --- | --- |
| 1. Audit | Facts and gap inventory | Source/config/instruction checks documented without invented functionality |
| 2. Documentation/design | Product, architecture and tokens | Audience, stack, data scope and safety direction resolved |
| 3. Landing/brand | Public synthetic prototype | Responsive interactive previews, keyboard/reduced-motion support and measured performance |
| 4. Core tracking | Dashboard/logger/history/journal and optional cycle UI | Synthetic fixture flows cover empty/error/edit/delete |
| 5. Secure persistence | Authentication, database, consent and privacy operations | Ownership, persistence, restore and lifecycle tests pass |
| 6. Observations | Versioned rules and appointment summaries | Provenance, missingness, clinical wording and export accuracy reviewed/tested |
| 7. Deployment | Release candidate and operations | Accessibility/security checks, monitoring, rollback and incident owner ready |

Real-user health collection is blocked until phase 5 protections are verified. Safety/testing apply throughout, not only in phase 7.

Future PR checks: formatting, lint, types, domain tests, isolated database integration tests, critical browser flows, production build, secret/dependency scanning and migration review. Choose executable tools after stack approval. Previews use synthetic data and separate credentials.

## Decisions still needed

Owners, staffing, schedule, CI provider, reviewers, budget and release thresholds. No dates or provider commitments are implied.
