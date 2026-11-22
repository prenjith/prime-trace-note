# Prime-2 counterexample at zero spectral width

**Paper:** Alessandro Maria Masullo, *The Music of the Primes* (20 November 2026 draft)

**Location:** Definition 10.4.3.7 (p. 473), Theorem 12.5.1.1 (pp. 519–520), equations (12.5.1.1)–(12.5.1.4).

**Claim:** The published trace formula, interpreted with its explicitly permitted zero-width spectral interval, is mathematically false. An explicit family of admissible smooth test functions gives a nonzero limit on the geometric side and a zero limit on the displayed spectral side.

## 1. Permitted specialization

Definition 10.4.3.7 allows compact intervals

$$
I=[-\alpha,\alpha],\qquad \alpha\geq0.
$$

In particular, choose

$$
F=\mathbb Q,\qquad I=\{0\}.
$$

Theorem 12.5.1.1 describes its spectral sum as running over zeros in the **interior** of the relative vertical strip

$$
\Omega(C_F)_I
=
\{c:|\operatorname{Re}(c)-1/2|<\alpha\}.
$$

For $\alpha=0$, this set is empty.

Consequently, the displayed spectral sum vanishes identically, regardless of the location of any zeta zeros.

The theorem therefore asserts that its geometric expression equals only the two pole contributions:

$$
G(\varphi)
=
M(\varphi)(|\cdot|^{1/2})
+
M(\varphi)(|\cdot|^{-1/2}).
\tag{1}
$$

I will exhibit smooth compactly supported test functions for which this identity is impossible.

## 2. Construct an explicit test family

Choose a nonnegative function

$$
b\in C_c^\infty((-1,1)),\qquad b(0)=1.
$$

For sufficiently small $\delta>0$, define the radial test function on the idele class group of $\mathbb Q$ by

$$
\varphi_\delta(g)
=
b\left(
\frac{\log|g|-\log2}{\delta}
\right).
$$

Its support lies in the norm interval

$$
2e^{-\delta}<|g|<2e^\delta.
$$

For $\delta<\log2$, we have

$$
\varphi_\delta(1)=0,
$$

so it satisfies the explicit test-function condition of Theorem 12.5.1.1.

The support can be chosen sufficiently narrow to contain no positive integral prime power other than $2$.

## 3. Evaluate the geometric side

Consider the non-Archimedean part of (12.5.1.1)–(12.5.1.2).

For every prime $p\ne2$, the relevant valuation shells have norms $p^n$, none of which lie in the support of $\varphi_\delta$, once $\delta$ is sufficiently small.

Therefore every such local contribution vanishes.

At $p=2$, the valuation shell with

$$
|g|_2=2
$$

contributes.

On this shell,

$$
|1-g|_2=2.
$$

Thus

$$
\frac{|g|_2^{1/2}}{|1-g|_2}
=
\frac{1}{\sqrt2}.
$$

Since $\varphi_\delta(g)=b(0)=1$ throughout this shell, the local integral equals

$$
\frac{\mu_2(\mathbb Z_2^\times)}{\sqrt2}.
$$

The normalization factor printed in the theorem is

$$
\frac{\log2}{\mu_2(\mathbb Z_2^\times)}.
$$

Hence the complete non-Archimedean contribution is exactly

$$
\boxed{
G_{\mathrm{fin}}(\varphi_\delta)
=
\frac{\log2}{\sqrt2}.
}
\tag{2}
$$

This expression is independent of $\delta$.

The Archimedean term is an ordinary integral supported near real numbers of absolute value $2$. Its denominator $|1-g|$ stays uniformly separated from zero on this support, and the Haar measure of the support is $O(\delta)$.

Therefore,

$$
G_\infty(\varphi_\delta)=O(\delta).
$$

Combining the local terms gives

$$
\boxed{
G(\varphi_\delta)
=
\frac{\log2}{\sqrt2}+O(\delta).
}
\tag{3}
$$

In particular,

$$
\lim_{\delta\to0^+}G(\varphi_\delta)
=
\frac{\log2}{\sqrt2}>0.
$$

## 4. Evaluate the claimed spectral side

Because $I=\{0\}$, the interior spectral sum is empty.

The right-hand side of Theorem 12.5.1.1 consists solely of its two pole terms.

For either $s=1/2$ or $s=-1/2$, the Mellin transform of the radial test function is

$$
M_s(\varphi_\delta)
=
\int_0^\infty
b\left(\frac{\log t-\log2}{\delta}\right)t^s\frac{dt}{t},
$$

using the standard normalized Haar measure on the norm-one component.

Substituting

$$
t=2e^{\delta u}
$$

gives

$$
M_s(\varphi_\delta)
=
\delta\,2^s
\int_{-1}^{1}b(u)e^{s\delta u}\,du.
$$

Since $b$ is smooth and compactly supported,

$$
M_{1/2}(\varphi_\delta)=O(\delta),
$$

and

$$
M_{-1/2}(\varphi_\delta)=O(\delta).
$$

Thus the claimed spectral side satisfies

$$
\boxed{
S(\varphi_\delta)=O(\delta).
}
\tag{4}
$$

Consequently,

$$
\lim_{\delta\to0^+}S(\varphi_\delta)=0.
$$

## 5. Contradiction

Theorem 12.5.1.1 requires

$$
G(\varphi_\delta)=S(\varphi_\delta)
$$

for every admissible $\delta$.

But equations (3) and (4) imply

$$
\frac{\log2}{\sqrt2}+O(\delta)=O(\delta).
$$

Taking $\delta\to0^+$ yields

$$
\boxed{
\frac{\log2}{\sqrt2}=0,
}
$$

which is impossible.

Therefore the displayed trace identity cannot hold with the zero-width interval and strict-interior spectral sum as stated.

This counterexample uses only elementary local-field valuations, Haar integration, and smooth compactly supported functions. It does not assume the Riemann Hypothesis or the existence of zeros off the critical line.

## 6. Implications and possible repairs

The problem is that the strict-interior spectral restriction loses contributions when the interval collapses to zero width, while the geometric expression retains its prime-power contribution.

A proposed correction would have to explain at least one of the following:

1. Why $I=\{0\}$ should be excluded despite the parameter range in Definition 10.4.3.7.
2. Whether zero-width spectral data must include boundary evaluations rather than a strict-interior sum.
3. How the geometric expression changes with the spectral interval if a restricted-zero formula is intended.
4. How the corrected identity follows from the geometric and spectral kernel constructions.

Excluding $\alpha=0$ would avoid this particular counterexample, but would not by itself justify the comparison between the window-dependent spectral expression and the window-independent geometric expression.

**Conclusion:** Theorem 12.5.1.1, under the stated zero-width specialization and strict-interior interpretation, admits an explicit unconditional counterexample. A modified statement and a new justification of the spectral/geometric comparison are necessary.

This establishes failure of the printed formula in the specified case, not impossibility of every conceivable replacement trace formula.
