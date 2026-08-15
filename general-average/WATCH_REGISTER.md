# WATCH REGISTER

Package: general-average · as_at: 2026-08-13

| # | Item | Watch |
|---|---|---|
| W1 | YAR version | Current = YAR 2016; watch for any CMI revision; many contracts still use YAR 1994/1974 |
| W2 | Rule Paramount | A reasonableness gate: it admits nothing unless the sacrifice or expenditure was reasonably made or incurred. Watch case law on what that reasonableness standard requires. **It is not a fault gate** — corrected 2026-08-15, TSCR-6 |
| W3 | Official text capture | CMI official YAR 2016 text verified 2026-08-15 for the Rule Paramount, Rule D and **Rule VI** only (see `YAR_SOURCE_PROVENANCE.md`). **The remaining definition objects have not been checked against it, and two are known to carry pre-2016 content** — see the residual defects in that file. The public-derived migration did **not** change this: three objects are `primary_verified` and three are `unverified_legacy`, exactly as before |
| W5 | Private evidence availability | The verbatim evidence behind the verified objects now lives outside this repository, addressed by `evidence_id` and `private_location_key` — see `PRIVATE_EVIDENCE_BOUNDARY.md`. Watch that the vault stays available and that its `evidence_sha256` values continue to match `EVIDENCE_INDEX.json`. A mismatch is investigated, never reconciled by editing a hash — added 2026-08-15, YAR public-derived migration |
| W4 | Edition of the incorporated Rules | The salvage treatment under Rule VI has moved **twice**: allowed under YAR 1994, removed by YAR 2004, restored subject to qualifications by YAR 2016. Any statement about salvage in GA is edition-dependent and must name its edition. Watch for contracts still incorporating 1994 or 2004 — added 2026-08-15, TSCR-9 |