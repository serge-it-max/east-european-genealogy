# Keeping the research record

A family-history project runs for years and across many sessions. The agent starts every
session with no memory, so the written record is the project. These are the formats that
held up, and the failure each one answers.

## The source table of a parish

One file per parish, one continuous table by year:

| Year | Shelfmark | Births | Marriages | Deaths | Online copy | State |
|---|---|---|---|---|---|---|

- **Never drop a year.** An empty row shows where the gap is.
- **The shelfmark column records an observation.** Use three kinds of value: a known
  shelfmark; `not in <catalogue>` (status unknown, a reason to re-check); `lost (checked
  <date>: <list>)`, allowed only after checking at least three independent places.
- **Re-check cheapest first:** the same year in neighbouring parishes' tables (several
  villages share one case), the film's groupId, then the case itself. A neighbour's
  shelfmark is a candidate to open.
- **Never remove a link to a scan because a catalogue is silent.** A live scan outweighs
  the absence of a row in a list.
- **The State column records how far the book has been read**: entered in full, read for
  some surnames only (say which), not started. Keep it in this table; a section heading
  alone gets lost. A project re-read a book it had already processed in full because the
  state sat under a heading nobody searched.

Below the table, keep the lasting context of the parish: the clergy and their years, where
the books begin, features of the source, family analyses with dates.

## Leads

A lead is anything that points further. Each one goes into the tracker in the same step it
is written, with:

- the file section and the shelfmark it comes from;
- an availability label: `[online]`, `[offline]`, `[not checked]`, or `[mixed]` with the
  split. `[online]` and `[offline]` need evidence in the item: a scan count, "no scans" in
  the catalogue, reading room only. Unknown stays `[not checked]`; never guess.

When a check settles the label, change it in the same step. When a lead is worked through,
tick it with a link to the result. Never close a task that still holds unticked leads;
move them to an open task first and say where. One project once closed a task holding 86
open leads, and another found 109 leads without a label, which every session then
re-checked from scratch.

## Rejected versions

Keep one register of rejected and settled versions per family line: the claim, why it fell,
the date, the source that settled it. Before taking up a "new" idea on a line, read that
line's register. Mark the original section in its heading ("rejected, see register") and
keep its text; deleting it invites the same idea back in a month.

Run a short cleanup once a week: move the week's rejected versions to the registers, mark
stale "next steps", look for entries that contradict earlier ones in the same file.

## Persons and places in a database

- **Search first, create second.** Before creating a person, look for the parents by name,
  surname and patronymic, and look at the candidate's family.
- **A person with no anchor stays local.** Godparents, priests and unrelated couples go into
  the local database only. Promote them when they turn up again as real kin.
- **Weak links are comments.** A relationship row needs evidence that would convince a
  stranger; a patronymic alone writes a comment on both persons.
- **Namesakes kept apart get the ban in words** on both records ("do not merge: different
  person, see …"). Code will not read it, so check by eye before any merge.
- **Merges go through one tool** that records the reason and keeps the merged record's
  spelling as an alias. One-off merge scripts leave no trace and break the next import.
- **Places:** a settlement-type prefix or a change of district does not create a new place;
  record the old form as an alias. Two rows are one place when they share people, or when
  both give a district and the districts do not contradict (one inside the other, the same
  land in two languages, a district split off from another). A row with no district links
  nothing on its own.
- **Raw data stays raw.** Keep downloaded snapshots and dictated lines unchanged, dated;
  new data is a new snapshot. Interpret in code, never by editing the raw file.
- **Ask the database before the file history.** Batch entry often goes straight into the
  database. Before saying "this was not entered", query it.

## Citations and ages

Store a citation per record (archive, case, folio or image, entry number), and link facts
to it; one entry usually supports several facts. Store each stated age as its own row
(person, source, year, age) and take the median when several exist. The tree's dates stay
canonical: a source's disagreement goes into the source's row.
