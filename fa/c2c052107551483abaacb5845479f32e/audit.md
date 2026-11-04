# Audit of my own FA output — every factual claim in fa_draft.md, checked against source

Method: each claim re-tested against the 16 graded `recommendation.md` files in the outputs export, or
recomputed from `data_room/registry_results.json`. Screens were re-run with deliberately looser patterns than
the ones that produced the original counts, because a tight pattern fails in the direction of a clean finding.

## Claims that FAILED and are now corrected

| # | Claim as written in v5 | Verdict | What is true | Where it came from |
|---|---|---|---|---|
| 1 | "fifteen of sixteen never say that this trial measured protection at all" / "Only run 16 (9993e8bb) does the second" | **WRONG** | **Fourteen of sixteen.** Run 08 (f9779a6c) states it too, at `:354`: "The development pathway has to rest on immunogenicity (as this trial's own endpoints do)". Like run 16's `:304`, it sits in a set-aside table row — for 08 the "Human challenge or field-efficacy trial" row. Both state it; neither states it in its gaps section. | My original screen required the absence to be predicated on "outcome measure(s)", "endpoint in", "every outcome", "immunogenicity only" or similar. Run 08's parenthetical phrasing matched none of them. |
| 2 | "All of these proposals then ask for a bridging or correlate study, and in fifteen of sixteen that request has nothing underneath it" | **WRONG** | Four runs propose no such study at all. Runs 03 (`:391–392`), 04 (`:186`), 11 (`:368`) and 13 (`:240`) set aside field efficacy and human challenge on feasibility and ethics grounds and offer nothing in their place. | I never checked it. I inferred it from the Golden's next-study list and from the runs I had read in full, and asserted it for all 16. Two of the four are my anchor runs — 03 (weakest) and 11 (median). |

Correcting #2 strengthens the finding rather than weakening it: in those four runs the protection gap is neither
named nor addressed, where previously I claimed it was addressed on an unstated basis.

## Claims that PASSED

| Claim | Check |
|---|---|
| 16/16 carry the adjuvanted two-dose regimen on line 1 | Line 1 of all 16 names AS03 or the adjuvant |
| 16/16 name durability and breadth as open | Confirmed; runs 01, 03 and 16 use wording my first regex missed (persistence / Day-57 / booster), re-checked individually |
| 03 and 05 are the weakest at 0.77; 09 and 11 are the median pair at 0.84 | Recomputed over all 16 scores: mean 0.8375, median 0.84, min 0.77. Median runs 09, 11; min runs 03, 05 |
| Run 11 `:115` "No correlate of protection for H7N9 is established in these files…" | Verbatim match |
| "which every run has" (a where-the-data-fall-short section) | 03 `:109`, 05 `:118`, 09 `:102`, 11 `:89` — all present, all four anchor runs |
| 13/16 compare the counts without mentioning the differing baselines; only 04, 09, 14 mention it | Re-run with six wording variants after the first regex missed run 14's phrasing. 04 `:36`, 09 `:75`, 14 `:64` |
| The convention is stated twice in the room | `dossier.md` §6, and registry OM2 description: "combined summed read counts for Day -7 and Day 1 samples for post-vaccination 1 timepoints and Day 29 read counts for post-vaccination 2 timepoints" |
| All 16 quote the IP-10 rise of 4.461 against 1.867 | Both figures present in all 16 |
| Day 29 vs first-dose baseline = 11 DE genes across six cell types; Day 2 peak 3,024 | Recomputed from OM2: monocytes 0, DC 1, neutrophils 0, NK 8, B 1, T 1; Day-2 sum 618+1091+1116+60+51+88 |
| Run 03 `:137` dose-2 reactogenicity; run 05 `:231` "dose 2 is unlikely to be gentler" | Verbatim matches |
| Run 14 `:64` names the baselines, bias direction, cytokine corroboration | Verbatim |
| Run 09 `:75` the power argument | Verbatim |
| All 15 registry outcome measures are serology, cytokine or transcriptomic | Enumerated all 15; no protection, efficacy or challenge endpoint |
| 16/16 cite the Day-29 one-dose HAI GMT of 7.3 | Present in all 16 |

## Earlier corrections already recorded

- M3 was first counted at 8/16 and is 4/16; the first pattern swept in conservative planning language ("treat
  recipients as unprotected between doses") and run 16's correctly framed "immunogenicity milestones, not
  protection dates". Recorded in error_modes.md.
- The dose-sparing over-claim was first attributed to runs 08, 12 and 15 and is run 12 only. Run 08 labels the
  15 µg arm "a different product; context only"; run 15 ties its claim to adjuvant dependence.
- The transcript reconstruction used before the outputs export arrived gave body-file snapshots for 6 of 16 runs
  and would have mis-stated two counts; superseded.

## Pattern in my own errors

All five errors ran the same way: a pattern tight enough to produce a clean count, with the misses falling
outside it, or an unchecked inference that fitted the story I already had. Four of the five inflated the
prevalence of a failure or the tidiness of a finding. The one claim I never tested at all (#2) is the one that
was flatly false.

## Not independently verified — flagged rather than asserted

The claim that supplement figures S43–S58 are physically absent, and that the Golden scored 0.78 submitted as a
deliverable, comes from the Taiga env linter and from run and grader statements. Multiple runs and graders assert
the page gap independently, but I did not render the PDF myself. It is in calibration.md, not in the FA.

---

# Audit pass 2 — adversarial re-test, targeting my own error pattern

Pass 1 found that my errors came from patterns tight enough to yield a clean count, and from unchecked
generalisations. Pass 2 therefore re-tested every "every run…" claim across all 16, and re-ran each count with
deliberately looser patterns.

## FAILED again — the pass-1 correction was itself wrong

| Claim | Verdict | What is true |
|---|---|---|
| Pass 1 corrected #2 to: "03, 04, 11 and 13 set aside field efficacy and human challenge and put nothing in their place, so in those four the protection gap is neither stated nor worked." | **WRONG — over-corrected** | **All 16 do this.** Every run places field efficacy and/or human challenge in a set-aside section: 01 `:327,:337`, 02 `:186`, 03 `:391–392`, 04 `:186`, 05 `:342`, 06 `:390`, 07 `:234`, 08 `:354`, 09 `:330`, 10 `:429`, 11 `:368`, 12 `:308`, 13 `:240`, 14 `:433`, 15 `:234`, 16 `:304`. None proposes protection-closing work. Only 06 (`:391`, conditional on regulators), 09 (`:330`, "the route is immunobridging") and 12 (`:308`, "can wait for pivotal planning") mention a nonclinical or bridging route at all. |

Cause: my pass-1 screen counted the presence of keywords like "bridging" or "challenge study" as evidence that a
run *proposed* such work. Those keywords sit in set-aside rows that say the opposite. I read a keyword hit as a
proposal without opening the row. This is the same failure as #1 and #2 — a pattern standing in for reading —
and it produced a tidy four-run finding where the truth is uniform across the panel.

## Also narrowed

| Claim | Verdict | What is true |
|---|---|---|
| "the Day-29 one-dose HAI GMT of 7.3 read as sub-protective" in every run | **Overstated** | All 16 cite 7.3 and all 16 reject single-dose use, but the explicit "sub-protective / below 1:40" framing co-occurs with the number in only 8. The others read it as a floor or non-response (15 `:15` "below the 1:10 detection limit"). Draft now says "treated as insufficient and single-dose use rejected", which holds for all 16. |

## PASSED on re-test

| Claim | Check |
|---|---|
| "which every run has" — a where-the-data-fall-short section | All 16, by heading: 01 `:87`, 02 `:70`, 03 `:109`, 04 `:49`, 05 `:118`, 06 `:133`, 07 `:71`, 08 `:167`, 09 `:102`, 10 `:91`, 11 `:26/:89`, 12 `:74`, 13 `:82`, 14 `:89`, 15 `:103`, 16 `:115` |
| No run elevates the signature to a correlate or surrogate | Adversarial sweep returned 6 candidates; all 6 are set-aside row titles naming the option being rejected (02 `:182`, 03 `:389`, 05 `:340`, 08 `:350`, 10 `:428`, 16 `:15` under "Stop (as a decision tool)"). Restraint holds 16/16, established by reading the rows, not by pattern |
| "every figure tied to its source" — a provenance table in all 16 | All 16. Runs 09 `:253` and 10 `:321` first read as absent because they title it "with the file it came from" rather than "with source" — another false negative of the same kind |
| Every run rejects single-dose use | All 16 address it; explicit rejections e.g. 11 `:49` "no support for a single-dose regimen at this formulation", 16 `:57` "A single-dose use of this formulation is not supported" |
| Run 14's handling carries all three clauses in the deliverable | `:64` verbatim: "This is not an artefact of the baseline: dose-2 comparisons use a single Day-29 draw, while dose-1 comparisons average two draws (DOS §6). That difference would, if anything, reduce the number of genes called after dose 2, and the cytokines below show the same amplification." |
| 14/16 never state the endpoint-inventory fact | Re-stressed with a net keyed on measures/endpoints/record rather than titres; surfaced run 08 in pass 1 and nothing further in pass 2 |

## Status

Four errors found across two passes, all of mine, all running the same way: a pattern substituted for reading, and
every time the pattern produced a cleaner finding than the truth. Pass 2 found one new failure and it was in the
pass-1 correction itself, which is the strongest argument for the third pass rather than for declaring this clean.
