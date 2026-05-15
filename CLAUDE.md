# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**temp_corrections_ap90** is a working repository for analyzing and applying a batch of corrections to the AP90 (Apte 1890) dictionary. The corrections originate from the CORRECTIONS repo's English spell-check error lists and cross-dictionary abbreviation comparison.

## Architecture

| File | Purpose |
|---|---|
| `ap90.txt` | AP90 entries flagged for review |
| `ap90_error.txt` | Source: `CORRECTIONS/english_error/output/ap90_error.txt` — English spell errors in AP90 |
| `md.txt` / `md_error.txt` | MD dictionary entries and errors (cross-reference) |
| `mw72.txt` / `mw72_error.txt` | MW72 entries and errors (cross-reference) |
| `shs.txt` / `shs_error.txt` | SHS entries and errors (cross-reference) |
| `wil.txt` / `wil_error.txt` | WIL entries and errors (cross-reference) |
| `yat.txt` / `yat_error.txt` | YAT entries and errors (cross-reference) |
| `remove_commas.py` | Utility to normalize comma usage in error files |
| `Apte.S2H.works.txt` | Apte abbreviations: Sanskrit-to-Human-readable name list |
| `Apte.S2H-.Names.of.works.or.authors.pdf` | PDF reference for Apte abbreviations |

## Workflow

1. Start from the CORRECTIONS repo's `english_error/output/<dict>_error.txt` files
2. Cross-reference errors with other dictionaries to distinguish genuine errors from intentional usage
3. Apply confirmed corrections via `updateByLine.py` to the source `csl-orig` files

## Dependencies

- **Python 3**
- **CORRECTIONS** sibling repo — source of `_error.txt` files
