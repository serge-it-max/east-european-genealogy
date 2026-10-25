# Ukrainian archives: where the records are and how to reach them

Ukrainian archives hold the records of the right-bank provinces of the Russian Empire
(Podolia, Volhynia, Kyiv), of New Russia (Kherson, Katerynoslav, Taurida) and of Austrian
Eastern Galicia. Most of what is online sits in four places: the archives' own sites, the
archives' FamilySearch copies, Wikimedia Commons with Ukrainian Wikisource, and volunteer
catalogues. Routes below were checked in October 2026; sites change, so check before you
trust one.

## The archives most often needed

| Archive | Short | What it holds for genealogy |
|---|---|---|
| Central State Historical Archive, Kyiv | TsDIAK | Kyiv Spiritual Consistory (f. 127: metric books, confession lists), the collection of metric books (f. 224: 18th-century books, including Podolian Uniate deaneries before 1795), the Kyiv central revision commission on nobility (f. 481, 1840s verification files) |
| Central State Historical Archive, Lviv | TsDIAL | Galician metric books (f. 201 Greek Catholic consistory and others), szlachta legitimation files (f. 165, op. 3), Przemyśl grod and land court books (f. 13, f. 14) |
| State Archive of Khmelnytskyi oblast | DAKhmO | Podolian province: treasury chamber revision tales (f. 226), consistory metric books and confession lists (f. 315), noble deputy assembly (f. 230) |
| State Archive of Vinnytsia oblast | DAVinO | Podolian revision tales and court books, estate records |
| State Archive of Odesa oblast | DAOO | Kherson consistory metric books (f. 37), New Russian revision tales |
| State Archive of Zhytomyr oblast | DAZhO | Volhynian consistory, Roman Catholic books |
| State Archive of Kyiv (city) | DAK | parts of 18th-century church records, including Uniate soul lists of right-bank deaneries |

Use the archive's own abbreviation and the triple fond / opys (inventory) / sprava (case)
in every note: "DAKhmO f. 315, op. 1, spr. 7049". A short form fond_opys_case ("315_1_7049")
helps when reading aloud and searching FamilySearch keywords.

## Catalogues

**ARCHIUM** (TsDIAL `archium.tsdial.archives.gov.ua`, TsDIAK `archium.cdiak.archives.gov.ua`;
some oblast archives run the same software). It searches down to case titles. The results
page loads by JavaScript, so call the endpoint directly:

    GET <host>/api/v1/search/act/?Search=<query>&Type=all&FondNumber=0&Page=1&Limit=100

The JSON carries rendered HTML rows "Fond N | Opys N | Sprava N | title | dates" (in Ukrainian). Matching
is stemmed. It indexes case titles, never names inside the files, and some fonds have no
case list online at all.

**TsDIAK list of FamilySearch-digitized cases** (`cdiak.archives.gov.ua/fs.php`). A table of
about a quarter of a million cases with the DGS number of the FamilySearch copy. Direct
query:

    https://cdiak.archives.gov.ua/project_data/search.php?fond_search=<F>&opys_search=<O>&sprava_search=<S>

Empty fields act as wildcards. Scripts get a 403 from the CDN; open it in the browser. Check
it before calling any TsDIAK case offline.

**uaroots.com.ua.** A volunteer catalogue of archive cases by settlement (about 140 000
cases, 26 000 settlements, TsDIAK, TsDIAL, oblast archives and some Polish ones), with a name
index for the cases volunteers have transcribed. For each village it lists every case that
mentions it: archive, fond/opys/case, years, type (metric book, confession list, other).
It needs a login; the user signs in, and Claude works in that browser tab through the
site's own search pages, one query at a time. Search results cap at 100; when a surname
gives more, narrow the query by place or year the way a reader would. Do not script the
site's internal API or page through its index in bulk.

Coverage of the name index is uneven: dense for some southern parishes after 1860, thin for
Podolia before 1870. Check the village's case list against your source table every time.

**rodometrika.** A catalogue of metric books by parish and year. It is one catalogue, and a
year missing there means "status unknown", never "lost". Write `not in rodometrika` in the
source table and re-check elsewhere.

**Duck Inspector** (`inspector.duckarchive.com`). Maps Ukrainian shelfmarks to online copies,
FamilySearch films among them. Live in October 2026; test it on a known pair before relying
on it, and pause between requests if it answers 429.

## Archive sites with scans

**DAOO e-archive.** The Odesa archive publishes scans as DjVu files with predictable paths:

    metric books:  https://archive.od.gov.ua/wp-content/old-files/EL_ARH/M/0037/0037_03/0101-0200/0037_03_0131_DAOO.djvu
    inventories:   https://archive.od.gov.ua/wp-content/old-files/EL_ARH/F/0762_01_DAOO.djvu

A metric-book case can run to hundreds of megabytes (the example above is about 260 MB).
Open one case when the user needs it; do not fetch a run of them.

Several villages of one district are often bound in one case. When a year is missing for
your village, look at the same year for neighbouring parishes: the shelfmark may already
be known there. A neighbour's shelfmark is a candidate to open, never an answer.

**DAKhmO** has an ARCHIUM catalogue and a public file server with scanned cases. **Ukrainian
Wikisource** carries many inventories (the pages in the archive namespace, "Arkhiv:"), and **Wikimedia Commons** carries
whole cases uploaded as PDF or DjVu, named by shelfmark ("DAKhmO 226-80-437. 1796." followed by the case
title in Ukrainian). A PDF page opens directly with
`https://commons.wikimedia.org/w/index.php?title=File:<name>&page=<N>`. Search Commons by the
shelfmark in both "226-80-437" and "f. 226, op. 80, spr. 437" forms, the latter in Ukrainian letters.

## FamilySearch copies

Most Ukrainian metric books and many revision tales are on FamilySearch as images, unindexed.
Read `familysearch-techniques.md`. Two Ukraine-specific points:

- The FamilySearch catalogue files the films under the archive and fond, and the place
  search lists them under the modern or the historical place name, often only one of them.
  Search both.
- Szlachta legitimation files of TsDIAL f. 165, op. 3 are filmed in alphabetical runs, several
  dozen cases per reel, and the catalogue's item number is a hint only. Map the reel by its
  divider cards (in `familysearch-techniques.md`).

## Publications

- Ukrainian historical journals are often in the NBUV journal repository. When its main site
  does not connect, the same PDFs come through the IRBIS-NBUV interface (UJRN database):
  search, find `Image_file_name=PDF/<code>.pdf` in the result, then download with
  `C21COM=2&I21DBN=UJRN&P21DBN=UJRN&IMAGE_FILE_DOWNLOAD=1&Image_file_name=PDF/<code>.pdf`,
  following redirects and sending a browser User-Agent.
- Printed armorials and szlachta studies cite fond and case in their footnotes. Read the
  footnotes, then the case; the text itself is a reconstruction.

## Searching names in Ukrainian sources

- Search the Ukrainian, Russian and Polish forms of a name and a village, each in its own script: Ukrainian
  «Бирлівка», Russian «Бирловка», Polish «Byrłówka».
- Uniate books of the 18th century often give Latin or Polish forms in a Cyrillic hand;
  priests sign in both scripts.
- Revision tales of szlachta and of peasants are separate files of the same revision. A
  family absent from the peasant tale may be in the szlachta or odnodvortsy tale of the same
  year.
