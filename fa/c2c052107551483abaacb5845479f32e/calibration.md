# Phase 5 — calibration notes (not FA material; panel/task quality)

1. **Nothing discriminates.** Five of seven A items are met 16/16 and six of seven B traps never fire. The whole
   0.77–0.92 spread rests on B5 (a defective item), A3 (a defective item) and A6 (an articulation ask). A fairer
   grader scores this panel *higher*, so grader tightening cannot move the mean toward the ≤0.55 gate. This
   agrees with `pilot_analysis.md` §4 and §7 on the conclusion, and corrects it on B5: that document treats B5 as
   the one real trap; it is not.

2. **B5 should be withdrawn or rewritten, not narrowed by direction.** The refuting fact the item names is
   neutralised by the room itself (Day 29 ≈ pre-vaccination: 11 DE genes vs 3,024; cytokine fold changes on a
   common pre-vaccination baseline rising 1.867 → 4.461). Rewriting it to cover "larger after dose 2" would
   penalise a conclusion that is correct and corroborated. The defensible residue is an item about *discharging a
   stated convention*, which only 3 of 16 did — i.e. grade the basis, not the direction.

3. **A3 is not derivable from the room.** Only 15 µg arm is A/H3N2v; both H7N9 arms are 3.75 µg; no H7N9
   dose-ranging exists. Keep the item as "AS03 is necessary at 3.75 µg" and accept, or credit, an attempt that
   declines the cross-subtype dose comparison.

4. **The Golden cites values the room cannot produce.** Golden point 6's r-values (GBP5 r≈0.86, IFIT r≈0.84,
   PSME2 r≈0.78, MHC-I r≥0.74) are sourced to figures S43–S58, which multiple attempts established are absent
   from the mounted PDF. Per Taiga's env linter the Golden submitted as a deliverable scored **0.78**, below the
   panel mean, docked for fabricated coefficients. A reference solution that loses points under its own guidance
   is a blocking defect for calibration.

5. **A genuine room inconsistency the panel found and the grading document does not mention.** `dossier.md` §6
   says the first-dose baseline is the **mean** of the Day −7 and Day 1 draws; the registry OM2 description says
   **"combined summed read counts"** for the same two draws. Attempt 10 (ef72c97f) flags it at
   `recommendation.md:350`. Mean and sum are not the same reference frame. Confirmed [computed] against both files.

6. **Two environment defects, both prevalent, neither a model failure** (per the skill, tooling friction is weak FA
   material and indicates a task defect): no PDF rasteriser anywhere in the image, so every run hand-wrote a
   200–400-line content-stream interpreter before any analysis; and the prompt requires `/outputs/` (plus a stray
   `$/outputs/$`) which uid 1000 cannot create, so all 16 wrote to `/tmp/outputs/` and disclosed the substitution.
   Difficulty must live in the problem, not the tooling.

7. **Panel homogeneity.** 16/16 put a labelled lead recommendation on line 1 carrying the adjuvanted two-dose
   regimen; 16/16 cite the IP-10 4.46 figure; 16/16 reject the H3N2v benchmark and the 1.4× cross-antigen reading.
   This is a recognition panel, which is `pilot_analysis.md`'s own root-cause finding and remains correct.
