# FA draft — trace-based, no scores, no ratios. Job 30f4652b

Labels are runNN plus the short run id. Transcript locations are in transcript_traces.md; verification for
every factual claim is in verify_checklist.md. Score and prevalence language deliberately absent, including
"weakest-scoring", which is a score reference.

## What did the model do wrong?

Every run reached the correct primary verdict: carry forward the AS03 adjuvanted two-dose regimen rather than
the antigen alone, and flag durability and breadth as open.

The trial's lack of any protection endpoint goes unstated, and this is not a knowledge gap. run03 (890bbf23)
counts the registry's outcome measures early in its episode and remarks that there are only fifteen, then builds
a table printer so all of them can be read at once. run05 (b07ef105) enumerates what the results section holds
and goes back to confirm nothing else is hidden there. Both therefore had the complete measure inventory in one
view, by their own construction, and neither wrote the absence into the proposal. run08 (f9779a6c) and run16
(9993e8bb) do state it, but place it in a set-aside row rather than the section on where the data fall short.
The divergence is at the writing stage, not the analysis.

No run proposes work to close that gap. Every run dismisses field efficacy and human challenge on feasibility
or ethics grounds, which is defensible, but none puts anything in their place. run12 (1596ccf2) comes closest:
it names a nonclinical challenge or passive-transfer study and then defers it to pivotal planning rather than
proposing it as the next study.

The baseline convention governing the gene-count tables goes unnamed before runs compare across it. run05
raises the question itself, early on: it is unsure whether the post-second-dose fold changes are referenced to
the pre-vaccination draw or to Day 29, notes the registry wording is ambiguous on the point, and says it needs
to verify. It never returns to it. Later in the same episode it re-verifies its gene counts against the
registry for numerical accuracy, which means re-reading the outcome measure whose own description states the
reference-frame rule, and it still publishes the cross-dose comparison. run03 arrives at the same omission
differently: it parses every gene table out of the supplement and reconciles the counts against the registry,
then reads the registry's gene-count definition, accepts the threshold half of it as sound, and moves on,
leaving the reference-frame half of the same description unapplied. Both carry the comparison into their
recommendations, run03 into a requirement to measure dose-2 reactogenicity directly and run05 into a claim that
dose 2 is unlikely to be gentler.

## What should the model have done?

State what the trial measured. The fifteen outcome measures in the registry record are serology, cytokines or
gene counts, and none is a protection, efficacy or challenge endpoint. run03 and run05 already had this in
front of them, so the correction is only to write it into the section on where the data fall short that every
run has, rather than leaving it out or placing it in a set-aside row as run08 and run16 did.

Propose a route to close that gap. Field efficacy and human challenge are genuinely foreclosed, so what remains
is a nonclinical challenge, passive-transfer or immunobridging path with a stated acceptance criterion. run12
names one; putting it forward as the next study rather than deferring it is the move.

Name the baseline convention before comparing across it. run14 (f8782a66) does the whole thing in one sentence:
it names both baselines, points out that the dose-2 convention would if anything return fewer genes because
dose 1 averages two draws where dose 2 uses one, and corroborates the direction with cytokine fold changes
measured from a single baseline. run09 (9687c0b1) makes the same point from the other end, that dose 1 drew on
two baseline samples and so had more power rather than less. run04 (0842f297) flags the caveat plainly. For
run05 the correction is smaller still: close the question it had already opened.

One thing the runs were right to decline. run08, run11 (60c1bbbc) and run16 each independently reconstruct the
supplement's printed page labels and establish that the figures carrying the signature-to-peak-HAI correlation
are absent from the mounted file, and run11 cross-checks that the missing labels account exactly for the offset
between printed and physical numbering. Declining to quote a coefficient therefore rested on a verified
property of the data room, not on a misreading of it.

Everything else was already correct in every run: the adjuvanted regimen as the asset, the one-dose Day 29 HAI
GMT of 7.3 treated as insufficient and single-dose use rejected, durability and breadth named as open, every
figure tied to its source alongside a reasoned set-aside list, and the interferon signature kept as a predictor
of HAI titre rather than promoted to a protection marker.
