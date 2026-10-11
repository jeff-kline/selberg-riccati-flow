# Admission record — selberg-riccati-flow

State: CANDIDATE, version 0.1.0 (frozen 2026-10-11). Verdict: NOT YET ADMITTED.
No tag, archive or DOI yet.
Standard: Jeff Kline's public research standard,
https://jeff-kline.github.io/posts/research-program/index.html

## Action owners

| Action | Owner | Status |
|---|---|---|
| Local edits and tests | author, with AI assistance | done for the candidate |
| Create GitHub repository and push | requires the author's authorization (freeze bundle) | not started |
| Tag v0.1.0 and GitHub Release | requires the author's authorization (freeze bundle) | not started |
| Enable the repository in Zenodo | author (Zenodo portal) | not started |
| Public-site listing and living metadata | requires the author's authorization (admission bundle) | not started |

Archive route: Zenodo GitHub integration. The DOI is minted only after the
GitHub Release, so the candidate carries no DOI and CITATION.cff has no
release date.

## P1 — prior work and credit

| Check | Status | Note |
|---|---|---|
| Closest work | PASS | Selberg, Erdős, Kuhn, Breusch, Wirsing I–II, Bombieri, Wiener–Geller, 3-4-1, Tao, Saidak, Hildebrand, Debruyne–Vindas, Kahane, McNamara; the author's sparse-Mertens papers and releases (Section 16) |
| Original sources | PASS | Wirsing I–II, Bombieri, Kuhn, Selberg 1949, Saidak, Debruyne–Vindas, McNamara read or checked in the original; metadata checked against Crossref |
| Contribution type | PASS | new proof method and an L2 estimate; arithmetic bounds and the abstract Tauberian theorem credited to Wirsing; certificate credited as continuing the author's program |
| Novelty | PASS | bounded to the sources listed in Section 16.3; "priority not settled" stated in paper and README |
| Residuals | PASS | not consulted: Ingham's review, Wright 1952, Amitsur 1961, Diamond–Zhang, Bateman–Diamond, Zhang, Richter |

## A1 — claim and artifact consistency

| Check | Status | Note |
|---|---|---|
| Principal claim | PASS | two proof audits covering the paper end to end: no proof defects; optional findings resolved |
| Scope | PASS | dependence on Wirsing's Satz 2 (stated without detailed proof), the density hypothesis, and pair-dependent constants stated next to the claim |
| Evidence | PASS | proofs, cited classical results, prior-work comparison and AI audits kept separate |
| Credit | PASS | arithmetic bounds classical; pointwise bound and Satz 2 Wirsing's |
| Public prose | PASS | README introduction mirrors the abstract; prose audit findings resolved |
| Metadata | PASS | title, author, version and status agree across paper, README and CITATION.cff |
| Adversarial check | PASS | four AI audits, findings and dispositions in audit/LEDGER.md; not peer review |

## R1 — release and stewardship

| Check | Status | Note |
|---|---|---|
| Reproduction | PASS | clean build from `git archive` of the candidate is byte-identical; see VERIFICATION.md |
| Artifact integrity | PASS | MANIFEST.sha256 covers every tracked file except itself |
| Hygiene | PASS | no private paths, credentials or placeholders in tracked files |
| Stewardship | PASS | CORRECTIONS.md |
| Tag | PENDING | after authorization |
| Archive | PENDING | Zenodo GitHub integration |
| Citation | PENDING | DOI after archive |
| Metadata | PENDING | Zenodo record check after archive |

Verdict: NOT YET ADMITTED. Admission is a release decision, not peer review or
a correctness certificate.
