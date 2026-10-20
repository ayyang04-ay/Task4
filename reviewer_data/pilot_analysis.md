# Pilot analysis — job 30f4652b (2026-10-14), 16 samples, Opus 5.5

Source: `run data/Anton_...job_30f4652b_2026-10-14.zip`. Grader = agentic_grader,
single holistic score, model claude-opus-5-5, 16 independent problem runs.

## 1. Scores

| attempt | score | attempt | score |
|---|---|---|---|
| 01 | 0.83 | 09 | 0.84 |
| 02 | 0.88 | 10 | 0.80 |
| 03 | 0.77 | 11 | 0.84 |
| 04 | 0.90 | 12 | 0.79 |
| 05 | 0.77 | 13 | 0.80 |
| 06 | 0.92 | 14 | 0.88 |
| 07 | 0.88 | 15 | 0.85 |
| 08 | 0.80 | 16 | 0.85 |

Mean **0.8375** · min 0.77 · max 0.92 · 13/16 ≥0.80 · 16/16 ≥0.50 · 0 refusals.
Gate = mean ≤0.55 → **NOT CLEARED** (fails by a wide margin).

Distribution shape: **unimodal, tight, high** (0.77–0.92, SD ≈ 0.045). This is the
"too-easy / failing-high" panel, not the bimodal high/low signature of a working
task. No attempt is near the floor; nothing discriminates.

## 2. Per-item performance across the 16 (from grader rationales)

| Item | Result across 16 | Discriminates? |
|---|---|---|
| A1 configuration attribution | **MET 16/16** — every attempt carries forward only the adjuvanted 2-dose regimen on line 1, cites 0% SC + floor titres | No |
| A2 two-dose necessity | **MET 16/16** — Day-29 GMT 7.3 rejected; several attempts independently derive "≤1/10 reached 1:40" | No |
| A3 dose-sparing as adjuvant effect | **PARTIAL ~14/16** — substance present; the explicit "¼ of 15 µg" framing usually absent | Weakly (see §4 — arguably unfair) |
| A4 durability gap | **MET 16/16** | No |
| A5 breadth gap | **MET 16/16** — and H3N2 cross-antigen correctly excluded as breadth | No |
| A6 no-protection-endpoint / signature restraint | **MET or near-MET 16/16** — signature never elevated; often only the explicit "no outcome measures protection / HAI is a surrogate" sentence is soft | Weakly |
| A7 provenance + set-aside | **MET 16/16** — large sourced ledgers + set-aside tables | No |
| B1 unadjuvanted carry-forward | avoided 16/16 | — |
| B2 single-dose sufficient | avoided 16/16 | — |
| B3 signature elevated to surrogate | avoided 16/16 | — |
| B4 keratin/hornerin as biology | avoided 16/16 | — |
| B5 cross-dose DE-count comparison | **fires ~15/16, graded minor** — model compares dose-1 vs dose-2 DE counts across the §6 baseline break, but the direction is "larger after dose 2" (not the "wanes" example), it's background not decision-driving, and cytokines on a common baseline corroborate | This is the ONLY trap that bites — and weakly |
| B6 cross-cell-type loading | avoided 16/16 | — |
| B7 H3N2v recall / 1.4× cross-antigen as merit | avoided 16/16 | — |

**Every load-bearing A item is met in every attempt. Six of seven B traps never
fire. The entire score spread (0.77–0.92) is produced by exactly three soft
deductions: B5 (minor, mitigated), A3 (framing), A6 (explicitness).**

## 3. The model out-performs the Golden on the hardest item

On A6/B3, multiple attempts went *beyond* the Golden: they decoded the supplement
and found Table S186 is titled "Combined A/H7N9 Study Arms" — i.e. the ISG
signature is derived on the **pooled** arms, so it trivially "predicts" HAI
because it is really marking AS03 receipt. Several also found Figures S43–S58
(the correlation-with-peak-HAI figures) are **absent** from the PDF, so they
declined to quote r-values. That is a *sharper* restraint argument than our
proxy-of-a-proxy. The full-supplement datadump armed the model to kill the trap,
rather than baiting it.

## 4. Two of the three deductions are grader artifacts, not difficulty

- **A3 (dose-sparing ¼-of-15 µg):** att_06 notes 15 µg is a *different subtype*
  (H3N2v), so refusing to use it as a dose reference is scientifically correct.
  Penalizing the absent comparison penalizes correct restraint — a
  grader-vs-domain-truth defect, not a real miss.
- **A6 (say "no protection endpoint" explicitly):** the required *behaviour*
  (don't elevate the signature) is met 16/16; the deduction is for not stating a
  sentence. That is close to a formatting ask.

A *fairer* grader would therefore score this **higher**, not lower. Grader
tightening cannot reach ≤0.55; best case it caps near 0.65–0.75 and does so
unfairly.

## 5. Root cause

Every one of the seven "independent causes" is a **recognition** item — spot the
inert unadjuvanted arm, spot the recall baseline, spot the surrogate, spot the
contamination, spot the baseline break, spot the loading split. anton-scope's
Stage-0 gate predicts exactly this: recognition panels run 0.83–0.968; we landed
at 0.84, dead centre. Opus 5.5 recognises all of it, first pass. There is no
hidden basin it falls into — the unadjuvanted 0% is glaring and leads every memo.

The standard "too-easy" fix (strip sentences that state their own consequence)
**does not apply**: the room states no conclusions; the model derives them
independently and correctly. There is no leaked sentence to remove.

## 6. Options to actually move the mean (each is a design reopen, not a tweak)

Ranked by plausibility of reaching ≤0.55:

1. **Replace the basin with a forced derivation that flips.** Introduce a decisive
   quantity where the obvious route lands on the wrong side of a decision
   threshold, and the correcting fact is mounted but uncued. The current serology
   is too clean (190.3, 85.7 — unambiguous, no leveraged point, no aggregation
   artifact), so this almost certainly needs a **new decisive datum** added to the
   room (e.g. a dose-response or bridging quantity with a non-obvious correct
   reduction). Stage 1/2 work.
2. **Uncued second-state join (champion lever).** Make the correct carry-forward
   conclusion depend on joining two measurement states where the single-state read
   is defensible-but-wrong, with nothing cueing the second state. The §6 baseline
   break is the second measurement state, but it is already cued (dossier §6 states it) and the
   model mostly handles it — so a *new* uncued join is needed, not this one.
3. **Accept recognition and change the panel expectation.** If the panel model
   stays Opus 5.5, a recognition task of this shape will not clear ≤0.55. Only
   viable if the gate or panel model changes — not our call.

## 7. Bottom line

The task is well-built, fully grounded, refusal-free, and the grader is sound —
but it measures recognition, and Opus 5.5 passes recognition. Mean 0.84 with no
bimodality is a **design verdict, not a tuning problem**. Lowering the pass rate
to the gate requires reopening the basin (Stage 1/2) around a genuine derivation
with an uncued, mounted correcting fact — most likely by adding one decisive
datum the current room does not contain. Incremental grader hardening is the
wrong instrument and, if made fair, would raise the mean.

Soft/no-fix: the A3 cross-subtype dose-reference deduction and the A6
explicitness deduction are grader-fairness issues, not what is holding the score
down; fix only if the task is rebuilt.
