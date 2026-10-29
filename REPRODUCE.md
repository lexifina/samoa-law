# How this repository was made (Samoa)

This file is written by the build on 2026-10-30, the day the source data was retrieved.

## Sources

| Source | Address | Retrieved | Licence |
| --- | --- | --- | --- |
| MJCA Samoa, consolidated legislation | <https://mjca.gov.ws/legislation/legislation.html> | 2026-10-29 | Official legislation; no licence stated on mjca.gov.ws |
| MJCA Samoa, consolidated legislation: Criminal Procedure Act 2016 (official version as at 31 December 2024) | <https://firebasestorage.googleapis.com/v0/b/mjca-samoa.firebasestorage.app/o/legislation%2FCriminal%20Procedure%20Act%202016.pdf?alt=media> | 2026-10-30 | Official legislation; no licence stated on mjca.gov.ws |
| MJCA Samoa, consolidated legislation: Evidence Act 2015 (official version as at 31 December 2024) | <https://firebasestorage.googleapis.com/v0/b/mjca-samoa.firebasestorage.app/o/legislation%2FEvidence%20Act%202015.pdf?alt=media> | 2026-10-30 | Official legislation; no licence stated on mjca.gov.ws |
| MJCA Samoa, consolidated legislation: Labour and Employment Relations Act 2013 (official version as at 31 December 2024) | <https://firebasestorage.googleapis.com/v0/b/mjca-samoa.firebasestorage.app/o/legislation%2FLabour%20and%20Employment%20Relations%20Act%202013.pdf?alt=media> | 2026-10-30 | Official legislation; no licence stated on mjca.gov.ws |
| MJCA Samoa, consolidated legislation: Sale of Goods Act 1975 (official version as at 31 December 2024) | <https://firebasestorage.googleapis.com/v0/b/mjca-samoa.firebasestorage.app/o/legislation%2FSale%20of%20Goods%20Act%201975.pdf?alt=media> | 2026-10-30 | Official legislation; no licence stated on mjca.gov.ws |

Every word of law in this repository comes from these sources. Lexifina reads them and records each act's dated versions, and the laws that made each change, in one corpus file. This repository is built from that file.

## What is in it

| Act | Title | Versions | Span |
| --- | --- | ---: | --- |
| `constitution` | Constitution of the Independent State of Samoa 1960 | 1 | 2024-12-31 to 2024-12-31 |
| `crimes-act-2013` | Crimes Act 2013 | 1 | 2024-12-31 to 2024-12-31 |
| `companies-act-2001` | Companies Act 2001 | 1 | 2024-12-31 to 2024-12-31 |
| `property-law-act-1952` | Property Law Act 1952 | 1 | 2024-12-31 to 2024-12-31 |
| `criminal-procedure-act-2016` | Criminal Procedure Act 2016 | 1 | 2024-12-31 to 2024-12-31 |
| `evidence-act-2015` | Evidence Act 2015 | 1 | 2024-12-31 to 2024-12-31 |
| `labour-employment-relations-act-2013` | Labour and Employment Relations Act 2013 | 1 | 2024-12-31 to 2024-12-31 |
| `sale-of-goods-act-1975` | Sale of Goods Act 1975 | 1 | 2024-12-31 to 2024-12-31 |

The build made 8 commits:

| Commits | Kind |
| ---: | --- |
| 8 | first version of an act |
| 0 | one law on its in-force day |
| 0 | changes no amendment note explains, credited to the publisher |

Other counts:
- 0 commits on the branch `future`: laws not yet in force on 2026-10-30.
- 0 commits dated 1 January 1970: in force before 1970, with the real day in their `In-force` trailer.
- 0 laws in the record.
- 8 tags.

## Dates

Each commit is dated at noon (Pacific/Apia) on the day the change took effect. The other dates, enacted and published, are trailers.

When a law gives no date of its own, the default rule applies: Revision notes: "This is the official version of the Constitution as at 31 December 2024." The revised text is dated by that as-at day; no general rule on the entry into force of Acts was used. https://firebasestorage.googleapis.com/v0/b/mjca-samoa.firebasestorage.app/o/legislation%2FConstitution%20of%20the%20Independent%20State%20of%20Samoa%201960.pdf?alt=media

## How the history is built

`tools/build.py` turns the corpus into this history in one pass: one commit per law, on the day it took effect. The same corpus always gives the same commit hashes. `tools/check_repo.py` reads every version back from git and compares it with the corpus. `tools/on.py` shows the law as it stood on any date. The corpus format is described in `tools/SCHEMA.md`.

- Corpus: sha256 `438d97588995c0cfdc63f9d4b6ccc5139b23692c5a3dfe245e03e56e8b007ed3` (1817771 bytes).
- Builder blob hashes (`git hash-object`): `build.py` `a4faa25af85facb64b956b372f6b528aafdd7ec1`, `check.py` `3d00541d258745461ab52b1b0cb4e1716a27a95d`, `on.py` `644a6c0857fbcc72562032b58d57aa113fee0641`.
- Python 3.12.10; git version 2.46.0.windows.1.

## Checks

8 versions of 8 acts read back from git on the day each took effect and on the day before: 0 mismatches. Trailers: 0 commits whose trailers git cannot parse. Health: 0 merge commits on main, 0 commit dates that go backwards, 0 commits dated after the build.

A second build from the same corpus into an empty folder gave identical hashes for all 8 history commits and 8 tags (history tip `ab2eeae882462118fe0899afbc43a1324ea6c60c`).

## Decisions made by hand

- Single version: the Ministry publishes only the current revised Constitution, "as at 31 December 2024". It is recorded as the oldest version available, dated by that as-at day.
- Part and Division headings are kept as their own files; the Schedules (First and Second repealed, Third the forms of oath) are one file; the signatures of the Constitutional Convention and the Revision Notes are omitted.
- The two text columns of the PDF were read in reading order with pdftotext; running heads and page numbers were removed and wrapped lines joined.
- Statutes added in phase 2: each is the Ministry's official revised PDF "as at 31 December 2024", one version, recorded as the oldest version available and dated by that as-at day; unit files are Parts, Divisions, sections and schedules; running heads and page numbers removed, wrapped lines joined, subsection and paragraph labels split onto their own lines.
- Criminal Procedure Act 2016: the Ministry's official revised PDF "as at 31 December 2024", one version, recorded as the oldest version available and dated by that as-at day; unit files are Parts, Divisions, sections and schedules; running heads and page numbers removed, wrapped lines joined, subsection and paragraph labels split onto their own lines.
- Evidence Act 2015: the Ministry's official revised PDF "as at 31 December 2024", one version, recorded as the oldest version available and dated by that as-at day; unit files are Parts, Divisions, sections and schedules; running heads and page numbers removed, wrapped lines joined, subsection and paragraph labels split onto their own lines.
- Labour and Employment Relations Act 2013: the Ministry's official revised PDF "as at 31 December 2024", one version, recorded as the oldest version available and dated by that as-at day; unit files are Parts, Divisions, sections and schedules; running heads and page numbers removed, wrapped lines joined, subsection and paragraph labels split onto their own lines.
- Sale of Goods Act 1975: the Ministry's official revised PDF "as at 31 December 2024", one version, recorded as the oldest version available and dated by that as-at day; unit files are Parts, Divisions, sections and schedules; running heads and page numbers removed, wrapped lines joined, subsection and paragraph labels split onto their own lines.

## What AI did and did not do

The scripts that read the sources and build this repository were written by Claude Code running Claude Opus 5.5 (`claude-opus-5-5`) under Lexifina's direction.

No model wrote, translated or corrected legal text. No model runs at build time. Every word of law in this repository comes from the official sources above.

The commit messages are written by `build.py` from the source data.

Model use at data-build time:
- none
- none
- none
- none
- none
