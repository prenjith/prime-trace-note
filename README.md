**See also:** [Explicit prime-2 counterexample to Theorem 12.5.1.1 at zero spectral width](counterexample-12.5.1.1.md)

# Note on the shell cutoff in *The Music of the Primes*

**Reference:** Alessandro Maria Masullo, *The Music of the Primes*, Chapter 11, §11.3.2, Theorem 11.3.2.1, pp. 493–496, particularly equation (11.3.2.3).

**Manuscript:** https://math216.wordpress.com/wp-content/uploads/2026/11/the-music-of-the-primes.pdf

## 1. Mathematical obstruction

The proof introduces a decreasing filtration of divisorial strata:

$$
E_{k+1}\subseteq E_k,
$$

with indicator functions

$$
\alpha_k=\mathbf{1}_{E_k}.
$$

The shell operator involves the multiplier

$$
\alpha_{k+1}(y)-\alpha_k(y).
$$

In equation (11.3.2.3), an additional cutoff $\alpha_j(y)$ is applied to the same variable, with $j\to\infty$.

For every $j\geq k+1$,

$$
E_j\subseteq E_{k+1}\subseteq E_k.
$$

Consequently, for every $y$,

$$
\boxed{
\alpha_j(y)\bigl(\alpha_{k+1}(y)-\alpha_k(y)\bigr)=0.
}
$$

**Proof:** If $y\notin E_j$, then $\alpha_j(y)=0$. If $y\in E_j$, then $y\in E_{k+1}\subseteq E_k$, so $\alpha_{k+1}(y)=\alpha_k(y)=1$. Either way, the product is zero.

This identity holds pointwise, not merely almost everywhere or in an asymptotic sense.

## 2. Consequence for the trace calculation

Any integral containing this product as a multiplicative factor is therefore identically zero for all $j\geq k+1$, provided the indicators act on the same kernel variable as displayed.

In particular,

$$
\lim_{j\to\infty}
\int
\alpha_j(y)
\bigl(\alpha_{k+1}(y)-\alpha_k(y)\bigr)
K(x,y)\,d\mu(y)
=0
$$

whenever the expression is defined.

However, Theorem 11.3.2.1 seeks to recover a generally nonzero local prime-power contribution.

For the rational field $\mathbb Q$, consider the shell at $p=2$ and a nonnegative smooth radial test function concentrated near idelic norm $2$, with value $1$ at that norm. The claimed local expression contains a positive contribution at the corresponding prime-power term, assuming the displayed normalization.

The proposed cutoff calculation therefore cannot recover the asserted nonzero trace.

## 3. Mathematical significance

The problem is structural: the cutoff projects onto a region disjoint from the shell on which the original kernel is supported.

No dominated-convergence argument can change the exact identity

$$
\alpha_j(\alpha_{k+1}-\alpha_k)=0.
$$

The calculation would require a modified cutoff that preserves the shell, followed by a separate proof that the modified approximation converges in the sense required for the trace.

This affects the justification of the geometric trace calculation subsequently used in Chapter 12, including Theorem 12.5.1.1.

## 4. Scope of the objection

This establishes a mathematical defect in the printed cutoff argument. It does not, by itself, prove that the desired trace identity is false or that no alternative derivation exists.

The same underlying obstruction has already been documented in this issue. This comment provides an independent, elementary verification of the exact pointwise identity.

**Conclusion:** The cutoff limit in equation (11.3.2.3), as printed, cannot establish the nonzero shell trace asserted by Theorem 11.3.2.1. A replacement argument is necessary before this step can support the later trace formula.
