# Basmala is unnumbered in this edition except 1:1 — a numbering decision, not a neutral layout
**UID:** 202610132006
**Type:** Fleeting / Scratchpad
**Date:** 2026-10-13

## Context
Seeding the brain before documenting Surah 1. Noticed while verifying the corpus extraction; it will matter most to the Fatihah passage note (1:1–7) and every surah index header row.

## Observation / Question
In the corpus (Itani, ClearQuran edition A — Kufi/6236 numbering):
* `corpus/s001_al-fatihah.md` prints the basmala **as numbered ayah `[1:1]`**.
* Every other surah file carries it as an **unnumbered header line** (`Basmala: In the name of Allah, the Gracious, the Merciful`) captured from the book's title pages.
* `corpus/s009_at-tawbah.md` has **no Basmala header at all** — matching the transmitted exception for surah 9.
* The only numbered mid-corpus occurrence is inside Solomon's letter: `[27:30]` "It is from Solomon, and it is, 'In the Name of Allah, the Gracious, the Merciful." (capital "Name" — distinct rendering inside quoted text).

So this edition's numbering treats the basmala as an ayah in al-Fatihah only. Widely cited legal positions: Shafi'i — numbered ayah at every surah head except 9; Hanafi — ayah in Fatihah only; Maliki/Hanbali narrations — not an ayah at all. If correct, the corpus layout is the Hanafi/Kufi position made typographic — consistent with the 556-ruku Idad-e-Quran partition we use.

Consequences:
* In mushaf editions numbering the section basmala as ayah 1, verse refs in every surah except 1 and 9 shift by one. Pin all `[s:a]` refs to this corpus's scheme.
* Never treat "the basmala opens every surah" as a *verse*-claim in this brain; it is layout in this edition (Source: observable corpus fact).

## Next Steps
- [x] Confirmed the only numbered basmala lines are [1:1] and [27:30] via `rg "\] In the name" corpus/`.
- [ ] Verify the madhhab positions against a primary tafsir source (Ibn Kathir / al-Qurtubi on 1:1) before any Knowledge note restates them.
- [ ] When documenting Fatihah r1, link this note into the passage's Related Notes.

## Related Notes
* [Guidance as a road with conditions](../02-knowledge/202610132000-k-guidance_hudan_lil_muttaqin.md)
