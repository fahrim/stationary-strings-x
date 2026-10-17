# Stationary Strings Theorem X — Publication Package (Series Capstone)

> **Türkçe:** [README_TR.md](./README_TR.md)

**Stationary Strings Theorem X: Tokamak H-Mode and ELM Suppression, Runaway Electron-Positron Avalanche Quench, and the 30-Decade Universal Vortex-String Scaling Law**

Author: Fahri Meral · Date: October 17, 2026 · Version: v1 (Paper X)

> **Status:** Unpublished preprint (v1). Not peer-reviewed.

## Contents

| File | Description |
|---|---|
| `paper/duran_sicimler_teoremi_X.tex` | Main paper, Turkish (Tables 1–4, Figure 1 2×2) |
| `paper/duran_sicimler_teoremi_X_EN.tex` | English version |
| `figs/fig12_tokamak_elm_runaway_and_universal_scaling.pdf` | Tests T26–T28 figure (TR, 2×2) |
| `figs/fig12_tokamak_elm_runaway_and_universal_scaling.png` | Tests T26–T28 figure preview (TR) |
| `figs/fig12_tokamak_elm_runaway_and_universal_scaling_en.pdf` | Tests T26–T28 figure (EN, 2×2) |
| `figs/fig12_tokamak_elm_runaway_and_universal_scaling_en.png` | Tests T26–T28 figure preview (EN) |
| `CITATION.cff` | Citation record |
| `LICENSE` | MIT |

## Numerical reproduction

Tests T26–T28 are produced with the solver in the **Paper V repository**
([`stationary-strings-v`](https://github.com/fahrim/stationary-strings-v)):

```bash
git clone https://github.com/fahrim/stationary-strings-v
pip install numpy scipy matplotlib
python duran_sicimler_sim/solver_engine.py   # T1–T28 (28/28 PASS)
python duran_sicimler_sim/mini_check_x.py    # independent cross-check (15/15 PASS)
python duran_sicimler_sim/generate_figures.py  # Figure 1 (+_en)
```

The independent cross-check never imports the solver.

## Key findings

- T26 (Theorem X.1): FENE-P RMP Super-Peeling-Ballooning limit (`1.970942×` at `χ=0.75`),
  bounded ELM filament oscillation at `α_MHD = 1.5 α_crit^std`, and `H_98^string = 3.1560` (`χ=0.50`) / `5.5516` (`χ=0.75`) carrying ITER and SPARC into ignition.
- T27 (Theorem X.2): Chiral-elastic critical field enhancement `E_c^eff/E_c = S_loss(1+4Σ_string) = 23.788450` (`χ=0`) and `38.928355` (`χ=0.75`), quenching `E_||/E_c = 30` disruption runaway avalanches (`γ_RA^std = +33.5550 /s → γ_RA^string = −0.2654 /s < 0`).
- T28 (Theorem X.3): Scale-independent invariants `Π_Meral = µ_s^Meral = 0.2044088237` and `I_shield = 2√2`, with unit-slope (`m = 1.000000000000000`, `R^2 = 1.0`) universal scaling across 30 orders of magnitude (`10^-10 m → 3×10^20 m`).

## License

MIT — see `LICENSE`. Content is not peer-reviewed.
