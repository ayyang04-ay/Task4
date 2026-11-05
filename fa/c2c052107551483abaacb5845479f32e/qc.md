# QC of the writer's draft — "What did the model do wrong?"

Verdicts are against the 16 graded deliverables and the registry. Citations are run + line in
`outputs/attempt_NN_<hex>/recommendation.md`.

| # | Claim | Verdict | Evidence / correction stated as fact |
|---|---|---|---|
| 1 | All 16 correct in the primary verdict: adjuvanted two-dose regimen over antigen alone, durability and breadth flagged open | **supported** | Line 1 of all 16 names AS03 and stops the unadjuvanted formulation; gaps section in all 16 |
| 2 | Only 2/16 state that the trial failed to measure protection: A08, A16 | **supported** | A08 `:354`, A16 `:304` |
| 3 | Both set it aside rather than noting it as a gap | **supported** | Both sit in a set-aside row, not the gaps section each run has |
| 4 | 14/16 leave it out entirely, including both weakest runs A03, A05 | **supported** | — |
| 5 | Median-scoring runs (such as A09, A11) make a weaker claim: no correlate of protection established | **unsupported for A09** | A09 makes neither claim. The weaker claim is made by **5 runs: A01 `:122`, A02 `:83`, A11 `:115`, A13 `:186`, A15 `:200`**. A11 is the only median run among them, so it is not a median-run pattern |
| 6 | "which is false since there is titer-data" | **unsupported; the reverse is true** | The runs' statement is correct. A correlate of protection is an immune marker validated against clinical protection outcomes. This trial has no protection outcome, so none can be established from it. The 1:40 HAI threshold is an assay and reporting convention (`dossier.md` §4), not a validated H7N9 correlate. The grading document takes the same position: HAI titre is "itself a surrogate" and no protection endpoint exists in the room. Titre data is precisely what does not establish a correlate. The defect in those runs is that the claim is **narrower** than the structural one — no protection endpoint anywhere in the measure inventory — not that it is wrong |
| 7 | All runs dismissed field efficacy and human challenge on feasibility or ethics | **supported** | All 16, in set-aside sections |
| 8 | No models propose any studies to close that gap | **supported** | 0/16 |
| 9 | 3/16 mention a nonclinical or in vitro method | **partial** | The three are A06, A09, A12. A06 and A12 say nonclinical (A12 also passive-transfer); **A09 `:330` says immunobridging, which is a clinical and regulatory comparison, not in vitro**. No run proposes an in vitro method. Correct wording: "nonclinical or immunobridging" |
| 10 | but don't provide a plan, postponing it | **supported** | A12 `:308` "can wait for pivotal planning"; A06 `:391` conditions it on regulators; A09 names the route without a design |
| 11 | 13/16 compare dose 1 and dose 2 gene counts across different baselines | **supported** | 3/16 name the convention: A04 `:36`, A09 `:75`, A14 `:64` |
| 12 | "The more appropriate comparison is to compare the same dose, as the comparisons require a common baseline" | **unsupported, and contradicts the panel's best run** | Cross-dose comparison is legitimate here once the convention is addressed, and A14 `:64` — the most complete handling in the panel — does compare across doses. The room supports the comparison: against the first-dose baseline Day 29 shows 11 DE genes across all six cell types against 3,024 at Day 2, so the two reference points are nearly the same, and the cytokine fold changes are all from pre-vaccination and show the same amplification (IP-10 1.867 to 4.461). The correct move is to name the convention and discharge it, by any of three routes: argue the shift is immaterial, argue its direction (A14: the dose-2 convention would if anything find fewer genes), or corroborate on a common-baseline measure |
| 13 | 2/16 carry these comparisons into their endpoint decision, the weakest runs A03, A05 | **partial** | The runs are right. "Endpoint decision" is not: A03 `:137` makes dose-2 reactogenicity a measurement requirement (study design) and A05 `:231` concludes dose 2 is unlikely to be gentler (deployment expectation). Neither touches an endpoint |

## Citations

- Run ids should be lowercase as the Hub displays them: `f9779a6c`, `890bbf23`, `b07ef105`.
- Separator is inconsistent: "A08 (F9779A6C)" against "A03; 890BBF23". Pick one.
- Typo: "which are notable the weakest-scoring runs" → "notably".
- "there is titer-data" → "titre data" (and see row 6 — the clause should go).

## Consistency

Only the first paragraph was supplied, so the cross-paragraph check does not apply yet. Send the second and I
will check the two against each other for the same run.

## Must-fix, ranked

1. **Delete "which is false since there is titer-data" (row 6).** It is factually wrong, it inverts the finding,
   and it asserts the exact conflation the task was built to test — a reviewer will catch it immediately.
2. **Fix the run list in row 5.** A09 does not make the weaker claim; the five that do are A01, A02, A11, A13, A15.
3. **Drop or rewrite row 12.** As written it forbids a comparison the data support and marks A14's handling wrong.
4. **"endpoint decision" (row 13)** → study-design and deployment calls.
5. **"in vitro" (row 9)** → immunobridging.
6. Citation formatting: lowercase ids, consistent separator, the two typos.

---

# QC round 2 — "What should the model have done?" (shipping candidate)

| # | Claim | Verdict | Evidence / correction stated as fact |
|---|---|---|---|
| 1 | "all 16 outcome measures in the data room were serology, cytokines, or gene counts" | **wrong count** | There are **15** outcome measures, not 16. Enumerated from `registry_results.json` → `resultsSection.outcomeMeasuresModule.outcomeMeasures`: 15 entries, 2 primary and 13 secondary. The 16 appears to be the run count bleeding across. Also, they sit in `registry_results.json` specifically, not "the data room", which is three files |
| 2 | "A15 is the only model that noted this" | **wrong run, and wrong count** | It is **A16 (9993e8bb)** `:304`, "The package contains immunogenicity only", and **A08 (f9779a6c)** `:354`, "The development pathway has to rest on immunogenicity (as this trial's own endpoints do)". **Two runs, not one.** A15 (abf75de9) `:200` says something different: "The trial defines no protective titre, so a documented antibody response is our only proxy for protection" — that is the weaker claim, and A15 is one of the five runs making it (A01, A02, A11, A13, A15). **This also contradicts the shipped first paragraph**, which correctly says 2/16 and names A08 and A16 |
| 3 | "this note should belong in every run as a noted gap, not as a set-aside" | **supported** | Both A08 and A16 put it in a set-aside row; every run has a gaps section |
| 4 | "field efficacy/human challenge are nonviable" | **supported** | All 16 dismiss both on feasibility or ethics |
| 5 | "A12 names one but postpones/defers it as the next study move" | **inverted** | A12 (1596ccf2) `:308` names a nonclinical challenge or passive-transfer study and then defers it: it "can wait for pivotal planning". Naming it *as* the next study is the correction, not what A12 did. As written the sentence credits A12 with the move it failed to make |
| 6 | "A14 ... notes that dose 2 would likely find fewer DE genes since the other data (cytokines changes were fewer, so this would correlate; a reasonable hypothesis)" | **two errors** | (a) **The cytokines did not fall, they rose**: IP-10 goes 1.867 after dose 1 to 4.461 after dose 2, on a single pre-vaccination baseline. A14 cites them as showing "the same amplification", i.e. as corroboration that the response really is larger after dose 2. (b) **The reason dose 2 would find fewer genes is methodological, not cytokine-based.** A14 `:64` verbatim: "dose-2 comparisons use a single Day-29 draw, while dose-1 comparisons average two draws (DOS Section 6). That difference would, if anything, reduce the number of genes called after dose 2, and the cytokines below show the same amplification." Averaging two draws reduces noise, so the dose-2 convention is the more conservative one. The draft swaps the role of the cytokine evidence and inverts its direction. It is also an argument, not "a reasonable hypothesis" |
| 7 | "A09 also recognizes it, but to a different point" | **same point, not different** | A09 (9687c0b1) `:75` says dose 1 drew on two baseline samples and so had more statistical power, not less. That is A14's observation from the other end, not a different point |
| 8 | Closing list: adjuvanted regimen as asset; Day-29 HAI GMT 7.3 insufficient and single-dose rejected; durability and breadth open; every figure tied to its source with a reasoned set-aside list; signature kept as a predictor of HAI titre | **all supported, 16/16** | Verified individually across all 16 |

## Consistency with the shipped first paragraph

Row 2 is a direct contradiction: paragraph 1 says 2/16 and names A08 and A16; paragraph 2 says A15 is the only
one. A reviewer reading both will catch it. Nothing else conflicts.

## Typos

- "kept s a predictor" → "as a predictor"
- "Name the baseline conventions its using" → "it is using"
- "cytokines changes" → "cytokine changes"

## Must-fix, ranked

1. **A15 → A16, and two runs not one** (row 2). Wrong attribution, and it contradicts paragraph 1.
2. **16 → 15 outcome measures** (row 1).
3. **The A14 cytokine clause** (row 6). The cytokines rose; they are corroboration, not the reason fewer genes
   would be called. The reason is that dose 1 averages two baseline draws and dose 2 uses one.
4. **The A12 sentence** (row 5). It names a route and defers it; naming it as the next study is the fix.
5. **A09 "different point"** (row 7) → the same point from the other end.
6. Typos.
