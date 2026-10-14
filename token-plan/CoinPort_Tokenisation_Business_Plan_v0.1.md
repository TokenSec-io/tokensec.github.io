# CoinPort Asset & Securities Tokenisation — High-Level Business Plan (Draft v0.1)

**Status:** Draft for internal discussion — not yet reviewed by HN or the board
**Date:** 2026-09-27
**Author:** Peter Cooney (draft, with Claude)
**Proposed chain:** Redbelly Network
**Primary competitor identified:** Tokeniser, formerly Liquidise (AU-incorporated, AFSL 547681, expanding to UAE/Abu Dhabi)

---

## 1. Executive Summary

CoinPort proposes to expand from spot crypto exchange services into the **tokenisation of real-world assets (RWA) and securities** — issuing, managing, and providing liquidity for digital representations of funds, private company shares, property/debt instruments, and other regulated financial products. The initial technical approach is to build on **Redbelly Network**, a purpose-built, compliance-oriented Layer 1 blockchain that is already an ASIC-recognised participant in **Project Acacia** (Australia's first on-chain securitisation pilot with RBA/CBDC settlement).

This is a natural extension of CoinPort's existing AUSTRAC-registered DCE business and directly builds on the AFSL application already in flight (lodged 2026-08-12, ref TX000056588, currently in ASIC assessment) — see [[project_afsl_application]]. An AFSL is close to a *prerequisite* for tokenised securities activity, so this initiative should be sequenced to land after (or alongside, if authorisations can be added) the core AFSL.

The main identified competitor is **Tokeniser** (formerly Liquidise), an Australian company (Sydney-based, AFSL 547681) that already tokenises unit/mutual funds, property trusts, private company shares and debt on Ethereum, Arbitrum **and Redbelly Network**, using an AMM for secondary liquidity, and is expanding into the UAE (Abu Dhabi) via `uae.liquidise.com`. Notably, Tokeniser is *also building on Redbelly* — so CoinPort would not have first-mover advantage on the chain choice, but there is a large addressable market and multiple viable niches (see Opportunities, §5).

---

## 2. Why Redbelly Network

- **Purpose-built for RWA/compliance**, not a general-purpose chain retrofitted with compliance middleware — has built-in investor eligibility/whitelisting, digital registries, and "accountable" (non-fully-anonymous) validator design.
- **Australian nexus:** Redbelly Network Pty Ltd is an Australian-registered company, which may simplify commercial/legal relationships and support ASIC engagement.
- **Regulatory precedent already established:** Redbelly is a participant in **Project Acacia**, for which ASIC issued class/individual regulatory relief permitting real-money on-chain securities transactions on a public blockchain. This is a meaningful precedent CoinPort can point to with ASIC/HN rather than starting from zero.
- **Existing institutional partnerships:** e.g. Hutly (tokenising ~$1.8B in rent rolls), other real estate and structured-product pilots — signals a live ecosystem CoinPort could plug into (as an exchange/liquidity venue, custodian, or on/off-ramp) rather than needing to bootstrap issuance demand alone.
- **Risk:** Redbelly is a young, thin-validator-set network (order of ~40 institutional nodes). Chain-level counterparty concentration, liveness, and long-term decentralisation/regulatory risk need explicit diligence before committing.

## 3. Competitor Snapshot — Tokeniser (formerly Liquidise)

| Attribute | Tokeniser |
|---|---|
| Entity | Public unlisted Australian company |
| Licence | AFSL 547681 |
| Chains | Ethereum, Arbitrum, **Redbelly Network** |
| Settlement assets | USDT, USDC, native LIQ token |
| Asset classes | Unit/mutual funds, property trusts, private company shares, debt/private credit |
| Model | Tokenise illiquid holdings + proprietary AMM for secondary liquidity |
| Customers | Institutional investors, fund unit holders, VC fund LPs seeking liquidity on locked positions |
| Geographic expansion | Sydney HQ → Abu Dhabi/UAE (separate `uae.liquidise.com` site) |

**Read:** Tokeniser is not a spot-exchange-first business — it's a liquidity/AMM infrastructure and issuance platform for illiquid fund/private-market positions. It is already licensed and already live on Redbelly. CoinPort should not assume a "blue ocean" — this is a validated, licensed, moving competitor with ~2+ years of head start on the licensing pathway alone.

## 4. Leveraging the Existing CoinPort Business

CoinPort does not need to start from zero. Existing assets that are directly reusable:

1. **AUSTRAC DCE registration (100633359)** and live AML/CTF Program (`legal/docs/CoinPort_AML_CTF_Program_v3.1_2026.md`) — tokenised securities still touch fiat on/off-ramps and will need AML/CTF coverage; the existing program, Compliance Officer (Nicanor Nuqui), and reporting infrastructure extend rather than duplicate.
2. **AFSL application in ASIC assessment** — the compliance manual, RMF, responsible-manager evidence, and custody framework already being built for the core exchange business (`AFSL-docs/`) are ~80% of what's needed to add a "dealing in / providing custody for" securities authorisation later. Sequencing matters: better to land the core AFSL first, then vary/add authorisations, than to try to scope both at once and slow the current lodgement.
3. **Existing fiat rails** (Monoova/Xendit) — see [[coinport-vendors]] — give a ready-made AUD on/off-ramp for tokenised product subscriptions/redemptions without building new banking relationships from scratch.
4. **Custody infrastructure** already being scoped for the AFSL (see `AFSL-docs/Custody_Multisig_Options.md`) can likely be extended to hold tokenised securities, subject to RG133 review.
5. **Brand and existing retail/institutional customer base** — CoinPort already has a trusted, AUSTRAC-registered brand in the AU market; cross-sell of a tokenisation product to existing verified (KYC'd) customers is materially cheaper than Tokeniser or a new entrant acquiring customers cold.
6. **Corporate structure** — M1 Digital (parent) and CoinPort's NZ/PH subsidiaries could provide an existing multi-jurisdiction footprint if the product needs offshore SPVs or a UAE-style expansion later (mirroring Tokeniser's own AU→UAE path).
7. **Chatwoot/helpdesk and existing ops tooling** ([[coinport-vendors]]) reduces new-build for client servicing.

## 5. Opportunities

- **Cross-sell to CoinPort's existing verified customer base** — lower CAC than a standalone tokenisation start-up.
- **Niche differentiation vs Tokeniser:** Tokeniser focuses on *illiquid fund/private-market secondary liquidity*. CoinPort could differentiate toward:
  - Retail-accessible fractionalised access to asset classes currently gated to wholesale/institutional investors (subject to disclosure/PDS rules).
  - Specific verticals Tokeniser isn't obviously focused on (e.g. tokenised property income streams, carbon credits, or trade/invoice finance — all explicitly on Redbelly's roadmap).
  - Acting as a **secondary trading venue / liquidity partner for tokens issued by others** on Redbelly (exchange-style role) rather than competing head-on as an issuer/AMM.
- **Project Acacia halo effect** — being able to say CoinPort's chosen infrastructure has direct ASIC regulatory-relief precedent is a strong talking point for both ASIC engagement and institutional counterparties.
- **First-mover on the *exchange/distribution* layer** even if not on issuance — Redbelly's ecosystem (Hutly, real estate, structured products) will need off-ramps, secondary markets, and AUD conversion; CoinPort is well placed to be that layer given existing AUSTRAC/AFSL positioning.
- **Regional expansion path already proven by a direct competitor** (Tokeniser's AU→UAE move) — de-risks the idea that Australian tokenisation businesses can credibly expand into the UAE if CoinPort wants to follow later.

## 6. Threats & Risks

**Competitive**
- Tokeniser already has an AFSL, is already live on Redbelly, and is already expanding internationally — CoinPort is entering as a clear follower, not a first mover.
- Other AFSL holders/incumbents (fund administrators, exchanges) may move onto Redbelly or a competing RWA chain faster than CoinPort can secure the necessary authorisations.

**Regulatory**
- Tokenised securities are financial products under the Corporations Act — this is a different, generally *stricter* regulatory perimeter than crypto asset dealing under AUSTRAC alone. Likely needs specific AFSL authorisations (dealing, custody, possibly market operation if CoinPort runs a secondary market) beyond what's currently being sought — see RG104/RG133/RG166 material already in `AFSL-docs/`.
- Risk of delaying or complicating the *current* AFSL application if scope creep is introduced mid-assessment. HN should be consulted before any tokenisation authorisation is added to the live application — see [[afsl-drive-source-of-truth]].
- Regulatory relief that Redbelly/Project Acacia participants rely on may be narrow, temporary, or participant-specific (i.e. not automatically available to CoinPort just because CoinPort uses the same chain).
- AML/CTF Rules 2025 and any future Scams Prevention Framework obligations extend to new product types and need explicit legal sign-off, not assumed coverage under the existing v3.1 program.

**Technology / Chain risk**
- Redbelly is a young network with a small (~40 node) institutional validator set — concentration, liveness, and validator-governance risk.
- Vendor/platform risk: CoinPort would be dependent on Redbelly's roadmap, uptime, and continued regulatory goodwill (e.g. continued ASIC relief).
- Interoperability: Tokeniser already spans Ethereum + Arbitrum + Redbelly; a Redbelly-only strategy may under-serve institutional counterparties who expect multi-chain settlement/liquidity.

**Financial / Capital**
- CoinPort's FY2025 net assets ($130,511) are already below the AFSL NTA floor and need a capital injection for the *existing* licence — see [[afsl-fy2025-financials]]. A tokenised-securities authorisation will very likely carry its **own, higher** NTA/surplus liquid funds requirement (RG166), compounding the capital-raising need before this can be licensed.
- Build cost (smart contracts, registry integration, custody extension, legal/compliance uplift, PDS/TMD documentation if retail) is non-trivial and would compete for the same limited capital as the core AFSL build-out.

**Reputational**
- Early-stage RWA/tokenisation has had high-profile failures and regulatory enforcement actions internationally; any misstep would put CoinPort's core AUSTRAC/AFSL standing at risk, not just the new product line.

## 7. Potential Business Names (for the tokenisation product/brand)

Working assumption: launch as a **sub-brand of CoinPort** (leveraging existing trust/registration) rather than a fully separate entity, unless legal/licensing structuring requires a separate SPV.

- **CoinPort Tokenise**
- **CoinPort Capital Markets**
- **CoinPort RWA**
- **Harbour Ledger** *(nod to the CoinHarbour heritage without reusing the retired brand directly)*
- **Redbelly Markets by CoinPort** *(only viable with Redbelly's consent — trademark/partnership risk otherwise)*
- **Southern Cross Ledger**
- **Ledger & Co.**
- **CoinPort Structured Assets**
- **Token Harbour**

*Recommendation:* keep the CoinPort name in the brand (regulatory trust transfer, AUSTRAC/AFSL association is a genuine asset) unless legal advises a separate licensed entity is required, in which case a distinct name (e.g. a standalone SPV) becomes more important for liability ring-fencing.

## 8. Related / Adjacent Business Ideas

The core plan above mirrors Tokeniser's model fairly closely (issuer + AMM liquidity for fund/property/private-share tokens). Below are adjacent ideas that reuse the same AUSTRAC/AFSL/custody/Redbelly foundation but sit in a different niche, roughly ordered from "closest to core plan" to "most different":

1. **Secondary market / exchange layer for Redbelly-issued tokens** — CoinPort acts as the AUD on/off-ramp and trading venue for tokens *issued by others* on Redbelly (Hutly, future issuers), rather than being an issuer itself. Lowest incremental licensing burden (closer to CoinPort's existing "dealing/market" profile than to acting as issuer/responsible entity), fastest to stand up, but lower margin/ceiling than owning issuance.
2. **White-label tokenisation-as-a-service** — sell CoinPort's AFSL + AUSTRAC + custody + compliance infrastructure to smaller fund managers or AFSL holders who want to tokenise but don't want to build the regulatory stack themselves. Turns CoinPort's compliance build-out into a product, not just a cost centre; revenue is service fees rather than balance-sheet/product risk.
3. **Tokenised trade/invoice finance** — short-duration receivables funded via CoinPort's existing verified customer base, using Redbelly's registry/eligibility features. Different risk/duration profile from Tokeniser's fund-unit/property focus; shorter-dated instruments may sit in a more familiar RG166/custody risk band than long-dated property or PE positions.
4. **Tokenised carbon credits** — explicitly on Redbelly's roadmap and less contested than fund/property tokenisation. Leverages an exchange-style listing/trading model CoinPort already understands, but carbon-credit market integrity and additionality risk is a distinct diligence area from financial-product regulation.
5. **Retail fractionalised access wrapper** — take wholesale-only tokenised products from Redbelly issuers and offer retail-accessible fractional exposure (subject to PDS/TMD design). Genuinely different customer segment from Tokeniser's institutional/LP focus, but retail distribution of financial products carries the heaviest disclosure/TMD/design-and-distribution obligations of everything on this list.

**General tradeoff:** the further an option moves from "exchange/distribution" (#1) toward "issuer/responsible entity" (#3–#5), the more it inherits Tokeniser-style AFSL authorisation scope and capital burden (RG166/RG133), but also the higher the revenue ceiling. #1 and #2 are the cheapest/fastest to license and could be sequenced *before* #3–#5 as a way to generate revenue and market presence on Redbelly while the core AFSL and any securities-specific authorisation are still being built out.

## 9. Open Questions / Next Steps

1. Confirm with HN whether a securities-tokenisation authorisation should be added to the *current* AFSL application or pursued as a *variation* after the current lodgement is determined.
2. Scope which specific asset classes CoinPort would target first (property income, private credit, fund units, other) — drives which RGs (133, 166, 259) need fresh gap analysis.
3. Direct technical/commercial conversation with Redbelly Network re: partnership terms, node participation vs. pure integration, and whether CoinPort would need its own Project-Acacia-style relief or can rely on platform-level relief.
4. Capital plan: quantify the incremental NTA/surplus liquid funds requirement for a securities dealing/custody authorisation, and fold into the existing capital-injection conversation ([[afsl-fy2025-financials]]).
5. Legal review of whether a separate entity (under M1 Digital) is preferable to housing this inside CoinPort Pty Ltd directly.
6. Deeper competitive scan beyond Tokeniser (e.g. other Redbelly-ecosystem entrants, ASX-adjacent tokenisation pilots).

---

*This is a first-pass, high-level draft based on public information about Redbelly Network and Tokeniser (formerly Liquidise) only. No confidential counterparty information was used. Treat all competitor detail as sourced from public websites (redbelly.network, uae.liquidise.com) and general web search, current as of 2026-09-27.*
