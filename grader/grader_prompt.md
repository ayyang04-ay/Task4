# H7N9 adjuvanted vaccine — next-work recommendation: Golden Response and grading guidelines

## Task framing

The task hands a colleague the complete dataset from a first-in-human programme study of an inactivated influenza A/H7N9 vaccine and asks for the proposal that colleague would take to a programme review board: what to carry forward, what to run next, and how the regimen would be deployed. The deliverable is `/outputs/recommendation.md`, with the lead recommendation on the first line, every quantitative claim tied to the file it came from, and a section naming the next studies considered and set aside with the reason for each.

The data room is three files: `dossier.md` (the programme's authored assay and analysis conventions; carries the consolidated cross-antigen serology and the reference-frame and loading conventions), `registry_results.json` (the trimmed trial record: arms, design, and every outcome measure with its numbers), and `supplement.pdf` (the 1014-page systems-biology supplement: differential expression, differential abundance, and enrichment tables, plus the gene-signature figures). The weight of this task sits in **how the numbers were read and what was attributed to what**, not in the final go/no-go — a proposal that lands on "carry the adjuvanted regimen forward" for the wrong reasons is not a correct answer.

Accounting rules for this grade:

- A result counts as correct only where the value is right **and** the basis given produces it. A right number resting on records that do not yield it, or on no stated derivation, is not correct; analysis the attempt did but did not write down earns nothing.
- Where a product asks which studies or which configurations qualify, the **membership is the result** — the right set with the right reasons, not a matching count over a different set.
- Prose that disagrees with the attempt's own tables or cited numbers establishes nothing.
- A carried-forward error is penalized **once**, where it enters the chain. An error entering at two independent points is two errors.
- Impartial between methods, disciplines, formats and length. No verbosity penalty in either direction: a complete answer with extra material appended is not penalized for the extra; a constraint is enforced only where required content is *missing* because space went elsewhere.
- Judge the proposal as the several roles at a programme review board would — clinical, translational, regulatory, manufacturing — not from one discipline's view.

---

## Golden Response

**Lead recommendation (first line).** Carry forward the AS03-adjuvanted, two-dose A/H7N9 (A/Shanghai/2/2013, 3.75 µg HA + AS03) regimen as a single configuration; do not carry the H7N9 antigen forward as a standalone immunogen. The next study is a dose/durability-confirmation trial of that adjuvanted two-dose regimen with follow-up extended past Day 57 and a drifted-clade panel added; protection remains unestablished and cannot be inferred from the immunogenicity or the gene-signature data in hand.

**What the current data establish.**

1. *The response is a property of the adjuvanted configuration, not of the antigen.* The unadjuvanted A/H7N9 arm (Arm 3, 3.75 µg, two doses) does not respond: HAI GMT 5.0 → 5.2 → 5.0 across Day 1 / Day 29 / Day 57 and Neut 5.0 → 5.4 → 5.9, with 0% HAI and 0% Neut seroconversion (`registry_results.json`, GMT outcome measures for the A/H7N9 vaccine with and without AS03, and the HAI/Neut seroconversion measures). Values at or near 5 are the assigned below-detection value (`dossier.md` §4). AS03 is therefore necessary for any detectable A/H7N9 response; the antigen at this content does nothing on its own.

2. *Two doses are required; one is sub-protective.* In the adjuvanted arm (Arm 2) HAI GMT is 5.2 at baseline, **7.3 after one dose (Day 29)**, and **85.7 after the second dose (Day 57)**; Neut is 5.0 → 17.4 → 190.3 (`registry_results.json`). Seroconversion is 80% (HAI) and 100% (Neut), reported at Day 57 after the two-dose course (`registry_results.json`). The single-dose Day 29 HAI GMT of 7.3 sits below a 1:40 seroprotective titer; the immunogenic result is the two-dose result.

3. *Dose-sparing is real and is an adjuvant effect.* The A/H7N9 HA content is 3.75 µg — one quarter of the 15 µg used for the A/H3N2v comparator (`dossier.md` §1, `registry_results.json` arms). That quarter-dose antigen is immunogenic only with AS03 (per point 1), so the dose-sparing claim belongs to the adjuvanted configuration and not to the antigen.

**Where the data fall short (these define the next studies).**

4. *No durability data.* Immunogenicity is sampled only through Day 57 (HAI/Neut at Days 1, 29, 57; `dossier.md` §2, `registry_results.json`). Nothing in the room speaks to antibody persistence; the 12-month follow-up is for safety/serious events only (`dossier.md` §2). Any claim about duration of protection is unsupported.

5. *No breadth data.* The vaccine is monovalent A/Shanghai/2/2013 (`dossier.md` §1). There is no cross-clade or antigenic-drift panel for H7N9. The only cross-antigen serology in the room is A/H7N9-vaccine response measured against the A/H3N2 assay antigen (`dossier.md` §5), which is a heterosubtypic check, not H7N9 breadth. Breadth against drifted H7N9 is unestablished.

6. *No protection endpoint anywhere.* Every outcome measure in the record is serological or systems-biology — HAI/Neut titers and seroconversion, cytokine concentrations, and differentially expressed gene counts (`registry_results.json`). There is no challenge, no efficacy, and no clinical protection endpoint. The supplement reports a gene signature — interferon- stimulated genes, MHC-I and proteasome members — that correlates with **peak HAI titer** (`supplement.pdf`, signature-vs-titer figures and the table of top genes predicting peak HAI titer; e.g. GBP5 r≈0.86, IFIT r≈0.84, PSME2 r≈0.78, MHC-I members r≥0.74). This may be reported, but HAI titer is itself a surrogate, so the signature is a predictor of a surrogate and cannot be advanced as a validated correlate of protection or as a basis for an accelerated/surrogate approval endpoint. The chain is signature → HAI titer → protection (unmeasured), and the last link is absent from the room.

7. *The systems-biology contrast is interpretable only within its stated conventions.* The adjuvanted arm carries a large innate transcriptional response peaking at Day 2 (e.g. monocyte/dendritic/neutrophil differentially expressed gene counts in the high hundreds to ~2000) that is essentially absent in the unadjuvanted arm (counts of 0 across most cell types) (`registry_results.json`, differentially expressed gene outcome measure). This corroborates point 1. It does **not** on its own establish a mechanism or a protection marker, and three conventions bound how far the supplement can be read: first-dose tables (Days 2/4/29) are referenced to the mean of the Day −7 and Day 1 draws while second-dose tables (Days 30/32/36) are referenced to the Day 29 draw, so dose-1 and dose-2 counts are not on a common baseline (`dossier.md` §6); proteomic lysate input is 10 µg for B and NK preparations versus 25 µg for neutrophil, T, monocyte and dendritic preparations, so abundance is not comparable across cell types without accounting for it (`dossier.md` §7); and the comparator-arm differential-abundance tables are dominated by keratin and hornerin features (e.g. HRNR, KRT clusters), which are skin/handling contamination rather than vaccine biology.

**Next studies (recommended).**

- A confirmatory two-dose adjuvanted-regimen immunogenicity study with follow-up extended well past Day 57 to read antibody persistence, powered beyond the ten-per-arm of the current study. (Addresses gap 4.)
- A breadth/cross-clade immunogenicity arm or study testing the adjuvanted regimen against drifted H7N9 isolates. (Addresses gap 5.)
- A correlate-of-protection or challenge/bridging path, since no protection endpoint exists and the gene signature does not substitute for one. (Addresses gap 6.)

**Deployment.** The carried-forward product is the two-dose, AS03-adjuvanted, 3.75 µg A/H7N9 regimen — dose-sparing that stretches antigen supply for a pandemic stockpile, at the cost of a second dose and the logistics of adjuvant co-formulation; a single-dose deployment is not supported by these data.

**Set aside (next studies / options considered and rejected).**

- *Carrying the unadjuvanted A/H7N9 antigen forward, or a standalone-antigen dose study* — the unadjuvanted arm has 0% seroconversion and flat floor-level titers (`registry_results.json`); there is nothing to optimize.
- *A single-dose regimen* — Day 29 one-dose HAI GMT 7.3 is sub-protective (`registry_results.json`).
- *Advancing the interferon/gene signature as a surrogate or accelerated-approval endpoint* — it predicts peak HAI titer, itself a surrogate, and no protection endpoint exists in the room (`supplement.pdf`, `registry_results.json`).
- *Treating the A/H3N2v arm as a product benchmark* — its high titers (HAI 37.3 → 144.2; Neut 171.5 → 485.0; `registry_results.json`) are a recall response off a primed baseline in a seasonal-exposed population, not comparable to the primary response to a novel H7N9 antigen, and H3N2v is a separate comparator, not this programme's candidate.
- *Building a mechanistic/biomarker claim on the comparator-arm proteomics* — those tables are keratin/hornerin contamination (`supplement.pdf`, `dossier.md` §7).

*Equivalence note.* The lead may be stated as a carry-forward of the adjuvanted two-dose regimen in any wording; GMT values are accepted within normal rounding; the specific next-study designs may differ as long as durability, breadth and the protection gap are each addressed; seroprotection may be framed as a 1:40 HAI titer or via the seroconversion definition in `dossier.md` §4.

---

You are grading a programme-review-board proposal recommending what to carry forward from a first-in-human inactivated influenza A/H7N9 vaccine study and what to run next, written from a three-file data room (an authored conventions dossier, a trimmed trial registry record, and a 1014-page systems-biology supplement). The weight is on what the attempt attributed the immunogenicity to and on which claims it correctly declined to make, not on the final carry-forward verdict in isolation.

Start with the Golden Response for the H7N9 next-work recommendation above as your benchmark. This is an example of a correct answer for this task.

A) MUST BE PRESENT AND CORRECT
The following are the key requirements of a correct answer. Use the golden response and your judgment to identify any additional required content not listed here.

- **Attribution to the adjuvanted configuration (`registry_results.json`, `dossier.md`).** The thing carried forward is the AS03-adjuvanted A/H7N9 regimen, and the immunogenicity is attributed to the antigen-plus-AS03 configuration rather than to the H7N9 antigen. The most common way this task goes wrong is recommending or describing "the H7N9 vaccine" as the asset while treating the adjuvant as a detail — the unadjuvanted arm's 0% seroconversion and flat floor-level HAI/Neut titers (5.0→5.2→5.0; 5.0→5.4→5.9) establish that the antigen alone is inert, so attribution is the load-bearing judgment and an attempt that misses it has the wrong asset.
- **Two-dose necessity / single-dose insufficiency (`registry_results.json`).** The correct answer recognizes that the immunogenic result is the two-dose (Day 57) result — adjuvanted HAI GMT 85.7, Neut 190.3, 80%/100% seroconversion — and that one dose (Day 29 HAI GMT 7.3) is sub-protective. A proposal built on a single dose, or that reads the Day 29 figure as success, is wrong.
- **Dose-sparing identified as an adjuvant effect (`dossier.md` §1, `registry_results.json`).** The 3.75 µg content is a quarter of the 15 µg comparator content and is immunogenic only with AS03; the dose-sparing belongs to the configuration.
- **Durability named as an unestablished gap (`dossier.md` §2, `registry_results.json`).** Immunogenicity is read only to Day 57; persistence is unknown and is a next-study target. (The 12-month follow-up is safety-only.)
- **Breadth named as an unestablished gap (`dossier.md` §1, §5).** The vaccine is monovalent A/Shanghai/2/2013 with no cross-clade/drift panel; the H7N9-vs-H3N2 cross-antigen serology is not H7N9 breadth.
- **No protection endpoint, and the gene signature not elevated to one (`registry_results.json`, `supplement.pdf`).** The correct answer states that no outcome measure is a protection/efficacy/challenge endpoint — every measure is serological or systems-biology — and, if it discusses the interferon/gene signature, keeps it as a predictor of peak HAI titer (a surrogate) rather than a validated correlate of protection or a surrogate/accelerated approval basis. Reporting the correlation is acceptable; the required judgment is the restraint against elevating it.
- **Provenance and a set-aside section (prompt).** Quantitative claims are tied to the file they came from, and the deliverable contains a section naming next studies/options considered and set aside, each with a reason that traces to a value in the room. A clean recommendation with the triage hidden does not meet this.

B) PENALIZE FOR
The following are common errors observed on this task. This list is not exhaustive — apply your judgment to any other issues you identify.

- Recommending the unadjuvanted A/H7N9 antigen as a carry-forward, or proposing to optimize/dose-escalate the standalone antigen — refuted by 0% seroconversion and floor-level titers in the unadjuvanted arm (`registry_results.json`). (Does not fire on an attempt that correctly carries forward the adjuvanted configuration and merely notes the antigen alone failed.)
- Claiming a single dose is sufficient or seroprotective — refuted by the Day 29 one-dose HAI GMT of 7.3 (`registry_results.json`).
- Advancing the interferon/gene signature as a validated correlate of protection, an immune marker that can stand in for efficacy, or a surrogate/accelerated- approval endpoint — refuted because the signature's correlation of record is against peak HAI titer, itself a surrogate, and no protection endpoint exists in the room (`supplement.pdf`, `registry_results.json`). (Does not fire on an attempt that merely reports the correlation while declining to elevate it.)
- Citing comparator-arm proteomic hits — keratin/hornerin features such as HRNR or KRT clusters — as vaccine biology or mechanism, refuted by their identity as skin/handling contamination (`supplement.pdf`, `dossier.md` §7).
- Comparing differentially expressed gene or protein counts across the first and second dose (or treating the Day 30/32/36 figures as on the same footing as Day 2/4) to argue the second dose adds little or the response wanes — refuted by the different baselines for first- and second-dose tables (`dossier.md` §6).
- Comparing protein abundance across cell types without accounting for the 10 µg (B, NK) versus 25 µg (neutrophil, T, monocyte, dendritic) lysate loading (`dossier.md` §7).
- Treating the A/H3N2v arm's high titers (HAI 144.2, Neut 485.0) as evidence of superior product immunogenicity or as a benchmark the H7N9 candidate should match — refuted because those are a recall response off a primed baseline (pre-vaccination HAI 37.3, Neut 171.5) in a seasonally exposed population, not a primary response to a novel antigen (`registry_results.json`).
- Reading the ~1.4× cross-antigen HAI rise in the unadjuvanted H7N9 arm against the H3N2 assay antigen as evidence the unadjuvanted vaccine "works" or has cross-protective merit — refuted because the arm shows no rise against the H7N9 antigen and the product is an H7N9 vaccine (`dossier.md` §5).
- Any quantitative claim asserted without the derivation or file that produces it, whether or not the value is right.

C) NEUTRAL
The following are examples of acceptable variations that should not affect the score. Other variations may also be neutral — use your judgment.

- Reporting the interferon/gene-signature-to-peak-HAI correlation, naming the genes or quoting the r values — neutral, provided it is not elevated to a protection surrogate (see A/B).
- Which specific next-study designs are proposed, their order, sizing, or whether they are combined into one trial, as long as durability, breadth and the protection gap are each addressed.
- Stating seroprotection as a 1:40 HAI titer or via the seroconversion definition in `dossier.md` §4; reporting GMT values within normal rounding; floor values stated as "5", "<10" or "below detection".
- Whether the proposal also discusses safety/reactogenicity, cytokine data, manufacturing or regulatory pathway, provided the required content is present.
- Section ordering, headings, length, tables vs prose, and any additional correct analysis the prompt did not require.
- Discipline or framing of the write-up (clinical, regulatory, translational), terminology for the arms, and whether the H3N2v arm is described as comparator, benchmark or control, provided it is not used as a product benchmark (see B).
- Any method or route that establishes the same claims from the mounted files earns what the Golden's route earns; the Golden's particular wording, citations and order are examples, not requirements.
