# Selberg's formula as a Riccati flow, with an application to a sparse Mertens certificate

Jeffery Kline

[![Version DOI: 10.5281/zenodo.23301917](https://zenodo.org/badge/DOI/10.5281/zenodo.23301917.svg)](https://doi.org/10.5281/zenodo.23301917)

**Version 0.1.0 — admitted, released 2026-10-11.** The immutable release is
[`v0.1.0`](https://github.com/jeff-kline/selberg-riccati-flow/releases/tag/v0.1.0),
archived at version DOI [`10.5281/zenodo.23301917`](https://doi.org/10.5281/zenodo.23301917). The concept DOI
[`10.5281/zenodo.23301916`](https://doi.org/10.5281/zenodo.23301916) resolves to the latest version; cite the
version DOI for reproducibility. Admission under the project's
[public research standard](https://jeff-kline.github.io/posts/research-program/index.html)
is a release decision, not peer review or a correctness certificate. The
tagged snapshot keeps its prepublication "release candidate" wording because
the DOI did not exist when it was made.

The paper is [paper/main.pdf](paper/main.pdf); its source is
[paper/main.tex](paper/main.tex).

## Introduction

This paper gives a different proof of the mean-square form of a classical
bound for the error in the prime number theorem, using a differential
equation derived from Selberg's formula.

Write $\psi(x)=\sum_{n\le x}\Lambda(n)$ for the Chebyshev function and

```math
f(t)=e^{-t}\psi(e^t)-1 .
```

The prime number theorem says $f(t)\to0$. Wirsing showed in 1962–64,
by elementary real-variable methods built on Selberg's symmetry formula,
that $\psi(x)=x+O(x/\log x)$, that is, $f(t)=O(1/t)$. Bombieri and Wirsing
later reached $O(x/(\log x)^A)$ for every $A$.

This paper gives a different proof of the mean-square form of the first
bound, the energy bound

```math
\int_0^T t^2 f(t)^2\,dt = O(T).
```

Let $b(s)$ be the Laplace transform of the prime-power measure
$\sum_n \Lambda(n)n^{-1}\delta_{\log n}$. The proof has four steps.

1. On each horizontal line $s=\sigma+i\xi$, Selberg's formula becomes a
   Riccati equation for $\beta=\sigma b(\sigma+i\xi)$ as $\sigma$ decreases.
2. Positivity at the doubled frequency $2\xi$ keeps $\beta$ away from the
   equation's unstable fixed point $-1$, uniformly in $\xi$.
3. The substitution $W=\beta/(1+\beta)$ removes the quadratic term, leaving
   a linear equation whose forcing depends on the solution but stays small.
   This bounds the resolvent of the equation for the Laplace transform of $f$,
   uniformly in $\xi$.
4. A local density bound for primes, from a quadratic sieve, controls the
   starting line and the high frequencies.

The proof stays in the half-plane where the Laplace transform converges
absolutely. It uses no analytic continuation and no zero-free region.

The argument applies to the general coupled-source setting of the paper's
Theorem 2.1: a positive measure $\nu$ with $\nu([0,t])=t+O(1)$, coupled to a
bounded source $f$ by a first-order equation and a Selberg-type relation
with bounded error. With a local density hypothesis it gives the energy
bound; without it, the same method proves $f\in L^2(0,\infty)$. This supplies the hypotheses of Wirsing's abstract
Tauberian theorem that the Selberg relation does not give directly. That
theorem, which Wirsing stated without a detailed proof, then gives
$f(t)=O(1/t)$, with a constant that may depend on the measure.

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
  elementary remainder proofs we examined (Kuhn, Wirsing, Bombieri) work
  with real-variable convolution inequalities; Bombieri uses the Laplace
  transform only to prove a convolution identity on the real axis. The
  analytic proofs we examined (Wiener–Geller, the 3-4-1 argument, Tao) use
  the transform on the boundary line and give no rate. This
  argument uses the transform, never reaches the boundary, and gives a rate.
- **Positivity at $2\xi$ as a barrier for the flow.** The inequality is the
  one behind the 3-4-1 argument; the new part is using it to hold the flow
  away from $-1$ for a fixed time, uniformly in $\xi$, in place of
  analyticity.
- **The linearized resolvent.** The substitution removes the quadratic
  term; the remaining forcing depends on the solution but is small. The
  resolvent gives $f\in L^2$ in the general coupled-source setting without
  a density hypothesis. Through Wirsing's
  abstract theorem this makes his pointwise bound available beyond the
  arithmetic case. Wirsing obtained the corresponding input from arithmetic
  identities, which a general measure does not have.

The certificate continues the author's earlier work on sparse matrix
representations of the Mertens function, in particular
[*The singular spectrum of a sparse Mertens matrix*](https://doi.org/10.5281/zenodo.23004980),
whose Section 7.1 asks for explicit row coefficients with a uniform residual
bound. This paper supplies such coefficients, for a different family of
relations and an $\ell^1$ residual.

We did not find the three items above in the sources compared in Section 16
of the paper:
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
- The proofs were checked by separate fresh-context AI reviews, all using
  models from one AI provider. No human expert has
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
- `audit/`: the ledger of audit findings and dispositions.
- `ADMISSION.md`, `VERIFICATION.md`, `CORRECTIONS.md`, `CITATION.cff`,
  `MANIFEST.sha256`: release records.

## Role of AI

AI models did the derivations, literature search, exposition, and audits
under the author's direction. The author chose the question and is
responsible for the result and its corrections.

## License

GPL-3.0-only. See [LICENSE](LICENSE).
