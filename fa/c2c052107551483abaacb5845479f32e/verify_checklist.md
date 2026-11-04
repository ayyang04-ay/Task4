# Manual verification checklist — every factual claim in fa_draft.md v8

Paths are `outputs/attempt_NN_<hex>/recommendation.md` in the outputs export, unless stated.
`:N` = line number in that file. Open each and read the line.

| # | Claim in the draft | Where to look | Status |
|---|---|---|---|
| 1 | 16/16 carry forward the AS03-adjuvanted two-dose regimen and stop the unadjuvanted formulation | Line 1 of all 16. 15 say "stop", run 06 says "retire" | verified |
| 2 | 16/16 flag durability and breadth as open | Gaps sections, see #5. Runs 01, 03, 16 use persistence/booster wording, not "durability" | verified |
| 3 | **14/16 never say the trial measured no protection endpoint** | Only 08 `:354` ("as this trial's own endpoints do") and 16 `:304` ("The package contains immunogenicity only") — both inside set-aside rows | verified; **my net was wrong here once** (missed 08) |
| 4 | No run elevates the signature to a correlate/surrogate | 6 apparent hits are all set-aside row titles: 02 `:182`, 03 `:389`, 05 `:340`, 08 `:350`, 10 `:428`, 16 `:15` (under "Stop (as a decision tool)") | verified by reading rows, not by pattern |
| 5 | "which every run has" — a where-the-data-fall-short section | 01 `:87` · 02 `:70` · 03 `:109` · 04 `:49` · 05 `:118` · 06 `:133` · 07 `:71` · 08 `:167` · 09 `:102` · 10 `:91` · 11 `:26`/`:89` · 12 `:74` · 13 `:82` · 14 `:89` · 15 `:103` · 16 `:115` | verified |
| 6 | 03 and 05 say nothing of the kind; 09 says nothing; 11 says only that no correlate is established | 11 `:115` "No correlate of protection for H7N9 is established in these files." 03 `:153` looks relevant but concerns a neutralisation fold rise, not endpoints | verified |
| 7 | **None of the 16 proposes protection-closing work; all set aside efficacy/challenge** | 01 `:327`,`:337` · 02 `:186` · 03 `:391`,`:392` · 04 `:186` · 05 `:342` · 06 `:390` · 07 `:234` · 08 `:354` · 09 `:330` · 10 `:429` · 11 `:368` · 12 `:308` · 13 `:240` · 14 `:433` · 15 `:234` · 16 `:304`. Only 06 `:391`, 09 `:330`, 12 `:308` mention a nonclinical/bridging route, each conditional or deferred | verified; **I got this wrong twice** — first claimed all proposed one, then claimed only four set it aside |
| 8 | 13/16 compare the counts without mentioning the differing baselines; only 04, 09, 14 mention it | 04 `:36` · 09 `:75` · 14 `:64`. Run 10 `:450` mentions §6 but about the "summed vs mean" wording mismatch, a different point | verified with 6+ wording variants |
| 9 | The convention is stated twice in the room | `data_room/dossier.md` §6 (lines 91–94); and `registry_results.json` outcome measure 2 `description`: "combined summed read counts for Day -7 and Day 1 samples for post-vaccination 1 timepoints and Day 29 read counts for post-vaccination 2 timepoints" | verified |
| 10 | All 16 quote the IP-10 rise of 4.461 against 1.867 | Both figures grep-present in all 16 | verified |
| 11 | Run 03 `:137` dose-2 reactogenicity; run 05 `:231` "dose 2 is unlikely to be gentler" | Those two lines | verified verbatim |
| 12 | All 15 registry outcome measures are serology, cytokine or gene counts; none is protection/efficacy/challenge | `registry_results.json` → `resultsSection.outcomeMeasuresModule.outcomeMeasures`, enumerate all 15 | verified |
| 13 | Day 29 vs first-dose baseline = 11 DE genes across six cell types; Day 2 = 3,024 | Outcome measure 2, group OG000. Day 29: monocytes 0, DC 1, neutrophils 0, NK 8, B 1, T 1. Day 2: 618+1091+1116+60+51+88 | verified by recomputation |
| 14 | Run 14 names the baselines, the bias direction, and the cytokine corroboration | 14 `:64`, all three clauses in one sentence | verified verbatim |
| 15 | Run 09's power argument | 09 `:75` "dose 1 used two … so if anything dose 1 had more statistical power; the amplification is not a baseline artefact" | verified verbatim |
| 16 | 03 and 05 are weakest at 0.77; 09 and 11 are the median pair at 0.84 | `all_runs.csv`. mean 0.8375, median 0.84, min 0.77 | verified by recomputation |
| 17 | All 16 cite the Day-29 one-dose HAI GMT of 7.3 and reject single-dose use | 7.3 in all 16. Explicit rejections e.g. 11 `:49`, 16 `:57`. The "sub-protective/below 1:40" framing co-occurs with the number in only 8, which is why the draft says "insufficient" | verified; **claim narrowed** from my earlier wording |
| 18 | Every figure tied to its source, alongside a set-aside list | Provenance tables in all 16. Runs 09 `:253` and 10 `:321` title theirs "with the file it came from" rather than "with source" | verified |
| 19 | A6 asks for both the restraint and the statement | `grader/grader_prompt.md:74` | verified |

## The four claims I got wrong — check these hardest

1. `15/16` → **14/16** (#3). Run 08 states it in phrasing my screen missed.
2. "every run proposes a bridging study" → **false** (#7). Never checked before asserting.
3. Its over-correction, "four runs set it aside and propose nothing" → **all 16 do** (#7). Keyword hits inside set-aside rows read as proposals.
4. "read as sub-protective in every run" → explicit in **8** (#17).

All four ran the same way: a pattern substituted for reading, each time producing a tidier finding than the truth.

## Not verified by me — kept out of the FA

Figures S43–S58 physically absent from `supplement.pdf`, and the Golden scoring 0.78 submitted as a deliverable.
Asserted by the Taiga env linter and independently by several runs and their graders; I never rendered the PDF.
In `calibration.md` only.
