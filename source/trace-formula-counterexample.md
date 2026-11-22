# Mathematical Counterexample and Structural Objections to Masullo's Main Trace Formula

**Paper:** Alessandro Maria Masullo, *The Music of the Primes* (November 20, 2026 draft)

**Primary target:** Theorem 12.5.1.1, pages 519–520

## 1. Overview

This analysis identifies a mathematical contradiction in the zero-width specialization of Masullo's central trace formula, together with several additional structural problems affecting its proposed proof.

The central issue concerns the relationship between the geometric trace and a spectral sum restricted to zeros within a specified vertical strip.

An explicit test-function construction over the rational field produces a nonzero geometric contribution while the corresponding zero-width spectral expression tends to zero.

The contradiction challenges the trace identity under that interpretation of the manuscript's permitted parameters.

It does not establish that the Riemann Hypothesis is false or that every possible corrected trace formula is impossible.

## 2. Zero-Width Spectral Counterexample

Definition 10.4.3.7 permits intervals of the form

$$
I=[-\alpha,\alpha],\qquad \alpha\geq0.
$$

Consider the specialization

$$
F=\mathbb Q,\qquad\alpha=0.
$$

Under the strict-interior interpretation used in the spectral trace formula, the corresponding spectral strip is empty.

Consequently, the spectral sum over zeros vanishes, leaving only the two pole terms.

The asserted identity becomes

$$
G(\varphi)
=
M_{1/2}(\varphi)+M_{-1/2}(\varphi),
$$

where $G(\varphi)$ denotes the geometric expression.

### Construction of the test function

Choose a nonnegative smooth function

$$
b\in C_c^\infty((-1,1))
$$

such that $b(0)=1$.

For sufficiently small $\delta>0$, define

$$
\varphi_\delta(g)
=
b\left(
\frac{\log|g|-\log2}{\delta}
\right).
$$

The support of this function lies in the interval

$$
2e^{-\delta}<|g|<2e^\delta.
$$

For $\delta<\log2$,

$$
\varphi_\delta(1)=0.
$$

Thus the test function satisfies the explicit vanishing condition imposed in the theorem.

### Evaluation of the geometric expression

For sufficiently small $\delta$, the support contains no positive integral prime power other than 2.

The relevant finite-place contribution therefore arises from the prime $p=2$.

On the local valuation shell satisfying

$$
|g|_2=2,
$$

the ultrametric inequality gives

$$
|1-g|_2=2.
$$

Hence

$$
\frac{|g|_2^{1/2}}{|1-g|_2}
=
\frac1{\sqrt2}.
$$

The local normalization factor is

$$
\frac{\log2}{\mu_2(\mathbb Z_2^\times)}.
$$

Integrating over the shell therefore gives

$$
G_{\mathrm{fin}}(\varphi_\delta)
=
\frac{\log2}{\sqrt2}.
$$

The Archimedean contribution is $O(\delta)$, because the support shrinks toward a point away from the singularity at 1.

Thus

$$
\boxed{
G(\varphi_\delta)
=
\frac{\log2}{\sqrt2}+O(\delta).
}
$$

Taking the limit,

$$
\lim_{\delta\to0^+}G(\varphi_\delta)
=
\frac{\log2}{\sqrt2}>0.
$$

### Evaluation of the spectral expression

Because the zero-width spectral strip has empty interior, no zeros contribute to the spectral sum.

Only the two Mellin-transform terms remain.

For $s=\pm1/2$,

$$
M_s(\varphi_\delta)
=
\int_0^\infty
b\left(
\frac{\log t-\log2}{\delta}
\right)t^s\frac{dt}{t}.
$$

Using

$$
t=2e^{\delta u},
$$

we obtain

$$
M_s(\varphi_\delta)
=
\delta 2^s
\int_{-1}^{1}b(u)e^{s\delta u}\,du.
$$

Therefore,

$$
M_{1/2}(\varphi_\delta)=O(\delta)
$$

and

$$
M_{-1/2}(\varphi_\delta)=O(\delta).
$$

The spectral expression consequently satisfies

$$
S(\varphi_\delta)=O(\delta).
$$

Hence

$$
\lim_{\delta\to0^+}S(\varphi_\delta)=0.
$$

### Contradiction

The claimed trace identity requires

$$
G(\varphi_\delta)=S(\varphi_\delta).
$$

Substituting the preceding calculations yields

$$
\frac{\log2}{\sqrt2}+O(\delta)
=
O(\delta).
$$

Letting $\delta\to0^+$ forces

$$
\boxed{
\frac{\log2}{\sqrt2}=0.
}
$$

This is impossible.

Therefore, the zero-width specialization cannot satisfy the asserted trace identity under the stated strict-interior spectral interpretation.

This counterexample uses no assumptions about the truth or falsity of the Riemann Hypothesis.

## 3. The More General Spectral-Window Problem

The preceding contradiction applies to a particular boundary case.

A possible repair would be to exclude $\alpha=0$, require strictly positive spectral width, or modify the contribution of boundary zeros.

However, a further difficulty concerns the relationship between a restricted spectral sum and the classical explicit formula.

The classical Weil explicit formula involves contributions from all relevant nontrivial zeros.

Masullo's proposed spectral expression instead involves zeros inside a specified vertical strip.

Formally, the omitted contribution takes the form

$$
D_\alpha(\varphi)
=
\sum_{\substack{\zeta(\rho)=0\\
|\operatorname{Re}\rho-1/2|\geq\alpha}}
m_\rho M\varphi(\rho-1/2),
$$

subject to the relevant convergence and normalization conventions.

For a restricted-zero formula to agree with an unrestricted geometric formula, this omitted-zero distribution must vanish on the admissible test-function space, or an additional correction term must account for it.

Neither conclusion follows merely from restricting the spectral operator.

This presents a fundamental proof obligation.

Showing that the omitted distribution vanishes for arbitrarily narrow positive-width strips would be closely related to proving that all nontrivial zeros lie on the critical line.

The desired conclusion cannot be assumed in the course of proving it.

## 4. Additional Structural Objections

### 4.1 Uniform biorthogonal estimates

Theorem 10.3.1.1 uses a uniform estimate for biorthogonal vectors associated with spectral evaluation functionals.

Suppose

$$
\ell_t(v_t)=1,\qquad
\ell_u(v_t)=0.
$$

Then

$$
1=(\ell_t-\ell_u)(v_t).
$$

By the duality inequality,

$$
1\leq
\|\ell_t-\ell_u\|\|v_t\|.
$$

Consequently,

$$
\boxed{
\|v_t\|
\geq
\frac1{\|\ell_t-\ell_u\|}.
}
$$

If the evaluation functionals corresponding to distinct zeros become arbitrarily close in dual norm, a uniformly bounded biorthogonal family cannot exist.

This creates a potential obstruction to the spectral estimates and associated nuclearity arguments.

### 4.2 Shell cutoff annihilation

In the proof of Theorem 11.3.2.1, the manuscript introduces decreasing sets

$$
E_{k+1}\subseteq E_k
$$

and indicators

$$
\alpha_k=\mathbf1_{E_k}.
$$

For every $j\geq k+1$,

$$
E_j\subseteq E_{k+1}\subseteq E_k.
$$

Therefore,

$$
\boxed{
\alpha_j(\alpha_{k+1}-\alpha_k)=0.
}
$$

When the cutoffs act on the same kernel variable as printed, the modified shell integrand vanishes identically.

Consequently, this cutoff calculation cannot recover a generally nonzero prime-power contribution.

A replacement cutoff and a separate limit argument would be necessary.

### 4.3 Noncommuting regularization limits

The trace construction uses multiple truncations and regularizations.

A mathematical audit reports test cases in which removing these restrictions in different orders produces different limiting values.

Without a valid interchange-of-limits theorem, the regularized trace is not established by the proposed sequence of operations.

### 4.4 Failure of operator-domain preservation

The norm cutoff used in Chapter 12 is reported not to preserve the Schwartz–Bruhat test-function space.

At non-Archimedean places, the multiplier may destroy local constancy.

This undermines operator manipulations that require the transformed functions to remain in the original analytic domain.

### 4.5 Geometric kernel normalization

The quotient-kernel and indented-kernel constructions require compatible measure normalizations and diagonal trace operations.

Reported counterexamples show that these properties cannot be inferred from the hypotheses as printed.

Additional analytic justification is necessary before the geometric expression can be identified with the spectral trace.

## 5. Consequences for the Main Argument

The proposed proof relies on a sequence of mathematical constructions:

1. Establish appropriate functional spaces and analytic estimates.
2. Construct spectral evaluation functionals associated with zeros.
3. Prove suitable nuclearity and trace-class properties.
4. Calculate geometric traces through local prime-power contributions.
5. Establish a global spectral-geometric trace identity.
6. Deduce restrictions on the locations of zeros.

The objections described above affect several of these stages.

In particular, the zero-width counterexample attacks a stated formulation of the central trace identity, while the cutoff and regularization problems challenge the method used to derive it.

Repairing one local calculation does not automatically resolve the others.

## 6. Scope of the Mathematical Result

The strongest conclusion supported by the explicit calculation is that the trace identity fails under the zero-width, strict-interior interpretation.

This conclusion depends on the zero-width case being included in the applicable statement of Theorem 12.5.1.1, rather than merely being permitted in an earlier definition.

The broader positive-width theorem has not been disproved by this example.

Likewise, failures of uniform estimates, kernel constructions, or limit arguments invalidate particular proof steps only when all their hypotheses and dependencies have been checked.

They do not automatically imply that no alternative proof can exist.

## 7. Final Conclusion

The analysis identifies a concrete mathematical contradiction in a boundary specialization of Masullo's central trace formula and several serious structural objections to its proof.

The principal findings are:

- The zero-width, strict-interior spectral formula yields an empty zero sum while the geometric prime-2 contribution remains nonzero.
- The restricted spectral formulation requires a rigorous account of zeros excluded from the spectral window.
- The reported biorthogonal estimates face a fundamental functional-analytic obstruction.
- The shell cutoff used in the printed argument annihilates the corresponding kernel contribution.
- The regularization and operator-domain arguments require additional mathematical justification.

Together, these issues show that substantial parts of the proposed derivation cannot be accepted without correction or further proof.

**The existing analysis does not disprove the Riemann Hypothesis, establish that every positive-width version of the trace formula is false, or prove that Masullo's approach is irreparable.**

It does identify specific statements and constructions that require rigorous mathematical repair.

## References

1. Masullo, Alessandro Maria. *The Music of the Primes*. November 20, 2026. https://math216.wordpress.com/wp-content/uploads/2026/11/the-music-of-the-primes.pdf
2. Riemann–Masullo formalization project: https://github.com/mccorvie/riemann-masullo
3. Chapter 11 shell-cutoff objections: https://github.com/mccorvie/riemann-masullo/issues/1358
4. Chapter 12 trace-formula audit: https://github.com/mccorvie/riemann-masullo/issues/2469
5. Uniform biorthogonal-bound objection: https://github.com/mccorvie/riemann-masullo/issues/1169

**Verification status:** Mathematical analysis incorporating publicly documented objections. The full set of claims has not been independently peer-reviewed, and the broader trace theorem has not been conclusively disproved.
