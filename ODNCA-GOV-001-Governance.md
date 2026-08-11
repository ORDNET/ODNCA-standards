# ODNCA-GOV-001 · Governance
## Who decides, how, and what no one may decide

**Status:** v1.0 — Adopted
**ODNCA** stands for **ORDnet Decentralized Names Coordination Authority**.
**Companion documents:** all ODNCA-STD and ODNCA-POL documents; decisions are anchored per ODNCA-STD-004 §3.2.

---

## 1. Design position

Governance here is deliberately small. The chain settles ownership, the published rules settle validity, and conformance is testable by anyone — so most questions that a naming authority traditionally decides are, in this ecosystem, already decided by math. What remains for governance is the genuinely human residue: recognising TLDs and namespaces, adopting and revising standards, applying the fair-use and abuse policies, and stewarding the keys. This charter covers that residue and nothing more.

## 2. The Board

- **Founding seat:** ORDnet, the founding steward, holds the first seat.
- **Standing invitations:** seats are reserved for ecosystem stewards — in the first place the parties for whom TLDs are withheld or retired under ODNCA-POL-001, whose stake in fair coordination predates this charter: the steward of the 1Sat Ordinals ecosystem and the BSV Association. An invitation stands until accepted or declined; declining costs nothing and closes no doors.
- **Growth:** further seats may be extended to operators and registrars recognised under ODNCA-POL-002 as the ecosystem grows. When the Board reaches three or more seated members, this charter is revisited by that Board.

## 3. Decision-making

- **Sole-steward phase (current):** the founding steward decides.
- **Multi-seat phase:** consensus is sought; failing consensus, simple majority decides; the founding seat breaks ties.
- **Always, in every phase:** every decision is **published with reasons** in the changelog (ODNCA-STD-002) and, where it changes recognised state, **anchored on-chain** (ODNCA-STD-004 §3.2). A decision that is not published is not a decision. The legitimacy of the sole-steward phase rests entirely on this transparency: the authority may currently be one party, but it is never a private one.

## 4. What governance cannot do

Some limits bind every phase and every majority:

1. **No power over chain facts.** Governance cannot invalidate a valid claim, reassign a name, or override first-seen-wins. (ODNCA-STD-003; POL-003 §1.)
2. **No expropriation.** Retirement never removes resolution of existing names; withheld TLDs activate only by or with their party's consent. (POL-001 §5.)
3. **No changing frozen math.** The pinned constants of the commitment layer and the hashed rulesets cannot be "amended" — changing them creates a demonstrably different namespace. (ODNCA-STD-004 §2, §6.4.)
4. **No secret measures.** Every warning, block, and delisting is published with its reason. (POL-003 §6; POL-002 §3.)

## 5. Changing a standard

1. **Proposal** — the change, its rationale, and its impact on existing names, vectors, and implementations, published openly.
2. **Review period** — **14 days** in which operators, registrars, and holders may comment; substantive comments are answered in the decision.
3. **Decision** — published per §3; conformance vectors updated in the same release, because a standard whose vectors lag it is two standards.

Editorial corrections (typos, clarifications with no behavioural effect) skip review and are marked as such in the changelog. Changes to frozen constants are not proposals — see §4.3.

## 6. TLD requests

The procedure for asking ODNCA to recognise (activate) a TLD:

1. **Submission.** The requesting party files: the TLD label; intended purpose and operator; whether the requester seeks Active status for open registration or activation as its own steward; and a declaration of known third-party rights on the term.
2. **Board screening.** The Board tests the request against: **technical conformance** (SNS-NAME-1; no collision with Active, Retired, or Withheld TLDs); **registered rights** (patent and trademark search on the term); and **prior association** (whether the term is primarily identified with a party that is not the requester). Where a potentially affected party is identifiable — a rights holder, a platform, a community steward — **that party is consulted directly** before any decision.
3. **Public window.** The request is published on submission; the 14-day comment window of §5 runs in parallel with screening.
4. **Decision within 30 days** of submission: *recognised* (activation record inscribed per ODNCA-STD-004 §3.2, activation height set no earlier than the inscription), *withheld* (the fair answer is that the term belongs to another party — who thereby receives a standing activation right per POL-001 §5), or *declined*, always with published reasons.

Screening is a rights-and-fairness test, never an auction: commercial terms, where applicable, are published separately and cannot buy a pass on §6.2.

## 7. Emergency actions

Direct blocks under POL-003 §4.1 (CSAM, active malware or phishing, court orders) are executed without waiting for any review or Board cycle, and published with reasons immediately after the fact. Speed there is the policy; transparency remains the check.

## 8. Keys

The Board stewards the published key inventory (resolver signing key, registrar issuer keys, commitment keys) under the rotation procedure of ODNCA-STD-001 §7.2 — every rotation signed by the predecessor key, published, and anchored on-chain. Key stewardship is the one governance duty where failure is unrecoverable, and is treated accordingly: keys are generated once, backed up offline, and never shared across roles.

---

*ODNCA — the ORDnet Decentralized Names Coordination Authority. Don't trust us — recompute us.*
