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

All 16 runs reach the correct primary verdict: carry forward the AS03-adjuvanted two-dose regimen, stop the
unadjuvanted formulation, and name durability and breadth as open.

1. **2/16 state that the trial measured no protection endpoint** — run 08 (f9779a6c) `:354` and run 16
   (9993e8bb) `:304` — and both put it in a set-aside row rather than their gaps section. 14/16 leave it out,
   including both weakest runs, 03 (890bbf23) and 05 (b07ef105), and median run 09 (9687c0b1). 1/16, median run
   11 (60c1bbbc) `:115`, substitutes a weaker claim: that no correlate of protection has been established, which
   is a point about reading a titre.

2. **16/16 set aside field efficacy and human challenge** on feasibility or ethics grounds — 03 `:391`, 05
   `:342`, 09 `:330`, 11 `:368`, and the same across the other twelve — and **0/16 propose a study to close the
   gap.** 3/16 (06, 09, 12) mention a nonclinical or immunobridging route, each hedged or postponed; 12 `:308`
   has it "can wait for pivotal planning".

3. **13/16 compare dose-1 and dose-2 gene counts across different baselines without naming the convention.**
   3/16 name it: 04 `:36`, 09 `:75`, 14 `:64`. The room states it twice, in `dossier.md` §6 and in the registry's
   own description of the gene-count measure. 16/16 still reach the right conclusion and cite the IP-10 rise of
   4.461 against 1.867, which sits on one common baseline, so the fault is in the workings.

4. **2/16 carry that unnamed step into a decision** — and they are the two weakest runs. Run 03 `:137` uses it
   to make dose-2 reactogenicity a measurement requirement; run 05 `:231` uses it to conclude that dose 2 is
   unlikely to be gentler.


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
