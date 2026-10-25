---
name: east-european-genealogy
description: Runs archival family-history research for the Russian Empire (Ukraine, Russia), Austrian Galicia and the Polish-Lithuanian Commonwealth, 1600 to 1900. Covers where to look first (lists of families before metric books), reading Cyrillic cursive and Latin parish forms without false readings, identifying people by the family around them instead of by name and age, recording what a source shows apart from what it implies, and tracking every lead until it is closed. Use whenever the user researches ancestors in Ukrainian, Russian, Polish or Galician archives, dictates or transcribes old metric records, asks where the records of a village or family are, wants a FamilySearch film or an archive case found, or asks whether two people in old records are the same, including casual phrasings like "find my great-great-grandfather's parents", "is this the same Ivan" or "what does this word in the scan say". Not for living people or 20th-century records.
---

# East European genealogy

This skill holds the working rules of a long-running family-history project: four family
lines, about sixteen thousand people, and archives in Ukraine, Poland and Russia. Every
rule below exists because breaking it once produced a wrong ancestor, a lost lead or a
wasted week. The reasons are written next to the rules on purpose. Without the reason, a
rule looks optional the first time it gets in the way.

The period is 1600 to 1900. Before 1600 there are almost no family-level records; after
1900 the sources change (civil registration, Soviet records) and other tools fit better.

## 1. Hard rules

These hold in every task. When a user instruction conflicts with one of them, say so once
and follow the user.

1. **Identify people by their family, never by name, age or place alone.** Two men with the
   same name and patronymic in the same village a generation apart are the normal case in
   these records. A match needs the family around the person: spouse, parents, children,
   siblings, house number, godparents. A wife is found through her husband, a child through
   both parents.
2. **Lists of families first, metric books second.** Start every search from lists that
   show whole households: confession lists, revision tales, tax and inventory lists. Read
   year-by-year metric books only around what a list points to, for an expected event or a
   specific year. Paging through metric books blind is the most expensive way to find
   nothing.
3. **Record the observation, never the conclusion.** "The year is not in catalogue X" is an
   observation. "The book did not survive" is a conclusion, allowed only after checking at
   least three independent places, with the date and the list of what was checked.
4. **Absence of a hit is not absence of the record.** A search that returned nothing says
   what was searched, with which spellings, where. Write that down, so the next session does
   not repeat it or, worse, trusts it.
5. **Check a doubtful letter against a known word on the same sheet.** When you look for a
   specific surname, the eye completes it from similar outlines. One session "found" the
   same sought surname root four times in a row, and all four were other names. Any reading
   that matches what you hoped to find stays unconfirmed until a reference word on the same
   page settles the doubtful letter.
6. **Documents outrank reconstructions.** When a published genealogy, an armorial or an
   online tree disagrees with a document you have read, keep the document's version as the
   primary one. Record the disagreement as a note; never enter the secondary version as a
   relationship.
7. **Weak evidence goes into a note. The tree takes only proven links.** A link that rests
   on a patronymic alone, or on a surname and a village, is a hypothesis. Write it as a comment on both
   persons, with what would confirm or refute it.
8. **Every lead is tracked the moment it is written.** A lead is anything that points
   further: an unread case, a "not checked" mark, a side finding. Put it in the tracker the
   user uses (an issue, a checklist item, a plan file) in the same step, with its
   availability label. A lead that lives only in prose gets lost; this happened often
   enough to make it a rule.
9. **The user passes bot checks and logins.** Never solve a CAPTCHA, never enter a password,
   never use a solver, proxy or fingerprint trick. Open the page, tell the user which tab
   and what to pass, wait, then continue. Never write a source off as "blocked" without
   asking the user to pass the check first.
10. **No invented facts.** No guessed IDs, dates or shelfmarks in notes. If a value is not in
    front of you, write that it is unknown.

## 2. The research cycle

### 2.1 Fix the question and the family

Write one research question: who, which link, which period. Then collect what is already
known about the whole family around the target person: every child, every
spouse, every godparent, every village. The answer to "who were his parents" is usually
found through a sibling's marriage or a child's baptism more often than through his own record.

If the user keeps a database or a tree, query it first. Ask for the known relatives and
their villages before any outside search. A concrete cross-reference with the user's own
data beats general historical context every time; context is background for a lead, never
the lead itself.

### 2.2 Build the place model

For each village, find the administrative chain **on the date of each record**: state,
province (guberniya / województwo / crown land), district (uyezd / powiat / Kreis, later
Bezirk), parish,
deanery, and for the Orthodox and Greek Catholic churches the eparchy. Districts were split
and renamed many times. The district a family "moved" to is often the same land under a new
name.

A settlement-type prefix (village, sloboda, hamlet) or a change of district does not make a
new place. Treat the old form as an alias of the same place. Two places of the same name
are one place only when they share people, or when both give a district and the districts
do not contradict each other. A row with no district links nothing on its own.
Read `references/research-records.md` before merging or creating places in a database.

### 2.3 Find the lists

For each target village and period, list which family lists exist and where. The kinds, in
rough order of usefulness:

- revision tales (revizskie skazki), Russian Empire, ten revisions from 1719 to 1858;
- confession lists (ispovednye vedomosti), Orthodox; Greek Catholic and Roman Catholic
  status animarum and Easter confession lists;
- Polish-Lithuanian tax registers: podymne (hearth tax), pogłówne (poll tax), ofiara;
- estate inventories (inwentarze), owner and inhabitant lists, land registers;
- nobility proofs: lists of szlachta, noble assembly cases, the 1830s-1840s nobility
  verification files in the former Polish lands.

Then read metric books only for the events and years the lists point to. Read
`references/sources-ukraine.md`, `references/sources-poland.md` or
`references/sources-russia.md` for the catalogues and search routes of each country.

### 2.4 Find the case online

A case catalogue saying "inventory only" or showing no scan says nothing about whether the
case is online. Before labelling a case offline, check:

1. the archive's own catalogue and its list of FamilySearch-digitized cases;
2. FamilySearch: the catalogue by place, and the image search by shelfmark keyword;
3. Wikimedia Commons and Wikisource, where volunteers upload Ukrainian archive cases;
4. volunteer catalogues and indexes for the region.

Read `references/familysearch-techniques.md` before working with unindexed FamilySearch
films. Most East European records there are images only and a name search will not find
them.

Archive sites change. When a route or URL from the references fails, tell the user it
failed, look for the current one on the site itself, and note the change with the date.

### 2.5 Read the source

Read `references/reading-manuscripts.md` before reading any 18th or 19th century
manuscript, and `references/record-conventions.md` before interpreting what a record says
about surnames, ages, estates and relationships.

The order for a long book:

1. **Map the film first.** Open every 15th to 20th image and write down the year and record
   type. You get a table "images N to M = births of year Y".
2. **Scan the key column.** Births: the father. Marriages: the groom, and the bride when you
   look for a daughter. Deaths: the deceased. Write down **every** occurrence of the
   surname, the unpromising ones included. Namesakes are separated later by house, parents
   and godparents, and that needs the full list.
3. **Read the found entry in full**, at full resolution: date, house number, child, parents
   and their parents when given, godparents, midwife, priest, margin notes.
4. **Write each entry down at once**: book, image, date, house, persons as written, notes,
   confidence. Keep the spelling of the source; put your normalized form beside it.

### 2.6 Decide identity

Read section 1, rule 1, again. Then:

- Compare the whole household across two or more lists. A family that has the same
  children in the right order with roughly right ages in two revisions is the same family.
- Use the house number. In Galician villages it often stays with a family for decades; a
  matching house is strong support, a different house is a reason to doubt.
- Ages are a loose check only (plus or minus two years, much more for the elderly). Read
  `references/record-conventions.md`, section on ages.
- A difference in recorded estate (noble, townsman, peasant) is no argument against a link.
  Impoverished szlachta lost rank across the 19th century, and some families rose.
- Keep two candidates as two persons until a distinguishing fact appears. A merge on thin
  data joins the wrong men, and splitting them later costs far more than waiting.
- When the user has decided that two namesakes are different people, write that decision on
  both records in words, so nobody merges them later by accident.

### 2.7 Record and track

After each unit of work:

- the source table of the parish gets its row (read `references/research-records.md`);
- every rejected version goes into the register of rejected versions for that family line,
  with the reason and date; the original section keeps a note in its heading;
- every lead goes into the tracker with an availability label: `[online]`, `[offline]`,
  `[not checked]`, or `[mixed]` with the split. `[online]` and `[offline]` need evidence:
  a scan count, a catalogue saying "no scans", an order-only note;
- a lead that gets worked through is marked done with a link to the result.

### 2.8 When the trail goes cold

Do not re-read the same sources a second time. Widen the circle:

1. open the leads already written down but never opened;
2. search by place instead of by surname: catalogues by village and its neighbours;
3. new kinds of source: estate archives of the landowner, court books, church visitations,
   published armorials and their footnotes, regional historical journals;
4. design the hypothesis of how the family entered the village: dowry, purchase of a share,
   service to a landowner, a priest's family, a neighbouring village whose name the surname
   carries (Serednytsky from Serednytsia);
5. add at least one new direction per session, and in the report keep new sources apart
   from repeated passes.

## 3. Working with the user

**Dictation mode.** When the user dictates records from a scan, process each record
silently: search, create, link, note. Do not confirm each record and do not recap. Speak
only for a real blocker: a required field missing, or a contradiction you cannot resolve.
Audit the whole batch at the end: missed matches with persons already in the tree, and
dictated details that did not make it into the data (a patronymic, an age, a house).

**Questions to the user.** Questions about identity and kinship are answered by documents
and by the family around the person; the user often knows less than the documents do.
Resolve the obvious cases yourself: a child with the same name, parents and birth date in
two copies of a record is one child. Put to the user only real choices of scope,
money or policy, a few at a time.

**Language.** Reply in the user's language. Quote sources in their original script and
spelling; never transliterate names you quote. Search in the language of the source.

**Scans.** Some users read the manuscripts themselves and want the agent to download, crop
and queue. Ask once which way the user works, and keep to it.

Read `references/agent-conduct.md` before launching background agents, running long
searches, or searching text in Cyrillic or Polish on Windows.

## 4. References

| File | Read it before |
|---|---|
| `references/reading-manuscripts.md` | reading any 18th-19th century manuscript or a doubtful word |
| `references/record-conventions.md` | interpreting surnames, women's names, ages, estates, margin notes |
| `references/sources-ukraine.md` | searching Ukrainian archives and their FamilySearch copies |
| `references/sources-poland.md` | searching Polish archives, Galician parishes, grod and court books |
| `references/sources-russia.md` | searching Russian provincial archives and service-people records |
| `references/familysearch-techniques.md` | working with unindexed FamilySearch films or its search |
| `references/research-records.md` | writing source tables, leads, rejected versions, places |
| `references/agent-conduct.md` | background agents, bot checks, Cyrillic and diacritics in tools |
