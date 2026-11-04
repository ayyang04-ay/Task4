# Phase 0 — input manifest. Task c2c052107551483abaacb5845479f32e (RLS pu3h8f5d), job 30f4652b

Mode: **GRADED** — writer-authored grading document present (`grader/grader_prompt.md`, A/B/C + Golden),
identical to `grading_config.json:grader_guidance` (only trailing-newline difference). Agentic grader,
single holistic score, no sub-items; A/B item ids must be assigned by FA, not read from the record.

| Row | Status | Detail |
|---|---|---|
| Run export located | PASS | Uploaded zip and `run data/Anton_...job_30f4652b_2026-10-14.zip` are the **same** export (byte-identical except README.md and grader_files_manifest.json, both metadata-only wording/field diffs). No second half exists. |
| Export complete | **FAIL (waiver needed)** | `export_selection.included = [transcripts, grading]`; `excluded = [outputs, task_files, grader_files]`. Both archives carry the identical selection, so `outputs/` (the graded `recommendation.md`) is **not in the bundle**. |
| Clusters present | PASS | No `_ERROR.txt`; transcripts 16/16, grading 16/16. `metadata.grading_transcript` is **null** in all 16 despite the README promising it. |
| Trajectory IDs | **BLOCKED** | Export labels: `attempt_NN_<8hex>`; `all_runs.json` carries full run uuids. Hub display form not known — must come from the writer, not be constructed. |
| Run count and status | PASS | 16/16 `completed`, `from_episode`; 0 refused; 0 truncated; 0 T&S. Scores 0.77–0.92, mean 0.8375. |
| Data room | PASS (substituted) | `task_files/` excluded from export, but the repo ships the shipped room: `data_room/{task_prompt.txt,dossier.md,registry_results.json,supplement.pdf}`. Transcript tool results show `/tmp/world/filesystem` sizes 5490 / 395410 / 11316320 — exact match to the repo bytes, so the room as the runs saw it is in hand. `supplement.pdf` sha256(first16) 637a9202fd30641e per validation_log. |
| Grading document | PASS | See above. |
| Reference solution | PASS | Golden Response is inside the grading document. No separate golden/answer-key file (grader_files excluded). |
| Stats availability | PASS (degraded) | `numpy 2.5.3` present; **`scipy` absent**. Mann-Whitney + BH to be hand-implemented if a panel test is needed. |

## Deliverable recovery (consequence of the outputs/ exclusion)

`outputs/attempt_NN_*/recommendation.md` does not exist in the export. Reconstructed from transcripts:

| Trajectory | Final-text route | Recovered bytes | Fidelity |
|---|---|---|---|
| attempt_03, 05, 06, 07, 08, 09, 11, 13, 15, 16 | `str_replace_based_edit_tool create` on `.../recommendation.md` | 26,936–41,892 | Full file as written at that call; later `sed`/python edits may follow |
| attempt_01, 04, 10, 12 | `create` on `recommendation_body.md` + a build script that concatenates body + generated tables | 20,345–30,821 | **Body only** — headers/ledger table appended at assembly |
| attempt_02 | `create` on `rec_body.md`, assembled by `cat rec_body.md evidence_register.md rec_files.md > recommendation.md` | 24,521 | **Body only** |
| attempt_14 | `create` on `part1_proposal.md` + `assemble.py` | 25,856 | **Part 1 only** |

All 16 then iterate with in-place python/`sed` edits after the create, so **no recovered text is guaranteed
to be the graded final state.** Citations must therefore anchor to transcript event positions
(`attempt_NN_<hex>` + event index in the flattened stream) or to verbatim strings, not to deliverable
line numbers.

## Blockers for the writer to clear before Phase 1

1. **Trajectory ID form** — verbatim as the Hub shows it.
2. **Waive or fix the `outputs/` gap** — either accept transcript-anchored citations, or re-export the job
   from Taiga with `outputs` (and ideally `task_files`, `grader_files`) selected.
3. **Scope** — fresh Phase 1 enumeration, or QC of findings already drafted.
4. **Status of `reviewer_data/pilot_analysis.md`** — it already contains a 7×A / 7×B prevalence matrix.
   It is written from grader rationales and its counts are approximations ("~14/16", "~15/16", "MET or
   near-MET"). Per the skill, rationale parsing is a screen only and fails in the direction of inventing
   penalties, so every cell needs reading before it can carry a prevalence claim. Treat it as the writer's
   prior hypothesis to verify, or as replaceable?

## Pre-existing material that constrains the FA (read, not yet verified)

- `reviewer_data/pilot_analysis.md`, `NEXT_SESSION_BRIEF.md`, `problem_card.md`, `validation_log.md`.
- `run data/qa_report_pu3h8f5d_v1_fb819df4.zip` — Taiga QA, 16 findings over 6 runs. It cites 10 of the
  16 panel trajectories by short id (01,02,03,04,05,06,07,08,09,10 → cd3e5696, b73e9851, 890bbf23,
  0842f297, b07ef105, 1f19cd35, 06a4976d, f9779a6c, 9687c0b1, ef72c97f); attempts 11–16 are never cited.
  Three of its findings bear directly on what may be called a model error:
  - Golden point 6's r-values (GBP5 r≈0.86 etc.) cite 19 pages (S24–S26, S43–S58) that are **absent from
    the mounted PDF**; the golden submitted as a deliverable scored **0.78**, below the panel mean.
  - The A3 dose-sparing item rests on a cross-subtype (H3N2v, 15 µg) comparator the golden itself rejects;
    9 of 10 QA-sampled runs were docked for declining it.
  - The B5 cross-dose DE-count item's refuting fact is undercut by the registry's own Day-29 ≈ 0 DE counts
    and its common-baseline cytokine fold changes; graders split on applying it.
