# Auracare - Women Health Companion

Audit: 2026-10-24, commit `5d12b73` (Initial commit).

## Existing, verified functionality

The repository tracks only `.gitattributes`, containing `* text=auto`. Inventory and history checks found no application source, package manifest, lockfile, frontend, backend, database, API, authentication, environment configuration, UI, routes, tests, or deployment configuration. README.md and AGENTS.md were absent. Ancestor AGENTS.md checks found no instructions. No runnable product functionality exists to preserve, replace, or test.

The untracked `Microsoft/Windows/PowerShell/ModuleAnalysisCache` is unrelated machine-generated data and was left untouched. Git internals and that cache are excluded from application-source assessment. No secrets were read. Audit used file inventory, git ls-files/status/log, and instruction-file checks; it did not establish runtime behavior.

## Proposed functionality

Auracare helps users record symptoms, understand personal patterns, access reviewed education, and prepare for healthcare conversations. Separate public marketing from an authenticated health application. Begin with reliable records and transparent rules, without diagnostic claims.

Recommended architecture, pending approval: TypeScript, React/Next.js, server-side services, PostgreSQL, and managed authentication. None is installed. There is no existing technology stack to change.

Documentation index:

- [Product overview](docs/PRODUCT_OVERVIEW.md)
- [Features](docs/FEATURES.md)
- [Brand identity](docs/BRAND_IDENTITY.md)
- [Design system](docs/DESIGN_SYSTEM.md)
- [Frontend](docs/FRONTEND.md)
- [Backend](docs/BACKEND.md)
- [Architecture](docs/ARCHITECTURE.md)
- [Data model](docs/DATA_MODEL.md)
- [User flows](docs/USER_FLOWS.md)
- [Pipeline and roadmap](docs/PIPELINE.md)
- [API specification](docs/API_SPECIFICATION.md)
- [AI and clinical safety](docs/AI_AND_CLINICAL_SAFETY.md)
- [Security and privacy](docs/SECURITY_AND_PRIVACY.md)
- [Testing](docs/TESTING.md)
- [Deployment](docs/DEPLOYMENT.md)

There are no verified install, development, build, or test commands. Add them after scaffolding. No application code or dependency was changed during this documentation phase.

## Decisions still needed

Confirm stack, audience, age policy, launch geography, clinical reviewer, hosting/data region, authentication provider, and retention policy. Next: resolve architecture decisions, then build an accessible landing prototype with synthetic data.
