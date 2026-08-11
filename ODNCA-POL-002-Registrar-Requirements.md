# ODNCA-POL-002 · Registrar Requirements
## What it takes to register names — and what it takes to be recognised

**Status:** v1.0 — Adopted
**Companion documents:** ODNCA-STD-001 (Resolution), ODNCA-STD-003 (SNS-NAME-1), ODNCA-POL-001 (TLD Fair-Use), ODNCA-POL-003 (Dispute & Abuse).

---

## 1. The permissionless base

Nobody needs ODNCA's permission to register names. The minimum viable registrar is **a static HTML page that produces inscriptions conformant with the SNS protocol** — a form, a wallet connection, a correctly shaped JSON body on a one-satoshi output. Anyone may build one, today, without contact, accreditation, or fee. Chain access cannot be granted because it cannot be denied.

This document therefore does not define who *may* register names. It defines what a **recognised registrar** is: a registrar listed by ODNCA, integrated in the coordinated ecosystem (resolver TLD lists, tooling, directory listing), and holding itself to the conduct rules below.

## 2. Requirements for recognition

### 2.1 Technical conformance

1. **Correct claims.** Registrations produced by the registrar conform to ODNCA-STD-003: valid JSON(5) form, correct normalization expectations, one-sat outputs, both accepted script orders handled correctly.
2. **Vector conformance.** The registrar's tooling agrees with the frozen conformance vectors — same valid/invalid verdicts, same canonical keys.
3. **Verified before sold-as-owned.** A registrar MUST NOT represent a name as successfully registered until the claim is on-chain; propagation delays (the `no_holder` window, ODNCA-STD-001 §4.4) are disclosed, not hidden.

### 2.2 Offering conduct

4. **Recognised TLDs only.** A recognised registrar offers registration only within the Active TLD set (ODNCA-POL-001). Offering withheld or retired TLDs — or unrecognised TLDs presented as if ecosystem-resolvable — forfeits recognition.
5. **Own-policy freedom, honestly labelled.** A registrar MAY restrict its own offering however it wishes — character subsets (e.g. letters and digits only), curated name lists, pricing tiers. Such restrictions are the registrar's policy and MUST be presented as such, never as chain-level validity rules.
6. **No false exclusivity.** A registrar MUST NOT claim to be the only path to registration, nor that names registered elsewhere are invalid. The base layer is permissionless and recognised registrars say so.

### 2.3 Display honesty

7. **Fallback disclosure.** Where the registrar's tooling resolves or pays names, the `fallback` flag is disclosed inline per ODNCA-STD-001 §5.
8. **Lookalike caution.** Non-ASCII and mixed-script names are visually distinguished per ODNCA-STD-001 §10.
9. **Blocklist adherence.** The registrar's resolution surfaces honour ODNCA-POL-003 statuses, including their honest display (a blocked name is shown as blocked, never as nonexistent).

## 3. Recognition lifecycle

- **Application:** request to ODNCA with the registrar's operating details and a conformance run against the vector set. Assessment results are published.
- **Listing:** recognised registrars appear in the public operator directory with their conformance date.
- **Withdrawal:** recognition is ODNCA's only lever, and losing it is the only sanction — chain access is untouched and untouchable. Grounds for withdrawal: breach of §2, persisting after notice. Withdrawals are published with reasons.

## 4. The founding registrar

ORDnet's own portal operates under this policy on identical terms, and currently applies an own-policy restriction (letters-and-digits offering) that is stricter than the standard requires — an illustration of §2.2.5, and deliberately so: the standard does not bend to its founder, and the founder does not claim privileges under the standard.

---

*ODNCA — the ORDnet Decentralized Names Coordination Authority. Don't trust us — recompute us.*
