# Instructor notes: Hands-on G²RINS

## Before class

* Open the notebook in Colab once yourself and run it top to bottom (about 3 minutes, mostly the install cell).
* Share the "Open in Colab" link from the README with students (Brightspace or the Zoom chat).
* Tested with `g2rins` v1.0.0 (pinned in the install cell) and Python 3.12–3.13.

## Suggested timing (about 30 minutes)

| Minutes | Section |
|---|---|
| 0–5 | Sections 0–2: open Colab, run the test cell, install, load helpers |
| 5–10 | Activity 1: polystyrene string, generative graph, one chain |
| 10–17 | Activity 2: ensemble, M<sub>n</sub>, M<sub>w</sub>, Đ; students try the three distributions |
| 17–24 | Activity 3: EO/PO copolymer from Figures 1 and 3; change the composition |
| 24–30 | Activity 4: random, blocky and alternating sequences; wrap-up questions |
| optional | Bonus: PEG-*b*-PMMA diblock (macroinitiator) |

Start the install cell (Section 1) while Dr. Zaldivar is still introducing G²RINS, so that it is finished when the hands-on part begins.

## Answers to the in-notebook questions

**1.1** A styrene unit is 104 g/mol, so a 1000 g/mol chain has 1000/104 ≈ 9–10 units (the two H end groups add only 2 g/mol).

**2.1** `schulz_zimm(10000, 5000)` gives Đ ≈ 2, typical of step-growth polymerization (most-probable distribution) or conventional free-radical
polymerization. `log_normal(5000, 1.05)` and `poisson(3000)` are narrow, as in living anionic polymerization.

**2.2** 200 chains is a small random sample, so the histogram fluctuates around the target. With 2000 chains it follows the target curve much more
closely (statistical noise decreases roughly as 1/√N). The same idea applies to the size of a molecular-dynamics simulation box.

**3.1** Average repeat-unit mass = 0.8(44.05) + 0.2(58.08) = 46.9 g/mol. The end groups (CH<sub>3</sub>O– and –H) add about 32 g/mol, so a
1400 g/mol chain contains about (1400 − 32)/46.9 ≈ 29 repeat units.

**4.1** The blocky copolymer: long EO runs are hydrophilic and long PO runs are more hydrophobic, so blocky EO/PO chains are amphiphilic and
can form micelles, like the Pluronic PEO–PPO–PEO surfactants. Random and alternating chains have no separate hydrophobic block.

**4.2** No. The initiator can attach to either repeat unit with equal weight, so the first unit is E or P at random. After that, the
alternating weights force every next unit to be the other kind.

**B.1** The first histogram (target `gauss(3500, 1000)`, M<sub>n</sub> ≈ 3,500 g/mol) is the **whole diblock chain**: the outer distribution
sets the total molecular weight. The second (target `gauss(1500, 300)`, M<sub>n</sub> ≈ 1,500 g/mol) is the **PEG block** (with its CH<sub>3</sub>O– end),
the inner stochastic object that acts as the macroinitiator. (Tested: 400 chains gave M<sub>n</sub> = 3,470 and 1,490 g/mol.)

**B.2** PMMA block ≈ 3,500 − 1,500 ≈ 2,000 g/mol, i.e. about 2,000/100.1 ≈ 20 MMA units. Good students will note this is an average:
the two block lengths fluctuate independently, so individual chains vary.

## Troubleshooting

| Problem | Fix |
|---|---|
| "Warning: This notebook was not authored by Google" | Click **Run anyway**. |
| `NameError: name 'show_graph' is not defined` | The helper cell (Section 2) was not run. Run it, then rerun the cell. |
| `ModuleNotFoundError: No module named 'g2rins'` | The install cell (Section 1) was not run or the session restarted. Run Sections 1 and 2 again. |
| A cell runs for a long time | Large molecular weights take longer. Wait, or use **Runtime → Interrupt execution** and choose a smaller value. |
| Anything else | **Runtime → Restart session**, then run all cells from the top. |
| A typo in a G²RINS string | The error message usually points to the position of the problem. Copy the original string back from the notebook. |
