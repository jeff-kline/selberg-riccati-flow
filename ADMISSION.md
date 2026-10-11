# Admission record — selberg-riccati-flow

Current verdict: ADMITTED.
State: ADMITTED, version 0.1.0 (2026-10-11).
Standard: Jeff Kline's public research standard,
https://jeff-kline.github.io/posts/research-program/index.html

Admission is a release decision under that standard. It is not peer review or
a correctness certificate.

## Release record

| Item | Value |
|---|---|
| Tag | `v0.1.0` (annotated, tag object `881678276b2f80a8dcf2d7c82bb92a305f0902d2`) |
| Tagged commit | `22dcb5bbdb382ef3c09d8334757c5bb15b62235f` |
| GitHub Release | https://github.com/jeff-kline/selberg-riccati-flow/releases/tag/v0.1.0 (2026-10-11 17:29 UTC) |
| Version DOI | https://doi.org/10.5281/zenodo.23301917 (Zenodo record 23301917) |
| Concept DOI | https://doi.org/10.5281/zenodo.23301916 |
| Archive route | Zenodo GitHub integration |
| Archived file | `jeff-kline/selberg-riccati-flow-v0.1.0.zip`, 471810 bytes, SHA-256 `9bb7f871cbf58a3cda93302042d3915a09deee80ad79d3c39eb67b7a4fe019e9`, MD5 `2e3a27a312f34be9936c014e66d0bfbc` (matches Zenodo's checksum) |
| Byte identity | the Zenodo file equals the GitHub API tag zipball, downloaded twice before the Release and pinned |
| Secondary check | `git archive v0.1.0` (zip, twice): SHA-256 `9cee724672530947905f7d5cbbf5fc2dc62c1ebcf271fce83917ba45164cd0bd`; deterministic, not expected to equal the provider zip |
| Zenodo metadata | title, creator (Kline, Jeffery), version `v0.1.0` (the tag name), date 2026-10-11, license GPL-3.0-only, type software, repository link at `v0.1.0`: all checked |

The tagged snapshot keeps its prepublication "release candidate" wording; the
DOI was added only to this living repository.

## Action owners

| Action | Owner | Status |
|---|---|---|
| Local edits and tests | author, with AI assistance | done |
| Create GitHub repository and push | Claude, on the author's authorization | done 2026-10-11: repository jeff-kline/selberg-riccati-flow |
| Make the repository public | Claude, on the author's instruction | done 2026-10-11 |
| Tag v0.1.0 and GitHub Release | Claude, on the author's authorization | done 2026-10-11 |
| Living metadata with DOI | Claude, on the author's authorization | done 2026-10-11 |
| Enable the repository in Zenodo | author (Zenodo portal) | done 2026-10-11 |
| Public-site listing | Claude, on the author's approval of title and blurb | live 2026-10-11 (jeff-kline.github.io commit 04a7c9e, Pages build verified): "Prime number theorem with remainder via a Riccati flow" |

Archive route: Zenodo GitHub integration. The DOI was minted after the GitHub
Release, so the tagged candidate carries no DOI; the living repository does.

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
| Tag | PASS | `v0.1.0` -> `22dcb5b`, annotated, never moved |
| Archive | PASS | Zenodo record 23301917 holds the pinned tag zipball, byte-identical |
| Citation | PASS | version DOI 10.5281/zenodo.23301917 resolves; README, CITATION.cff and paper cite it |
| Metadata | PASS | Zenodo title, creator, version, date, license and type match |

Verdict: ADMITTED 2026-10-11. Admission is a release decision, not peer review
or a correctness certificate. Named residual risks: the pointwise bound without
the density hypothesis relies on Wirsing's Satz 2, which he stated without a
detailed proof; priority of the method is not settled (Diamond–Zhang, Ingham,
Wright, Amitsur and Bateman–Diamond were not consulted); all audits were by AI
models from one provider; no human expert has reviewed the proofs.
