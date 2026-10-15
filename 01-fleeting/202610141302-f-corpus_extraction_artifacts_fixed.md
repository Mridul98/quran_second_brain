# Corpus extraction artifacts fixed — trust the lines, but know the two classes
**UID:** 202610141302
**Type:** Fleeting / Scratchpad
**Date:** 2026-10-14

## Context
While seeding/building surahs 1–5, several passage agents flagged "typography quirks" in the corpus (e.g., "nursingmothers" at [2:233], "onethird" at [4:12] and [73:20], "twothirds" at [4:176]). Verified against the source PDF with pymupdf page-by-page text search.

## Observation / Question
There are **two distinct classes** of apparent quirks in this corpus:
1. **Extraction artifacts (FIXED 2026-10-14):** the PDF wraps hyphenated compounds at line ends ("one-\nthird", "nursing-\nmothers"), and the extractor's dehyphenation joined them without preserving the hyphen. All 4 occurrences corrected in corpus (s002, s004 x2, s073), and the extractor rule patched to keep hyphens after numeral fragments. The affected passage notes (p00230, p00402, p00424) were updated in place.
2. **Genuine book typography (REMAINS — do NOT "fix"):** the book itself prints unbalanced quotation marks (the quote opened at [2:215] is never closed; [2:222] closes with a stray ”; [4:176] ends a clause with a dangling ”; [5:116]'s quote opens unclosed; some lines use backtick-quotes e.g. [3:158]-ish "“/" mixed with `` ` ``; occasional mid-line capitalization like "And Remember" [5:7]). These are faithfully reproduced by the corpus — the corpus is a *facsimile*, not a copyedit. Quote them verbatim and, where relevant, gloss the fact rather than silently normalizing.

Also observed and left as-is: casing/term drift *within the book* itself ("Holy Month" [2:217] vs "Sacred Month" [5:2] vs lowercase "holy month" [2:194]; "Sabeans" [2:62] vs "Sabians" [5:69]; "Embracing"/"Bounteous" for *wad-si'u*), which is translation variance worth knowing, not an artifact.

## Next Steps
- [x] Fixed the 4 hyphen-join artifacts; patched `scripts/extract_pdf.py`; synced the 3 affected notes.
- [ ] When any note quotes lines with unbalanced quotes (2:215/222, 4:176, 5:116), keep the [sic] gloss — never normalize the book's typography in place; a future "edition typography map" could collect them.
- [ ] If re-extraction is ever run, re-diff corpus/ against a backup — the rule fix should be a no-op beyond these 4 lines.

## Related Notes
* [Basmala numbering in this edition](202610132006-f-basmala_numbering_in_this_edition.md)
