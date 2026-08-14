# CURRENT STATUS — GENERAL AVERAGE

| Field | Value |
|---|---|
| Package | general-average |
| As at | 2026-08-15 |
| Instruments | York-Antwerp Rules 2016 (CMI) |
| Current stage | **FOUNDER_REVIEW** — TSCR-6 resolved; package **not** complete (see residuals) |

## Metrics (corrected 2026-08-15)
- Rule definition objects: **6** — `YAR-PARAMOUNT`, `YAR-A`, `YAR-C`, `YAR-D`, `YAR-VI`, `YAR-XVII`
- Instrument register entries: 4 (YAR 2016 current; 1994/1974/1924 lineage)
- Trap / negative-knowledge objects: 4
- Boundary objects: 1
- Sequence: 1 chain, 5 nodes
- Verified against primary source: **2** (`YAR-PARAMOUNT`, `YAR-D`) — see `YAR_SOURCE_PROVENANCE.md`
- Unverified against primary source: **4** (`YAR-A`, `YAR-C`, `YAR-VI`, `YAR-XVII`)

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

### Newly surfaced, NOT corrected

Verifying Rule D surfaced a **HIGH-severity inversion in `YAR-VI`** — it states the YAR 2004 rule that
salvage is *not* allowed in GA, whereas **YAR 2016 Rule VI(a) allows it**. This is the same class of
defect as TSCR-6 and affects `TRAP-SALVAGE-GA` and sequence node 4. It is **out of TS-P03 scope** and
is recorded, with the other residuals, in `YAR_SOURCE_PROVENANCE.md`. **It needs its own TSCR.**

## Validation (2026-08-15)
- JSON parse (`YAR_DEFINITIONS.json`, `YAR_SEQUENCE.json`): PASS
- Rule D / Rule Paramount vs primary source: PASS
- Residual inverted "fault bars contribution" propositions in active objects: **0**
- Reference resolution: node 3 resolves; **node 5 still references 3 non-existent objects** (`YAR-XVIII/XIX/XX`) — pre-existing, out of scope, recorded
- Citation / Contradiction / Completeness / Integrity: **not re-run** — no automated validator exists in this repository; the checks above were performed deterministically and by hand