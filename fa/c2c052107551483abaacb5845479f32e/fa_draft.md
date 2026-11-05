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

A16 (9993e8bb) is the only run that models the first point and A14 (f8782a66) the third; no run models the second.

The runs should have stated what the trial measured. All 15 outcome measures in the registry are serology,
cytokines or gene counts, and none is a protection, efficacy or challenge endpoint. That absence, rather than the
weakness of any single titre, is what a bridging study exists to close. It belongs in the section on where the
data fall short that every run already has, not in a set-aside row where A08 and A16 put it.

They should then have named a route to close it. Field efficacy and human challenge really are foreclosed, so what
remains is a nonclinical challenge, passive-transfer or immunobridging path with a stated acceptance criterion.
A12 (1596ccf2) names one and then postpones it; naming it as the next study is the move.

On the gene counts, the baseline convention should have been named before comparing across it. A14 does this in
one sentence: it names the two baselines, notes that the dose-2 convention would if anything find fewer genes, and
backs the direction with cytokine fold changes measured from a single pre-vaccination baseline. A09 (9687c0b1)
adds that dose 1 drew on two baseline samples and so had more power, not less. The registry also reports Day 29
against the first-dose baseline at 11 differentially expressed genes across six cell types, against 3,024 on Day
2, so the two reference points are nearly identical and the comparison holds once that is said.

Everything else was already right in all 16: the adjuvanted regimen as the asset, the Day-29 one-dose HAI GMT of
7.3 treated as insufficient and single-dose use rejected, durability and breadth named as open, every figure tied
to its source alongside a reasoned set-aside list, and the interferon signature kept as a predictor of HAI titre
rather than promoted to a protection marker.
