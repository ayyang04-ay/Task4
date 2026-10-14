# Validation log — H7N9 next-work recommendation (build 2026-10-14, branch claude/elegant-mccarthy-uk0tco)

Repo was a fresh empty clone; room reconstructed from the uploaded corpus, not
from the prior session's untracked disk state. `trial_summary.md` (WU397
mRNA-1010) was present in the uploads but belongs to a different build and was
excluded — it appears in no mount decision.

## Data-room manifest (shipped)
- `data_room/task_prompt.txt`      — board-proposal prompt (verbatim).
- `data_room/dossier.md`           — authored conventions layer (verbatim; no conclusions).
- `data_room/registry_results.json`— NCT02921997, trimmed + scrubbed (see below).
- `data_room/supplement.pdf`       — 1014-pp Creech supplement, verbatim (sha below).
- `grader/grader_prompt.md`        — five-section grader + Golden Response.

## Registry trim / scrub
KEPT: protocolSection {identificationModule, conditionsModule, designModule,
armsInterventionsModule, eligibilityModule}; resultsSection {participantFlow,
baselineCharacteristics, outcomeMeasures (all 15), adverseEvents}; hasResults.
DROPPED: descriptionModule (interpretive/objective prose), statusModule (real
dates), sponsorCollaboratorsModule, oversightModule, contactsLocationsModule,
referencesModule (Creech publication — primary leak), documentSection (largeDoc
links), derivedSection, resultsSection.moreInfoModule (PI contact — paper bridge).
Scrub assertion (passed): none of {Creech, buddy, vanderbilt, 1786231,
referencesModule, largeDoc, documentSection, pmid, briefSummary,
detailedDescription} present in the shipped JSON.

## World-gate propositions (computed from raw files, not echoed from the Golden) — ALL PASS
- P1 Unadjuvanted A/H7N9 never rises above the assigned floor: HAI 5.0/5.2/5.0,
  Neut 5.0/5.4/5.9; 0% HAI and 0% Neut seroconversion. (Configuration attribution.)
- P2 Adjuvanted single-dose HAI (Day29) = 7.3 is sub-protective (< 40); two-dose
  (Day57) = 85.7. Neut 5.0→17.4→190.3. (Two-dose necessity.)
- P3 Adjuvanted seroconversion 80% HAI / 100% Neut vs 0%/0% unadjuvanted.
- P4 ABSENCE ANCHOR: no protection/efficacy/challenge/infection endpoint word in
  any outcome-measure title or description (empty hit set). The entire OM list is
  serological or systems-biology — no in-vivo protection endpoint exists, mounted
  by absence. (Grounds the ISG proxy-of-proxy restraint.)
- P5 Every OM classifies as serological / cytokine / transcriptomic (no outlier).
- P6 A/H3N2v arm baseline is primed (HAI 37.3, Neut 171.5), rising to 144.2 / 485.0
  — a recall response, not comparable to the naive H7N9 primary. (Benchmark trap.)

## Supplement grounding — PASS
- Comparator basin: hornerin/HRNR, keratin/KRT1/KRT5 present in differential-
  abundance tables (contamination, not biology).
- Signature: Figures S43–S54 titled "… activity following vaccination and
  correlation with peak HAI titer" (MHC I, GBP4, GBP5, PSME2 …); Table S186
  "Overlap in top 50 genes that best predict peak HAI titer". The correlation of
  record is against peak HAI **titer** (a surrogate) — exactly the proxy-of-proxy.
  Per-gene r-values live in figure images; kept illustrative in the Golden and
  C-neutral in the grader — no A/B item gates on them.

## Grader statics — PASS
- Five sections; A/B/C headings and the verbatim bridge line present (bridge sits
  once, after the Golden, saying "above").
- No caps/ceilings/bands/ladders/multipliers/severity rankings. "weight" appears
  only as descriptive framing ("where the weight sits"), not a scoring weight.
- No B item mirrors or negates an A item; the report-vs-elevate collision on the
  gene signature is disarmed with explicit "does not fire on …" guards.

## Three-axis validation (law 11)
- Ceiling: the Golden is fully derivable from the shipped room (all anchors above).
- Floor: the obvious first pass — "H7N9 vaccine was immunogenic (85.7 HAI, 80%
  seroconversion), carry it forward" — lands in the basin (antigen attribution,
  possible single-dose/ signature-surrogate over-reach).
- Grader: B items catch each floor behavior with its refuting mounted fact.

## ISG redesignOld B10 ("signature predicts protection", foreclosed by "correlation figures
absent") is DELETED: corpus verification falsified its premise — the supplement
carries the signature->peak-HAI-titer correlation explicitly. Reframed as
proxy-of-a-proxy: reporting the correlation is C-neutral; elevating it to a
validated protection correlate / surrogate / accelerated-approval endpoint is the
B item, foreclosed by the absence anchor (P4). Old absence-anchor #12 dropped
(unenforceable — the supplement states the correlation). Surfacing the signature
is NOT graded (it is partial retrieval); the graded judgment is the restraint.

supplement.pdf sha256 (first16): 637a9202fd30641e  | 1014 pages

## Remaining (user, in RLS) — NOT executable here
- Panel calibration: 16 independent API samples at T=0.7-1.0 (Opus 5). Subagent
  fanout is NOT a substitute. Target mean < 0.55; bimodal high/low is the working
  signature. Cannot be run from this session — no independent-sampling tool.
- Record both RLS IDs (short pu3h8f5d / URL task_c2c052107551483abaacb5845479f32e)
  in the task; confirm the Golden earns full marks under its own guidelines on a
  live grade.
