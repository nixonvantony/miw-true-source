# YAR SOURCE PROVENANCE

Package: general-average · created 2026-08-15 under **TS-P03 / TSCR-6**

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
| Size | 291,174 bytes · 8 pages |
| SHA-256 | `0c364edb0d165eeaa61ca48bbbe0bb58dce2d6500c7a1f3110d39fdf56f3c01c` |
| Currency | Carries the CMI Assembly corrections of Genoa (September 2016) and Antwerp (October 2022), so it is the maintained text, not the as-adopted New York text |

**The source file itself is deliberately NOT committed to this repository.** `miw-true-source` is a
**public** GitHub repository; the YAR 2016 text is CMI copyright. What is recorded here is
metadata only — citation, URL, hash, date. See "Rights position" below.

## Scope of verification performed

Verified against the primary source, word for word:

- `YAR-PARAMOUNT` — Rule Paramount (created 2026-08-15; did not previously exist)
- `YAR-D` — Rule D (text **corrected** 2026-08-15)

**Nothing else in this package has been checked against the primary source.** Every other object
remains on its pre-2026-08-15 footing.

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

## Residual defects observed and DELIBERATELY NOT corrected

Verifying Rule D required reading the surrounding structure, which surfaced the following. They are
**outside TS-P03 scope** and are recorded here rather than fixed, so that the correction stays
auditable and the founder decides whether they warrant their own TSCRs.

| Object | Observed | Severity |
|---|---|---|
| `YAR-VI` | States that salvage payments *"shall not be allowed in general average"*. That is the **YAR 2004** rule. **YAR 2016 Rule VI(a) reverses it** — salvage expenditure *shall* be allowed in GA, subject to the qualifications in VI(b)–(d). The object states the opposite of the instrument it is labelled with. `TRAP-SALVAGE-GA` and `YAR_SEQUENCE` node 4 both rest on it | **HIGH — inversion, same class of defect as TSCR-6** |
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
