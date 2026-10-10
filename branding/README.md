# TokenSec brand guide

Live, browsable version: https://claude.ai/artifact/ULSsNbwkZTrtj7MYaWwiLd. Tokens are in `tokens.json`, compiled to `tokens.css` (custom properties, light and dark themes, and `.ts-*` type classes). Component styles are in `components/bundle.css`.

TokenSec tokenises securities: ordinary and preference shares, corporate bonds and notes, and other regulated instruments. Each token is a legal interest recorded on a register. TokenSec is a CoinPort business, and the brand borrows its credibility from that regulated history, not from crypto culture.

The brand should feel like a modern share registry: exact, calm and well documented. It should never feel like a trading app or a token launch.

## Who we speak to

Design every page for the most careful reader in the room.

| Audience | What they need from us | What earns their trust |
| --- | --- | --- |
| **Issuers**: Australian private companies and scale-ups raising capital, property and infrastructure sponsors, corporate debt issuers, fund managers | A cheaper, faster way to issue, manage and transfer securities | Plain cost and timeline figures, named legal structures, references to the AFSL and the register |
| **Investors**: wholesale and sophisticated investors, family offices, and existing CoinPort verified customers where an offer permits | Access to private shares and bonds in smaller units, with a path to sell | Key terms up front, risk stated as clearly as return, eligibility shown before anything else |
| **Professional partners**: advisers, lawyers, accountants, custodians, registries | Confidence that the structure holds up | Exact terminology, documents they can read, no marketing gloss |

Most readers are financially literate but not crypto-native. Explain the chain only when it changes what the reader gets: faster settlement, a live register, fractional units.

## Voice

- Write like an experienced company secretary explaining something to a client: plain, exact and unhurried.
- Use Australian English: *tokenisation*, *licence* (noun), *organisation*, *cheque*. Write dates as `10 Oct 2026` and money as `A$4,250,000`. Spell out the currency the first time in a document.
- Use sentence case for headings, buttons and labels. Reserve uppercase for the `label` style.
- Name the instrument precisely: “ordinary shares”, “fixed-rate senior secured notes”, never just “tokens” or “assets”.
- Prefer “digital securities” or “tokenised shares” to “tokens” in customer copy. Say “blockchain” once, then “the register”.
- Address the reader as *you* and the company as *we*. Use *TokenSec* in legal and formal text.
- Never promise returns, use urgency (“last chance”, “don't miss out”) or use exclamation marks, rocket or moon imagery, emoji, or words like *revolutionary*, *disrupt* or *democratise*.
- Put risk next to return at the same size and weight, never in a footnote. Use the RiskNotice component.

| Write | Don't write |
| --- | --- |
| Buy shares in Harbour Logistics from A$10,000. | Own a piece of the next big thing! |
| Settles in minutes, not days. Your holding is recorded on the issuer's register. | Lightning-fast, trustless, on-chain ownership. |
| Coupon 8.5% p.a., paid quarterly. Your capital is at risk. | Earn 8.5% passive income. |
| Wholesale investors only. Check your eligibility. | Exclusive VIP access. |

## Name and wordmark

- Write the name as **TokenSec**: one word, capital T and capital S. Never *Tokensec*, *TOKENSEC* or *Token Sec*.
- The wordmark is set in Poppins SemiBold (600) at `-0.01em` tracking. *Token* is in `ink` and *Sec* in `ledger`. On `ledger-deep`, both parts use `on-deep`.
- The endorsement line *a CoinPort business* sits under or beside the wordmark in the `small` style, `ink-muted`, on first-touch surfaces: the website footer, decks and the investor portal sign-in.
- The logo mark is the **unit block**: a 3×3 grid of squared tiles (`radius-xs` corners) with the top-right tile in brass. It shows one security divided into registered units, and the brass tile is the investor's holding. Tiles are `ledger` with the held tile in `seal-fill`. On `ledger-deep`, the tiles are `on-deep` and the held tile stays brass.
- In the lockup, the mark sits left of the wordmark at about the wordmark's cap height plus descender (32px mark beside a 24px wordmark), with a `space-3` gap. Use the mark alone for favicons and app icons, on a `ledger-deep` rounded square.
- Never recolour, rotate or rearrange the tiles, move the brass tile, or add chain links, coins or other symbols to the mark.

## Colour

The palette comes from the paper and inks of a printed share certificate: a deep register green, brass from the seal, and cool off-white paper.

- Use `paper` for the page, `paper-raised` for cards and `paper-sunk` for wells and table headers. Set text in `ink`, and use `ink-muted` for metadata.
- `ledger` is the brand colour. Use it for one primary action per view, for links and for active states. Use `ledger-deep` for large brand fields such as the header band and hero slabs, with `on-deep` text.
- `seal` is an accent. Use it for bonds and fixed-income products and for the pending state, at no more than about 10% of a screen.
- Keep instrument colours consistent everywhere: **equity** uses `ledger` on `ledger-soft`, **debt** uses `seal` on `seal-soft`, and **other** instruments use `ink` on `paper-sunk`.
- Statuses: `settled` (blue) means done, issued or verified; `seal` means pending; `danger` means failed or halted. Always pair a status colour with a word.
- Text on a ledger fill is `on-ledger`, and text on `seal-fill` is `on-seal`. Never hard-code white.
- Every text pair named in a token's usage note meets 4.5:1 contrast in both themes. Control borders (`line-strong`) and the focus ring meet 3:1.

## Typography

- Use **Poppins** for everything a person reads. Load it from Google Fonts in weights 400, 500 and 600: `https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600&display=swap`. Fall back to `"Segoe UI", system-ui, sans-serif`.
- Use 600 for headings, 500 for figures, labels and buttons, and 400 for running text. Avoid 700 and above, and avoid italics except in legal citations.
- Poppins is geometric and wide. Keep body copy at `body` (16/26) and at most about 65 characters per line. Don't set paragraphs in 500.
- Set all amounts, percentages and dates in tables with `font-variant-numeric: tabular-nums`, right-aligned.
- Use the `identifier` style (system monospace) only for ISINs, contract addresses, transaction hashes and register references. Shorten long hashes in the middle (`0x7f3a…c91e`) and offer a copy action.

## Layout and spacing

- Use a 4px base unit (`space-1` to `space-16`). Separate sections with `space-16` on desktop and `space-12` on mobile, and pad cards with `space-6`.
- Use a 12-column grid at a maximum width of 1200px with a 16px mobile gutter.
- Corners stay squared: `radius-sm` for controls, `radius-md` for cards and `radius-xs` for tags. Don't use pill shapes.
- Structure comes from `line` borders and `paper-sunk` fills. Use `shadow-float` only for menus and dialogs.
- Lead every offering page with eligibility and key terms (instrument, issuer, price per unit, minimum, term or coupon, closing date), then the story.

## Data display

- Show money with its currency symbol and thousands separators (`A$1,250,000`). Write percentages as `8.50% p.a.` with the period stated.
- Write a unit count with its instrument: `2,500 ordinary shares`, `40 notes of A$1,000`.
- Show a fractional holding as units, not decimals of a share, unless the terms define fractions.
- Draw charts in `ledger` for equity, `seal-fill` for debt and `ink-muted` for benchmarks, on `paper-raised` with `line` gridlines.

## Iconography

- No icon set has been supplied yet. Use a single-weight outline set at 1.5px stroke on a 24px grid (Lucide is the recommended interim choice), coloured `ink` or `ink-muted`, and `ledger` only when the icon is the action.
- Don't use emoji, coin or rocket icons, padlocks for security claims, or chain links as decoration.

## Imagery and motif

- The brand motif is the **unit tile**: a block split into small squared tiles (`radius-xs`, `space-1` gaps), showing one security divided into registered units. Use it for heroes, covers and empty states.
- When you use photography, show real places and people in work settings: a warehouse, a building site, a boardroom. Avoid stock traders at screens, glowing networks and 3D coins.
- Use motion only to confirm state, such as a holding updating after settlement, at 150–200ms with ease-out. Respect `prefers-reduced-motion`.

## Compliance in the design

The brand's credibility depends on these. They are not optional.

- Show the licence line *TokenSec is a CoinPort business. [AFSL details once granted]* in every footer. Leave the placeholder until the licence or authorisation is confirmed, and never imply a licence is held before it is.
- Label every offer with its eligibility (for example *Wholesale investors only*) above the fold, before any return figure.
- Include a RiskNotice (general advice warning) on every page that mentions a return or a specific security.
- Link offer documents by their real names, such as *Information Memorandum* or *Product Disclosure Statement* and *Target Market Determination*.

## Components

Static HTML and CSS in `components/bundle.css`, prefixed `ts-`. Load the Poppins stylesheet and `tokens.css` first.

- **Button**: primary, secondary and quiet actions.
- **InstrumentTag**: the equity, debt or other label, plus status tags.
- **OfferingCard**: one offering with eligibility, key terms and progress.
- **RiskNotice**: the general advice warning that sits beside any return figure.
