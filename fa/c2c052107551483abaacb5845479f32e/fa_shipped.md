# FA as submitted — Task pu3h8f5d / c2c052107551483abaacb5845479f32e, job 30f4652b

Writer's final text, recorded VERBATIM. Hand-written texture (typos, spacing, capitalisation) is deliberate and
left unedited. Verification for every factual claim is in verify_checklist.md; the A04 correction applied here
was the last outstanding item (see qc.md, Resolution).

---

## What did the model do wrong?

note: AXX indicates attempt XX where XX is the number of the model run. 

All 16 runs were correct in their primary verdict: carrying forward the AS03 adjuvanted two-dose regimen rather than antigen alone and flagging durability and breadth as open questions. 

Only 2/16 state that the trial failed to measure protection: A08 (F9779A6C) and A16 (9993e8bb), and both set it aside rather than noting it as a gap. 14/16 runs leave it out entirely, including both of the weakest-scoring runs (A03; 890BBF23, A05; B07EF105). Median-scoring runs (such as A11) make a weaker claim: that no correlate of protection has been established.
All runs dismissed field efficacy and human challenge based on feasibility  or ethics. No models propose any studies to close that gap. 3/16 models mention a nonclinical or immunobridging plan, but don't provide a plan to do so (postpoining it). 
13/16 runs compare dose 1 and dose 2 gene counts across different baselines without separating comparisons (comparing dose 1 to dose 2).  2/16 runs carry these comparisons forward into their final decision, which are notable the weakest-scoring runs (A03, A05). 

## What should the model have done?

High-performing models should: 
State what the trial measured: all 15 outcome measures in the data room were serology, cytokines, or gene counts; note that none of it was protection, efficacy, or challenge endpoints. A08 and A16 noted this, but this note should belong in every run as a noted gap, not as a set-aside. 
Propose a route to close that gap: field efficacy/human challenge are nonviable, so the answer should be a nonclinical challenge, passive-transfer, or some immunobridging studies. A12 names one but postpones/defers it as the next study move. 
Name the baseline conventions its using in comparisons (dose 1 or dose 2). A04, A09, and A14 are the only runs that explicitly name their baseline comparisons/conventions. 
Everything else was already correct in all 16 runs: the adjuvanted regimen as the asset, the day-29 one-dose HAI GMT of 7.3 treated as insufficient and therefore single-dose use rejected, durability and breadth named as open, every figure/claim tied to its source alongside a reasoned set-aside list (as instructed), and the interferon signature kept s a predictor of HAI titer rather than promoted to a protection marker. 

---

## Run id map

| Label | Run id | Score |
|---|---|---|
| A03 | 890bbf23 | 0.77 (weakest) |
| A04 | 0842f297 | 0.90 |
| A05 | b07ef105 | 0.77 (weakest) |
| A08 | f9779a6c | 0.80 |
| A09 | 9687c0b1 | 0.84 (median) |
| A11 | 60c1bbbc | 0.84 (median) |
| A12 | 1596ccf2 | 0.79 |
| A14 | f8782a66 | 0.88 |
| A16 | 9993e8bb | 0.85 |

Panel: 16 runs, claude-opus-5-5, mean 0.8375, range 0.77-0.92, 0 refusals.
