# ODNCA-POL-001 · TLD Fair-Use Policy
## Stewardship of the recognised top-level-domain set

**Status:** v1.0 — Adopted
**Companion documents:** ODNCA-STD-002 (Protocol Parameters Registry — the live TLD lists), ODNCA-STD-003 (SNS-NAME-1), ODNCA-POL-002 (Registrar Requirements).

---

## 1. The honest starting point

On the chain, TLD creation is **permissionless**. Anyone can inscribe a valid registration under any TLD — `fable.claude` works today, without asking anyone. ODNCA cannot prevent this, and does not pretend to: per SNS-NAME-1, such names are *valid*.

What ODNCA stewards is something else: **the recognised TLD set** — the list of TLDs that the coordinated ecosystem offers for registration and serves in resolution. Resolvers load this list live from the registry (single source, ODNCA-STD-002); registrars offer within it; browsers, mail, and tooling follow the resolver. Recognition, not permission, is the instrument.

## 2. TLD categories

Every TLD is, from the ecosystem's point of view, in exactly one category:

| Category | Registration | Resolution | Meaning |
|---|---|---|---|
| **Active** | open | ✓ | In the registrable set; offered by recognised registrars |
| **Retired** | closed | ✓ existing names | Registration ended; names already claimed keep resolving forever |
| **Withheld** | not offered | — | Deliberately left untouched out of respect for a third party's rights or moral claim |
| **Unrecognised** | — | `unknown_tld` | Exists (or may exist) on chain; not part of the coordinated set |

Current assignments are parameters, not policy text: the live lists are published in ODNCA-STD-002 and served by the registry. At adoption: Active = `web3, bitcoin, crypto, blockchain, ordnet`; Retired = `bsv, bitcoinsv`; Withheld = `1sat`.

## 3. Fair use: why a TLD is withheld or retired

ODNCA recognises that names carry rights and claims that exist outside the chain, and chooses — voluntarily, as policy — to respect them:

- **Registered rights.** Where a party holds trademark or comparable registration on a term, ODNCA does not offer that term as a TLD. This is why `.bsv` and `.bitcoinsv` are not offered: the BSV Association holds the registration of these names. (Names claimed under these TLDs before retirement continue to resolve — retirement never expropriates existing holders.)
- **Moral and platform claims.** Rights need not be registered to be respected. `.1sat` is withheld so that the 1Sat Ordinals platform retains the ability to issue it for its own ecosystem — although no registration of the term exists. Prior association and community stewardship count.
- **The general principle.** Where a TLD term is identified primarily with a party that is not the applicant, the fair answer is to leave it to that party — or to no one.

This policy binds ODNCA and recognised registrars. It cannot bind the chain, and does not claim to: an unrecognised claim under a withheld TLD remains an on-chain fact. It simply resolves nowhere in the coordinated ecosystem.

## 4. Recognising a new TLD

A party wishing a TLD recognised (activated) requests it from ODNCA. The assessment is published and covers:

1. **Technical conformance** — the TLD label satisfies SNS-NAME-1; no collision with any Active, Retired, or Withheld TLD.
2. **Fair-use screening** — no evident third-party registered rights or primary association with a non-applicant party (§3).
3. **Steward capability** — where the TLD is to be operated by the applicant, the applicant meets ODNCA-POL-002.

Outcomes (recognised / withheld / declined) are published with reasons in the parameter registry's changelog. Commercial terms of activation, where applicable, are published separately and are never a substitute for the screening above.

## 5. Changes and reversals

Category changes (activation, retirement, withholding) are parameter changes: announced, dated, and recorded in ODNCA-STD-002. Two rules are absolute:

- **Retirement never removes resolution of existing names.** Closing a TLD to new registration is policy; expropriating claimed names is impossible and would not be done if it were possible.
- **A withheld TLD activates only by, or with the consent of, the party for whom it is held.**

---

*ODNCA — the ORDnet Decentralized Names Coordination Authority. Don't trust us — recompute us.*
