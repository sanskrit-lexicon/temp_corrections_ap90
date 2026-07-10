# temp_corrections_ap90

_Created: 14-06-2026 · Last updated: 11-07-2026_

Working repository for analyzing a batch of English spell-check corrections for the
**AP90** (Apte 1890) Sanskrit–English dictionary, cross-referenced against several
sibling Cologne dictionaries. Part of the [sanskrit-lexicon](https://github.com/sanskrit-lexicon)
project (Cologne Digital Sanskrit Dictionaries).

> This is a **staging / analysis workspace**, not a delivery repo. Corrections are
> reviewed here; confirmed changes are applied to the canonical `csl-orig` sources
> through the standard correction workflow, not committed back into these `.txt`
> exports.

## Status

Active as of July 2026. Source `*_error.txt` lists are drawn from the
[sanskrit-lexicon/CORRECTIONS](https://github.com/sanskrit-lexicon/CORRECTIONS)
English spell-check pipeline (`english_error/output/`). Two issues have been filed
against this repo — one still open (a `question`/`trivial` query on SHS corrections,
June 2026), one closed (Apte 1965 literary-source transcode). No corrections have
yet been promoted from this workspace into `csl-orig` via a committed change file.

## Contents

| File | Purpose |
|---|---|
| [`ap90.txt`](https://github.com/sanskrit-lexicon/temp_corrections_ap90/blob/main/ap90.txt) | AP90 dictionary text (source under review) |
| [`ap90_error.txt`](https://github.com/sanskrit-lexicon/temp_corrections_ap90/blob/main/ap90_error.txt) | English spell errors flagged in AP90 (370 lines), from `CORRECTIONS/english_error/output/ap90_error.txt` |
| [`md.txt`](https://github.com/sanskrit-lexicon/temp_corrections_ap90/blob/main/md.txt) / [`md_error.txt`](https://github.com/sanskrit-lexicon/temp_corrections_ap90/blob/main/md_error.txt) | MD dictionary text + errors (cross-reference) |
| [`mw72.txt`](https://github.com/sanskrit-lexicon/temp_corrections_ap90/blob/main/mw72.txt) / [`mw72_error.txt`](https://github.com/sanskrit-lexicon/temp_corrections_ap90/blob/main/mw72_error.txt) | MW72 text + errors (cross-reference) |
| [`shs.txt`](https://github.com/sanskrit-lexicon/temp_corrections_ap90/blob/main/shs.txt) / [`shs_error.txt`](https://github.com/sanskrit-lexicon/temp_corrections_ap90/blob/main/shs_error.txt) | SHS text + errors (cross-reference) |
| [`wil.txt`](https://github.com/sanskrit-lexicon/temp_corrections_ap90/blob/main/wil.txt) / [`wil_error.txt`](https://github.com/sanskrit-lexicon/temp_corrections_ap90/blob/main/wil_error.txt) | WIL text + errors (cross-reference) |
| [`yat.txt`](https://github.com/sanskrit-lexicon/temp_corrections_ap90/blob/main/yat.txt) / [`yat_error.txt`](https://github.com/sanskrit-lexicon/temp_corrections_ap90/blob/main/yat_error.txt) | YAT text + errors (cross-reference) |
| [`remove_commas.py`](https://github.com/sanskrit-lexicon/temp_corrections_ap90/blob/main/remove_commas.py) | Utility to normalize comma usage in error files |
| [`Apte.S2H.works.txt`](https://github.com/sanskrit-lexicon/temp_corrections_ap90/blob/main/Apte.S2H.works.txt) | Apte abbreviations: source-abbreviation → human-readable name list (202 lines) |
| [`Apte.S2H-.Names.of.works.or.authors.pdf`](https://github.com/sanskrit-lexicon/temp_corrections_ap90/blob/main/Apte.S2H-.Names.of.works.or.authors.pdf) | PDF reference for the Apte abbreviations |

The cross-reference dictionaries (MD, MW72, SHS, WIL, YAT) are present so a spelling
flagged in AP90 can be checked against how the same or a related headword is spelled
elsewhere, distinguishing a genuine scan/typo error from intentional usage (Latin,
technical, or proper-name forms).

## Workflow

1. Start from the `CORRECTIONS/english_error/output/<dict>_error.txt` lists.
2. Cross-reference each flagged form against the sibling dictionaries here to
   separate genuine errors from intentional usage.
3. Apply confirmed corrections to the canonical `csl-orig` AP90 source through the
   Cologne correction workflow (`updateByLine.py` change files), documented in
   [csl-corrections/docs/correction-workflow.md](https://github.com/sanskrit-lexicon/csl-corrections/blob/main/docs/correction-workflow.md).
   Corrections are **never** made directly to source files — they are expressed as
   change files applied by scripts.

## Dependencies

- **Python 3** — for [`remove_commas.py`](https://github.com/sanskrit-lexicon/temp_corrections_ap90/blob/main/remove_commas.py).
- [sanskrit-lexicon/CORRECTIONS](https://github.com/sanskrit-lexicon/CORRECTIONS) —
  upstream source of the `*_error.txt` spell-check lists.

_Dr. Mārcis Gasūns_
