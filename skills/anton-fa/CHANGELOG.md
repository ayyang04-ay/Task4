# Changelog

## 2026-10-30 — rebuilt around prevalent error modes

Direction change from the client, relayed by team lead: the interest has moved
from scores to **failure modes in trajectories**. Where a default grader scores
runs with no writer-authored grading document, the scores carry almost no
information. The client wants error modes identified on their own merits — large or
small, impactful or benign — and ranked by **prevalence**, on the reasoning that a
small error shared across six trajectories has more leverage on model development
than a large error in one.

### Changed

- **Unit of analysis is the error mode, not the run.** Phase 1 produces an
  error-mode ledger ordered by prevalence, then consequence. Runs are where modes
  are found and counted.
- **Two operating modes.** Graded (a writer-authored grading document scored the
  runs; errors may be mapped to items) and trajectory-only (default grader or no
  meaningful document; errors identified intrinsically, runs not ranked by score).
- **Error taxonomy added** (`references/error-taxonomy.md`): eleven classes with
  definitions and tells, built from the lead's starter list — faulty logic,
  hallucinated features, unjustified inferences — and extended from an observed
  panel.
- **Prevalence discipline added** (`references/prevalence.md`). A mode must be
  stated as a predicate another reader can apply without judgment before anything
  is counted. Loose definitions produce counts that mean nothing.
- **Weakest and median reading restored.** Both are read in full; prevalence is
  established by searching every remaining trajectory for each candidate mode.
- **Deliverable before transcript.** The output file the grader judged is
  typically 30-50 KB against 1-4 MB of transcript JSON, is the artifact that was
  assessed, and yields citable line numbers.
- **Conduct-not-motive rule added** as a non-negotiable. Every FA claim retracted
  in the session behind this rebuild was a motive claim.
- **Phase 0 is now a gate.** A parse manifest with pass/fail per row, covering
  split exports, failed clusters, as-scored data-room reconstruction, trajectory
  labels obtained verbatim, and stats-library availability.
- **Phase 4 (revision support) added.** Drop-in replacements with location,
  original, replacement and reason; minimal edits; the writer's structure and voice
  preserved. Previously the skill prohibited replacement wording outright, which
  left the operator improvising off-script.
- **Grading-document handling narrowed to four questions**
  (`references/graded-mode.md`). The writer already audits the document; the skill
  reads it once for the four things that otherwise produce wrong claims — are items
  binary, which analytical routes are accepted, which items are conjunctive, and
  where the accounting rules apply. The accepted-routes question alone invalidated
  a drafted claim.
- **Verdict / rationale split.** The grader verdict is ground truth and is never
  re-adjudicated. The rationale is auditable: figures and characterisations are
  verified before being repeated, and conflicts are surfaced rather than silently
  resolved. As grading documents receive less audit, this check is the early
  warning.

### Deprecated

- **Best-run contrast** and **divergence notes** as standing phases. Both were
  built for a single-run FA scored against a golden; under a prevalence brief the
  same evidence is better carried by the ledger, which already records which
  trajectories do and do not show each mode. Restore if the brief returns to
  per-run scoring against a reference solution.
- **Grader-gap checking as part of the best-run contrast.** Retained, moved to
  Phase 5 calibration notes.

### Retained from the previous version

The non-invention rule, the grader-reach integrity check, the epistemic labels
([transcript] / [computed] / [inference]), the Phase 3 claim-verification table,
the overlap check, and the instruction not to defer when the writer's reading is
unsupported. The last two in particular earned their place.

## 2026-10-30b — verification and the item matrix

### Added

- **Citation audit as a default** (`references/verification.md`). On the first
  print of any citation: verbatim match, location resolves, surrounding context
  supports the attribution, correct table row. One or two tool calls per paragraph.
  Stated explicitly that it catches citation and context errors and **not**
  inference errors, so a clean audit is never evidence the claims are sound.
- **Coverage screen** (Phase 1c). Which trajectories referenced each data-room
  file; a file most trajectories ignored is a candidate mode. The screen produces
  candidates only — apparent non-use must be confirmed against the transcript,
  because trajectories routinely read a file without naming it in their output. On
  the reference panel the screen produced two false positives out of two flags.
- **Item matrix** (Phase 1e, graded mode). Trajectories down, A and B items across,
  with per-item totals and B-item severity where the rationale qualifies it. Built
  semi-automatically: parse to generate the grid, then confirm every fired and
  uncertain cell by reading the rationale.
- **Rationale parsing recorded as a screen only.** Automated extraction from
  rationale prose fails systematically and in the direction that invents penalties:
  "Not triggered: B1, B2, B4…" places the negation beside the first item only. A
  naive parse reported eleven penalties against a trajectory whose rationale had
  cleared all but one. Uncertain cells are reported as uncertain.

## 2026-11-05 — reviewer-set output rules, transcript tracing, verification hardening

Feedback from the client reviewer on a submitted FA, plus the analyst errors made producing it.

### Added

- **What the FA may contain.** Reviewer-set rules: no scores (not valid without the grader documents, and
  "weakest-scoring" counts as a score reference), no k-of-n ratios, failure modes and the runs carrying them
  only, and strict section discipline — nothing a run did well may appear in the failure paragraph, and nothing
  prescriptive either. Praise inside a failure item gets the item rejected.
- **The requirement-basis test.** A mode is valid only where the requirement it breaches is stated in the
  prompt or the data room. An implicit expert norm is task ambiguity and belongs in calibration notes. Two
  strengtheners: whether the prompt names the deliverable section the omission belongs in, and whether the runs
  themselves built that section, which forecloses the ambiguity objection. Where the prompt permits the
  behaviour, the mode is weak — say so rather than shipping it.
- **Phase 1g, trace each mode to the trajectory.** Position, not quote, worked from thinking blocks as well as
  tool calls. Three recurring shapes named: raised then abandoned, encountered then unapplied, established then
  unwritten. The last is a reporting failure and must not be written as a failure to recognise.
- **Analyst failure modes** in `references/verification.md`, with the rule each produces.
- **Export gaps** in the same file: the `outputs` cluster is often excluded, thinking text lives in `data`, and
  the grading transcript is often null.

### Changed

- **Phase 3e** now checks the output rules and notes that hand-written texture is deliberate.
- **Phase 3f** measures overlap rather than judging it, and carries two limits: do not offer stylistic
  AI-detection judgments, because reading cannot separate model output from a writer's own register and
  attempting it led to the writer's idiom being misattributed to this skill; and do not generate polished prose
  for the writer, because prose handed over is edited rather than replaced, which leaves long matched runs
  intact. Give bare facts instead.
