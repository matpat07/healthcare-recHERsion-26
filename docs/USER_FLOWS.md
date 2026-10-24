# User flows

## Existing, verified functionality

No journeys, navigation or forms are implemented.

## Proposed functionality

1. Discover: hero -> labeled synthetic demo -> scope/privacy -> sign-in when available.
2. Onboard: account -> plain-language purposes -> separate optional consent -> timezone/preferences -> empty dashboard. Cycle tracking is skippable.
3. Log: symptom -> occurrence/severity -> optional note -> save -> persisted confirmation -> history. Errors preserve in-memory input; duplicate submissions are prevented.
4. Review: filter timeline/table -> inspect -> edit with version check or confirmed delete -> refresh dependent outputs. Concurrent edits are resolved visibly.
5. Journal: date -> write -> explicit save status -> history. Warn before leaving unsaved work; do not promise offline recovery before it exists.
6. Learn: topic -> reviewed article -> sources/review date -> optional appointment question. Reading choices do not imply diagnoses.
7. Observe: range -> data sufficiency check -> counts, coverage, sources and limitations. Insufficient-data states explain missingness without pressuring disclosure.
8. Prepare: range/records -> questions -> preview -> exclude sections -> export. Explain that downloaded copies are outside application deletion control.
9. Privacy: review purposes -> withdraw optional consent/export/delete -> confirm impact and timing -> completion status.
10. Session expiry: reauthenticate and safely resume; never imply unsaved records were persisted.

## Decisions still needed

Sign-in methods, onboarding length, unsaved-input recovery, deletion wording, stored versus on-demand summaries, support and usability research.
