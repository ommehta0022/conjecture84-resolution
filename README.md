# Resolution of Graffiti.pc Conjecture 84: A Sharp Universal Lower Bound for Maximum Induced Trees in Connected Graphs

[![DOI](https://img.shields.io/badge/DOI-10.17605%2FOSF.IO%2F9RXS7-blue)](https://doi.org/10.17605/OSF.IO/9RXS7)
[![DeepMind PR](https://img.shields.io/badge/DeepMind%20Benchmark-PR%20%237669-success)](https://github.com/google-deepmind/formal-conjectures/pull/7669)
[![License: Apache 2.0](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

**Author:** Om Atul Mehta  
**Permanent DOI:** [10.17605/OSF.IO/9RXS7](https://doi.org/10.17605/OSF.IO/9RXS7)  
**OSF Project:** [https://osf.io/9rxs7/](https://osf.io/9rxs7/)  
**Formal Conjectures Benchmark PR:** [google-deepmind/formal-conjectures #7669](https://github.com/google-deepmind/formal-conjectures/pull/7669)

---

## Abstract
We present the first complete analytical proof and machine verification of Conjecture 84 from Ermelinda DeLaViña's *Written on the Wall II* (WOWII #84, status O), tracked as an open research benchmark in Google DeepMind's `formal-conjectures` repository:

$$\operatorname{tree}(G) \ge \frac{2 \operatorname{rad}(G)}{\delta(G)}$$

where $\operatorname{tree}(G)$ is the maximum order of an induced subtree, $\operatorname{rad}(G)$ is the metric radius, and $\delta(G)$ is the minimum degree. 

We prove that the inequality holds universally across all simple connected finite graphs:
1. **Regime 1 ($\delta(G) \ge 2$):** Diametrical shortest paths are chordless, yielding $\operatorname{tree}(G) \ge \operatorname{diam}(G) + 1 \ge \operatorname{rad}(G) + 1 > \frac{2 \operatorname{rad}(G)}{\delta(G)}$ with a universal positive margin $\ge 1$.
2. **Regime 2 ($\delta(G) = 1$):** Reduces to $\operatorname{tree}(G) \ge 2 \operatorname{rad}(G)$. For $\operatorname{diam} \ge 2 \operatorname{rad} - 1$, diametrical shortest paths satisfy the bound; for $\operatorname{diam} \le 2 \operatorname{rad} - 2$, the leaf's neighbor is forced to be a central vertex, and appending the leaf to the Erdős–Saks–Sós (1986) induced subtree extends its order by $+1$ with zero cycles.
3. **Sharpness:** The constant $2$ is exact and unimprovable: the family of cycle-leaf graphs $C_{2k} + \text{leaf}$ ($k \ge 2$) achieves exact equality with zero residual ($0.00$ error).

---

## Repository Contents
- [`paper.tex`](paper.tex): Complete publication-grade LaTeX manuscript formatted with AMS/SIAM environments.
- [`Conjecture84_Theorem.lean`](Conjecture84_Theorem.lean): Formal Lean 4 module resolving `WrittenOnTheWallII/GraphConjecture84.lean`.
- [`verify_conjecture84.py`](verify_conjecture84.py): Python/SymPy/NetworkX test suite exhaustively verifying all 995 graphs in the Read & Wilson Graph Atlas (0 counterexamples).
- [`RESEARCH_DISCOVERY_REPORT.md`](RESEARCH_DISCOVERY_REPORT.md): Comprehensive mathematical report and proof breakdown.
- [`conjecture84_submission_package.zip`](conjecture84_submission_package.zip): Bundled archive for journal and preprint submission.

---

## Citation
```bibtex
@article{mehta2026conjecture84,
  title={Resolution of Graffiti.pc Conjecture 84: A Sharp Universal Lower Bound for Maximum Induced Trees in Connected Graphs},
  author={Mehta, Om Atul},
  year={2026},
  doi={10.17605/OSF.IO/9RXS7},
  url={https://doi.org/10.17605/OSF.IO/9RXS7},
  note={Google DeepMind formal-conjectures PR \#7669}
}
```
