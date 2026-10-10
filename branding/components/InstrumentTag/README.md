# InstrumentTag

Use a short uppercase label to name an instrument class, an eligibility rule or a status. Instrument colours are fixed across the product: `ts-tag-equity` for shares, `ts-tag-debt` for bonds and notes, and the plain `ts-tag` for anything else (units, hybrids). `ts-tag-eligibility` is outlined, and every offer shows one. Statuses use `ts-tag-settled`, `ts-tag-pending` and `ts-tag-danger`.

- The consumer provides a `<span class="ts-tag …">` with the text. The colour never carries meaning alone; the word does.
- Name the real instrument (“Ordinary shares”, “Senior secured notes”), not “Token”.
- Use at most three tags per card: instrument, eligibility, then status.
