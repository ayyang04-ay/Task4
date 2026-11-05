# Changelog — drop-in replacements for the shipping FA

Retype these; do not paste. Each row is exact find/replace against your text. Sentence count is unchanged
except where noted.

## Paragraph 2 — "What should the model have done?"

### 1. Outcome measure count and location
FROM: `all 16 outcome measures in the data room were serology, cytokines, or gene counts`
TO:   `all 15 outcome measures in the registry record were serology, cytokines, or gene counts`
WHY: There are 15, not 16 (2 primary, 13 secondary). They sit in registry_results.json, not across the
three-file data room.

### 2. Wrong run, wrong count  [highest priority]
FROM: `A15 is the only model that noted this`
TO:   `A08 and A16 are the only models that noted this`
WHY: A16 (9993e8bb) states it at line 304, "The package contains immunogenicity only", and A08 (f9779a6c) at
line 354, "The development pathway has to rest on immunogenicity (as this trial's own endpoints do)". A15
(abf75de9) line 200 says something different - "The trial defines no protective titre" - which is the weaker
claim. Two runs, not one. As written this also contradicts your first paragraph, which says 2/16 and names A08
and A16.

### 3. A12 credited with the move it failed to make
FROM: `A12 names one but postpones/defers it as the next study move.`
TO:   `A12 names one but defers it rather than proposing it as the next study.`
WHY: A12 line 308 says the study "can wait for pivotal planning". Naming it as the next study is the
correction, not what A12 did.

### 4. A14's reasoning - cytokine direction and logical role both inverted
FROM: `notes that dose 2 would likely find fewer DE genes since the other data (cytokines changes were fewer, so
this would correlate; a reasonable hypothesis)`
TO:   `notes that the dose-2 convention would if anything find fewer DE genes, because dose 1 averages two
baseline draws while dose 2 uses one, and that the cytokines show the same amplification on a common baseline`
WHY: The cytokines rose, they did not fall - IP-10 goes 1.867 after dose 1 to 4.461 after dose 2, from a single
pre-vaccination baseline. A14 cites them as corroboration that the response really is larger after dose 2, not
as the reason fewer genes would be called. That reason is methodological: averaging two draws reduces noise, so
the dose-2 convention is the more conservative. A14 line 64 verbatim: "dose-2 comparisons use a single Day-29
draw, while dose-1 comparisons average two draws (DOS Section 6). That difference would, if anything, reduce the
number of genes called after dose 2, and the cytokines below show the same amplification."

### 5. A09 makes the same point, not a different one
FROM: `A09 also recognizes it, but to a different point.`
TO:   `A09 recognizes the same point from the other end: dose 1 drew on two baseline samples and so had more
power, not less.`
WHY: A09 line 75 is A14's observation inverted, not a separate one.

### 6. Grammar
FROM: `Name the baseline conventions its using in comparisons`
TO:   `Name the baseline convention it is using in comparisons`

FROM: `note that none of it was protection, efficacy, or challenge endpoints`
TO:   `note that none of them was a protection, efficacy, or challenge endpoint`

FROM: `kept s a predictor of HAI titer`
TO:   `kept as a predictor of HAI titer`

## Paragraph 1 — still outstanding from the shipped version

### 7. Contradicts your own opening sentence  [highest priority]
FROM: `carry these comparisons forward into their final decision`
TO:   `carry these comparisons forward into their study-design and deployment recommendations`
WHY: Sentence 1 says all 16 got the primary verdict right, which is correct - the cross-dose claim never
touched the carry-forward decision. A03 line 137 makes dose-2 reactogenicity a measurement requirement in a
proposed study; A05 line 231 concludes dose 2 is unlikely to be gentler. Neither is the final decision.

### 8. Plural implies runs that do not exist
FROM: `Median-scoring runs (such as A11) make a weaker claim`
TO:   `One median-scoring run (A11) makes a weaker claim`
WHY: The median pair is A09 and A11; only A11 makes it. Of the five runs that do (A01, A02, A11, A13, A15),
A11 is the only median one.

### 9. Missing noun
FROM: `3/16 models mention a nonclinical or immunobridging, but don't provide a plan`
TO:   `3/16 models mention a nonclinical or immunobridging route, but don't provide a plan`

### 10. Typos
FROM: `postpoining it` TO: `postponing it`
FROM: `which are notable the weakest-scoring runs` TO: `which are notably the weakest-scoring runs`

### 11. Citation formatting
Run ids are lowercase as the Hub displays them: `F9779A6C` to `f9779a6c`, `890BBF23` to `890bbf23`,
`B07EF105` to `b07ef105`. The separator also flips between `A08 (F9779A6C)` and `A03; 890BBF23` - pick one.

## Order to apply

1. Edit 2 and edit 7 first: both are contradictions a reviewer would catch on one read.
2. Then 4, which is the only one that misstates a run's scientific reasoning.
3. Then 3, 5, 8, 1.
4. Then 6, 9, 10, 11.

---

# Changelog — trace-based draft (factual fixes only)

### 1. Heading scope
FROM: `Failing/low performing runs committed the following errors:`
TO:   `The following errors recur across the panel:`
WHY: Two of the three errors are panel-wide, and the draft says so itself ("every run dismisses field
efficacy ... no run volunteers any compensatory studies"). run08, run16 and run12 are cited under this heading
and are not low performers. "Low performing" is also a score reference.

### 2. Knowledge gap vs omission
FROM: `Failed to recognize/note the lack of protection endpoint data.`
TO:   `Failed to note the lack of protection endpoint data.`
WHY: The traces disprove a recognition failure. run03 counts the measures and builds a printer so all can be
read at once; run05 enumerates the results section and checks nothing else is hidden. They recognised it and
did not write it down, which is the point of the trace.

### 3a. run05's question concerns the cytokines
FROM: `it is unsure whether the post-second-dose fold changes are references to the pre-vax draw or to D29`
TO:   `it is unsure whether the post-second-dose cytokine fold changes are referenced to the pre-vax draw or to D29`
WHY: The registry titles those measures "Fold Change in Cytokine and Chemokine Concentrations From
Pre-vaccination", which is the wording run05 calls ambiguous. Naming the measure keeps the claim checkable.

### 3b. The comparison it ships is a different measure
FROM: `It still publishes the cross-dose comparison.`
TO:   `It still publishes a cross-dose gene count comparison without naming the convention that governs those tables.`
WHY: The comparison is of DE gene counts, governed by dossier Section 6 and the DE measure's own description,
not by the cytokine wording it queried. Without this the question raised and the error shipped look like the
same object, and a reviewer opening the transcript will see they are not.
