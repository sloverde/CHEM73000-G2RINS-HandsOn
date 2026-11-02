# Hands-on G²RINS for Polymer Chemistry

A beginner-friendly Google Colab notebook that accompanies the guest lecture
**"How to Make Polymers Machine-Readable: An Introduction to G²RINS"** by **Dr. Gervasio Zaldivar** (de Pablo Lab, NYU),
given in **CHEM 73000 Polymer Chemistry (Part 2), CUNY**, on November 3, 2026.

No Python or Colab experience is needed: students run cells and change a few numbers.

## Open the notebook

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/sloverde/CHEM73000-G2RINS-HandsOn/blob/main/G2RINS_HandsOn.ipynb)

Click the badge above. Or, in [Google Colab](https://colab.research.google.com), choose
**File → Open notebook → GitHub** and paste the address of this repository.
To keep your own copy, use **File → Save a copy in Drive**.

## What students do (about 30 minutes)

| Activity | Topic | Course connection |
|---|---|---|
| 0 | How to run a notebook | |
| 1 | Write polystyrene in G²RINS, draw its generative graph and one chain | Polymer structure |
| 2 | Generate 200 chains; compute M<sub>n</sub>, M<sub>w</sub>, Đ; compare distributions | Molecular weight (Lecture 4) |
| 3 | The EO/PO copolymer from the preprint (Figures 1 and 3) | Chain copolymerization |
| 4 | Random, blocky and alternating copolymers | Reactivity ratios, block copolymers |
| ⭐ | A glycerol-initiated three-arm star | Polymer architecture |

## Files

| File | Purpose |
|---|---|
| `G2RINS_HandsOn.ipynb` | The student notebook |
| `INSTRUCTOR_NOTES.md` | Timing, answers to the in-notebook questions, and troubleshooting |

## Credits

* The notebook uses the **G²RINS** Python package (v1.0.0) by the de Pablo group: <https://github.com/depablolab/g2rins>.
  Its full user guide, with 12 worked examples, is `G2RINS_guide.ipynb` in that repository.
* Paper: G. Zaldivar, Y. Tian, G. Sun, C. Kappatou, P. Eiden, N. B. Wulkow, V. Settels, J. J. de Pablo,
  *G2RINS: A Generative String-and-Graph Polymer Representation to Assist Computational Materials Discovery*,
  ChemRxiv (2026). [doi:10.26434/chemrxiv.15007504/v1](https://doi.org/10.26434/chemrxiv.15007504/v1)
* Teaching materials prepared by Prof. Sharon Loverde, College of Staten Island / CUNY Graduate Center.

## License

Released under the GNU General Public License v3.0 (see `LICENSE`), the same license as the G²RINS package it builds on.
