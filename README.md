# NP-Completeness: Complexity Theory and Polynomial-Time Reductions

An academic report examining NP-completeness, the complexity classes **P** and **NP**, and how polynomial-time reductions establish computational hardness. Prepared for an Algorithms course at CUNY, based primarily on Chapter 34 of *Introduction to Algorithms* (CLRS).

## Report

**[Read the full NP-Completeness report](ANGEL_CORONEL_ALGO_REPORT.pdf)**

The five-page report develops the foundations of NP-completeness and presents a proof that **CLIQUE is NP-complete** using a reduction from **3SAT**.

## Topics Covered

- **Decision problems and tractability:** Why complexity theory studies yes/no questions and uses polynomial running time as a standard of efficiency.
- **P and NP:** Polynomial-time decision algorithms, verifiers, and polynomial-size certificates.
- **NP-hardness and NP-completeness:** Formal definitions and the role of reductions in transferring hardness.
- **Canonical NP-complete problems:** CIRCUIT-SAT, SAT, and 3-CNF-SAT.
- **Proof by reduction:** Showing that `3SAT <=p CLIQUE` while establishing `CLIQUE` membership in NP.
- **Algorithm design implications:** Why approximation, heuristics, and tractable special cases matter when exact polynomial-time algorithms are not known.

## Central Proof: 3SAT to CLIQUE

The report explains a standard NP-completeness proof for the CLIQUE decision problem:

1. **Membership in NP:** A proposed clique of size `k` can be verified in polynomial time by checking its size and the edges among all selected vertices.
2. **Polynomial-time construction:** Given a 3-CNF formula with `k` clauses, construct a graph with a vertex for every literal occurrence. Connect vertices from *different* clauses when their literals are not contradictory.
3. **Correctness:** The formula is satisfiable **if and only if** the resulting graph contains a clique of size `k`.
4. **Conclusion:** Because 3SAT is NP-complete and reduces to CLIQUE in polynomial time, and CLIQUE belongs to NP, CLIQUE is NP-complete.

This proof is an exposition of an established result, **not a claim of a new complexity-theory discovery**.

## Repository Contents

The repository documents a written mathematical analysis; it does not include a CLIQUE solver, experimental benchmarks, or an implemented reduction.

## Reference

Cormen, T. H., Leiserson, C. E., Rivest, R. L., & Stein, C. (2009). *Introduction to Algorithms* (3rd ed.), Chapter 34: NP-Completeness. MIT Press.

## Author

Angel Coronel  
Algorithms — CUNY
