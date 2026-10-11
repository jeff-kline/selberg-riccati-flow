# Selberg's formula as a Riccati flow, with an application to a sparse Mertens certificate

Jeffery Kline

**Version 0.1.0 — release candidate.** No DOI or stable citation exists yet.
Admission under the project's
[public research standard](https://jeff-kline.github.io/posts/research-program/index.html)
is a release decision, not peer review or a correctness certificate.

The paper is [paper/main.pdf](paper/main.pdf); its source is
[paper/main.tex](paper/main.tex).

## Introduction

Write $\psi(x)=\sum_{n\le x}\Lambda(n)$ for the Chebyshev function and

```math
f(t)=e^{-t}\psi(e^t)-1 .
```

The prime number theorem says $f(t)\to0$. Wirsing showed in 1962–64,
by elementary real-variable methods, that Selberg's symmetry formula
implies the rate $\psi(x)=x+O(x/\log x)$, that is, $f(t)=O(1/t)$.

This paper gives a different proof of the mean-square form of that bound:

```math
\int_0^T t^2 f(t)^2\,dt = O(T).
```

Let $b(s)$ be the Laplace transform of the prime-power measure
$\sum_n \Lambda(n)n^{-1}\delta_{\log n}$. The proof has four steps.

1. On each horizontal line $s=\sigma+i\xi$, Selberg's formula becomes a
   Riccati equation for $\beta=\sigma b(\sigma+i\xi)$ as $\sigma$ decreases.
2. Positivity at the doubled frequency $2\xi$ keeps $\beta$ away from the
   equation's unstable fixed point $-1$, uniformly in $\xi$.
3. The substitution $W=\beta/(1+\beta)$ makes the equation linear. This
   bounds the resolvent of the equation for the Laplace transform of $f$,
   uniformly in $\xi$.
4. A local density bound for primes, from a quadratic sieve, controls the
   starting line and the high frequencies.

The proof stays in the half-plane where the Laplace transform converges
absolutely. It uses no analytic continuation and no zero-free region.

The argument applies to any positive measure that satisfies a Selberg-type
relation with bounded error. Without the density hypothesis, the same
method proves $f\in L^2(0,\infty)$. That is the input needed to apply
Wirsing's abstract Tauberian theorem to a general measure, and it then gives
$f(t)=O(1/t)$.

As an application, the energy bound closes a sparse divisor–cofactor
certificate for the Mertens function $M(N)=\sum_{n\le N}\mu(n)$, giving

```math
M(N)=O\!\left(\frac{N}{\log N}\right),\qquad
\psi(x)=x+O\!\left(\frac{x}{(\log x)^{1/3}}\right).
```

These rates are classical. The contribution is the method.

## Contribution and prior work

The arithmetic bounds are classical, and the pointwise bound is Wirsing's.
What we believe is new:

- **Selberg's formula as a differential equation in $\sigma$**, solved
  quantitatively inside the half-plane of absolute convergence. The
  elementary proofs (Selberg, Erdős, Kuhn, Wirsing, Bombieri) avoid the
  Laplace transform; the analytic proofs (Wiener–Geller, the 3-4-1
  argument, Tao) use it on the boundary line and give no rate. This
  argument uses the transform, never reaches the boundary, and gives a rate.
- **Positivity at $2\xi$ as a barrier for the flow.** The inequality is the
  one behind the 3-4-1 argument; the new part is using it to hold the flow
  away from $-1$ for a fixed time, uniformly in $\xi$, in place of
  analyticity.
- **The linearized resolvent**, and its consequence $f\in L^2$ for a
  general positive measure without a density hypothesis. Through Wirsing's
  abstract theorem this makes his pointwise bound available beyond the
  arithmetic case. Wirsing obtained the corresponding input from arithmetic
  identities, which a general measure does not have.

We did not find these in the sources compared in Section 16 of the paper:
Diamond's 1982 survey, and the primary papers of Kuhn, Wirsing and Bombieri
for each remainder mechanism it describes. The comparison was bounded, not
exhaustive. Ingham's review, Wright (1952), Amitsur (1961) and the
Diamond–Zhang monograph were not consulted, so priority is not settled.

## Evidence and limits

- The energy theorem, the density bound for primes, the passage to the
  certificate, and the bounds on $M(N)$ and $\psi(x)$ above are proved in
  the paper. Classical inputs (Chebyshev and Mertens estimates, Selberg's
  formula, a quadratic sieve) are proved or cited explicitly.
- The pointwise bound $f(t)=O(1/t)$ without the density hypothesis uses
  Wirsing's Satz 2 (1964), which he stated without a detailed proof. Its
  implied constant may depend on the particular measure.
- The energy bound is sharp in the abstract setting; the paper gives an
  explicit example.
- The certificate has a floor and gives no rate better than the classical
  ones. Several finite inverse estimates that motivated the work remain
  open (Sections 14–15).
- The proofs were checked by separate AI reviews. No human expert has
  reviewed them. Agreement among AI audits is evidence about a process, not
  independent validation. No numerical computation is used as evidence.

## Reproduce

Requirements: pdfLaTeX (tested with TeX Live) and Poppler's `pdfinfo` and
`pdftotext`. No Python is needed.

```sh
make paper                        # three pdfLaTeX passes; fixed SOURCE_DATE_EPOCH
make check                        # TeX log, page count, unresolved references
shasum -a 256 -c MANIFEST.sha256
```

`make check` checks the document's consistency; it does not check proofs.

## Repository contents

- `paper/`: LaTeX source `main.tex` and reading copy `main.pdf`.
- `audit/`: audit reports and the ledger of findings and dispositions.
- `ADMISSION.md`, `VERIFICATION.md`, `CORRECTIONS.md`, `CITATION.cff`,
  `MANIFEST.sha256`: release records.

## Role of AI

AI models did the derivations, literature search, exposition, and audits
under the author's direction. The author chose the question and is
responsible for the result and its corrections.

## License

GPL-3.0-only. See [LICENSE](LICENSE).
