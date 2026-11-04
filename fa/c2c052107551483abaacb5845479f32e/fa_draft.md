# FA draft v5 — H7N9 next-work recommendation, job 30f4652b (16 × Opus 5.5)

RETYPE, DO NOT TRANSCRIBE.
SCOPE: model conduct only, load-bearing failures only, anchored on the weakest runs — 03 (890bbf23) and
05 (b07ef105), both 0.77 — and the median pair, 09 (9687c0b1) and 11 (60c1bbbc), both 0.84.
CUT BY INSTRUCTION as immaterial, retained in error_modes.md: comparator-arm keratin/hornerin never
characterised (13/16, never misused); "time to protection" treated as measurable (4/16); run 12's
antigen-sparing over-claim (1/16). Grading-document findings stay in calibration.md, unreferenced here.
Counts: paragraph 1 = 14 sentences, paragraph 2 = 10 sentences.

## What did the model do wrong?

All sixteen runs get the main call right. Each carries forward the AS03-adjuvanted two-dose regimen rather than
the antigen on its own, and each flags durability and breadth as open questions. The failure is narrower, and it
turns up almost everywhere: fifteen of sixteen never say that this trial measured protection at all. A6 asks for
two things — don't turn the interferon signature into a protection marker, and say that nothing in the record is a
protection endpoint. Every run does the first. Only run 16 (9993e8bb) does the second, and it buries the line in a
set-aside table instead of putting it where it discusses the gaps. The two weakest runs, 03 (890bbf23) and 05
(b07ef105), say nothing of the kind. The median pair splits: 09 (9687c0b1) also says nothing, while 11 (60c1bbbc)
says only that no correlate of protection has been established, which is a point about how to read a titre rather
than about what the study measured. All of these proposals then ask for a bridging or correlate study, and in
fifteen of sixteen that request has nothing underneath it. The second problem is about workings rather than
answers. Thirteen of sixteen set the dose-1 and dose-2 gene counts side by side without mentioning that the two
are measured against different baselines, though the room says so twice — in `dossier.md` §6 and again in the
registry's own description of the gene-count measure. Their conclusion holds up: the innate response really is
bigger after dose 2, and all sixteen quote the IP-10 rise of 4.461 against 1.867, which does sit on one common
baseline. What matters is where the claim ends up — run 03 uses it at line 137 to argue that dose-2 reactogenicity
needs measuring directly, and run 05 at line 231 to conclude that dose 2 is unlikely to be gentler. So in both of
the weakest runs a design call and a deployment call rest on a step the run never justified, and only 04, 09 and
14 mention the baseline rule anywhere.

## What should the model have done?

Run 16 (9993e8bb) shows what the first item needed, and run 14 (f8782a66) shows what the second needed. On A6 the
line to write is a plain one: all fifteen outcome measures in the registry are serology, cytokines or gene counts,
not one of them measures protection, efficacy or challenge, and that gap — not the shakiness of any single titre —
is what a bridging study would be for. It belongs in the section on where the data fall short, which 03, 05, 09
and 11 all have, rather than in a table at the back. Every run already behaved as though it knew this, so writing
it down is what turns the caution into a finding, and it is what justifies the correlate study each of them goes on
to propose. On the gene counts, run 14 does the whole job in one sentence: it names the two baselines, points out
that the dose-2 convention would if anything find fewer genes, and backs the direction with cytokine fold changes
measured from a single baseline. Run 09 makes a neater version of the same point, that dose 1 had two baseline
draws behind it and so had more statistical power rather than less. The registry settles it either way. Measured
against the first-dose baseline, Day 29 shows eleven differentially expressed genes across all six cell types,
against 3,024 on Day 2, so the Day-29 reference is effectively pre-vaccination. One sentence of that would have
left the conclusion standing and given the calls in 03 and 05 something to stand on. The rest was already right
everywhere: the adjuvanted regimen as the asset, the Day-29 one-dose HAI GMT of 7.3 read as sub-protective,
durability and breadth named as open, and every figure tied to its source alongside a reasoned set-aside list.
