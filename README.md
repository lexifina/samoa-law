# Samoa: law history in git

The law of Samoa as a git history. Each provision is one file, each law gets one commit on the day it took effect, and the law that made each change is the commit's author. `git blame` names the law behind every paragraph and `git log` lists every change to an article.

It follows the shared design of [lexifina/global-law](https://github.com/lexifina/global-law), which places it at `ws/`.

This is a first build: the Constitution and, added in phase 2, core statutes (criminal law and procedure, evidence, companies, sale of goods, property and labour law). The Ministry publishes one current revised text of each Act, so each has one version, the oldest version available.

## What is in it now

| Folder | Act | Versions | History |
| --- | --- | ---: | --- |
| `constitution/` | Constitution of the Independent State of Samoa 1960 | 1 | Official revised version as at 31 December 2024; earlier versions are not published online by the Ministry |
| `companies-act-2001/` | Companies Act 2001 | 1 | Official revised version as at 31 December 2024; earlier versions are not published online by the Ministry |
| `crimes-act-2013/` | Crimes Act 2013 | 1 | Official revised version as at 31 December 2024; earlier versions are not published online by the Ministry |
| `property-law-act-1952/` | Property Law Act 1952 | 1 | Official revised version as at 31 December 2024; earlier versions are not published online by the Ministry |
| `criminal-procedure-act-2016/` | Criminal Procedure Act 2016 | 1 | Official revised version as at 31 December 2024; earlier versions are not published online by the Ministry |
| `evidence-act-2015/` | Evidence Act 2015 | 1 | Official revised version as at 31 December 2024; earlier versions are not published online by the Ministry |
| `labour-employment-relations-act-2013/` | Labour and Employment Relations Act 2013 | 1 | Official revised version as at 31 December 2024; earlier versions are not published online by the Ministry |
| `sale-of-goods-act-1975/` | Sale of Goods Act 1975 | 1 | Official revised version as at 31 December 2024; earlier versions are not published online by the Ministry |

The per-act `README.md` in each folder lists every provision.

## Where the text comes from

The text is the Constitution of the Independent State of Samoa 1960 as published by the Ministry of Justice and Courts Administration of Samoa (MJCA, mjca.gov.ws), the official version revised by the Legislative Drafting Division under the Revision and Publication of Laws Act 2008, retrieved on 29 October 2026. Its Revision Notes say: "This is the official version of the Constitution as at 31 December 2024." The Ministry's published PDF has a born-digital text layer.

The Acts are the Ministry's official revised versions of the same kind, each "as at 31 December 2024" by its own Revision Notes; the Criminal Procedure, Evidence, Labour and Employment Relations and Sale of Goods Acts were retrieved on 30 October 2026.

Language: English (the Constitution is also authoritative in Samoan, which is not in this record).

## Not included yet

- The Samoan-language text of the Constitution.
- Earlier versions of the Constitution and the Constitution Amendment Acts that made each change (the Revision Notes list them, but their texts are not in this record).
- Every other Act of Samoa. The Ministry also publishes some 270 consolidated Acts; only those listed in the table above are in this record.

## Dates

The single version is dated 31 December 2024, the day the Ministry states the revised Constitution is "as at". It is not the day the Constitution took effect (it came into force on Independence Day, 1 January 1962); the record has no older text. The commit is dated noon, Pacific/Apia, on that day, and is authored by the publisher as "oldest version available".

## How it is checked

Every version is read back from git on the day it took effect and on the day before; both must match the corpus the repository was built from. The results are in `REPRODUCE.md`.

## How it is built

Lexifina reads the sources listed here and records each act's dated versions, and the laws that made each change, in one corpus file. `tools/build.py` writes this repository from that file, and the same corpus always gives the same commit hashes; `REPRODUCE.md` gives the details and the checks. A model (Claude) wrote Lexifina's code; it wrote no legal text, and no model runs when the history is built.

Lexifina reads the sources listed here and records each act's dated versions, and the laws that made each change, in one corpus file.

## What "author" means

The author of a commit is the law that made the change. Its e-mail address cannot exist, so `git blame` and `git log --author` name laws. A version with no law of its own (the oldest version available) is authored by the publisher and says so. The committer is always Lexifina.
