# CURRENT STATUS — GENERAL AVERAGE

| Field | Value |
|---|---|
| Package | general-average |
| As at | 2026-08-16 |
| Instruments | York-Antwerp Rules 2016 (CMI) — maintained text, carrying the Genoa (Rule XVII) and Antwerp October 2022 (Rule XXI(b)) corrections |
| Current stage | **FOUNDER_REVIEW** — TSCR-6, TSCR-9 and the Rule XXI gap resolved; public-derived migration applied; package **not** complete (see residuals) |
| Architecture | **PUBLIC DERIVED / PRIVATE EVIDENCE** — adopted 2026-08-15 |

## Architecture — PUBLIC DERIVED / PRIVATE EVIDENCE

This package is the **production pilot** for the model. It has been adopted as the canonical True
Source architecture but applied nowhere else yet — no other package has been migrated.

`YAR_DEFINITIONS.json` now holds MIW-authored propositions and verification pointers, and holds **no
substantial source wording**. Verbatim evidence lives outside this repository, addressed by
`verification.evidence_id` and resolved through `EVIDENCE_INDEX.json` to a logical
`private_location_key`. See [`PRIVATE_EVIDENCE_BOUNDARY.md`](../PRIVATE_EVIDENCE_BOUNDARY.md).

What the migration did **not** do:

- It did not change any object's verification state. Three objects are `primary_verified`
  (`YAR-PARAMOUNT`, `YAR-D`, `YAR-VI`) and three are `unverified_legacy` (`YAR-A`, `YAR-C`,
  `YAR-XVII`) — the same split as before. *(That 3/3 split describes the package as it stood on
  2026-08-15. TS-P07 later added three further `primary_verified` Rule XXI objects, making the current
  split 6/3; it upgraded none of the three `unverified_legacy` objects. See Metrics above.)*
- It did not correct any legal content. The known `YAR-C` and `YAR-XVII` defects are now carried
  explicitly on the objects as `known_defect`, and remain open.
- It did not create the missing `YAR-XVIII` / `XIX` / `XX` objects, resolve sequence node 5, or touch
  the `COVERAGE_MATRIX` hygiene items.
- It did not remove verbatim wording from earlier commits. **Historical public source exposure
  remains in Git history** — a separate founder decision.

## Metrics (recomputed from the files 2026-08-16)
- Rule definition objects: **9** — `YAR-PARAMOUNT`, `YAR-A`, `YAR-C`, `YAR-D`, `YAR-VI`, `YAR-XVII`, `YAR-XXI-A`, `YAR-XXI-B`, `YAR-XXI-B-ORIGINAL`
- Rules of YAR 2016 as published by CMI: **32** (Rule of Interpretation + Rule Paramount + A–G + I–XXIII); rules held as objects: **8** (Rule XXI is held as two paragraph-level objects, plus one superseded state)
- Instrument register entries: 4 (YAR 2016 current; 1994/1974/1924 lineage)
- Trap / negative-knowledge objects: **5**
- Boundary objects: 1
- Sequence: 1 chain, **6** nodes
- Registered sources: **4** — `CMI-YAR-2016`, `CMI-YAR-2004`, `CMI-YAR-TABULAR-1994-2004-2016`, `CMI-YAR-2016-PRE-2022`
- Evidence records: **5**
- Verified against primary source: **6** (`YAR-PARAMOUNT`, `YAR-D`, `YAR-VI`, `YAR-XXI-A`, `YAR-XXI-B`, `YAR-XXI-B-ORIGINAL`) — see `YAR_SOURCE_PROVENANCE.md`
- Unverified against primary source: **3** (`YAR-A`, `YAR-C`, `YAR-XVII`) — unchanged; no verification state was upgraded on 2026-08-16
- Superseded objects: **1** (`YAR-XXI-B-ORIGINAL`) — primary-source accurate for a state that no longer applies; carries no reasoning node

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
| Finding | **YAR 2016 Rule VI(a) ALLOWS** salvage expenditure in general average where the operations were carried out to preserve the property from peril, subject to paragraphs (b), (c) and (d). The object asserted the opposite. Its first limb was the **YAR 2004** Rule VI(a) position — salvage payments left to lie where they fell and not allowed in GA — under a 2016 label. Its second limb (Art. 14 / SCOPIC excluded) is correct under 2016, but by **VI(d) alone** as a carve-out from an allowance; the label "particular charges" is in neither edition |
| Severity vs TSCR-6 | **Higher.** TSCR-6's Rule D defect was 1994 wording with the same legal effect. This one **reverses the legal proposition** |
| `YAR_DEFINITIONS.json` | `YAR-VI` **corrected** — VI(a) and VI(d) verbatim; VI(b)'s five gateways and VI(c) added as structured fields; `edition_history` recorded; object ID unchanged |
| `CANDIDATE_TRAPS_AND_MISSING_POINTS.md` | `TRAP-SALVAGE-GA` rewritten. Object ID unchanged; **still a negative-knowledge object**. The Art. 14 / SCOPIC guard it was built for survives — VI(d) is exactly where "not allowed in general average" is still the right answer — and the trap now teaches the **edition boundary** rather than reversing a sentence. It also warns against the opposite over-correction ("YAR 2016 allows salvage", stated flat) |
| `YAR_SEQUENCE.json` | Node 4 restated; no longer encodes a blanket exclusion of salvage. Structure and `governing_objects` unchanged |
| `WATCH_REGISTER.md` | W3 extended to record Rule VI as verified; **W4 added** — salvage treatment is edition-dependent and any statement of it must name its edition |
| Scope discipline | `YAR-C`, `YAR-XVII`, `YAR-A`, the `YAR-XVIII/XIX/XX` danglers and the `COVERAGE_MATRIX` hygiene items were **not** touched. `YAR-D` and `YAR-PARAMOUNT` were **not** touched |
| QP exposure | **CONTAMINATION FOUND — `QP2407` Q8.** Confirmed read-only; **no QP edited**. See below |
| Verification | JSON parses; `YAR-VI` resolves; node 4 references resolve; **0 active objects present the YAR 2004 salvage exclusion as YAR 2016 law** |

### TS-P07 — Rule XXI was not held at all, and the gap was consumed downstream — **RESOLVED 2026-08-16**

Not a correction: a **gap closure**. Rule XXI had no representation in this package in any form. The
package was silent rather than wrong, and a downstream consumer filled the silence from general
literature — most of which predates the October 2022 amendment.

| Field | Value |
|---|---|
| Classification | **Gap, with confirmed downstream consumption** — the stale LIBOR-based interest proposition reached MIW written-answer material once |
| Primary authority | CMI, *York-Antwerp Rules 2016 (English version)* — the maintained text — SHA-256 `0c364edb…`, **re-retrieved 2026-08-16 and byte-identical** to the TSCR-6 / TSCR-9 record. For the superseded state: CMI's own "(old)" posting, SHA-256 `2d0472e8…`, newly registered as `CMI-YAR-2016-PRE-2022` |
| Finding — current | Rule XXI(b) fixes the rate **for each calendar year** at the **USD Prime Rate plus 2 per cent per annum**, on the Prime Rate the **Wall Street Journal** publishes for that **calendar year**'s **first banking day**. It is a US dollar rate whatever currency the adjustment is drawn in |
| Finding — superseded | As adopted in May 2016 the paragraph used **twelve-month ICE LIBOR in the currency of the adjustment plus four percentage points**, with a US dollar fallback. The amendment changed benchmark **and** margin **and** removed the currency-matching limb |
| Finding — Rule XXI(a) | **Unchanged.** Verified as textually identical in the as-adopted and maintained texts. The CMI amendment footnote is attached to paragraph (b) alone |
| Finding — edition | **No YAR 2022 edition exists.** The edition was not renumbered by either the Genoa or the Antwerp intervention |
| Finding — Genoa | Separately identified: the CMI Assembly at **Genoa in September (2016)** restored wording dropped in error from **Rule XVII**, not Rule XXI. Recorded at instrument level only; `YAR-XVII` was **not** touched |
| `YAR_DEFINITIONS.json` | `YAR-XXI-A`, `YAR-XXI-B` and `YAR-XXI-B-ORIGINAL` **added**, all `primary_verified`; `superseded_objects` block added |
| `EVIDENCE_INDEX.json` | Source `CMI-YAR-2016-PRE-2022` registered; evidence `EVID-YAR-2016-XXI` and `EVID-YAR-2016-XXI-B-ORIGINAL` added |
| `CANDIDATE_TRAPS_AND_MISSING_POINTS.md` | `TRAP-YAR-XXI-LIBOR` added — stale benchmark, phantom 2022 edition, and the paragraph-(a) over-reach |
| `YAR_SEQUENCE.json` | Node 6 added; `YAR-XXI-B-ORIGINAL` deliberately excluded from `governing_objects` and recorded under `excluded_superseded` |
| `YAR_INSTRUMENT_REGISTER.md` | Amendment history added distinguishing Genoa from Antwerp; adoption venue corrected Beijing → New York; edition-identity negative knowledge added |
| Scope discipline | `YAR-A`, `YAR-C`, `YAR-XVII`, `YAR-D`, `YAR-PARAMOUNT`, `YAR-VI` and the `YAR-XVIII/XIX/XX` danglers were **not** touched. No placeholder object was created to make node 5 resolve |
| QP exposure | **Not re-audited in this session.** The downstream solvedQP repository was corrected separately before this work; this package was rebuilt above it, not from it |
| Verification | See "Validation — Rule XXI (TS-P07)" below |

**How the evidence was created.** No vault existed on this machine, and the architecture prototype
(`5e66d30`) records that none exists as a persistent store — the private layer is a git-ignored
working-tree directory. The hashing convention was therefore not guessed: it was **recovered by
reproducing two existing upstream `evidence_sha256` values** (`EVID-YAR-2016-PARAMOUNT` and
`EVID-YAR-2016-D`) from the registered source PDF. Both reproduce exactly, which establishes the
convention as SHA-256 over the UTF-8 bytes of the rule body with whitespace collapsed, headings and
superscript footnote markers excluded. The two Rule XXI hashes were then computed the same way.
`EVID-YAR-2016-VI` was not reproduced, as expected — its scope is a deliberate partial composition of
paragraphs (a) and (d), which is not derivable without the original editorial choice.

### Validation — Rule XXI (TS-P07), 2026-08-16

Session-local deterministic checks, run as one-off scripts. **There is still no repository CI or
validator**; nothing was installed.

- JSON parse (`YAR_DEFINITIONS.json`, `EVIDENCE_INDEX.json`, `YAR_SEQUENCE.json`): PASS
- Object IDs unique (**9/9**); evidence IDs unique (**5/5**): PASS
- Object key set matches the upstream schema **exactly** on all 9 objects; `relationships` key set uniform: PASS
- Every asserted `evidence_id` and `source_id` resolves; `public_objects` back-references complete: PASS
- Object-level hashes agree with `EVIDENCE_INDEX.json`: **0 mismatches**
- `EVIDENCE HASH MISMATCHES: 0` — recomputed from the private layer for the **2 passages present in this
  working tree**. The 3 passages created in earlier sessions are not present locally and were **not**
  recomputed; that is recorded rather than reported as a pass
- `unverified_legacy` objects assert no evidence: PASS (3 objects, unchanged — **no verification state
  was upgraded**)
- Node 6 resolves; object `reasoning_nodes` back-references resolve; every referenced trap exists: PASS
- **`SUPERSEDED OBJECT IN GOVERNING_OBJECTS: 0`** — `YAR-XXI-B-ORIGINAL` carries an empty
  `reasoning_nodes` list and appears in no chain node
- **`ACTIVE RULE XXI OBJECTS PRESENTING LIBOR AS THE OPERATIVE BENCHMARK: 0`** — LIBOR survives only as
  the mechanism that was replaced, and in the superseded object
- **`OBJECTS CLAIMING A 2022 EDITION: 0`**
- Boundary audit: source PDFs committed **0**; absolute machine paths **0**; malformed `vault://` keys
  **0**; conflict markers **0**; source-wording fields in public objects **0**
- Verbatim-overlap inspection against the private passages: **longest shared run 10 words** —
  *"announced on the first banking day of that calendar year"* — classified
  **OPERATIVE_TERMINOLOGY_NECESSARY** and deliberately retained. See the overlap-policy note below
- Semantic retrieval, answered from the **public layer alone**: **8/8 PASS**
- Reference resolution: nodes 1–4 and 6 resolve; **node 5 still references 3 non-existent objects**
  (`YAR-XVIII/XIX/XX`) — pre-existing, out of scope, and deliberately **not** forced to pass by creating
  placeholder objects

### Overlap policy — how the word-run diagnostic is to be read

The word-run count is a **diagnostic, not a definition of correctness**. Accuracy governs. Two rules
were applied on Founder review, 2026-08-16:

**Operative wording is never distorted to lower the count.** Instrument and rule titles, defined terms,
benchmark names, numerical requirements, units and dates stay exactly as the Rules put them —
*USD Prime Rate*, *2 per cent per annum*, *Wall Street Journal*, *first banking day*, *calendar year*,
*twelve-month ICE LIBOR*, *four percentage points*. An intermediate draft had replaced *first banking
day* with "opening banking day" purely to reduce overlap. That was an over-application of the boundary:
it degraded a date basis on which an adjustment turns, for no rights benefit. It was reverted, and the
exact term restored at every site.

**A single continuous run reproducing a substantial share of a paragraph is still reduced.** A draft
carried one 16-word continuous run — about **40 per cent** of the 40-word operative paragraph — which
is substantial reproduction rather than operative terminology, and the in-force
[`PRIVATE_EVIDENCE_BOUNDARY.md`](../PRIVATE_EVIDENCE_BOUNDARY.md) does not permit it. It was reduced by
changing **connectives and clause order only**; every operative term above survived verbatim and the
proposition became no vaguer.

The working line between the two: a run is acceptable where it consists of operative terms plus
unavoidable connectives and does not reproduce a substantial proportion of the source paragraph. The
surviving 10-word run is the date-basis clause at about **25 per cent** of the paragraph, and it earns
its place — the date basis is one of the few elements the October 2022 amendment did **not** change, so
stating it in the same terms in both the current and superseded objects is what makes that visible.

**Nothing in this package was made less accurate for copyright reasons.**

### Downstream QP exposure — `DOWNSTREAM_QP_REPAIR_REQUIRED`

The MIW estate (the local `Marine-Intelligence-Weekly` working copy) was searched read-only for the proposition, not
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

## Validation — public-derived migration (2026-08-15)

Session-local deterministic checks. **There is still no repository CI or validator**; these were run
as one-off scripts and are not installed.

- JSON parse (`YAR_DEFINITIONS.json`, `EVIDENCE_INDEX.json`, `YAR_SEQUENCE.json`): PASS
- Object IDs unique (6/6), evidence IDs unique (3/3): PASS
- Every asserted `evidence_id` resolves to an index entry; every `source_id` resolves to a registered source: PASS
- `BROKEN PUBLIC→PRIVATE TRACEABILITY LINKS: 0`
- `EVIDENCE HASH MISMATCHES: 0` — every `evidence_sha256` recomputed from the actual private vault
- Evidence-hash continuity with the architecture prototype (`5e66d30`): identical, same passage bytes
- `ABSOLUTE MACHINE PATHS IN PUBLIC DATA: 0`; conflict markers: 0; source PDFs committed: 0
- Verification-state regression: 3 `primary_verified` / 3 `unverified_legacy`, unchanged by migration
- Sequence resolution: nodes 1–4 resolve; **node 5 still references 3 non-existent objects** — unchanged
- Verbatim-overlap inspection against the removed wording: longest shared run 7 words, all runs at 6–7 words being terms of art
- Semantic regression, answered from the public layer alone: Rule A, Rule D, Rule Paramount, Rule VI, Rule VI(d), Rule XVII — all answerable; `YAR-C` and `YAR-XVII` answer subject to their recorded `known_defect`