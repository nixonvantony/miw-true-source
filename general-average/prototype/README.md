# PROTOTYPE — public-derived knowledge / private evidence

**Status: ARCHITECTURE PROTOTYPE. Not canonical. Not a migration.**

Branch: `architecture/public-derived-private-evidence-prototype`, cut from `c598a9d`.

`general-average/YAR_DEFINITIONS.json` remains the canonical object file and is **unchanged** on this
branch. These files sit alongside it so the two models can be compared directly.

## What this tests

Whether a public knowledge object can carry the full reasoning load without carrying the source
wording — by holding an MIW-authored proposition plus a deterministic pointer to the evidence that
verified it, instead of the verbatim rule text.

## Files

| File | Contains | Committed |
|---|---|---|
| `YAR_PUBLIC_OBJECTS.json` | Three derived public objects — `YAR-PARAMOUNT`, `YAR-D`, `YAR-VI` | Yes |
| `EVIDENCE_INDEX.json` | Evidence and source metadata only — identity, hashes, dates, location keys | Yes |
| `../../_prototype-private-evidence/` | Simulated private layer holding the verbatim passages | **No — `.gitignore`d** |

## Scope

Only the three objects corrected under TSCR-6 and TSCR-9 are prototyped. `YAR-A`, `YAR-C` and
`YAR-XVII` are deliberately left alone, as are the missing `YAR-XVIII` / `XIX` / `XX` objects.

## The boundary

The public object states **what the law is** and **what evidence establishes it**. It does not
reproduce the evidence. The chain is:

```
public object → evidence_id → EVIDENCE_INDEX entry → source_id → source sha256 → locator
                                                   → private_location_key → private evidence
```

`private_location_key` is logical (`vault://cmi/yar/2016/rule-vi`), never a machine path, so the
public layer stays valid wherever the private layer physically lives.

`evidence_sha256` is defined as the sha256 of the UTF-8 bytes of the verbatim passage itself, not of
the file carrying it — the passage keeps its identity across reformatting and relocation.

## What this is not

Not a rights judgment. The separation is worth having even if quotation turns out to be cleared,
because it stops evidence and derived knowledge from becoming architecturally coupled. The rights
flag in `../YAR_SOURCE_PROVENANCE.md` is untouched and still open.

No private repository was created. No source PDF was added. No canonical file was modified.
