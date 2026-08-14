# YAR SOURCE PROVENANCE

Package: general-average · created 2026-08-15 under **TS-P03 / TSCR-6** · extended 2026-08-15 under **TSCR-9**

## Why this file exists

Before 2026-08-15 this package held **no independent primary source** behind any of its York-Antwerp
objects. `WATCH_REGISTER` W3 described the working text as "CMI reproduction + BIMCO guidance", and no
such artifact was held in the tree. The package's `YAR-D` object was therefore being used to verify
itself, which is why TSCR-6 was raised rather than silently actioned.

This file records the primary source now used, and — as importantly — the exact **boundary** of what
that source has so far been used to verify.

## Primary source

| Field | Value |
|---|---|
| Title | York-Antwerp Rules 2016 (English version) |
| Issuer | Comité Maritime International (CMI) — the body that adopts the Rules |
| URL | https://comitemaritime.org/wp-content/uploads/2023/01/YAR-2016-English-Version.pdf |
| Retrieved | 2026-08-15 (HTTP 200, CMI's own domain, no redirect) |
| Size | 291,174 bytes · **12 pages** |
| SHA-256 | `0c364edb0d165eeaa61ca48bbbe0bb58dce2d6500c7a1f3110d39fdf56f3c01c` |
| Currency | Carries the CMI Assembly corrections of Genoa (September 2016) and Antwerp (October 2022), so it is the maintained text, not the as-adopted New York text |

**Re-verified 2026-08-15 under TSCR-9.** The file was retrieved again from the same CMI URL and is
**byte-identical** — same 291,174 bytes, same SHA-256. The source identity recorded under TSCR-6 stands
unchanged. One correction to the record itself: the page count was written as 8 and the document has
**12** pages. The hash governs identity, so this is a clerical error in the TSCR-6 record, not a change
of source; it is corrected above rather than silently left.

## Secondary sources used for the edition comparison (TSCR-9)

Rule VI cannot be stated correctly without knowing what it replaced, so two further CMI-hosted texts
were read. Both are metadata-only records; neither file is committed.

| Purpose | Title | URL | Bytes | SHA-256 |
|---|---|---|---|---|
| The superseded rule | York-Antwerp Rules **2004** (English version), CMI | `https://comitemaritime.org/wp-content/uploads/2023/01/YAR-2004-English-Version.pdf` | 166,772 | `b9e6c79a1b2a6acb8b64e13efb451be4024a4a85a3d2d5b0dc1a1e84fffc0c07` |
| The 1994 limb | *York-Antwerp Rules 2016 — Tabular Format* (CMI's own three-column 1994 / 2004 / 2016 comparison) | `https://comitemaritime.org/wp-content/uploads/2018/06/2016-York-Antwerp-Rules-Tabular-Format-Final-Clean.pdf` | — | `c21b948273e20f3a8dac0c0ccf55934bac43269f6e9faf4128a45ea677e6aeaf` |

Both retrieved 2026-08-15 from CMI's own domain, HTTP 200, no redirect.

**The source file itself is deliberately NOT committed to this repository.** `miw-true-source` is a
**public** GitHub repository; the YAR 2016 text is CMI copyright. What is recorded here is
metadata only — citation, URL, hash, date. See "Rights position" below.

## Scope of verification performed

Verified against the primary source, word for word:

- `YAR-PARAMOUNT` — Rule Paramount (created 2026-08-15 under TSCR-6; did not previously exist)
- `YAR-D` — Rule D (text **corrected** 2026-08-15 under TSCR-6)
- `YAR-VI` — Rule VI (text **corrected** 2026-08-15 under TSCR-9; paragraphs (a) and (d) verbatim,
  (b) and (c) structurally represented — see the rights note below)

**Nothing else in this package has been checked against the primary source.** `YAR-A`, `YAR-C` and
`YAR-XVII` remain on their pre-2026-08-15 footing.

## Findings

### Rule D — what it actually does

> Rights to contribution in general average shall not be affected, though the event which gave rise to
> the sacrifice or expenditure may have been due to the fault of one of the parties to the common
> maritime adventure, but this shall not prejudice any remedies or defences which may be open against
> or to that party in respect of such fault.

Rule D **preserves** the right to contribution notwithstanding the fault of a party, and **relocates**
the consequence of that fault into remedies and defences under the applicable law. It does **not** bar
the party at fault from claiming. The adjustment proceeds; the fault is litigated separately.

Any rule that a party at fault cannot recover in GA is a rule of the **applicable law**, not of the
York-Antwerp Rules — which is exactly why the **New Jason Clause** exists.

### Rule Paramount — what it actually governs

> In no case shall there be any allowance for sacrifice or expenditure unless reasonably made or
> incurred.

A **reasonableness gate**. Under the Rule of Interpretation it overrides both the lettered and the
numbered Rules — *"Except as provided by the Rule Paramount and the numbered Rules, general average
shall be adjusted according to the lettered Rules"* — but its subject matter is whether the sacrifice
or expenditure was reasonable, not who was at fault. The pre-correction claim that it "bars GA where
fault of party claiming" was a **misattribution**, not an overstatement: the Rule Paramount says
nothing whatever about fault.

### Rule D source-fidelity defect (corrected)

The pre-correction `YAR-D` text read *"one of the parties to the adventure"* with a semicolon before
*"but"*. That is the **YAR 1994** wording, carried in the register under a **YAR 2016** label. The
substantive effect of the two versions is the same, so no downstream answer was misled — but the
object was not the text it claimed to be, and has been corrected to the 2016 wording.

### Rule VI — what it actually does (TSCR-9)

> (a) Expenditure incurred by the parties to the common maritime adventure in the nature of salvage,
> whether under contract or otherwise, **shall be allowed in general average** provided that the salvage
> operations were carried out for the purpose of preserving from peril the property involved in the
> common maritime adventure and subject to the provisions of paragraphs (b), (c) and (d)

and, at the other end of the same Rule:

> (d) Special compensation payable to a salvor by the shipowner under Article 14 of the International
> Convention on Salvage, 1989 to the extent specified in paragraph 4 of that Article or under any other
> provision similar in substance (such as SCOPIC) **shall not be allowed in general average** and shall
> not be considered a salvage expenditure as referred to in paragraph (a) of this Rule.

The pre-correction `YAR-VI` object read *"Salvage payments, including interest and legal costs, shall
not be allowed in general average"* and described Art. 14 / SCOPIC compensation as *"particular
charges"*. Set against the two paragraphs above:

- The **first limb was an inversion**. It is the **YAR 2004** Rule VI(a) rule — *"shall lie where they
  fall and shall not be allowed in general average"* — carried under a **YAR 2016** label. Unlike the
  Rule D defect under TSCR-6, this was **not** a wording-fidelity defect with the same legal effect: the
  object asserted the opposite of the instrument it named.
- The **second limb was right for the wrong reason**. Art. 14 / SCOPIC compensation *is* excluded under
  YAR 2016 — but by **VI(d) alone**, as a carve-out from an allowance, not as an instance of a general
  exclusion. The phrase **"particular charges" appears in neither edition** and was never source text.
- The **qualifications were absent entirely**. VI(b)'s five gateways and VI(c)'s environmental-skill
  inclusion had no representation in the object at all.

### The edition history — verified, not assumed

| Edition | Rule VI(a) | Source |
|---|---|---|
| YAR 1994 | *"Expenditure incurred by the parties to the adventure in the nature of salvage … shall be allowed"* | CMI tabular comparison, sha256 `c21b9482…` |
| YAR 2004 | *"Salvage payments … shall lie where they fall and shall not be allowed in general average"*, save a credit/debit proviso where one party paid another's proportion | CMI YAR 2004, sha256 `b9e6c79a…` |
| YAR 2016 | *"shall be allowed in general average provided that …"* and *"subject to the provisions of paragraphs (b), (c) and (d)"* | CMI YAR 2016, sha256 `0c364edb…` |

The treatment therefore moved **twice**. The 2004 exclusion is a real historical proposition and
remains correct **about YAR 2004**; it is wrong only when presented as the current rule. That is the
distinction the corrected `TRAP-SALVAGE-GA` now teaches, and it is why the acceptance test for this
correction is not "zero mentions of salvage exclusion".

## Residual defects observed and DELIBERATELY NOT corrected

Verifying Rule D required reading the surrounding structure, which surfaced the following. They are
**outside TS-P03 scope** and are recorded here rather than fixed, so that the correction stays
auditable and the founder decides whether they warrant their own TSCRs.

| Object | Observed | Severity |
|---|---|---|
| ~~`YAR-VI`~~ | ~~States that salvage payments *"shall not be allowed in general average"*. That is the **YAR 2004** rule…~~ **RESOLVED 2026-08-15 under TSCR-9.** Confirmed on inspection, corrected against the CMI primary text, and the dependency chain (`TRAP-SALVAGE-GA`, `YAR_SEQUENCE` node 4) corrected with it. Retained here as the audit trail of how the defect was found | ~~HIGH~~ — **CLOSED** |
| `YAR-C` | Reproduces YAR 1994 Rule C. Omits YAR 2016 Rule C.2 (no allowance for environmental damage or escape/release of pollutants) and paraphrases C.3 | MEDIUM |
| `YAR-XVII` | A paraphrase, not the 2016 wording. YAR 2016 Rule XVII(a)(i) works from *"actual net values of the property at the termination of the common maritime adventure"* | MEDIUM |
| `YAR-A` | Matches YAR 2016 Rule A paragraph 1 exactly. Paragraph 2 is not held | LOW — accurate as far as it goes |
| `YAR_SEQUENCE` node 5 | References `YAR-XVIII`, `YAR-XIX`, `YAR-XX`. **None of these objects exists.** Three dangling references remain after TS-P03 (the `YAR-PARAMOUNT` dangler is now resolved) | MEDIUM — TSCR-8(c) territory |
| `COVERAGE_MATRIX` | Q6 asserts coverage via "Rule F"; no `YAR-F` object exists. Q3 asserts Rules XVII–XX; only `YAR-XVII` exists | MEDIUM — TSCR-8(c), already logged |

These are the substance of the future **TS-P06 full YAR corpus** work. TS-P03 does not close them and
does not claim to.

## Rights position — FLAGGED FOR FOUNDER

`miw-true-source` is a **public** repository and already contains verbatim CMI rule text
(`YAR-A`, `YAR-C`, `YAR-D`, `YAR-VI`, `YAR-XVII`) committed before this correction. The corpus-wide
policy in `RulesApp-Local-Input/true-source/COPYRIGHT_AND_DISTRIBUTION_STATUS.md` defaults every
source and derivative to `local-internal-use-only` and states expressly that such material must not be
"committed to a public repository".

This correction did **not** change that posture and did not widen it: the source PDF was not
committed, and the only text added is the Rule Paramount's single sentence, which TSCR-6 expressly
requested. But the pre-existing exposure is real and is **not something this session can adjudicate**.
It needs a founder decision — either a rights clearance covering this repository, or a move to
private.

### TSCR-9 addendum — the flag is carried forward, not resolved

TSCR-9 replaced a wrong `YAR-VI` text with a correct one. That necessarily changes what is reproduced,
so the exposure was actively minimised rather than allowed to grow:

- **No source file committed.** The YAR 2016, YAR 2004 and tabular-comparison PDFs were all retrieved
  to a scratch directory outside the repository and are recorded here by citation and hash only.
- **Verbatim reproduction confined to VI(a) and VI(d).** These are the two paragraphs that carry the
  legal proposition and the correction. Paragraph (b)'s five gateways and paragraph (c) are represented
  structurally in `paragraph_b_gateways` and `paragraph_c` instead of being reproduced — the substance
  is exact, the wording is not the CMI's.
- **No YAR 2004 text reproduced into the objects.** The 2004 rule is characterised and cited; the one
  fragment quoted anywhere in the package is the seven-word phrase *"shall lie where they fall"*, which
  is what makes the edition distinction legible and is quoted as a citation.
- **Net effect on the `YAR-VI` object: the verbatim CMI wording it carries is longer than before**,
  because the pre-correction text was a short paraphrase of the wrong edition. That is unavoidable if
  the object is to be source-faithful, and it is the reason this addendum exists rather than a bare
  "no change".

The founder decision required is unchanged and still open: **rights clearance for this public
repository, or a move to private.**
