# Transcript traces — where each failure mode is visible in the trajectory

Locations are thinking-block indices in the run's Taiga transcript (T0NN), countable from the start of the
episode. Descriptions, not quotations. Scores and ratios deliberately absent.

## Mode A — the trial's lack of any protection endpoint is never stated (A03, A05, A09 among those omitting it)

Not a knowledge gap. Both weakest runs establish the fact in-transcript and then leave it out of the deliverable.

- **A03 (890bbf23), T003:** while sizing the registry file, it counts the outcome measures and remarks that
  there are only fifteen. **T005:** it then writes a dedicated table printer so all fifteen can be viewed at
  once. The complete measure inventory was therefore in front of it, in one view, by its own construction.
- **A05 (b07ef105), T041:** it enumerates what the results section contains - participant flow, baseline
  characteristics, outcome measures, adverse events - and goes back to check whether anything else is hidden
  there. It satisfies itself that nothing else exists.

Both had the inventory and the confirmation that nothing else is in the record. Neither wrote the absence into
the proposal. The divergence from the golden route is at the writing stage, not the analysis stage.

## Mode B — no route proposed to close the protection gap

The runs did go down the correlation path. They did not talk themselves out of it: they established that the
evidence is not in the room.

- **A08 (f9779a6c), T019:** reconstructs the PDF's printed page labels and concludes the genuinely missing
  pages are 37-39 (Figures S24-S26) and 56-71 (Figures S43-S58), the per-gene activity-versus-peak-HAI figures.
- **A11 (60c1bbbc), T028:** independently reaches the same two ranges and cross-checks that the nineteen
  missing labels account exactly for the offset between printed and physical numbering.
- **A16 (9993e8bb), T015:** same conclusion, and notes Table S186 on overlap in top predictive genes survives
  at the end of the document.
- **A08, T033:** having found the figures gone, it works through Table S186 in full across its page range to
  establish what the surviving table does and does not support.

So the sequence is: look for the correlation evidence, establish it is physically absent, analyse what remains,
decline to quote a coefficient. The decision not to report rested on a verified property of the mounted file,
not on an erroneous assumption about the data room or the prompt. Three runs derive it independently.

Consequence for the FA: failing to report the signature-to-titre correlation cannot be a failure mode, because
the figures the correlation is cited to are not in the data room. What remains is that no run proposes work to
close the protection gap - A12 (1596ccf2) names a nonclinical challenge or passive-transfer study and defers it
rather than putting it forward as the next study.

## Mode C — the baseline convention is not named before comparing across it (A03, A05 among those omitting it)

Two different routes to the same omission, both traceable.

- **A05 (b07ef105), T008:** raises the exact question unprompted - it is unsure whether the post-second-dose
  fold changes are referenced to the Day 1 pre-vaccination draw or to Day 29, notes the registry wording is
  ambiguous on this, and says it needs to verify. **It never returns to it.** No later block resolves the
  question. **T065:** it re-verifies its DE gene counts and totals against the registry for numerical accuracy,
  which means re-reading the outcome measure whose own description states the reference-frame rule, and still
  publishes the cross-dose comparison. The comparison then carries into its deployment claim about dose-2
  reactogenicity. This is a run that opened the right line of enquiry, flagged it as unresolved, and shipped
  without closing it.
- **A03 (890bbf23), T026, T027, T030:** parses every DE gene table out of the supplement and reconciles the
  per-table counts against the registry. **T051:** reads the registry's DE-gene outcome definition, judges the
  threshold half of it sound (FDR and fold-change criteria), and moves on to the dossier. It validated one half
  of the measure's definition and left the reference-frame half of the same description unapplied.

## Where to verify

Thinking blocks are in `transcripts/attempt_NN_<hex>.json`, under
`contexts[0].conversation.data[].contents[]` where `type` is `Thinking`; the text is in the `data` field.
Block indices above count Thinking blocks in order from the start of the episode.
