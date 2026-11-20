# Extremal constants for a family of weighted prime sums

Fix $b>1$. Under RH, the normalized ordinary-prime deficit has limsup $B_b+L_b$ and liminf at least $B_b-L_b$. If the distinct positive ordinates of nontrivial zeta zeros are linearly independent over $\mathbb Q$, the liminf equals $B_b-L_b$.

Let $W_b(t)$ equal $b(1-1/t)$ for $1<t\le b$, $b^2/t-1$ for $b<t<b^2$, and zero elsewhere. Define $P_b(y)=\sum_{p\ {\rm prime}}(\log p)W_b(p/y)$ for $y>0$, with natural logarithms. Its expected main term is $b(b-1)y\log b$. Write $B_b=2\sqrt b(\sqrt b-1)^2$ for the asymptotic prime-square contribution, $D_b(y)=b(b-1)y\log b-P_b(y)$ for the deficit and $H_b(s)=(b^s-1)(b^s-b)/(s(s-1))$ for the Mellin transform. For $\rho=1/2+i\tau$ the identity $b/b^\rho=\overline{b^\rho}$ gives

$$
 H_b(\rho)=e^{i\tau\log b}h_\rho,\qquad
 h_\rho=\frac{\sqrt b\,(b+1-2\sqrt b\cos(\tau\log b))}{1/4+\tau^2}>0.
$$

[Formal proof of the strip and phase identities](https://github.com/leecrossley/prime-band-mellin/tree/v1.0.0)

Assume RH and count each nontrivial zeta zero with its multiplicity. Here $\gamma$ is Euler's constant, $C_0=2+\gamma-\log(4\pi)=\sum_\rho 1/[\rho(1-\rho)]$, $\Lambda$ is the von Mangoldt function, and $R(b)=\sum_n\Lambda(n)(b/n-1)_+$. The Mellin transform is taken with density $t^{s-1}dt$. At $s=0,1$ the analytic transform takes its continuous limiting value. [Zero-sum identity](https://arxiv.org/pdf/1202.0729)

For $y>1$, the von Mangoldt explicit formula for $W_b$ consists of the main term, minus $\sum_\rho y^\rho H_b(\rho)$, minus $\sum_{j\ge1}y^{-2j}H_b(-2j)$. One may first smooth the weight in log coordinates. The zero coefficients are bounded by a common $O_b((1+|\Im\rho|)^{-2})$, the prime side is finite, and the trivial zeros have a geometric majorant. Taking the smoothing width to zero recovers the continuous weight, including its corners. Removing prime squares contributes $\sum_p(\log p)W_b(p^2/y)$. Partial summation with the prime number theorem gives its limit after normalization by $\sqrt y$ as $\int_1^b W_b(v^2)\,dv=2\sqrt b(\sqrt b-1)^2=B_b$. [Explicit formula and prime number theorem](https://people.maths.ox.ac.uk/greenbj/papers/primenumbers.pdf)

We can compute the sum $L_b=\sum_\rho h_\rho$ explicitly. Set $S(b)=\sum_\rho b^\rho/[\rho(1-\rho)]$. Conjugate zeros pair, so $L_b=\sqrt b[(b+1)C_0-2S(b)]$. Applying the explicit formula to the original ramp at the single scale $b$ gives

$$
 \begin{aligned}
 S(b)&=R(b)-b(\log b-1-\gamma)-\log(2\pi)+T(b),\\
 T(b)&=\sum_{j\ge1}\frac{b^{-2j}}{2j(2j+1)}
 =1+\log b+\frac{(b-1)\log(b-1)-(b+1)\log(b+1)}2 .
 \end{aligned}
$$

For the first equality integrate $(-\zeta'/\zeta)(s)b^s/[s(s-1)]$ on a vertical line to the right of 1. Its inverse Mellin transform is $R(b)$. Shifting to the left gives the double-pole residue $b(\log b-1-\gamma)$ at 1, the residue $\log(2\pi)$ at 0, the sum $S(b)$ at nontrivial zeros, and $-T(b)$ at trivial zeros. The quadratic denominator gives an absolutely convergent zero sum and vanishing horizontal integrals along the usual ordinates avoiding zeros. The kernel is continuous at its cutoff, including $b=2$. The series for the logarithm and the inverse hyperbolic tangent give the displayed value of $T$. In particular $R(b)=0$ for $1<b\le2$. [Explicit formula and contour estimates](https://people.maths.ox.ac.uk/greenbj/papers/primenumbers.pdf)

Prime powers with exponent at least three contribute $O_b(y^{1/3}(\log y)^2)$. Dividing the explicit formula by $\sqrt y$ now gives an absolutely convergent series,

$$
 \frac{D_b(y)}{\sqrt y}=B_b+\sum_{\rho}h_\rho e^{i\tau\log(by)}+o(1).
$$

Thus the normalized liminf is at least $B_b-L_b$. The limsup equals $B_b+L_b$. To see equality, fix any finite set of ordinates. Simultaneous approximation gives arbitrarily large times at which all their phases are as close as desired to $+1$. Absolute convergence controls the rest. If the distinct positive ordinates are linearly independent over the rationals, Kronecker's theorem also allows all the finite phases to approach $-1$. With that additional hypothesis the liminf equals $B_b-L_b$. Linear independence plays a similar role in classical prime number races. [Rubinstein and Sarnak](https://www.math.uwaterloo.ca/~mrubinst/publications/Chebyshev.pdf)

At $b=2$ the lower endpoint is approximately $0.2199792174$ and the upper endpoint is approximately $0.7505835310$. The executable certifies $0.2198<B_2-L_2<0.2201$ and $0.7504<B_2+L_2<0.7508$. The short rigorous intervals distinguish what the certificate checks from the extra displayed decimal places.

## A sufficient dilation and a small-scale obstruction

Replace 2 by a fixed $b>1$ and use the ramp difference with coefficients $(b,-(b+1),1)$ at $y,by,b^2y$. The drift from squares is $2\sqrt b(\sqrt b-1)^2\sqrt y$. The height-independent bound for the zeros is $C_0\sqrt b(\sqrt b+1)^2\sqrt y$. The former wins when

$$
 b>\left(\frac{1+\sqrt{C_0/2}}{1-\sqrt{C_0/2}}\right)^2
 =1.84529052\ldots.
$$

This gives a first sufficient width for eventual bias. At the other end, take $y=2/b$. For $1<b<\sqrt2$ the single prime 2 contributes $(b-1)\log2>2(b-1)\log b$, already exceeding the main term. At $b=\sqrt2$ it gives equality.

## Verification

The explicit formula, prime number theorem and simultaneous phase approximation are used in the written proof. The executable certifies the dyadic numerical enclosures. The strip and phase identities have a separate Lean proof. [Formal proof of the strip and phase identities](https://github.com/leecrossley/prime-band-mellin/tree/v1.0.0)

The recorded run used Python 3.9.6 on arm64 macOS. The verifier requires Python 3.9 or later and uses only the standard library.

```sh
bash verify-release.sh
```

The command checks the release manifest, reruns the arithmetic, and compares its output with the recorded result.

[Recorded verification output](evidence/check.txt) · [SHA-256 manifest](SHA256SUMS) · [Tagged publication](https://github.com/leecrossley/prime-band-extrema/releases/tag/v1.0.0)

## Related result

[Eventual positivity at 151/100](https://github.com/leecrossley/prime-band-151-100/tree/v1.0.0) · [Conditional oscillation at the same dilation](https://github.com/leecrossley/prime-band-three-halves-oscillation/tree/v1.0.0)
