# Structure

| Folder | What it holds |
| --- | --- |
| `constitution/constitution/` | The Constitution of the Independent State of Samoa 1960, one file per article |
| `act/<year>/<name>/` | An Act of Samoa, by the year in its title, e.g. `act/2013/crimes/` (Crimes Act 2013) |
| `ordinance/<year>/<name>/` | An Ordinance (the law of Western Samoa before independence, still in force), e.g. `ordinance/1961/infants/` |
| `data/` | `paths.json` (act id to folder), `versions.json` (every act's versions and source PDF), charts |
| `tools/` | `on.py` (the law on a day), `check_repo.py` and the build tools |

Inside an act's folder there is one file per provision: `sec-NNN.md` a section (`sec-012-a.md` section 12A),
`part-NN.md` a Part heading, `div-<...>.md` a Division heading, `sched-NN.md` a Schedule, `enacting-formula.md` the
long title and enacting words; `README.md` lists them. No folder holds more than 1,000 entries.

Dates: each commit is dated noon Pacific/Apia on the day its text is in force from (`In-force:` trailer). The
Ministry publishes one revision of each act, "as at 31 December 2024" (`In-force-basis: as-at`), so each act has one
version so far; later revisions and Acts passed after that day go on top as new commits.
