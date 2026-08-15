# PRIVATE EVIDENCE BOUNDARY

**Adopted 2026-08-15. Applied so far to the `general-average` package only.**

This repository is public. The knowledge in it is MIW's own; the sources behind that knowledge are
other people's. This document states where the line runs and how a reader crosses it legitimately.

## Why the boundary exists

Two reasons, and the second matters even if the first is one day resolved.

1. **Rights.** Instrument texts are copyright of the bodies that adopt them — the CMI for the
   York-Antwerp Rules. Reproducing substantial wording in a public repository is not something a
   corpus-construction session can authorise.
2. **Architecture.** Coupling derived knowledge to source evidence makes both worse. Evidence cannot
   be relocated, re-hashed or restricted without editing the knowledge layer, and the knowledge layer
   cannot be published without carrying the evidence with it. Separating them once removes a whole
   class of future problem, whatever the rights answer turns out to be.

## What the public layer contains

MIW-authored knowledge and verification pointers: object IDs, instrument identity, edition, locator,
term, a concise MIW-authored proposition, verification status, source ID, evidence ID, source
SHA-256, evidence SHA-256, retrieval date, edition history, reasoning relationships, traps, and
coverage or watch metadata.

The proposition must be **independently understandable**. A public object that degrades into
*"see private source"* has failed: it would move the rights problem without keeping the knowledge.

## What the private layer contains

Primary-source files, substantial verbatim wording, extracted passages, verification excerpts, source
captures, and any other rights-sensitive evidence. It lives outside this repository and outside any
public Git history.

## How `evidence_id` works

Each verified public object names an `evidence_id`. That ID resolves in
[EVIDENCE_INDEX.json](general-average/EVIDENCE_INDEX.json), which carries metadata only — never
wording — and gives a `private_location_key` such as `vault://cmi/yar/2016/rule-vi`. The key is
**logical**: local configuration maps the vault root, so the public layer stays valid wherever the
evidence physically lives.

```
object_id → evidence_id → EVIDENCE_INDEX → source_id → source_sha256
                                         → evidence_sha256 → locator
                                         → private_location_key → private evidence
```

## How hashes provide verification

- `source_sha256` identifies the source document as retrieved.
- `evidence_sha256` is the SHA-256 of the UTF-8 bytes of the verbatim passage itself, **not** of the
  file carrying it — so the passage keeps its identity across reformatting and relocation.

A public object and its private evidence agree only if the hashes match. A mismatch means one side
moved, and it is investigated — **never** reconciled by editing a hash to fit.

## If private evidence is unavailable

The public layer keeps working. Propositions, relationships and traps are all readable without it;
only the ability to re-check wording is lost. An unavailable vault therefore downgrades
*auditability*, not *usability*, and the public object must never be rewritten to compensate.

An object with **no** evidence is a different case, and an honest one. `YAR-A`, `YAR-C` and
`YAR-XVII` carry `unverified_legacy` and assert no evidence ID at all, because none exists. That is a
recorded gap, not a broken link. Verification state is never upgraded by migration.

## Prohibitions

- **No absolute local paths in public data.** Use a `vault://` key — never a Windows drive path, a
  Unix home path, or any other local filesystem address. Such a path is machine-specific and leaks
  the operator's filesystem into the public record. This prohibition is absolute, which is why no
  literal example of a forbidden path appears anywhere in this repository.
- **No source PDFs or substantial verbatim wording in this repository**, in any file or commit.
- **No fabricated evidence.** Never invent an `evidence_id`, copy a hash forward without recomputing
  it, or record verification that did not happen. An object with no evidence says so.
- **No proposition built by copying a source sentence and deleting the quotation marks.** Terms of art
  are unavoidable and permitted; copied prose is not.

## Known limitation — historical Git exposure

Removing verbatim wording from the current tree does **not** remove it from earlier commits, which
remain publicly reachable. That is a separate decision for the founder and is not addressed by this
boundary, which governs the repository going forward.
