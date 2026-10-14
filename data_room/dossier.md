# Programme reference — assay conventions, analysis parameters, and consolidated serology

Internal reference for the H7N9 adjuvanted vaccine programme. States the
methods and conventions used to generate the mounted datasets. Carries no
interpretation of the results.

---

## 1. Study configuration

Three parallel groups, ten participants each, healthy adults 18–49, single site.

| Group | Vaccine | HA content | Adjuvant | Schedule |
|---|---|---|---|---|
| 1 | A/H3N2v (A/Minnesota/11/2010) | 15 mcg | none | one dose, Day 1 |
| 2 | A/H7N9 (A/Shanghai/2/2013) | 3.75 mcg | AS03 | two doses, Day 1 and Day 29 |
| 3 | A/H7N9 (A/Shanghai/2/2013) | 3.75 mcg | none | two doses, Day 1 and Day 29 |

The A/H7N9 HA content of 3.75 mcg was the content used for this programme.
AS03 is an oil-in-water emulsion adjuvant.

Group 1 was administered open-label. Groups 2 and 3 were administered blinded;
the HAI, neutralization, cytokine and sequencing assays were run masked to
A/H7N9 adjuvant allocation.

## 2. Sampling schedule

Venous blood at Day −7, 1, 2, 4, 8, 29, 30, 32, 36, 57.

| Assay | Days drawn |
|---|---|
| HAI, neutralization | 1, 29, 57 (Group 1: 1, 29) |
| Serum cytokines (24 analytes) | 1, 2, 4, 8, 29, 30, 32, 36 |
| RNA-seq, proteomics (sorted cells) | −7, 1, 2, 4, 8, 29, 30, 32, 36 |

Safety: solicited reactions through 8 days after each dose; unsolicited adverse
events through 28 days after each dose; serious and medically-attended events
through 12 months after the last dose for the A/H7N9 groups and 1 month for the
A/H3N2v group.

## 3. Cell separation

PBMC and neutrophils recovered by Ficoll; neutrophils purified from the PMN
fraction with anti-CD15 microbeads. Magnetic sorting then isolated CD19 (B),
CD3 (T), CD56 (NK), CD11c (dendritic), CD14 (monocyte) populations. Compartment
purity exceeded 99% on flow cytometry performed during assay optimization.

## 4. Serology conventions

Titers are measured in two-fold serial dilutions beginning at 1:10. A titer
below the 1:10 detection limit is assigned a value of 5 for computation.

Seroconversion is defined as: a pre-vaccination titer below 1:10 together with a
post-vaccination titer of at least 1:40; or a pre-vaccination titer of at least
1:10 together with at least a four-fold rise.

Geometric mean titers are reported with 95% confidence intervals from 1000
bootstrap replicates. A confidence interval reported as [NA, NA] indicates all
contributing values were at the assigned below-detection value.

HAI was performed against the homologous assay antigen for each group.
Neutralization seroconversion was a secondary endpoint; the neutralization assay
format is not specified in this reference.

## 5. Consolidated serology — both assay antigens, all groups

Reported as geometric mean fold rise from the pre-vaccination draw, with 95%
confidence interval where available.

| Group | Assay | vs A/H3N2 antigen | vs A/H7N9 antigen |
|---|---|---|---|
| 1 | HAI | 3.9× (Day 29) | no rise above baseline |
| 1 | Neut | reported | no rise above baseline |
| 2 | HAI | no rise above baseline | 16.6× (Day 57) |
| 2 | Neut | no rise above baseline | reported |
| 3 | HAI | 1.4×, lower CI bound above 1 (Day 29) | no rise above baseline |
| 3 | Neut | not significant | no rise above baseline |

Comparison of A/H3N2-directed HAI fold change, adjuvanted versus unadjuvanted
A/H7N9 group: p = 0.052 (upper one-sided Welch's t-test). Neutralization
equivalent: p = 0.087.

## 6. Transcriptomic analysis parameters

Paired-end RNA sequencing, 25 million reads, aligned to GRCh38, Ensembl
version 99. Differential expression by negative-binomial generalized linear
model per group, cell type and post-vaccination day. A gene was called
differentially expressed at absolute fold change of at least 1.5 and
false-discovery-rate-adjusted p below 0.05.

Baseline for first-dose comparisons is the mean of the Day −7 and Day 1 draws.
The Day 29 draw is the baseline for second-dose comparisons in the A/H7N9
groups. Day 2, 4 and 29 tables are referenced to the first-dose baseline; Day
30, 32 and 36 tables are referenced to the second-dose baseline.

## 7. Proteomic analysis parameters

TMT10-plex isobaric labelling, LC-MS/MS, data-dependent acquisition sampling the
15 most abundant ions per survey scan. Proteins identified against UniProt,
annotated to Ensembl version 101. Quantified at a minimum of two unique
peptides.

Lysate input: 10 mcg for B and NK cell preparations; 25 mcg for neutrophil, T
cell, monocyte and dendritic cell preparations. Protein log2 ratios were
normalized within each cell type to align the medians of the ratio
distributions. Proteins with at least 85% non-missing observations were
retained; remaining missing values were imputed by k-nearest-neighbour.
Differential abundance was called at a false-discovery-rate-adjusted p below
0.15.

Where several proteins share a sequence cluster at 50% identity, the shared
cluster identifier is reported in the cluster column; members of one cluster are
one quantified feature.

## 8. Enrichment analysis parameters

Over-representation testing by goseq against KEGG, MSigDB Reactome, MSigDB GO
Biological Process and Blood Transcription Module gene sets, accounting for gene
length bias. Each enrichment row reports gene-set size, the count and percentage
of differentially expressed set members, the up- and down-regulated split, a
Jaccard index against the differentially expressed set, and the adjusted p-value.
