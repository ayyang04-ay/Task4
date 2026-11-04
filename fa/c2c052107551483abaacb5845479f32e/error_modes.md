# Phase 1 — error-mode ledger. Task pu3h8f5d / c2c052107551483abaacb5845479f32e, job 30f4652b

Mode: GRADED (writer-authored A/B/C + Golden). 16/16 completed, 0 refused. Scores 0.77–0.92, mean 0.8375.

## Reading coverage

| Source | Coverage |
|---|---|
| Graded deliverables `outputs/attempt_NN_*/recommendation.md` | **All 16, in the export** (third archive, `export_selection.included = [outputs]`). Line numbers below are from these files and are citable. |
| Grader rationales | All 16 read cell by cell, from two independent sources (export `grading/*.json` and the Hub page) — identical text. |
| Transcripts | All 16 flattened and screened. Full-text reads: attempts 05 (0.77, weakest), 09 (0.84, median), 14 (0.88, the sharpest handling of the contested item). |
| Data room | `dossier.md` and `registry_results.json` read in full; every value below recomputed from the registry. |

Earlier reconstruction from transcripts is superseded; 6 of 16 reconstructions were body-file snapshots and would have mis-stated two counts.

## Ledger — ordered by prevalence, then consequence

| # | Mode | Class | Prevalence | Consequence | Evidence | Correct move | Graded? |
|---|---|---|---|---|---|---|---|
| M1 | The structural absence anchor is never established: the attempt does not state that the trial's outcome-measure inventory contains no protection / efficacy / challenge endpoint. | Absence not retrieved | **15 of 16** — all but attempt 16 (9993e8bb) | Low on conduct, high on basis. Every attempt behaves correctly (none elevates the signature), but the premise licensing the correlate-of-protection next study is never written down. Under the grading document's own rule — "analysis the attempt did but did not write down earns nothing" — the gap is unestablished. | Only attempt 16 (9993e8bb) states it, and only inside a set-aside cell: `recommendation.md:304` "The package contains immunogenicity only." 8 of 16 (01, 02, 06, 07, 11, 12, 13, 15) instead assert the **different, weaker** claim that no validated protective titre exists, e.g. attempt 11 (60c1bbbc) `:115` "No correlate of protection for H7N9 is established in these files." That is a claim about interpreting a titre, not about what the trial measured. The remaining 7 (03, 04, 05, 08, 09, 10, 14) state neither. | State the inventory fact: all 15 outcome measures are serological, cytokine or transcriptomic; none is a protection, efficacy or challenge endpoint. Verified [computed]: enumerating `resultsSection.outcomeMeasuresModule` gives 15 measures, every one serology / cytokine / DE-count. | A6 |
| M2 | Comparator-arm differential-abundance hits are never identified as keratin/hornerin handling contamination. | Mounted fact unengaged | 13 of 16 — present only in 06 (1f19cd35), 13 (15a5af69), 16 (9993e8bb) | **Benign.** No attempt cites them as vaccine biology, so the B-item does not fire. The cost is that 13 attempts leave the comparator proteomics uncharacterised rather than explained. | Keyword sweep for `keratin|hornerin|HRNR|KRT<n>` over all 16 deliverables: non-zero only in 06, 13, 16. | Name the comparator-arm DA tables as skin/handling contamination (`dossier.md` §7 clustering convention + the HRNR/KRT features). | not in grader as a miss — B4 is avoided 16/16 |
| M3 | "Time to protection" treated as a quantity the trial measures or a design parameter a next study could shorten, although no protection endpoint exists. | Internal inconsistency / loose predicate | **4 of 16** (04, 07, 09, 10) | Low. Only in attempt 07 (06a4976d) does it contradict the same document's own statement that no protective titre is established; in 04, 09 and 10 there is no countervailing statement, so it is loose usage rather than self-contradiction. | attempt 07 `recommendation.md:184` "plans should assume **8 weeks from first dose to protection**"; attempt 04 `:55` "Time to protection is the key deployment parameter"; attempt 04 `:114` "how we could shorten time to protection"; attempt 09 `:224` "**Time to protection**"; attempt 10 `:113` "the main determinant of time to protection". | Name the quantity for what the trial can time: days to a documented serological response. | not in grader (graders called it "loose wording") |

## Modes examined and REJECTED as model error — each is a defect in the grading document

These are the deductions that produce the entire 0.77–0.92 spread. Each was tested against the room, not against the rationales.

| Grader item | Fired | Why it is not a model error |
|---|---|---|
| **B5 — comparing DE-gene counts across the dose-1 / dose-2 baseline break** | ~15 of 16; called "the real error" (08), "a significant error" (05), "one clear methodological error" (01) | Three independent findings, all [computed] from `registry_results.json`: (1) The convention is mounted **twice**, not once — `dossier.md` §6 and the OM2 description itself ("combined summed read counts for Day -7 and Day 1 … and Day 29 read counts for post-vaccination 2 timepoints"). (2) The break is quantitatively negligible **in this dataset**: AS03 arm Day 29 post-dose-1, measured against the *first-dose* baseline, is **11 DE genes across all six cell types — 0.36% of the 3,024 Day-2 dose-1 peak**. The dose-2 reference draw is empirically indistinguishable from pre-vaccination. (3) The conclusion is independently supported on a genuinely common baseline: IP-10 fold change is reported "From Pre-vaccination" throughout — 1.867 (Day 2, dose 1) → 0.869 (Day 29) → **4.461 (Day 2, dose 2)**, i.e. ~2.4×, against 6,364/3,024 = 2.10× from the DE counts. **All 16 deliverables cite the 4.46 figure.** So every attempt supported the claim with a common-baseline measure in its own document; 3 (04 `:36`, 09 `:75`, 14 `:64`) additionally named and discharged the convention — attempt 14 arguing the bias direction correctly: "dose-2 comparisons use a single Day-29 draw, while dose-1 comparisons average two draws (DOS §6). That difference would, if anything, reduce the number of genes called after dose 2". Separately, the item's own wording penalises arguing "the second dose adds little or the response wanes" — **a direction no attempt took.** All 16 argued the opposite. |
| **A3 — dose-sparing as a quarter of the 15 µg comparator** | partial in ~14 of 16 | [computed] from `armsInterventionsModule`: Arm 1 = 15 µg **A/H3N2v (A/Minnesota/11/2010)**; Arms 2 and 3 = 3.75 µg A/H7N9 ± AS03. The only 15 µg arm is a different subtype, there is no H7N9 dose-ranging arm, and the Golden itself rules that arm non-comparable ("not comparable to the primary response to a novel H7N9 antigen"). Declining the comparison is the better-supported reading under the prompt's "Work only from the mounted files". Graders conceded this while deducting: attempt 09's grader — "Defensible, arguably more rigorous, but it doesn't match the Golden's framing." |
| **A6 — state the protection gap explicitly** | soft in ~8 of 16 | Partly valid, and it is M1 above. But the graders' complaint is that the *sentence* is absent while the *behaviour* is correct 16/16. The valid residue is narrower than the deduction: what is missing is the endpoint-inventory fact, not the restraint. |

## Panel-level finding

Every load-bearing A item is met in 16 of 16. Six of seven B traps never fire. The three deductions that generate the
score spread are two grading-document defects (B5, A3) and one articulation ask (A6) whose valid core is M1.
There is no prevalent model error mode of consequence on this panel: the remaining modes are an unstated structural
premise (M1), an unengaged benign fact (M2) and a wording slip (M3).

This contradicts `reviewer_data/pilot_analysis.md` §2, which records B5 as "the ONLY trap that bites". It bites the
grader, not the model. That document's matrix was built from grader rationales and its counts are approximations
("~14/16", "~15/16"); the counts above are from the graded deliverables.

## Epistemic labels

- [computed] — M1 inventory enumeration; the 11-vs-3,024 DE figures; IP-10 1.867/0.869/4.461; 6,364/3,024 = 2.10×; the arm HA contents. All recomputed from `data_room/registry_results.json`.
- [transcript] — every quoted line of every `recommendation.md`; attempt 01's in-episode self-correction at ev433.
- [inference] — that M1's consequence is "low on conduct, high on basis"; that B5's negligible baseline shift makes the comparison defensible rather than merely lucky. Both are my judgment, not statements from the room.

## Correction to this ledger (made after first writing)

M3 was first recorded as "8 of 16 use protection as the predicate of a serological quantity". That count was
produced by a pattern that swept in two things that are not errors: operational instructions to treat recipients as
unprotected between doses, which are conservative planning language and in attempt 08 (f9779a6c) `:290` are tied
explicitly to the programme's seroconversion definition; and attempt 16 (9993e8bb) `:240` "These are immunogenicity
milestones, not protection dates", which is the correct framing. The mode as now stated is 4 of 16 and is thin.
Recorded here because the first count would have reached the FA.
