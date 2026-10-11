# Verification record

This record covers the document build and the release files. It does not
check proofs; see `audit/LEDGER.md` for the proof reviews.

## Environment

- pdfTeX 3.141592653-2.6-1.40.22 (TeX Live 2021, MacPorts), default fonts
- Poppler `pdfinfo` / `pdftotext` 26.07.0
- macOS 26.6.2, `shasum` 6.01
- No Python is needed to build or check the paper.

## Commands

```sh
make paper                        # three pdfLaTeX passes; SOURCE_DATE_EPOCH=1791590400
make check                        # no TeX warnings or bad boxes, 30 pages, no "??"
shasum -a 256 -c MANIFEST.sha256  # every tracked file except the manifest itself
```

## Expected output

- `make check` prints the PDF title, author, subject and `Pages: 30`, then
  `check: PASS (document consistency only; not a proof check)`.
- Every line of `shasum -a 256 -c MANIFEST.sha256` reports `OK`.

## Clean reproduction

The commands above were run on 2026-10-11 in fresh `git archive` extractions
of the tagged candidate `v0.1.0`, with the tracked PDF deleted first and no
TeX auxiliary files. `make paper` and `make check` passed, and the rebuilt PDF
was byte-identical to the tagged `paper/main.pdf`.

The living repository adds the version DOI to the paper's title page, so its
PDF differs from the tagged one. A fresh `git archive` rebuild of the living
tree reproduces the living `paper/main.pdf` byte for byte
(SHA-256 `6c4a05c9e910994a1e999c826317d762c48a51a90dcdca901111764c81c9eff9`).

## Exclusions

Build auxiliaries (`paper/*.aux`, `*.log`, `*.out`, `*.toc`) are not tracked.
The release-audit tooling used during preparation is not part of the release.
