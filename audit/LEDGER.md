# Audit ledger

Append-only. Each entry records the audit scope, the pinned input, the
auditor type, findings, and dispositions. AI auditors are process-separated
AI reviewers, not independent experts.

## 2026-10-11 — candidate audits at 168664d

Pinned input: commit 168664d; paper/main.tex sha256
af6f56834261d5f7be009d0d79f2a8fec164f9678936f227dcbc7299dfa7041a.
Four read-only audits ran in parallel in fresh contexts. All four auditors
are Claude models (two Opus, two Sonnet) under the same AI provider; they
are process-separated AI auditors, not independent experts. Raw findings are
summarized below with their dispositions; all fixes are in the next commit.

### Proof audit, analytic half (Sections 2–8, Remarks 16.1–16.3, Appendix A) — PASS

Hand re-derivation of every statement in scope, including the Riccati
derivation and constants, the exclusion lemma numbers, the resolvent decay,
translation and tail estimates, the Poisson start line, closure, the
Section 8 interval bound and L2 theorem, the self-convolution identity, the
hypothesis map against Wirsing II p. 15, both examples in Section 16, and
Appendix A. No proof defects. Optional findings:

| ID | Finding | Disposition |
|---|---|---|
| F1 | "exactly the missing hypothesis" overstates: L2 supplies the O(1) remainder and f -> 0 | Fixed: "supplies the hypotheses ... that the Selberg relation does not give directly" (abstract, Section 1, README, CFF) |
| F2 | Lemma 8.1 cites (2.1)–(2.3) but uses other hypotheses of Theorem 2.1 | Fixed |
| F3 | (8.8) derived only for t >= t_delta | Fixed: small-t range added |
| F4 | Remark 16.2 identification "up to a constant" omits O(e^-t); dangling referent | Fixed |
| F5 | Satz 2 list omits "as xi -> infinity", "eta < xi", countable exception | Fixed |
| F6 | "does not supply the self-convolution equation" is informal | Fixed: "does not by itself bound f*f" |
| F7 | Satz 2 caveat missing from abstract | Fixed |
| F8 | "Selberg's formula implies" stronger than Section 16 | Fixed: "by elementary methods built on Selberg's symmetry formula" (paper, README, CFF) |
| F9 | Notation collisions (beta, g, v, e) | Partly fixed: Wirsing's exponent disambiguated; others left (local, unambiguous in context) |
| F10 | "a" used before defined in Section 3 | Fixed |
| — | "Section 5" of Wirsing II not confirmed from the scan | Not changed; consistent with the paper's page range |

### Proof audit, arithmetic and transfer half (Sections 1, 9–15, 17) — PASS

Verified the arithmetic instance of the hypotheses (including f(0) = -1),
Selberg's formula, the sieve and Proposition 10.2, the certificate,
coverage and flux formulas, coprimality removal, sampling, the
Cauchy–Schwarz step (no log log loss), Theorem 13.2, Corollary 13.3, the
floor remark, the Section 14 similarity and SVD identities, the Section 15
identities, and that open statements are never used as proved. Optional
findings:

| ID | Finding | Disposition |
|---|---|---|
| T1 | Period should be comma after (1.1) | Fixed |
| T2 | Corollary 13.3 proof omits log 2 <= t < 1 | Fixed |
| T3 | Bound on lambda_d skips a step | Fixed |
| T4 | Section 17 status omits the L2 theorem | Fixed |
| T5 | Mass bound in Section 12 unused | Not changed (harmless context) |
| T6 | "previously excluded primes" unclear | Fixed |
| T7 | Ray identity when X < 4 | Fixed: noted as trivial |

### Prose and claim audit — PARTIAL -> resolved

| ID | Finding | Disposition |
|---|---|---|
| P1 | README names MANIFEST.sha256 and VERIFICATION.md, not yet present | Fixed at freeze |
| P2 | ADMISSION.md stale (DRAFT, all PENDING) | Fixed at freeze |
| P3 | Satz 2 condition not near the claim (abstract, README, CFF) | Fixed |
| P4 | Process-history wording ("earlier estimate", "did not close") | Fixed |
| P5 | Optional: gloss technical terms in README; AI-role wording differs; title case differs; Section 17 closing | Not changed (optional; title case follows prior releases) |

### Citation and prior-art audit — PARTIAL -> resolved

Citation keys all resolve; metadata checked against Crossref and other
records. Searched corpus: Crossref, arXiv, web search, the author's four
public releases; sources dated 1937–2026; searches through 2026-10-11.
Not accessible: Diamond–Zhang monograph, Bateman–Diamond 1969, Zhang's
papers, Kahane full text, Richter's proof, Ingham's review.

| ID | Finding | Disposition |
|---|---|---|
| C1 | Must-fix: certificate (Sections 11–13) extends the author's sparse-Mertens program (singular-spectrum release, Section 7.1); not cited | Fixed: paragraph in Section 16.4, README sentence, bibliography (Kline 2019, 2020, 2020b; both releases). Root agent checked Section 7.1 of that release. Section 14 operators found in none of the four releases |
| C2 | Selberg 1949 footnote 2 on Beurling primes | Fixed (checked in the PDF) |
| C3 | Kahane 1997 L2 PNT for Beurling systems | Fixed (metadata from Crossref) |
| C4 | McNamara's dynamical proof using Selberg's formula | Fixed (metadata from Crossref) |
| C5 | Selberg sieve and Montgomery–Vaughan uncited | Fixed (Selberg 1947 pages from three bibliographic sources; MV from Crossref) |
| C6 | Debruyne–Vindas published version | Fixed |
| C7 | README should state B(t) = t + O(1) | Fixed (README and abstract) |
| C8 | Optional: Geller/Gellert spelling; Amitsur 1969 correction; Richter | Not changed |
| — | No source found for the method items (a)–(d); absence of hits is not evidence of non-existence | Novelty wording unchanged: bounded, priority not settled |
