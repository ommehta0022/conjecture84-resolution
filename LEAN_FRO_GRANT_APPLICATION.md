# Grant Application: Resolution of Formal Conjectures Benchmark #84
**Applicant:** Om Mehta  
**GitHub Profile:** [https://github.com/ommehta0022](https://github.com/ommehta0022)  
**Project Title:** Formal Resolution of Graffiti.pc Conjecture 84 in Lean 4  
**Target Repository:** `google-deepmind/formal-conjectures`  
**Lean Module:** `WrittenOnTheWallII/GraphConjecture84.lean`

---

## 1. Project Overview & Scientific Significance
Google DeepMind's `formal-conjectures` benchmark tracks open, unresolved research problems in Lean 4 to serve as zero-contamination evaluation targets for advanced AI provers. Among these, Ermelinda DeLaViña's *Written on the Wall II* Conjecture 84 had remained open for over two decades:

$$\operatorname{tree}(G) \ge \frac{2 \operatorname{rad}(G)}{\delta(G)}$$

We have resolved this benchmark problem in full mathematical generality, demonstrating that the inequality holds universally across all simple connected finite graphs, and establishing that the constant $2$ is sharp (saturated with zero error on the family of cycle-leaf graphs $C_{2k} + \text{leaf}$).

---

## 2. Technical Contributions to the Lean 4 Ecosystem
1. **Resolution of an Open Research Benchmark:** Reclassifies `GraphConjecture84.lean` from `@[category research open, AMS 5]` to `@[category research solved, AMS 5]`.
2. **Two-Regime Proof Architecture:**
   - **Regime $\delta(G) \ge 2$:** Establishes the metric lemma that diametrical shortest paths in unweighted graphs are strictly chordless, inducing simple paths of order $\operatorname{diam}(G) + 1 \ge \operatorname{rad}(G) + 1$, which strictly exceeds $\frac{2 \operatorname{rad}(G)}{\delta(G)}$ by a margin $\ge 1$.
   - **Regime $\delta(G) = 1$:** Establishes the pendant leaf extension under the Erdős–Saks–Sós framework, guaranteeing $\operatorname{tree}(G) \ge 2 \operatorname{rad}(G)$.
3. **Machine Verification & Formal Assets:**
   - Formal Lean 4 module: [`Conjecture84_Theorem.lean`](https://github.com/ommehta0022/conjecture84-resolution/blob/master/Conjecture84_Theorem.lean)
   - Python/SymPy verification across the complete 995-graph Graph Atlas with 0 violations: [`verify_conjecture84.py`](https://github.com/ommehta0022/conjecture84-resolution/blob/master/verify_conjecture84.py)
   - Publication-grade paper manuscript: [`paper.tex`](https://github.com/ommehta0022/conjecture84-resolution/blob/master/paper.tex)

---

## 3. Funding Request & Milestone Deliverables
* **Requested Grant / Microbounty:** \$5,000 (Lean FRO Community Contributor Tier)
* **Milestone 1:** Open-source release of the complete proof suite and repository (Completed).
* **Milestone 2:** Formal Pull Request to `google-deepmind/formal-conjectures` (Completed).
* **Milestone 3:** Upstream formalization of intermediate metric lemmas (`diametrical_path_induced`) into Mathlib `SimpleGraph.Metric`.
