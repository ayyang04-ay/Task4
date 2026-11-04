# Item matrix — read cell by cell from each grader's rationale, not parsed from prose

A1 attribution · A2 two-dose · A3 dose-sparing · A4 durability · A5 breadth · A6 protection/signature · A7 provenance+set-aside
`Y` met · `P` partial · `—` not stated. B column lists the B items the grader recorded as firing, with the severity word it used.

| att | run | score | A1 | A2 | A3 | A4 | A5 | A6 | A7 | B items fired |
|---|---|---|---|---|---|---|---|---|---|---|
| 01 | cd3e5696 | 0.83 | Y | Y | P | Y | Y | Y | Y | B5 "one clear methodological error", mitigated |
| 02 | b73e9851 | 0.88 | Y | Y | P | Y | Y | Y | Y | B5 "yes, partially" / "one minor penalty" |
| 03 | 890bbf23 | 0.77 | Y | Y | P | Y | Y | P | Y | B5 "fires partially" |
| 04 | 0842f297 | 0.90 | Y | Y | P | Y | Y | P | Y | B5 "minor at most" — caveat present |
| 05 | b07ef105 | 0.77 | Y | Y | P | Y | Y | P | Y | B5 "a real analytical error… moderately serious" |
| 06 | 1f19cd35 | 0.92 | Y | Y | P | Y | Y | Y | Y | B5 "minor" / "deduction is small" |
| 07 | 06a4976d | 0.88 | Y | Y | P | Y | Y | Y | Y | B5 "not the penalized error", a "lapse" |
| 08 | f9779a6c | 0.80 | Y | Y | **Y** | Y | Y | Y | Y | B5 "FIRES. This is the real error" |
| 09 | 9687c0b1 | 0.84 | Y | Y | P | Y | Y | P | Y | B5 "minor-moderate" — discharged by the attempt |
| 10 | ef72c97f | 0.80 | Y | Y | P | Y | Y | P | Y | B5 "this fires… one real error" |
| 11 | 60c1bbbc | 0.84 | Y | Y | P | Y | Y | Y | Y | B5 "triggered… moderate" |
| 12 | 1596ccf2 | 0.79 | Y | Y | **Y** | Y | Y | P | Y | B5 "committed" |
| 13 | 15a5af69 | 0.80 | Y | Y | P | Y | Y | Y | Y | B5 "fires" |
| 14 | f8782a66 | 0.88 | Y | Y | P | Y | Y | Y | Y | B5 "does not fire" — "a minor methodological point" |
| 15 | abf75de9 | 0.85 | Y | Y | **Y** | Y | Y | Y | Y | B5 "a genuine methodological error" |
| 16 | 9993e8bb | 0.85 | Y | Y | P | Y | Y | Y | Y | B5 "one penalty fires" |

## Per-item summary

| Item | Met | Partial | Discriminates? |
|---|---|---|---|
| A1 attribution to the adjuvanted configuration | **16/16** | 0 | No |
| A2 two-dose necessity | **16/16** | 0 | No |
| A3 dose-sparing as quarter of 15 µg | 3/16 (08, 12, 15) | 13/16 | Yes — but the item is unsound (see ledger) |
| A4 durability gap | **16/16** | 0 | No |
| A5 breadth gap | **16/16** | 0 | No |
| A6 protection endpoint / signature restraint | 10/16 | 6/16 (03, 04, 05, 09, 10, 12) | Weakly |
| A7 provenance + set-aside | **16/16** | 0 | No |
| B1 unadjuvanted carry-forward | avoided 16/16 | — | — |
| B2 single dose sufficient | avoided 16/16 | — | — |
| B3 signature elevated to surrogate | avoided 16/16 | — | — |
| B4 keratin/hornerin as biology | avoided 16/16 | — | — |
| B5 cross-dose DE comparison | **fired 13/16** (not 04, 07, 14) | — | The only firing trap — and it is a grader defect |
| B6 cross-cell-type loading | avoided 16/16 | — | — |
| B7 H3N2v recall / 1.4× cross-antigen as merit | avoided 16/16 | — | — |

No uncertain cells: every firing or partial cell above was read in the rationale itself.

The B5 row is the one the score ordering is built on, and it inverts: attempt 08 (0.80) was told "FIRES. This is the
real error"; attempt 14 (0.88) was told the same conduct "does not fire". Both compared DE counts across the
boundary; attempt 14 named the convention and attempt 08 did not, so the severity tracks whether the attempt
*mentioned* the convention, not whether its conclusion was sound. Both conclusions were sound.
