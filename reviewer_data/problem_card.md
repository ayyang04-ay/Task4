# Problem card — H7N9 adjuvanted vaccine, next-work recommendation

RLS short ID: pu3h8f5d
RLS URL ID:   task_c2c052107551483abaacb5845479f32e
Campaign:     camp_0589d1e96758477586df0e43dd8eeec1
Branch:       claude/elegant-mccarthy-uk0tco  (shipped; prior nice-cori-69c2j3 was never committed)

## Source
- Creech et al., Front Immunol 2026, DOI 10.3389/fimmu.2026.1786231 (EXCLUDED from room; context only).
- 1014-page supplementary file (mounted verbatim).
- ClinicalTrials.gov NCT02921997 results record (mounted, trimmed + scrubbed).

## Lane
Assay interpretation / translational decision-making (non-structural).

## What this task measures
Difficulty is a cluster of independently-failable judgments about what this
specific evidence can and cannot support — not one calculation. 6-7 independent
causes (per spine 2a check 4): configuration attribution, reference-frame
baseline mismatch, comparator-arm artifact discrimination, loading-split,
bulk-sort dilution, durability gap, breadth limit. Each surface-defensible, each
foreclosed by a mounted fact.

## Corpus verification (this build, 2026-10-14)
- Registry is the REAL NCT02921997 record. Every quantitative anchor verified
  exact against outcome measures: Neut GMT Day57 190.3/5.9 (OM-14); HAI GMT
  5.2->7.3->85.7 (OM-12); Day29 one-dose HAI 7.3 / Neut 17.4 (OM-12/14); HAI
  seroconv 80%/0% (OM-1); Neut seroconv 100%/0% (OM-10); H3N2v recall 485 trap
  (OM-15); [NA,NA] all-floor imputation (OM-12/14 Day1 unadj); Day29 DE-count
  bridge 0,1,0,8,1,1 (OM-3).
- Supplement is the real 1014-pp Creech supplement. Keratin/hornerin comparator
  basin grounded (HRNR, KRT5, KRT1-as-cluster present in comparator-arm DA
  tables S43/S51/S53/S61/S65). DE/DA/enrichment tables all present.
- 1.4x cross-antigen HAI rise (unadjuvanted H7N9 arm vs A/H3N2) verified against
  the paper: statistically significant, lower 95% CI bound above fold change 1;
  Arm-1 3.9x; adjuvanted arm no cross-reactivity. Dossier §5 numbers check out.

## ISG item — design change from original spine (this build)
Original spine designed the interferon signature as: surface it = A, "predicts
protection" = B10 false optimum, foreclosed by "correlation figures absent."
CORPUS VERIFICATION FALSIFIED THAT PREMISE: the mounted supplement explicitly
carries the signature->titer correlation (Figures S42-S58; Table S186 "top 50
genes that best predict peak HAI titer"; GBP5 r=0.86, IFIT r=0.84, MHC-I r>=0.74,
PSME2 r=0.78). The over-claim is the source's own finding, so B10 as written is
invalid (a B needs a mounted REFUTING fact; the mount SUPPORTS it).

RESOLUTION (user 2026-10-14): mount the full supplement as a datadump; reframe
the ISG item as proxy-of-a-proxy. The correlation of record is against peak HAI
TITER (regularized regression, Table S186), so the chain is
ISG -> HAI titer -> protection(unmeasured). Graded judgment: the model may report
the correlation (it is mounted, expected, not a trap), but must NOT elevate the
signature to a validated protection marker / accelerated surrogate endpoint,
because the titer it predicts is itself a surrogate and the trial has NO in-vivo
protection endpoint anywhere (registry OM list is entirely serological — mounted
by absence). Determinate (no-protection-endpoint by absence), failable (the mount
invites the over-reach), survives the full-supplement dump.
- DELETE old B10.
- DROP absence-anchor #12 (unenforceable — supplement states the correlation).
- Old "surface the signature" A-item is now partial retrieval (titled figures in
  the ToC) — do not grade surfacing; grade the proxy-of-proxy restraint.

## Mount decisions
- Full supplement PDF, verbatim datadump (acceptable under the ISG reframe).
- Registry: trimmed JSON, results + arms/design modules; scrubbed of the
  publication reference, interpretive description text, and largeDoc links.
  As shipped the scrub also removed statusModule (real dates),
  sponsor/oversight/contactsLocations, derivedSection, and
  resultsSection.moreInfoModule — all bridges to the excluded Creech paper
  (PI contact) or unneeded; kept identification/conditions/design/arms/
  eligibility + all 15 outcome measures. Leak assertions in validation_log.md.
- Dossier: authored conventions layer only (no conclusions); carries the
  reference-frame fact and the absence anchors.
- Paper: NOT mounted (states its own conclusions — strip-wall fail).

## Panel calibration
16 independent API samples at T=0.7-1.0. NOT subagent fanout. Target mean <0.55;
bimodal high/low split is the working signature.

## As-shipped reconciliation (2026-10-14)
- Prompt revised twice after spine: deployment clause softened
  ("...plan for how the regimen would be deployed" -> "...account of what the
  dosing schedule would mean for implementing the regimen in a preparedness
  setting") to cut T&S refusal surface while keeping the two-dose compliance cue;
  user's final edit also changed "will mislead" -> "may mislead" and the lock
  line to "All files are up to date as of today." task_prompt.txt is the shipped
  text.
- grader_prompt.md reflowed to flat lines (content identical, A/B/C headers
  standalone). Old B10 deleted and absence-anchor #12 dropped per the ISG reframe
  above; grader grades proxy-of-proxy restraint, not signature surfacing.
- Phase 5 audit clean (no hard findings). Full world-gate / scrub / supplement
  grounding / statics / three-axis record in reviewer_data/validation_log.md.
- Status at handoff: pushed to pilot; awaiting the 16-sample run.
