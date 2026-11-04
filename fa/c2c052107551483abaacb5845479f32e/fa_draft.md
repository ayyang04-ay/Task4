# FA draft v2 — H7N9 next-work recommendation, job 30f4652b (16 × Opus 5.5)

RETYPE, DO NOT TRANSCRIBE. House format from Task jp2x8c9f: A-item indexed, prevalence per item,
non-discriminating items dismissed explicitly, second paragraph anchored on an exemplar run.
NOTE ON LABELS: this task's grading document uses A1–A7 for *items*, so trajectories are named
"run NN (hex)" throughout to avoid the collision the jp2x8c9f draft had with A14/A15.
Counts: paragraph 1 = 14 sentences, paragraph 2 = 15 sentences. Evidence in error_modes.md / item_matrix.md.

## What did the model do wrong?

The task is built on 7 A pillars, and on verified conduct only one of them discriminates. **A6** is that criterion
and 15/16 runs fail half of it: the item requires both restraint against elevating the interferon signature and a
statement that the trial measured no protection endpoint. All 16 pass the restraint, several going beyond the
Golden by showing that Table S186 pools both A/H7N9 arms and so marks AS03 receipt rather than response. The
failure is the second part — only run 16 (9993e8bb) states that the record contains immunogenicity only, and it
does so in a set-aside cell rather than in its account of where the data fall short. Eight runs (01, 02, 06, 07,
11, 12, 13, 15) substitute the weaker claim that no correlate of protection is established, which concerns how to
read a titre rather than what the trial measured, and the remaining seven (03, 04, 05, 08, 09, 10, 14) state
neither. So where a bridging study is proposed, it rests on a structural fact the proposal never states.
**A1, A2, A4, A5 and A7** — configuration attribution, two-dose necessity, the durability and breadth gaps, and
provenance with a set-aside section — passed 16/16 and are not relevant in FA. **A3** was recorded partial in
13/16, which makes it look like a second discriminating item, but it is not a model error: the only 15 µg arm is
Arm 1, A/H3N2v (A/Minnesota/11/2010), a different subtype, both A/H7N9 arms carry 3.75 µg with no dose-ranging arm
anywhere, and the Golden itself rules that arm non-comparable. The 13 runs that declined the quarter-dose framing
declined it correctly, and the 3 credited runs (08, 12, 15) were credited for the weaker reading. Among the B
items six of seven never fire. B5 — comparing DE-gene counts across the dose-1/dose-2 baseline break — fired in
13/16 and produces most of the 0.77–0.92 spread, but it does not survive the room: Day 29 measured against the
first-dose baseline gives 11 DE genes across all six cell types against a Day-2 peak of 3,024, so the dose-2
reference draw is indistinguishable from pre-vaccination, IP-10 rises 1.867-fold then 4.461-fold on a single
pre-vaccination baseline, and all 16 runs cite that figure. The item also penalises arguing that the response
wanes, which is a direction no run took. Two minor ungraded modes remain: 13/16 never identify the comparator-arm
keratin and hornerin features as handling contamination (only runs 06, 13 and 16 do), though none misuses them as
biology. And 4/16 (04, 07, 09, 10) treat time to protection as a quantity the trial measures, in run 07
(06a4976d) against its own statement that no protective titre is established.

## What should the model have done?

No run satisfies all 7 pillars: run 16 (9993e8bb) comes closest and is the exemplar for the discriminating
item, while run 14 (f8782a66) is the exemplar for the contested one. **A6.** Run 16 is the only one to state the inventory
fact, and the correct version is explicit: all 15 outcome measures in the registry record are serological,
cytokine or transcriptomic, none is a protection, efficacy or challenge endpoint, and that absence — not the
weakness of any particular titre — is the gap a bridging study exists to close. Stating it converts the restraint
all 16 runs already exercised into a conclusion the proposal has earned, and it is what licenses the
correlate-of-protection study the prompt asks for. **A3.** The correct move is the one 13 runs made: decline the
quarter-dose comparison, because the 15 µg content belongs to a different subtype and no unadjuvanted higher-dose
A/H7N9 arm exists. The supportable claim is narrower — AS03 is necessary at 3.75 µg, since the unadjuvanted arm
returns 0/10 seroconversion and floor-level titres — and antigen sparing relative to a higher unadjuvanted dose is
untested in this study. **B5.** Run 14 shows the complete handling: it names the differing baselines, argues that
the dose-2 convention would if anything reduce the number of genes called, and corroborates the direction with
cytokine fold changes on a common baseline. Runs 04 and 09 also discharge the convention, and run 09 (9687c0b1)
adds that dose 1 drew on two baseline samples and so had more power rather than less. The defect in the other 13
is the undischarged convention, not the comparison — a basis error rather than a wrong answer, and it should be
graded as one. **B4 and the minor modes.** The comparator-arm tables should be named as skin and handling
contamination, which the dossier's sequence-cluster convention at section 7 and the HRNR and KRT features together
supply at no analytic cost, and the deployment parameter should be stated as days to a documented serological
response rather than time to protection. **A1, A2, A4, A5, A7.** Already met in every run: carry forward the
adjuvanted two-dose configuration rather than the antigen, treat the Day-29 one-dose HAI GMT of 7.3 as
sub-protective, name durability and breadth as unestablished, and tie every number to its file alongside a
reasoned set-aside section.
