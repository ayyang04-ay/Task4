# FA draft v3 — H7N9 next-work recommendation, job 30f4652b (16 × Opus 5.5)

RETYPE, DO NOT TRANSCRIBE. House format from Task jp2x8c9f: A-item indexed, prevalence per item,
non-discriminating items dismissed, second paragraph anchored on exemplar runs.
MODEL-SIDE ONLY. All grading-document and reference-solution findings are excluded by instruction and
live in calibration.md; nothing below asserts anything about how the runs were scored.
LABELS: this task's grading document uses A1–A7 for *items*, so trajectories are "run NN (hex)".
Counts: paragraph 1 = 12 sentences, paragraph 2 = 10 sentences. Evidence in error_modes.md / item_matrix.md.

## What did the model do wrong?

The task is built on 7 A pillars, and on model conduct one of them discriminates. **A6** requires both restraint
against elevating the interferon signature and a statement that the trial measured no protection endpoint; all 16
runs pass the restraint and 15/16 fail the statement. Only run 16 (9993e8bb) states that the record contains
immunogenicity only, and it does so in a set-aside cell rather than in its account of where the data fall short.
Eight runs (01, 02, 06, 07, 11, 12, 13, 15) substitute the weaker claim that no correlate of protection is
established, which concerns how to read a titre rather than what the trial measured, and the remaining seven (03,
04, 05, 08, 09, 10, 14) state neither. The cost is that where a bridging study is proposed, it rests on a
structural fact the proposal never states. The second and more widespread defect is a basis error rather than a
wrong answer: 13/16 compare differentially expressed gene counts across the dose-1 and dose-2 boundary without
ever discharging the reference-frame convention, which the room states twice — in `dossier.md` §6 and again in the
registry's own description of the DE-count outcome measure. The conclusion those runs reach is sound, the innate
response being larger after dose 2, and all 16 cite the IP-10 fold change of 4.461 against 1.867, which rests on a
single pre-vaccination baseline; but a stated convention bearing directly on the comparison is left unaddressed in
13 proposals, and only runs 04, 09 and 14 name it. Third, 13/16 never characterise the comparator-arm
differential-abundance tables: only runs 06, 13 and 16 identify the keratin and hornerin features as skin and
handling contamination. No run misuses them as vaccine biology, so this cost nothing, but the one systems-biology
artifact in the room was explained in three proposals out of sixteen. Fourth, 4/16 (04, 07, 09, 10) treat time to
protection as a quantity the trial measures or that a next study could shorten, which in run 07 (06a4976d) sits
against its own statement that no protective titre is established. One run over-claims on antigen content: run 12
(1596ccf2) states that the two-dose regimen uses half the HA of the 15 µg comparator and therefore saves antigen,
although that comparator is A/H3N2v, a different subtype, and the record holds no H7N9 dose-ranging arm. **A1,
A2, A4, A5 and A7** — configuration attribution, two-dose necessity, the durability and breadth gaps, and
provenance with a set-aside section — are met in all 16 and are not discriminating.

## What should the model have done?

No run satisfies all 7 pillars; run 16 (9993e8bb) comes closest on the discriminating item and run 14 (f8782a66)
models the handling of the second. **A6:** the correct move is to state the inventory fact outright: all 15
outcome measures in the registry record are serological, cytokine or transcriptomic, none is a protection,
efficacy or challenge endpoint, and that absence — not the weakness of any particular titre — is the gap a
bridging study exists to close. Run 16 is the only one to state it, and it belongs in the account of where the
data fall short rather than in a set-aside table; stating it converts the restraint all 16 runs already exercised
into a conclusion the proposal has earned, and it is what licenses the correlate-of-protection study the prompt
asks for. **The cross-dose comparison:** run 14 shows the complete handling: it names the differing baselines,
argues that the dose-2 convention would if anything reduce the number of genes called, and corroborates the
direction with cytokine fold changes on a common baseline. Run 09 (9687c0b1) adds the power argument, that dose 1
drew on two baseline samples and so had more power rather than less. Either route discharges the convention in one
sentence and leaves the conclusion exactly where it already stood. The room supports it directly: Day 29 measured
against the first-dose baseline gives 11 DE genes across all six cell types against a Day-2 peak of 3,024, so the
dose-2 reference draw is indistinguishable from pre-vaccination. **The comparator proteomics:** the dossier's
sequence-cluster convention at section 7 and the HRNR and KRT features together identify the contamination at no
analytic cost, and the deployment parameter should be stated as days to a documented serological response rather
than time to protection. **Antigen content:** the supportable claim is the narrower one — AS03 is necessary at
3.75 µg, since the unadjuvanted arm returns 0/10 seroconversion and floor-level titres, while sparing relative to
a higher unadjuvanted A/H7N9 dose is untested in this study — which 15 of 16 runs correctly confined. **A1, A2, A4, A5, A7:** already met in every run: carry forward the adjuvanted two-dose configuration rather than the
antigen, treat the Day-29 one-dose HAI GMT of 7.3 as sub-protective, name durability and breadth as unestablished,
and tie every number to its file alongside a reasoned set-aside section.
