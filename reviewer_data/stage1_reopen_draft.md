# Stage 1 reopen — candidate basins (within-room only, A & C)

Working against: shipped v1 (branch `claude/elegant-mccarthy-uk0tco`), pilot mean
0.8375 unimodal. Target: ≤0.55 mean, bimodal.

Pilot's recommendation (pilot_analysis §6) was that the room needs a new
decisive datum. User direction: explore A (new decisive quantity that flips)
and C (supplement-side derivation that changes next-study ranking) **without
adding data** first; then if those don't carry, consider adding.

Below I enumerate what the shipped room actually supports under each heading,
rate each for "verdict flip vs ranking flip vs frame change," and give a
blunt verdict on gate reach.

---

## Facts established from a fresh scan of the room (needed below)

- **DE counts (registry OM-2/3) are RNA-seq.** Dossier §6 states 25M reads per
  sample. These counts ARE on common footing across cell types. The §7 10/25 µg
  loading split applies only to proteomics (supplement DA tables), not to DE
  counts.
- **H3N2v arm (OM-3) DE counts** are essentially zero across every cell type
  even at Day 8: Mono 0,0,1; DC 0,0,2; Neut 0,0,41; NK 0,0,1; B 0,0,3; T 0,0,0.
  This arm has a strong serological response (HAI 37.3→144.2) but no innate
  transcriptional signature. Humoral and innate-transcriptional response are
  dissociable in the room.
- **Adjuvanted H7N9 Day 2 post-dose-1 DE counts:** Mono 618, DC 1091, Neut 1116,
  NK 60, B 51, T 88. Innate-dominant on common footing.
- **Dossier §5 p-values.** adj-vs-unadj H3N2-directed HAI fold change: p=0.052;
  Neut equivalent p=0.087. The adjuvanted arm shows LESS H3N2 cross-reactivity
  than the unadjuvanted — borderline-significant finding, UNCUED in prose.
- **Cytokine fold-change baseline.** OM-7 time-frame declares all post-dose-1
  AND post-dose-2 timepoints are referenced to "Day 1 Pre-Vaccination 1" — i.e.
  one baseline for both doses, UNLIKE DE (§6). This is uncued (not in dossier).
  Means cytokines at matched elapsed days (Day 8 vs Day 36) are on a common
  single baseline. The pilot noted "cytokines on a common baseline corroborate";
  models are using it to mitigate B5. So this is already working *against* the
  task, not for it.
- **Group 1 (H3N2v) is open-label; Groups 2/3 are blinded** (dossier §1). Model
  doesn't exploit this; no obvious design lever.
- **Supplement figure images are the signature r-values.** Validation log notes
  per-gene r-values live in figure images; no A/B item currently gates on them.
  Pilot found several models decoded enough to find Table S186 is pooled arms.

---

## Direction A — new decisive quantity that flips a verdict (within-room)

### A-cand-1: Breadth-urgency flip via §5 p=0.052
- **Scene.** Deliverable asks for a next-study ranking. The three gaps are
  durability, breadth, and the protection endpoint.
- **Naive answer.** All three equal, or durability-first by convention (simpler
  study, faster read).
- **Correct answer.** Breadth-first, because the adjuvanted arm shows
  statistically-trending LESS H3N2 cross-reactivity than the unadjuvanted
  (p=0.052). AS03 narrows the response, which is a liability for pandemic
  preparedness where the circulating strain may drift.
- **Basin.** Dossier §5 p-value, uncued in prose. A shallow read skips the
  p-value table or reads "no rise above baseline" for the adjuvanted arm as
  neutral, not as a *comparison* that trends.
- **Flip type.** Ranking flip (durability-first → breadth-first), not verdict
  flip (carry-forward unchanged).
- **Verdict.** Mild. The p-value is borderline (0.052 is "trending" not
  significant). A frontier model that reads §5 carefully will see the
  comparison, and from there the implication is a short step. Expect ~40-60%
  of attempts to catch it on Opus 5. Not enough to carry the gate alone.
- **Grader surface.** Thin — "did the next-study ranking prioritize breadth,
  and did it cite §5" is a one-line check. Would need company.

### A-cand-2: Within-arm vs pooled ISG r-value derivation
- **Scene.** Supplement Table S186 declares the top-50 ISG set is derived on
  the pooled A/H7N9 arms (adj + unadj). The pilot found this. The r-values
  (GBP5 0.86, IFIT 0.84, etc.) therefore are confounded with AS03 receipt.
- **Naive answer.** Report r≈0.74-0.86, treat signature as a real predictor
  of HAI; next study: enroll a signature arm.
- **Correct answer.** The r-value within the adjuvanted arm alone is likely
  much lower (if the signature really is marking AS03 receipt). Supplement
  may or may not carry the within-arm figure — need to verify. If it carries
  it: the next study is not a signature-biomarker arm, it's a confound-free
  signature study.
- **Flip type.** Would be a verdict flip on whether the signature is a
  biomarker candidate — but pilot shows models already recognize the pooling
  confound (B3 avoided 16/16, A6 near-MET 16/16). The derivation would need
  to force a NUMBER (within-arm r) that the shallow read gets wrong.
- **Verdict.** Soft. If the supplement carries a within-arm figure, this
  becomes a thin anchor (extraction-fragile per PDF-renderer QA critical).
  If it doesn't, the derivation is "declare the pooled r uninformative" —
  which models already do. Not a reliable lever.
- **Grader surface.** Thin without a numerical anchor.

### A-cand-3: Seroprotection fraction from GMT 85.7 + CBER bar
- **Scene.** Deliverable implies the adjuvanted arm is immunogenic (GMT 85.7
  comfortably above 1:40).
- **Naive answer.** 85.7 > 40, so most participants protected.
- **Correct answer.** 80% HAI SC means 8/10 reached ≥1:40. CBER requires ≥70%
  at ≥1:40 for licensure; this just meets the bar at n=10, with the lower CI
  bound well below.
- **Flip type.** Nominal/no flip — 8/10 ≥ 70% hits the bar. No decision changes.
- **Verdict.** Dead. The numbers don't flip anything.

---

## Direction C — supplement-side derivation that changes next-study ranking

### C-cand-1: Mechanism attribution via DE counts (RNA-seq, common footing)
- **Scene.** Deliverable asks what mechanism the next mechanistic study should
  probe.
- **Naive and correct answer agree:** innate (DC 1091, Neut 1116, Mono 618 vs
  B 51, T 88, NK 60 at Day 2 post-dose-1).
- **Verdict.** No flip. DE counts are on common footing — there's no correction
  that changes the attribution. Model reads these as-is.

### C-cand-2: Mechanism attribution via DA proteomics with loading correction
- **Scene.** Deliverable requires attributing the response to a compartment
  AND naming the next mechanistic study.
- **Naive answer.** Read supplement DA tables raw; whichever cell type has
  largest DA count wins. §7 says B/NK at 10 µg, others at 25 µg.
- **Correct answer.** Multiply B/NK counts by 2.5 before comparing. If the
  raw B/NK counts are moderate but corrected overtake the innate counts
  (plausible for B cells given a strong humoral response), the mechanism
  attribution flips from innate-dominant to humoral-dominant, and the next
  mechanistic study changes.
- **Flip type.** Verdict flip on mechanism attribution AND on next mechanistic
  study.
- **Catch.** Depends on actual supplement DA counts producing a flip when
  loading-corrected. Need to verify. Supplement PDF extraction is QA-blocked
  (no renderer in image). This is a THIN ANCHOR per Stage 2d.
- **Grader surface.** Clean: did they compare across cells, did they correct,
  did the corrected comparison change the mechanism attribution. Three
  independent checks, each failable, A-list candidates.
- **Verdict.** Promising IF the supplement numbers actually flip when
  corrected. Need to pull the DA counts to confirm. Also depends on the
  deliverable requiring mechanism attribution — currently it does not.

### C-cand-3: ISG signature necessity via H3N2v dissociation
- **Scene.** Deliverable discusses the ISG signature as a biomarker candidate
  for the next trial.
- **Naive answer.** Signature correlates with HAI (r=0.74-0.86); worth
  advancing as a correlate.
- **Correct answer.** The H3N2v arm (OM-3) produces a strong serological
  response (HAI 37.3→144.2, high SC) with essentially zero DE genes across
  all compartments — i.e. the ISG signature is NOT NECESSARY for a protective-
  magnitude humoral response. The signature marks AS03 receipt, not the path
  to antibody. This is a direct within-room derivation (join OM-2 with OM-3)
  that forecloses the biomarker claim more sharply than "it's a surrogate of
  a surrogate."
- **Flip type.** Strengthens the restraint on signature advancement — but
  does it FLIP a verdict a shallow model gets wrong? Pilot shows all 16
  attempts already decline to elevate the signature. So this doesn't flip
  behavior.
- **Grader surface.** OK — "did the attempt cite the H3N2v null-DE as a
  reason the signature isn't on the mechanistic path" is a one-line check,
  but it's grading sophistication, not catching a wrong answer.
- **Verdict.** Reinforces an already-met check. Won't move the gate.

---

## Bottom line — honest verdict on the room-only path

**The within-room A/C candidates do not clear the gate.** Specifically:

- **A-cand-1 (§5 breadth urgency)** gives a ranking flip that at best
  demotes attempts by one notch. Opus 5 reads §5 and gets there often enough
  that this alone doesn't produce bimodality.
- **A-cand-2 (within-arm ISG r)** depends on supplement carrying a specific
  figure and on extracting a number through a PDF renderer the image doesn't
  have. Thin anchor, extraction-fragile. Sophistication it would reward is
  already partly covered by the pooled-arm finding Opus 5 reaches.
- **A-cand-3 (seroprotection fraction)** doesn't flip.
- **C-cand-1 (DE mechanism)** doesn't flip.
- **C-cand-2 (DA loading correction)** is the only real within-room candidate
  — but (i) only if the supplement DA counts actually flip under correction
  (not verified; QA-blocked by renderer); (ii) requires expanding the
  deliverable to require mechanism attribution; (iii) still only reaches a
  single verdict flip, unlikely to be enough for the gate alone.
- **C-cand-3 (H3N2v dissociation)** reinforces an already-met check.

**Honest reading.** The pilot analysis was right. Opus 5 recognizes
everything this room can carry. The structural problem is that the room's
decisive quantities (0% unadjuvanted SC, 85.7 GMT, 7.3 single-dose GMT) are
all cleanly separated from their thresholds. There is no numerical
knife-edge on which a shallow-vs-correct derivation would land on opposite
sides. Within-room, we can at best stack weak levers (A-cand-1 + C-cand-2 if
it flips) and hope for a few-tenths movement in the mean. That is not the
gate.

---

## Next move — recommendation

**Add one decisive datum.** The pilot's #1 recommendation. Candidate shapes:

- **(α) Dose-response bridge within the adjuvanted configuration.** A short
  dose-ranging dataset (e.g. 3.75 µg vs 7.5 µg vs 15 µg, all with AS03) that
  under the naive read supports the shipped 3.75 µg forward, but under a
  correct derivation (e.g. ceiling effect in GMT above a certain content,
  reactogenicity-vs-immunogenicity trade, or a non-monotonic dose-response)
  forces a different forward dose. Flips the carry-forward spec.

- **(β) Antigen-content vs AS03-dose factorial.** Dissociates antigen dose
  from adjuvant dose. Naive read: higher AS03 → better response, use full
  AS03. Correct read: non-monotonic in AS03 OR a specific AS03 dose
  interacts with content below a threshold such that the shipped
  configuration is sub-optimal.

- **(γ) A manufacturing/stability potency bridge.** A measured potency drop
  under a stated storage condition that, when joined with the implementation
  framing, forces the next study to be stability-bridging rather than
  immunogenicity-first.

- **(δ) A seroprevalence/baseline-primed-fraction datum.** Pre-vaccination
  A/H7N9 serostatus in a defined cohort (not necessarily this trial's
  population). Changes the interpretation of the 1.4× cross-antigen rise
  (B7 currently) and the H3N2v recall framing. Could force an unanchored
  join: the correct next-study population needs defined priming status, which
  isn't a decision the current room engages.

- **(ε) A drifted-clade immunogenicity microdata.** A small panel of
  neutralization titers against drifted H7N9 isolates from stored sera.
  Naive read: 190.3 GMT against the vaccine antigen implies breadth. Correct
  read: breadth collapses against drifted clades, which flips the next-study
  priority to a specific drifted-clade panel rather than a general breadth
  arm.

**Of these, α and β most
 directly bear on the shipped verdict's
load-bearing judgment ("the thing to carry forward IS the adjuvanted
configuration AT this content"). ε changes the next-study ranking but keeps
the carry-forward. γ and δ require more world-building.

Flagging two anti-patterns to resist in the add-data lane:
- Stacking derivations (6 calculations instead of 3) does not add difficulty.
  One flipping derivation beats three stackable ones.
- Reactogenicity + implementation framing can pull the task toward
  bench-executable procedure or safety-threshold adjudication. Stay inside
  the design/specification/interpretation safety boundary.

## Decision asks (for the user)

1. Confirm the within-room path is insufficient to clear the gate (I think
   it is). If you disagree, name which within-room candidate you think
   carries, and I will attack it harder.
2. If adding data is on the table, which shape (α-ε, or something I missed)
   do you want me to develop into a full Stage 1 candidate with scene /
   naive / correct / basin / law-screen?
3. Any new mounted datum needs a plausible document carrier (programme
   memo, internal potency report, serosurvey table). Scope-of-world
   question: are we willing to add one authored document (not another
   third-party paper), or do we want the datum to live inside an expanded
   dossier?
