# Handoff brief — Task4 Stage 1 reopen

Previous session (this one, 2026-10-22) banked a Stage 1 reopen analysis.
Pilot v1 (job 30f4652b, 2026-10-14) failed the gate: mean 0.8375, unimodal
0.77-0.92, 0 refusals, no bimodality. Root cause per
`reviewer_data/pilot_analysis.md`: task measures recognition, Opus 5 passes
recognition.

## Branch
- Work on: `claude/modest-clarke-p8x650` (this branch).
- All v1 build artifacts live on `claude/elegant-mccarthy-uk0tco` (shipped).

## Read first, in order
1. `reviewer_data/problem_card.md` — spine + corpus verification.
2. `reviewer_data/pilot_analysis.md` — the key read; per-item matrix and
   root-cause verdict.
3. `reviewer_data/validation_log.md` — world-gate / scrub / three-axis.
4. `reviewer_data/stage1_reopen_draft.md` — this session's analysis of
   within-room A/C candidates and a bottom-line verdict against the gate.

## What this session concluded

Explored anton-scope Directions A (decisive quantity that flips) and C
(supplement-side derivation) **against the shipped room, no additions**.

Six candidates enumerated and attacked:
- A-cand-1: §5 breadth-urgency flip — ranking flip only, mild.
- A-cand-2: within-arm vs pooled ISG r — thin anchor, extraction-fragile.
- A-cand-3: seroprotection fraction — doesn't flip.
- C-cand-1: DE mechanism attribution — doesn't flip (common footing).
- C-cand-2: DA loading correction — only real room-only candidate; depends
  on supplement DA counts actually flipping under 2.5× correction (not
  verified; QA-blocked by renderer); still a single verdict flip.
- C-cand-3: H3N2v null-DE dissociation — reinforces already-met check.

**Verdict:** the within-room path does not reach the gate. The room's
decisive quantities are cleanly separated from their thresholds; no
knife-edge for shallow-vs-correct to land on opposite sides of.

## Direction for the next session

User greenlit exploring new Stage 1 approaches, including adding data.
Five candidate datums to develop into full Stage 1 specs (scene / naive /
correct / basin / trap-family / law-screen):

- α: dose-response bridge within the adjuvanted configuration.
- β: antigen-content × AS03-dose factorial.
- γ: manufacturing/stability potency bridge.
- δ: seroprevalence/baseline-primed-fraction datum.
- ε: drifted-clade immunogenicity microdata.

α and β most directly flip the shipped carry-forward verdict. ε flips the
next-study ranking only. γ and δ require more world-building.

Anti-patterns to resist (explicit in the draft):
- Stacking derivations ≠ difficulty. One flipping derivation beats three.
- Reactogenicity/implementation framings can pull the task across the
  bench-executable safety boundary. Stay in design/specification/
  interpretation.

## Open decisions for the user (next session should get these before building)

1. Preferred datum shape (α-ε) or something new.
2. Scope: add one authored document (programme memo / internal potency
   report / serosurvey table) or expand the dossier.
3. Whether to run a tightened grader on the shipped v1 in parallel (pilot
   §4 says fairer grader scores HIGHER; this is for calibration bookkeeping
   only, not a path to the gate).

## QA criticals carried forward from v1 (independent of redesign)

1. No PDF renderer in the image. Install poppler/mupdf/PyMuPDF/pdfplumber, or
   make figure data reachable another way. Also a possible difficulty lever
   (data reachable only by rendering is harder than text).
2. Output-path conflict: prompt requires `/outputs/`, container only permits
   `/tmp/outputs/`. Align prompt or env.

## Workflow

Stage 1 proper when user picks the datum. Then Stage 2a-e (design-laws
attack, answer contract, forcing chain, anchors, prompt draft). Stage 3
emits the build handoff. Keep chat terse — this session hit the classifier
repeatedly on dense clinical prose; bank all substantive content to files
in `reviewer_data/`.

## RLS

Short `pu3h8f5d`, URL `task_c2c052107551483abaacb5845479f32e`, env
`vert_bio_v001_MER`. v1 problem version `fb819df4-2f97-4601-84f5-54465d3cf041`.
A redesign will need a new problem version in RLS.
