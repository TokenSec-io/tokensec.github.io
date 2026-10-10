# OfferingCard

Summarises one offering in a list or grid. It always shows instrument, eligibility, issuer, key terms and progress, in that order. Keep it to one primary action.

- The consumer provides the issuer's legal name, the offering name, an instrument tag, an eligibility tag, six key terms (a `<dl>` of label and value) and the amount raised against the target.
- Progress is shown as unit tiles (`ts-units`, 20 tiles, each 5% of the target) plus the figures. Never show progress as a percentage alone.
- Return figures (coupon, target yield) appear at the same weight as the minimum and term, never enlarged. A page listing cards carries a RiskNotice.
- The ISIN or register reference sits in the footer in the `identifier` style.
- The example data in the preview is illustrative only.
