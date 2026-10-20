# Handoff brief — Anton Task 4 (H7N9 next-work recommendation)

Previous session kept hitting a Trust & Safety classifier on dense clinical
prose in chat; all build work was done via files + Bash and is committed. Start
fresh. **Keep chat terse; write substantive content to files, not inline.**

## Repo / branch
- Branch: `claude/elegant-mccarthy-uk0tco` (all work here; prior `nice-cori-69c2j3`
  never committed).
- Read first: `reviewer_data/problem_card.md` (locked spine + corpus verification),
  `reviewer_data/validation_log.md` (world-gate/scrub/statics/3-axis),
  `reviewer_data/pilot_analysis.md` (full pilot read — the key document now).
- RLS: short `pu3h8f5d`, URL `task_c2c052107551483abaacb5845479f32e`,
  problem version `fb819df4-2f97-4601-84f5-54465d3cf041`, env `vert_bio_v001_MER`.

## What is built and shipped
- `data_room/`: task_prompt.txt, dossier.md, registry_results.json (trimmed+
  scrubbed NCT02921997), supplement.pdf (1014 pp verbatim).
- `grader/grader_prompt.md`: five-section grader + Golden, flat lines.
- `run data/`: the pilot export (job 30f4652b) and the Taiga QA report.

## Pilot verdict (job 30f4652b, 16 × Opus 5.5)
**Mean 0.8375, range 0.77–0.92, 0 refusals, gate ≤0.55 NOT cleared.** Unimodal,
tight, high — the too-easy/failing-high panel. All 7 load-bearing A items met
16/16; 6 of 7 B traps never fire; the only trap that bites (cross-dose DE
comparison) is graded minor. The model out-performs the Golden on the signature
item (finds Table S186 pools both arms → confounded by AS03 receipt; finds
figures S43–S58 absent). See `pilot_analysis.md` for the full per-item matrix.

**Root cause: the task measures recognition, which Opus 5.5 passes. It has no
hidden basin the model falls into. Grader tightening cannot fix it — two of the
three current deductions (A3 cross-subtype dose reference, A6 explicitness) are
grader-fairness artifacts; a fairer grader scores HIGHER.** Reaching ≤0.55 needs
a Stage 1/2 design reopen around a genuine **derivation** with an uncued, mounted
correcting fact — most likely by adding one decisive datum the room lacks.

## Two QA criticals to fix regardless of the redesign
1. **No PDF renderer in the image** (`severe_missing_pdf_rendering_dependencies`).
   The supplement's key serology figures are vector Form XObjects not recoverable
   by text extraction, and the image has no poppler/mupdf/ghostscript/PyMuPDF/
   pdfplumber, no pip, no network. Every run hand-rolled a 200–400-line content-
   stream interpreter before any analysis. Either install a PDF toolchain in the
   env, or make the figure data reachable another way. NB: this is also a possible
   derivation lever — data reachable only by rendering is harder than text.
2. **Output-path conflict** (`severe_output_path_permission_mismatch`). Prompt
   requires `/outputs/`; container only permits `/tmp/outputs/`. Graders accepted
   the fallback, but align the prompt to the real writable path (or fix the env).

(Ignore the other ClaudeScope items per the owner.)

## Recommended next move
Decide with the owner: (a) reopen the basin for a derivation-based hidden basin
(the only path to the gate with Opus 5.5), or (b) hold. Do NOT ship v1 — it fails
the gate by a wide margin. Do NOT try to tune the grader to the gate; it is the
wrong instrument here and would be unfair.
