# FA draft v8 — H7N9 next-work recommendation, job 30f4652b (16 × Opus 5.5)

RETYPE, DO NOT TRANSCRIBE.
SCOPE: model conduct only, load-bearing failures only, anchored on the weakest runs — 03 (890bbf23) and
05 (b07ef105), both 0.77 — and the median pair, 09 (9687c0b1) and 11 (60c1bbbc), both 0.84.
CUT BY INSTRUCTION as immaterial, retained in error_modes.md: comparator-arm keratin/hornerin never
characterised (13/16, never misused); "time to protection" treated as measurable (4/16); run 12's
antigen-sparing over-claim (1/16). Grading-document findings stay in calibration.md, unreferenced here.
Counts: paragraph 1 = 15 sentences, paragraph 2 = 10 sentences.
AUDITED THREE TIMES; pass 3 found no new factual errors: see audit.md. Four claims were wrong across v5-v6 and are corrected here: 15/16 -> 14/16;
the false claim that every run proposed a bridging study; its over-correction to "four runs"; and
"read as sub-protective" narrowed to what all 16 actually do.

## What did the model do wrong?

All 16 runs get the primary verdict right: carry forward the AS03-adjuvanted two-dose regimen rather than the
antigen alone, stop the unadjuvanted formulation, and flag durability and breadth as open questions. All 16 also
get right the judgment the task was built around. Each one treats the interferon signature as a predictor of HAI
titre and refuses to promote it to a protection marker, and several go further than the Golden by showing that
Table S186 pools both A/H7N9 arms, so its "predictor" really marks AS03 receipt. The failures are narrower.

1. **Only 2 of 16 say what the trial actually measured.** The record holds serology, cytokines and gene counts
   and stops there: no protection, efficacy or challenge endpoint anywhere in it. Run 08 (f9779a6c) `:354` and
   run 16 (9993e8bb) `:304` state this, and both put it in a set-aside row rather than the gaps section that
   every run has. The two weakest runs, 03 (890bbf23) and 05 (b07ef105), leave it out, as does median run 09
   (9687c0b1). Median run 11 (60c1bbbc) `:115` makes a different and weaker claim, that no correlate of
   protection has been established — a point about how to read a titre rather than about what the study
   measured.

2. **All 16 file the protection question under "set aside" rather than answering it.** Each run puts field
   efficacy and human challenge in its set-aside section on feasibility or ethics grounds: 03 `:391`–`:392`,
   05 `:342`, 09 `:330`, 11 `:368`, and the same across the other twelve. Only 06, 09 and 12 gesture at a
   nonclinical or immunobridging route, each one hedged or postponed — 12 `:308` has it "can wait for pivotal
   planning". So 14 runs leave the gap unstated, and all 16 leave it unworked.

3. **Only 3 of 16 name the baseline convention before comparing across it.** Runs 04 `:36`, 09 `:75` and 14
   `:64` name it; the other 13 set the dose-1 and dose-2 gene counts side by side as though they were measured
   the same way. The room spells the convention out twice, in `dossier.md` §6 and again in the registry's own
   description of the gene-count measure. The conclusion survives — the innate response really is larger after
   dose 2, and all 16 cite the IP-10 rise of 4.461 against 1.867, which does sit on one common baseline — so
   the fault is in the workings.

4. **In the two weakest runs that unnamed step reaches a decision.** Run 03 `:137` uses it to make dose-2
   reactogenicity a measurement requirement, and run 05 `:231` to conclude that dose 2 is unlikely to be
   gentler. Each run therefore rests a study-design call and a deployment call on a step it never justified.


## What should the model have done?

Run 16 (9993e8bb) shows what the first item needed, and run 14 (f8782a66) shows what the second needed. On
A6 the line to write is a plain one: all fifteen outcome measures in the registry are serology, cytokines or
gene counts, not one of them measures protection, efficacy or challenge, and that gap — not the shakiness of
any single titre — is what a bridging study would be for. It belongs in the section on where the data fall
short, which all sixteen have, rather than in a table at the back. Every run already behaved as though it
knew this, so writing it down is what turns the caution into a finding, and it is what would have shown that
setting efficacy and challenge aside, as all sixteen do, still leaves something to close. On the gene
counts, run 14 does the whole job in one sentence: it names the two baselines, points out that the dose-2
convention would if anything find fewer genes, and backs the direction with cytokine fold changes measured
from a single baseline. Run 09 makes a neater version of the same point, that dose 1 had two baseline draws
behind it and so had more statistical power rather than less. The registry settles it either way. Measured
against the first-dose baseline, Day 29 shows eleven differentially expressed genes across all six cell
types, against 3,024 on Day 2, so the Day-29 reference is effectively pre-vaccination. One sentence of that
would have left the conclusion standing and given the calls in 03 and 05 something to stand on. The rest was
already right everywhere: the adjuvanted regimen as the asset, the Day-29 one-dose HAI GMT of 7.3 treated as
insufficient and single-dose use rejected, durability and breadth named as open, and every figure tied to
its source alongside a reasoned set-aside list.
