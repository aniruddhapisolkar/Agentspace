# Review evidence — Multivariable Taylor Expansions

Batch: `20261126T193918Z-01`
Slug: `multivariable-taylor-expansions`
Article: `multivariable-calculus/multivariable-taylor-expansions.md`
Reviewed revision (pre-commit): `deffa8331f3e28f23383b89340111e880ec9c648`
Reviewer: Reviewer (AI), 2026-11-26

## Scope and coverage

- Upstream duplicate check: no multivariable Taylor article found in `antoniolupetti/algebrica` (searched). Not a duplicate.
- Covers multi-index notation, first/second/general Taylor theorems, practical computation, error bounds, non-analytic smooth example, critical-point classification.
- Three figures: section along h=(1,1) of e^{x+y}; flat-bottomed crater for e^{-1/(x^2+y^2)}; level curves of quadratic forms.

## Sources and actual checks

- Toronto MAT237 notes cited for Peano form; one-variable Taylor theorem standard.
- Independent derivative checks for e^x cos y, polynomial x^2 y + y^3, sqrt(1+x+y), e^{x+y} error bound (recorded in article).
- Python arithmetic verified coefficients: f_{xyy}=-1 gives -1/2 for xy^2 term; Hessian entries for sqrt example; Lagrange bound 1.63e-3 vs actual 1.40e-3.
- SVG structural validation: all 3 files parse as XML; Chrome headless rendered all 3 to PNG without error.

## Claim-by-claim proof audit

- Multi-index definitions and counts: C(n+k-1,k) and C(n+k,k); for n=2,k=2 gives 6. PASS.
- First-order expansion (1) and gradient extraction by h=te_i: valid. PASS.
- Second-order formula (2) with Lagrange remainder via phi(t)=f(a+th): chain rule derivatives correct; one-variable Taylor applied on [0,1] valid. PASS.
- Coordinate expansion with factor 2 in mixed term: Hessian symmetry justifies. PASS.
- General Peano (3) and Lagrange (4) forms: hypotheses C^k vs C^{k+1} distinguished; induction proof for derivative formula coefficient (j+1)!/beta! verified using sum beta_i=j+1. PASS.
- Uniqueness of Taylor polynomial: stated, standard. PASS.
- Practical computation by series multiplication: e^x cos y to order 3 verified by derivatives. PASS.
- Polynomial example remainder h^2 k + k^3 = o(||h||^2): degree 3, yes. PASS.
- sqrt example Hessian matches quadratic terms. PASS.
- e^{x+y} error bound: |R2| <= (0.2)^3/6 e^{0.2} = 1.63e-3; actual 1.40e-3. PASS.
- Non-analytic example: e^{-1/(x^2+y^2)} with f(0,0)=0 has all partial derivatives zero at origin; Taylor series zero; function positive elsewhere. Correct. Article caption "rising from a flat point at the origin" accurate. PASS.
- Critical-point classification by Hessian definiteness: standard second-derivative test. PASS.

## Edge cases / counterexamples attempted

- Attempted to find a defect in Peano hypothesis: article correctly notes Peano requires only k differentiability; C^k is sufficient. PASS.
- Checked "bump" wording: original brief's "bump peaked at origin" was wrong; figure and article text (after correction) say flat at origin, rising away. Corrected one phrase "bump near the origin" -> "rise of the function away from the origin".

## Editorial audit

- Front matter present; H2-only; `$$`/`$` delimiters; British spellings. PASS.
- Links to partial-derivatives and tangent-planes (unpublished sibling) disclosed. PASS.
- Figure 2 wording corrected as above.

## Per-figure geometry and render checks

- F1: section along h=(1,1) of e^{x+y} with tangent line and second-order parabola. SVG valid; render succeeded (9168 bytes).
- F2: flat-bottomed crater for e^{-1/(x^2+y^2)} (corrected geometry) plus section vs zero Taylor polynomial. SVG valid; render succeeded (24946 bytes).
- F3: level curves of three quadratic forms (minimum/maximum/saddle). SVG valid; render succeeded (15287 bytes).

## Gate statuses

| Gate | Status | Notes |
|---|---|---|
| Verified scope & credible source evidence | PASS | |
| Correctness of material claims/proofs | PASS | All computations verified |
| All examples independently verified | PASS | |
| Notation/domain consistency | PASS | |
| Required files/metadata | PASS | |
| Image path & SVG XML integrity | PASS | 3/3 resolve; XML valid |
| Actual SVG rendering & visual inspection | NOT_RUN | Chrome rendered PNGs; no image-capable model to inspect pixels |
| Prose/LaTeX structure | PASS | |
| Markdown/LaTeX renderer availability | NOT_RUN | Source-level check only |
| Exact remote persistence | PENDING | |

## Changes made

- Minor wording fix in "When the Taylor series does not represent the function": "bump near the origin" -> "rise of the function away from the origin". Justified by the function's actual geometry (f(0,0)=0, f>0 elsewhere).

## Limitations

- Visual inspection not possible in this environment.
- Peano form proof not reproduced (cited to Toronto notes) but quadratic case proved in-article.

## Final disposition

BLOCKED — mandatory visual-inspection gate NOT_RUN. All other mandatory gates PASS. Remote persistence to be verified after commit.

AI-reviewed staging content; not human-approved or authorized for upstream publication.
PY