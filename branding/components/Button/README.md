# Button

Use buttons to commit an action; use links to move between pages. Use at most one **primary** (`ts-btn-primary`, a `ledger` fill with an `on-ledger` label) per view, for the action the page exists for. Use the default secondary for document and supporting actions, and **quiet** (`ts-btn-quiet`) for low-stakes actions inside cards and tables.

- The consumer provides a `<button>` (or an `<a>` for navigation) with the class `ts-btn` and an optional variant.
- Labels start with a verb, use sentence case and are specific: “Invest from A$10,000”, not “Invest now!”.
- Controls are 44px tall so they work as touch targets. Focus shows `focus-ring`.
- Never use a primary button for an irreversible action without a confirmation step that restates the amount and instrument.
