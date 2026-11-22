# Twenty Additional Mathematical Objections to Masullo's *The Music of the Primes*

**Manuscript:** *The Music of the Primes* (November 20, 2026 draft)

**Status:** Compilation of previously reported mathematical objections; not an independently peer-reviewed verification of all 20 claims.

## Overview

This report identifies 20 substantial mathematical objections concerning the analytic, spectral, functional-analytic, and trace-formula arguments in Masullo's *The Music of the Primes*.

The issues include false identities, incorrect asymptotic estimates, invalid limit interchanges, failures of operator-domain preservation, and counterexamples to stated propositions.

These objections are documented in existing public mathematical audits and formalization work. They should not be regarded as 20 newly discovered errors or 20 independently verified counterexamples.

## Part I: Major Structural Problems

**1. Global trace normalization error — Theorem 12.5.1.1, pp. 519–520**

The geometric and spectral expressions are reported to differ by a Tamagawa-volume factor associated with the norm-one idele class group.

For certain number fields, particularly imaginary quadratic fields, this produces a nontrivial discrepancy. Correcting the normalization may require revisiting the global trace formula and its local-to-global compatibility.

**2. Failure of uniform biorthogonal bounds — Theorem 10.3.1.1, p. 451**

The manuscript requires a uniform bound for a family of biorthogonal vectors associated with zeros of zeta or Hecke L-functions.

If distinct evaluation functionals become arbitrarily close, the norms of the corresponding biorthogonal vectors must become unbounded.

Indeed, if

$$
\ell_t(v_t)=1,\quad \ell_u(v_t)=0,
$$

then

$$
1\leq\|\ell_t-\ell_u\|\|v_t\|.
$$

Consequently,

$$
\|v_t\|\geq\frac1{\|\ell_t-\ell_u\|}.
$$

This is incompatible with a uniform norm bound whenever the functional differences approach zero. The reported application to zeta zeros challenges a central spectral estimate.

**3. Failure of strict cutoff-space inclusion — Theorem 11.1.2.1, p. 480**

A telescoping construction over the rational field is reported to produce equality between two cutoff spaces that the manuscript claims are strictly nested.

If established under all of the theorem's hypotheses, this invalidates the claimed strict filtration and requires reconsideration of later arguments depending on it.

**4. Kernel regularity does not transfer as claimed — Proposition 12.2.2.2(4), pp. 508–512**

The proposition transfers regularity properties between quotient kernels and their indented lifts.

A reported rank-one construction has a regular quotient diagonal but a lifted kernel whose local diagonal averages diverge.

This challenges the legitimacy of extracting traces from the lifted kernel using the stated regularity assumptions.

**5. Norm cutoff destroys Schwartz–Bruhat regularity — §12.4.1, pp. 516–517**

The cutoff operator used in the trace construction is reported not to preserve the Schwartz–Bruhat function space.

At a non-Archimedean place, multiplication by the proposed norm cutoff can destroy local constancy.

This matters because the operator manipulations require the resulting functions to remain in the appropriate domain.

**6. Noncommuting cutoff limits — §12.4.1, p. 514**

The manuscript removes different regularization cutoffs in succession.

A reported explicit prime-2 example gives different outcomes depending on the order of the limits.

Without a valid theorem permitting the interchange, the resulting trace cannot be identified with a unique expression by the printed argument.

**7. False stabilizer uniqueness — Proposition 8.2.0.4, p. 386**

The proposition asserts a uniqueness property for multiplicative stabilizers.

An adele having a zero coordinate can possess a larger stabilizer than the claimed one.

The argument therefore requires additional nonvanishing hypotheses or a revision of the underlying group action.

**8. Divergent Archimedean estimate — §§1.4.3 and 1.8.4.3, pp. 29 and 54**

The manuscript asserts a uniform estimate for a family of Archimedean approximations.

The public mathematical audit reports an explicit family for which Fatou's lemma forces divergence, contradicting the claimed uniform control.

The affected estimates may need stronger hypotheses or a different approximation scheme.

## Part II: Additional Mathematical Counterexamples

**9. Inconsistent additive-character conventions — pp. 557–558**

The stated real and $p$-adic additive characters reportedly fail to combine into a character that is trivial on the diagonal embedding of $\mathbb Q$.

The rational number $1/3$ supplies an explicit test: the real and 3-adic phases reinforce rather than cancel.

This can affect the normalization of Fourier transforms and Poisson summation.

**10. Invalid Cauchy integral representation — Theorem B.2.2.4, pp. 602–603**

The theorem's decay assumptions do not imply all the Hardy-space properties needed for its claimed integral representation.

An explicit entire Laplace transform is reported to violate the representation.

The proof therefore requires stronger analytic hypotheses or a revised contour argument.

**11. Incorrect gamma-factor asymptotics — Proposition 3.3.1.5(3), p. 133**

For $F=\mathbb Q(i)$, the relevant gamma-factor ratio grows like

$$
|\tau|,
$$

whereas the claimed estimate bounds it by

$$
O(|\tau|^{1/2}).
$$

These rates are incompatible as $|\tau|\to\infty$.

The correct exponent must be propagated through any later estimates that rely on this bound.

**12. Incorrect higher-order residue identity — Theorem B.3.2.1, pp. 604–606**

The reported counterexample uses

$$
f(z)=z^{-2},\qquad \Phi(z)=ze^{z^2}.
$$

The claimed higher-order residue calculation produces zero where the actual residue equals one.

This directly challenges the relevant contour-shifting identity.

**13. Invalid contour-height estimate — Lemma B.3.1.2, pp. 604–605**

The proof uses a lower bound on selected contour heights that does not follow from the stated upper-bound hypothesis.

Consequently, the claimed disappearance of horizontal contour contributions is not justified.

A corrected proof requires additional growth control and a valid sequence of integration contours.

**14. Incorrect local Euler-factor integral — Lemma B.4.1.7, pp. 611–614**

A one-sided contour integral is identified with a two-sided prime-power sum.

For the trivial character at the prime 2, a suitable compactly supported test function reportedly produces a nonzero prime-power sum while the corresponding contour integral vanishes.

This challenges the stated local explicit-formula calculation.

**15. Failure of periodization surjectivity — Proposition 4.2.2.2(1), p. 171**

The proposition claims that periodization of functions supported on a specified closed multiplicative interval is surjective.

However, the support and boundary requirements force identified endpoint values to vanish, preventing the constant function from appearing in the image.

The support conditions require revision.

**16. Incorrect coboundary support characterization — Proposition 4.2.2.2(2), p. 171**

The claimed representation of multiplicative coboundaries does not correctly account for their supports.

An explicit nonzero function of the form

$$
u(x)-u(\gamma x)
$$

violates the proposed support characterization.

The kernel of the periodization map must therefore be reconsidered.

**17. False boundedness criterion — Proposition D.3.3.10(3), p. 807**

The proposed criterion for bounded subsets of a weighted Schwartz space tests interior exponents but fails to control an included endpoint.

An example with unbounded endpoint behavior contradicts the claimed equivalence.

This affects the topology used for subsequent continuity and duality arguments.

**18. Invalid spanning family — Lemma 2.1.3.2(3), p. 68**

The proposed finite-coordinate subgroup indicators cannot generate all Schwartz–Bruhat functions.

Such indicators have symmetry properties not shared by general locally constant compactly supported functions.

For example,

$$
\mathbf1_{1+3\mathbb Z_3}
$$

is not even under $x\mapsto-x$, whereas the proposed symmetric generating functions are.

Thus the spanning assertion is false as stated.

**19. Incompatible Haar normalizations — Lemma A.3.1.3, p. 556**

The local Haar normalizations and the asserted global quotient measure are reported to disagree.

For the number field $\mathbb Q(i)$, the prescribed complex local measure gives a quotient mass of two instead of the asserted value one.

The normalization requires correction before it can be used consistently in global trace identities.

**20. False trace-norm equality — Lemma C.3.4.4(2), p. 698**

The manuscript asserts an equality of trace norms of the form

$$
\|AT\|_1=\|TA\|_1.
$$

This is false for general operators, even in two-dimensional matrix spaces.

The standard estimates are instead

$$
\|AT\|_1\leq\|A\|\|T\|_1
$$

and

$$
\|TA\|_1\leq\|A\|\|T\|_1.
$$

An equality requires additional assumptions and cannot be used unconditionally.

## Part III: Implications for the Claimed GRH Proof

The greatest concern is the interaction between the reported spectral, regularization, and trace-formula failures.

A simplified dependency structure is:

1. Functional-analytic estimates establish the spaces and operators.
2. Spectral arguments identify zero-associated functionals and their properties.
3. Nuclearity and regularization justify traces of the constructed operators.
4. Geometric calculations express those traces through local arithmetic contributions.
5. The global trace formula equates the geometric and spectral expressions.
6. A final argument would need to deduce the location of zeros from that identity.

Objections 1–6 concern several of these central stages.

The strongest candidates for extensive mathematical reconstruction are the failure of uniform biorthogonal bounds, lack of operator-domain preservation, and noncommutation of regularization limits.

Correcting isolated constants or strengthening simple hypotheses might resolve some individual problems. However, corrections to the spectral construction or to the mechanism producing the global trace formula could require substantial changes to the proof architecture.

## Conclusion

These 20 mathematical objections raise substantial questions about the correctness of statements and arguments throughout *The Music of the Primes*.

Some concern elementary false identities, while others affect the functional-analytic and spectral machinery used to construct the central trace formula.

The objections warrant individual verification against the original hypotheses, followed by a dependency analysis of all the results that use them.

**The documented errors are sufficient to show that important portions of the manuscript require correction or additional justification. They do not establish that the Riemann Hypothesis is false, that every possible replacement argument must fail, or that the underlying research program is mathematically irreparable.**

### Sources

- Manuscript: https://math216.wordpress.com/wp-content/uploads/2026/11/the-music-of-the-primes.pdf
- Formalization project: https://github.com/mccorvie/riemann-masullo
- Mathematical errata: https://github.com/mccorvie/riemann-masullo/blob/main/ERRATA.md
- Trace-formula audit: https://github.com/mccorvie/riemann-masullo/issues/2469
- Spectral-bound objection: https://github.com/mccorvie/riemann-masullo/issues/1169

**Research status:** Compilation of previously reported mathematical objections; not an independently peer-reviewed verification of all 20 claims.
