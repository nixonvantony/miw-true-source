# YORK-ANTWERP RULES INSTRUMENT REGISTER

Package: general-average · as_at: 2026-08-16

| Instrument | Exact title | Issuer | Adoption | Entry into force | Status | Role |
|---|---|---|---|---|---|---|
| YAR 2016 | York-Antwerp Rules 2016 | Comité Maritime International (CMI) | Adopted New York, May 2016; subsequently maintained — see amendment history below | contractual (no treaty EIF) | **current — maintained text, incorporating the Genoa and Antwerp corrections** | Core contractual rules (GA adjustment) |
| YAR 1994 | York-Antwerp Rules 1994 | CMI | 1994 (Sydney) | contractual | historical (still used) | Lineage only |
| YAR 1974 | York-Antwerp Rules 1974 | CMI | 1974 (Paris) | contractual | historical | Lineage only |
| YAR 1924 | York-Antwerp Rules 1924 | CMI | 1924 (Stockholm) | contractual | historical | Lineage only |

## Amendment history of the 2016 edition

The text CMI publishes today is not the text adopted in May 2016. Two separate CMI Assembly
interventions sit between them. They touched **different rules for different reasons** and must not be
run together — recorded 2026-08-16 from the maintained CMI text, in which each is carried by its own
footnote.

| # | Event | Rule affected | Nature | Recorded by |
|---|---|---|---|---|
| 1 | CMI Assembly, **Genoa, September** (2016) | **Rule XVII** — Contributory Values | A **restoration**, not a change of policy: the closing part of a sentence had been dropped in error from the text adopted in New York in May 2016, and wording that had stood in earlier versions was reinserted | Footnote on the Rule XVII page of the maintained CMI text |
| 2 | CMI Assembly, **Antwerp, October 2022** | **Rule XXI(b)** — the interest rate only | A **technical amendment**, described by CMI as made for technical reasons: the interest benchmark was re-based off LIBOR | Footnote attached to Rule XXI paragraph (b) of the maintained CMI text |

Notes on the limits of what the evidence supports:

- The Genoa footnote states the month (**September**) but **not the year**. 2016 is taken from the
  surrounding sentence, which refers to the text adopted in New York in May 2016, and from the CMI
  Assembly calendar. It is recorded as "September (2016)" rather than asserted flatly as a dated event.
- Genoa concerned **Rule XVII and not Rule XXI**. This package's `YAR-XVII` object is
  `unverified_legacy` and carries its own recorded defect; the Genoa correction is noted here at
  instrument level and `YAR-XVII` was deliberately **not** touched on 2026-08-16 — verifying it is
  TS-P06 work, not Rule XXI work.
- Antwerp concerned **Rule XXI(b) alone**. Rule XXI(a) is textually identical before and after, verified
  directly against both CMI postings.

## Edition identity — negative knowledge

**There is no "York-Antwerp Rules 2022" edition, and no "York-Antwerp Rules 2016 (revised)".** Neither
the Genoa nor the Antwerp intervention renumbered the edition. CMI continues to title the instrument
**York-Antwerp Rules 2016** and to record each correction as a footnote against the affected rule. Any
register, citation or answer naming a 2022 edition is wrong. See `TRAP-YAR-XXI-LIBOR`.

**Adoption-venue correction (2026-08-16):** this register previously recorded adoption as
"2016 (Beijing)". CMI states the 2016 text was approved by the CMI Conference held in **New York** in
May 2016, and the maintained text's own Genoa footnote refers to "the York-Antwerp Rules adopted in New
York in May 2016". Corrected on that authority.

## Source identity

Both CMI postings used as evidence are registered in [`EVIDENCE_INDEX.json`](EVIDENCE_INDEX.json) —
`CMI-YAR-2016` (the maintained text) and `CMI-YAR-2016-PRE-2022` (CMI's superseded posting, which
already carries the Genoa correction but predates the Antwerp amendment). Neither file is held in this
repository; they are recorded by URL, byte count and hash only, per
[`PRIVATE_EVIDENCE_BOUNDARY.md`](../PRIVATE_EVIDENCE_BOUNDARY.md).