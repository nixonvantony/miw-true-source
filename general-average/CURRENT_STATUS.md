# CURRENT STATUS — GENERAL AVERAGE

| Field | Value |
|---|---|
| Package | general-average |
| As at | 2026-08-15 |
| Instruments | York-Antwerp Rules 2016 (CMI) |
| Current stage | **FOUNDER_REVIEW** — TSCR-6 and TSCR-9 resolved; package **not** complete (see residuals) |

## Metrics (corrected 2026-08-15)
- Rule definition objects: **6** — `YAR-PARAMOUNT`, `YAR-A`, `YAR-C`, `YAR-D`, `YAR-VI`, `YAR-XVII`
- Instrument register entries: 4 (YAR 2016 current; 1994/1974/1924 lineage)
- Trap / negative-knowledge objects: 4
- Boundary objects: 1
- Sequence: 1 chain, 5 nodes
- Verified against primary source: **3** (`YAR-PARAMOUNT`, `YAR-D`, `YAR-VI`) — see `YAR_SOURCE_PROVENANCE.md`
- Unverified against primary source: **3** (`YAR-A`, `YAR-C`, `YAR-XVII`)

> The previous block claimed "Rule objects: 24 (Paramount + Rules A-G + I-XXIII)" and "Total
> structured objects: 33 / Verified: all". Those figures were not true of the tree and are corrected
> above. The broader register/coverage hygiene items raised as **TSCR-8** remain open.

## Correction record

### TSCR-6 — `TRAP-RULE-D-FAULT` stated the inverse of Rule D — **RESOLVED 2026-08-15**

| Field | Value |
|---|---|
| Primary authority | CMI, *York-Antwerp Rules 2016 (English version)*, SHA-256 `0c364edb…`, retrieved 2026-08-15. Full provenance in `YAR_SOURCE_PROVENANCE.md` |
| Finding | Rule D **preserves** the right to contribution notwithstanding fault and relocates the consequence of fault into remedies and defences under the applicable law. The Rule Paramount is a **reasonableness** gate and says nothing about fault. Both limbs of the old trap were wrong |
| `CANDIDATE_TRAPS_AND_MISSING_POINTS.md` | `TRAP-RULE-D-FAULT` rewritten against the primary text; object ID unchanged; still a negative-knowledge object; now also warns against the opposite over-correction |
| `BOUNDARY_GA_HV_HAM_ROT.md` | Both inverted rows ("Fault interaction", "Relationship") corrected |
| `YAR_SEQUENCE.json` | Node 3 restated; no longer encodes "party at fault cannot claim" |
| `WATCH_REGISTER.md` | W2 restated as a reasonableness gate; W3 restated to record the real verification boundary |
| `YAR_DEFINITIONS.json` | `YAR-PARAMOUNT` **added** verbatim (TSCR-6 requested it; it also clears the dangling reference from sequence node 3). `YAR-D` **corrected** — prior text was YAR 1994 wording under a YAR 2016 label |
| QP exposure | 58 questions / 35 papers in the exposed family; **0 consumed** the inverted proposition — confirmed read-only, no QP edited |
| Verification | JSON parses; every object referenced by node 3 resolves; zero active objects assert that fault bars contribution |

### TSCR-9 — `YAR-VI` carried the YAR 2004 salvage exclusion under a YAR 2016 label — **RESOLVED 2026-08-15**

Raised by TSCR-6, which surfaced the defect but was scoped not to fix it. Opened and closed here as a
**release-critical** correction request in its own right.

| Field | Value |
|---|---|
| Classification | **RELEASE-CRITICAL** — an inversion of a legal proposition in a candidate-facing object, with confirmed downstream consumption |
| Primary authority | CMI, *York-Antwerp Rules 2016 (English version)*, SHA-256 `0c364edb…`, **re-retrieved 2026-08-15 and byte-identical** to the TSCR-6 record. Edition comparison verified against CMI YAR 2004 (SHA-256 `b9e6c79a…`) and CMI's own 1994/2004/2016 tabular comparison (SHA-256 `c21b9482…`). Full provenance in `YAR_SOURCE_PROVENANCE.md` |
| Finding | **YAR 2016 Rule VI(a) ALLOWS** salvage expenditure in general average where the operations were carried out to preserve the property from peril, *"subject to the provisions of paragraphs (b), (c) and (d)"*. The object asserted the opposite. Its first limb was **YAR 2004** Rule VI(a) — *"shall lie where they fall and shall not be allowed in general average"* — under a 2016 label. Its second limb (Art. 14 / SCOPIC excluded) is correct under 2016, but by **VI(d) alone** as a carve-out from an allowance; the label "particular charges" is in neither edition |
| Severity vs TSCR-6 | **Higher.** TSCR-6's Rule D defect was 1994 wording with the same legal effect. This one **reverses the legal proposition** |
| `YAR_DEFINITIONS.json` | `YAR-VI` **corrected** — VI(a) and VI(d) verbatim; VI(b)'s five gateways and VI(c) added as structured fields; `edition_history` recorded; object ID unchanged |
| `CANDIDATE_TRAPS_AND_MISSING_POINTS.md` | `TRAP-SALVAGE-GA` rewritten. Object ID unchanged; **still a negative-knowledge object**. The Art. 14 / SCOPIC guard it was built for survives — VI(d) is exactly where "not allowed in general average" is still the right answer — and the trap now teaches the **edition boundary** rather than reversing a sentence. It also warns against the opposite over-correction ("YAR 2016 allows salvage", stated flat) |
| `YAR_SEQUENCE.json` | Node 4 restated; no longer encodes a blanket exclusion of salvage. Structure and `governing_objects` unchanged |
| `WATCH_REGISTER.md` | W3 extended to record Rule VI as verified; **W4 added** — salvage treatment is edition-dependent and any statement of it must name its edition |
| Scope discipline | `YAR-C`, `YAR-XVII`, `YAR-A`, the `YAR-XVIII/XIX/XX` danglers and the `COVERAGE_MATRIX` hygiene items were **not** touched. `YAR-D` and `YAR-PARAMOUNT` were **not** touched |
| QP exposure | **CONTAMINATION FOUND — `QP2407` Q8.** Confirmed read-only; **no QP edited**. See below |
| Verification | JSON parses; `YAR-VI` resolves; node 4 references resolve; **0 active objects present the YAR 2004 salvage exclusion as YAR 2016 law** |

### Downstream QP exposure — `DOWNSTREAM_QP_REPAIR_REQUIRED`

The MIW estate (`D:\Marine-Intelligence-Weekly`) was searched read-only for the proposition, not
re-audited generally. Result:

| QP | Status |
|---|---|
| **QP2407 Q8** | **CONTAMINATED.** Consumed `YAR-VI` directly and cites it as authority — *"under Rule VI, salvage payments are not allowed in general average"*, with Art. 14 / SCOPIC *"treated as particular charges"*, tagged `TRUE_SOURCE: YAR-VI`. The 2004 rule, given to candidates as YAR 2016 law. Carried in the answer body, the summary, the source map and the denormalised search indexes |
| QP2403 | **CORRECT.** States VI(a) allowance, the five VI(b) gateways and the VI(d) exclusion, and expressly records that the 2004 Rules had removed salvage and 2016 restores it |
| QP2510 | **CORRECT.** Same treatment as QP2403 |
| QP2606 Q3 | **CORRECT.** A 1994-vs-2016 comparison statement, verified against CMI's own tabular comparison |
| QP2410, QP2509, notes `p19` | **CORRECT / not exposed.** YAR 2004 appears as edition-lineage or Rule XXIII time-bar material, which is accurate and is legitimate historical knowledge |

**Repair queue: `QP2407` Q8 only.** Not edited in this session — out of scope by instruction. Repairing
it will also require regenerating the denormalised artefacts that carry the proposition
(`pastpapers_content_index.json`, `solvedqp_content_index.json`, `verification/QP2407/Q8.md`,
`docs/QP2407_TRUE_SOURCE_REVIEW.md`).

## Validation (2026-08-15)
- JSON parse (`YAR_DEFINITIONS.json`, `YAR_SEQUENCE.json`): PASS
- Rule D / Rule Paramount vs primary source: PASS
- **Rule VI vs primary source: PASS** (VI(a) and VI(d) verbatim; VI(b)/(c) substance checked limb by limb)
- Residual inverted "fault bars contribution" propositions in active objects: **0**
- **`ACTIVE YAR-2016 OBJECTS CARRYING THE YAR-2004 SALVAGE EXCLUSION: 0`**
- Edition-boundary check: statements about YAR 2004 / 1994 salvage treatment are **preserved** where historically correct — the acceptance test is not "zero mentions of salvage exclusion"
- Reference resolution: node 3 and node 4 resolve; **node 5 still references 3 non-existent objects** (`YAR-XVIII/XIX/XX`) — pre-existing, out of scope, recorded
- Regression check: `YAR-D` and `YAR-PARAMOUNT` byte-for-byte unchanged from the TSCR-6 correction
- Citation / Contradiction / Completeness / Integrity: **not re-run** — no automated validator exists in this repository; the checks above were performed deterministically and by hand