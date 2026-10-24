# Design system

## Existing, verified functionality

No tokens, components, CSS or animation libraries exist.

## Proposed functionality

Use exact base colors from BRAND_IDENTITY with semantic aliases for canvas, text, action, focus, selected and error. Decorative palette colors must not imply clinical status.

Spacing: 4/8/12/16/24/32/48/64/96px. Public max-width approximately 1200px, reading width 60-72 characters, mobile gutters 20px and desktop 40-64px. Use content-driven 4/8/12-column layouts around 640/960/1280px. Support 320px without horizontal page scrolling.

Type: fluid 40-88px hero, 28-48px section headings, 20-24px card headings, 16-18px body and 14px metadata. Radius: 12px fields, 20px cards; restrained borders and shadows. Pills suit tags rather than every container.

Components: navigation, buttons, labeled fields, date/time controls, symptom selector, severity input, record card, timeline, chart/table pair, article card, consent panel, dialog, alerts, loading and empty states. Define hover, keyboard focus, selected, disabled, invalid, loading, error and success behavior. Preserve input on failure and announce save results. Use native controls where practical.

Target WCAG 2.2 AA, pending verification: visible focus, skip link, semantic headings, explicit labels, accessible dialogs, 200% zoom, and approximately 44px touch targets. Charts require text summaries and equivalent tables. Error states need words, not just color.

Motion: 150-220ms control feedback, 300-500ms one-time section reveals using opacity/transform. Progressive enhancement keeps content visible without JavaScript. Reduced motion removes parallax, morphing, animated scrolling and chart drawing. Avoid scroll hijacking. Smooth anchor scrolling is optional and disabled for reduced motion.

## Decisions still needed

Final tokens, contrast testing, browser matrix, component ownership and chart tooling. No 3D dependency is currently justified.
