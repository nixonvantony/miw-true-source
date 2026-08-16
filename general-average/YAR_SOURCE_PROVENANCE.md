# YAR SOURCE PROVENANCE

Package: general-average · created 2026-08-15 under **TS-P03 / TSCR-6** · extended 2026-08-15 under **TSCR-9** · extended 2026-08-16 under **TS-P07 (Rule XXI)**

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
- `YAR-VI` — Rule VI (text **corrected** 2026-08-15 under TSCR-9; paragraphs (a) and (d) verified
  word for word and now held as private evidence, (b) and (c) never held verbatim and carried by the
  MIW proposition — see the rights note below)

Added 2026-08-16 under **TS-P07**, verified against the primary sources:

- `YAR-XXI-A` — Rule XXI(a), and verified as **unchanged** by comparing the maintained text against
  CMI's superseded posting
- `YAR-XXI-B` — Rule XXI(b), current basis (created; the rule was previously not held at all)
- `YAR-XXI-B-ORIGINAL` — Rule XXI(b) as originally adopted, verified against CMI's superseded posting
  and held as a **SUPERSEDED** state

**Nothing else in this package has been checked against the primary source.** `YAR-A`, `YAR-C` and
`YAR-XVII` remain on their pre-2026-08-15 footing.

## Second primary source — CMI's superseded posting (TS-P07)

Establishing that Rule XXI(b) *changed*, and that Rule XXI(a) *did not*, needs both states of the text.
CMI publishes both.

| Field | Value |
|---|---|
| Title | York-Antwerp Rules 2016 (English version) — CMI's superseded posting, labelled **"(old)"** on the CMI YAR page |
| Source ID | `CMI-YAR-2016-PRE-2022` |
| URL | `https://comitemaritime.org/wp-content/uploads/2023/01/YAR-2016-English-with-Rule-XVII-correction-1.pdf` |
| Retrieved | 2026-08-16 (HTTP 200, CMI's own domain, no redirect) |
| Size | 214,432 bytes · 12 pages |
| SHA-256 | `2d0472e8ceee67bd40956bf348e1bc1789e8e7ede9bf93de6c42b0fb6ba1ede6` |
| Currency | Already carries the **Genoa Rule XVII** correction, but **predates** the Antwerp October 2022 Rule XXI(b) amendment. It is therefore the primary witness to the superseded interest basis, and to nothing later |

**Re-verification of the maintained text, 2026-08-16.** `CMI-YAR-2016` was retrieved again from the same
CMI URL and is **byte-identical** to the TSCR-6 and TSCR-9 records — same 291,174 bytes, same SHA-256
`0c364edb…`. The source identity stands unchanged across three sessions.

**An acquisition hazard worth recording.** Neither filename nor file date distinguishes these two
postings correctly. The maintained text has the *plainer* filename and a PDF creation date of
2023-01-26; the superseded posting has the more specific-looking filename and a **later** creation date
of 2024-08-06. Anything that sorts by name or date will pick up the LIBOR text. The reliable
discriminator is Rule XXI(b) itself — LIBOR means the superseded posting. Recorded as `W7`.

## The two CMI Assembly interventions — distinguished (TS-P07)

The maintained text is not the text adopted in New York in May 2016. Two Assembly interventions sit
between them, and they are **different events on different rules**:

| Event | Rule | Nature |
|---|---|---|
| CMI Assembly, **Genoa, September** (2016) | **Rule XVII** | Restoration of a sentence-ending dropped in error from the adopted text; the wording had stood in earlier versions |
| CMI Assembly, **Antwerp, October 2022** | **Rule XXI(b)** | Technical amendment re-basing the interest benchmark |

The Genoa footnote gives the month but **not the year**; 2016 is inferred from its own reference to the
New York adoption of May 2016 and is recorded as an inference rather than asserted as a dated fact.

Genoa is recorded here and in `YAR_INSTRUMENT_REGISTER.md` at instrument level only. `YAR-XVII` is
`unverified_legacy` with a recorded defect of its own and was **not** touched under TS-P07 — verifying
it against the maintained text is TS-P06 work.

### Rule XXI — what it actually provides (TS-P07)

*Rule text not reproduced here.* The verified wording is held in the private evidence layer as
`EVID-YAR-2016-XXI` (maintained text, both paragraphs) and `EVID-YAR-2016-XXI-B-ORIGINAL` (the
superseded paragraph (b)). The public objects carry the propositions and the pointers.

- **Paragraph (a) — the period.** Interest runs on expenditure, sacrifices and allowances until three
  months after the adjustment is **issued**, with credit for payments on account and for the deposit
  fund. **Unchanged** by the October 2022 amendment — established positively, by comparing the two CMI
  postings, not inferred from the footnote's placement alone.
- **Paragraph (b) — the rate, current.** Re-struck for each calendar year at the **USD Prime Rate plus
  2 per cent per annum**, on the figure the **Wall Street Journal** carried for that year's **opening
  banking day**. A US dollar rate whatever the adjustment currency.
- **Paragraph (b) — the rate, superseded.** As adopted: **twelve-month ICE LIBOR in the currency of the
  adjustment plus four percentage points**, with a twelve-month US dollar fallback. The amendment moved
  the benchmark, moved the margin, and removed the currency-matching limb altogether — an answer that
  changes only the benchmark is still wrong.
- **Edition.** Unchanged and still **York-Antwerp Rules 2016**. There is no YAR 2022.

## Findings

### Rule D — what it actually does

*Rule text not reproduced here.* Since the public-derived migration the verified wording is held in
the **private evidence vault** as `EVID-YAR-2016-D`, not in this repository. The public object
**`YAR-D`** (`YAR_DEFINITIONS.json`) carries the proposition and the pointer; the passage was checked
word for word against the CMI primary source identified in the table above (sha256 `0c364edb…`,
retrieved 2026-08-15). What follows is the proposition that reading established.

Rule D **preserves** the right to contribution notwithstanding the fault of a party, and **relocates**
the consequence of that fault into remedies and defences under the applicable law. It does **not** bar
the party at fault from claiming. The adjustment proceeds; the fault is litigated separately.

Any rule that a party at fault cannot recover in GA is a rule of the **applicable law**, not of the
York-Antwerp Rules — which is exactly why the **New Jason Clause** exists.

### Rule Paramount — what it actually governs

*Rule text not reproduced here.* The verified wording is held in the private evidence vault as
`EVID-YAR-2016-PARAMOUNT`. The public object **`YAR-PARAMOUNT`** (`YAR_DEFINITIONS.json`) carries the
proposition and the pointer; the passage was created and checked against the same primary source.

A **reasonableness gate**: it allows nothing unless the sacrifice or expenditure was reasonably made
or incurred. Under the Rule of Interpretation it overrides both the lettered and the numbered Rules,
but its subject matter is whether the sacrifice or expenditure was reasonable, not who was at fault. The pre-correction claim that it "bars GA where
fault of party claiming" was a **misattribution**, not an overstatement: the Rule Paramount says
nothing whatever about fault.

### Rule D source-fidelity defect (corrected)

The pre-correction `YAR-D` text read *"one of the parties to the adventure"* with a semicolon before
*"but"*. That is the **YAR 1994** wording, carried in the register under a **YAR 2016** label. The
substantive effect of the two versions is the same, so no downstream answer was misled — but the
object was not the text it claimed to be, and has been corrected to the 2016 wording.

### Rule VI — what it actually does (TSCR-9)

*Rule text not reproduced here.* The verified wording of paragraphs **(a)** and **(d)** is held in the
private evidence vault as `EVID-YAR-2016-VI`, checked word for word against the CMI primary source
identified in the table above. Paragraphs **(b)** and **(c)** were never held verbatim; their
substance is carried by the MIW proposition in the public object **`YAR-VI`**
(`YAR_DEFINITIONS.json`), which also carries the pointer to the evidence.

The two limbs that carry the correction are:

- **VI(a)** — salvage-type expenditure **is allowed** in general average, provided the operations were
  undertaken to preserve the imperilled property in the adventure, and **subject to paragraphs (b),
  (c) and (d)**.
- **VI(d)** — a shipowner's liability for **Article 14** special compensation under the Salvage
  Convention 1989, and for anything substantially equivalent such as **SCOPIC**, is **excluded from
  general average** and does not count as salvage expenditure under paragraph (a).

The pre-correction `YAR-VI` object asserted that salvage payments, together with interest and legal
costs, were excluded from general average, and it described Art. 14 / SCOPIC compensation as
particular charges. Set against the two paragraphs above:

- The **first limb was an inversion**. It is the **YAR 2004** Rule VI(a) position — salvage payments
  left to lie where they fell, not allowed in GA — carried under a **YAR 2016** label. Unlike the
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
| YAR 1994 | Salvage-type expenditure incurred by the parties to the adventure was **allowed** in general average | CMI tabular comparison, sha256 `c21b9482…` |
| YAR 2004 | Allowance **removed** — salvage payments were left to lie where they fell and were not allowed in general average, save a credit/debit proviso where one party had paid another's proportion | CMI YAR 2004, sha256 `b9e6c79a…` |
| YAR 2016 | Allowance **restored, qualified** — stated by the proposition in object `YAR-VI`; wording held privately as `EVID-YAR-2016-VI` | CMI YAR 2016, sha256 `0c364edb…` |

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
| `YAR-XVII` | A paraphrase, not the 2016 wording. YAR 2016 Rule XVII(a)(i) works from the actual net values of the property at the termination of the common maritime adventure, which this object does not state | MEDIUM |
| `YAR-A` | Matches YAR 2016 Rule A paragraph 1 exactly. Paragraph 2 is not held | LOW — accurate as far as it goes |
| `YAR_SEQUENCE` node 5 | References `YAR-XVIII`, `YAR-XIX`, `YAR-XX`. **None of these objects exists.** Three dangling references remain after TS-P03 (the `YAR-PARAMOUNT` dangler is now resolved) | MEDIUM — TSCR-8(c) territory |
| `COVERAGE_MATRIX` | Q6 asserts coverage via "Rule F"; no `YAR-F` object exists. Q3 asserts Rules XVII–XX; only `YAR-XVII` exists | MEDIUM — TSCR-8(c), already logged |

These are the substance of the future **TS-P06 full YAR corpus** work. TS-P03 does not close them and
does not claim to.

## How verification now resolves — public derived / private evidence

Adopted 2026-08-15. The package no longer holds source wording in its public objects. The chain is:

```
public object (YAR_DEFINITIONS.json)
  → verification.evidence_id
  → EVIDENCE_INDEX.json          (metadata only: source id, hashes, locator, location key)
  → private_location_key         (vault://cmi/yar/2016/rule-vi — logical, never a machine path)
  → private evidence vault       (the verbatim passage, outside this repository)
```

Reading this file end to end therefore gives the propositions and the audit trail, but not the rule
text. That is deliberate. `evidence_sha256` is the SHA-256 of the passage bytes, so a claim can still
be re-checked against exactly what was verified, by anyone holding the vault.

**Three objects have evidence; three do not.** `YAR-PARAMOUNT`, `YAR-D` and `YAR-VI` are
`primary_verified` and name an `evidence_id`. `YAR-A`, `YAR-C` and `YAR-XVII` are `unverified_legacy`
and name none, because none exists. The migration did not upgrade a single verification state, and an
object with no evidence says so rather than pointing at something that is not there. Full rules in
[`PRIVATE_EVIDENCE_BOUNDARY.md`](../PRIVATE_EVIDENCE_BOUNDARY.md).

## Rights position — MATERIALLY IMPROVED, ONE ITEM STILL OPEN

**Forward exposure is closed.** The public YAR object layer carried roughly 3,600 characters of
source wording before the migration and carries none after it. No source PDF was ever committed, and
none is held even privately — the CMI texts are recorded by URL, byte count and hash only.

**The historical exposure remains and is the open item.** Removing the wording from the current tree
does not remove it from earlier commits, which stay publicly reachable in this repository's history.
That is a separate founder decision — leave it, clear it, or rewrite history — and this migration
deliberately does none of the three.

The record of the original flag follows, retained as the audit trail.

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

*End of the retained original flag.*

**Superseded 2026-08-15 by the public-derived migration**, which closed the forward exposure outright
rather than waiting on the clearance decision. What survives of the original flag is narrower and
purely historical: **verbatim CMI wording remains in earlier public commits of this repository.**
That is the one rights item still requiring a founder decision.
