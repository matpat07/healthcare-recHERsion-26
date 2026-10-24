# Frontend

## Existing, verified functionality

No framework, manifest, dependencies, routes, components or UI exists. No visual or browser test has run.

## Proposed functionality

Recommend TypeScript and React/Next.js for server-rendered public content and a separate authenticated layout. This is provisional, not installed.

Draft public routes: `/`, `/features`, `/learn`, `/learn/[slug]`, `/privacy`, `/accessibility`. Account routes: `/sign-in`, `/onboarding`. Private routes: `/app`, `/app/symptoms`, `/app/timeline`, `/app/cycle`, `/app/journal`, `/app/observations`, `/app/appointments`, `/app/settings/privacy`.

Landing storyboard:

1. Obsidian immersive hero, oversized editorial "Your health. A clearer picture.", porcelain text, violet/teal organic SVG form and honest availability CTA.
2. Porcelain editorial section: record, understand, prepare; one-time scroll reveals preserve reading order.
3. Keyboard-accessible feature tabs show logger, timeline and journal with clearly labeled synthetic records and reset controls.
4. Illustrative animated chart shows counts, date range and missing data; equivalent table and instant reduced-motion view remain available.
5. Appointment preview lets visitors select synthetic records and see the summary change.
6. Evidence and privacy sections describe only protections actually implemented before publication.

Use CSS/SVG biological forms first. Consider a lazily loaded Three.js/React Three Fiber island only if a measured user benefit justifies bundle cost, mobile performance and static fallback. Do not add 3D for decoration alone.

Private UI: calm navigation, prominent logging action, accessible forms, explicit empty/loading/error/expired-session states. Never put private results in public caches, static output, analytics or URLs. Route guards supplement server authorization.

Proposed performance targets: LCP <=2.5s, INP <=200ms, CLS <=0.1 at the 75th percentile. These are not measured results. Test low-end mobile and slow networks before adding effects.

## Decisions still needed

Framework/package manager approval, chart library, fonts, supported browsers, deployment rendering model and prototype-versus-public-release scope.
