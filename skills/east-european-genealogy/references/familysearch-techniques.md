# FamilySearch for East European records

Most metric books, revision tales and court files of the region are on FamilySearch as
images with no index. A name search does not reach them; they have to be found as films and
read. The routes below were checked on 25 October 2026 and run from a browser tab where the
user is logged in. Never handle the user's password; the user signs in. Read "Pace and the
Terms of Use" below before any work on the site.

## Finding the film

1. **Catalogue by place.** Search the historical and the modern name, in every language of
   the period. One village can be filed under one of them only.
2. **Image search by shelfmark keyword.** Many films carry the archive shelfmark as a tag.
   In Records → Images, use "More options" → Keyword with the short form **in quotation
   marks**:

       https://www.familysearch.org/en/records/images/search-results?keyword=%2237_4_60%22

   Without the quotes it returns nothing. Letter suffixes keep the archive's script
   («37_1а_65» with a Cyrillic а). Run a control first, a shelfmark from the same fond and
   inventory that you know is there, and take the control's shelfmark from FamilySearch
   itself; your notes may be wrong. A wrong control once made a whole inventory look untagged.
3. **The archive's own list of digitized cases**, where one exists (`sources-ukraine.md`).

## Reading a film

- Map it first: every 15th to 20th image, year and record type. The image group summary
  (Explore Images) shows the place and the date range.
- Write down the gaps: which years and record types are absent from the film. A negative
  search means nothing without them.
- The same `groupId` in two links means the same film, so the same archive case. Two
  villages under one groupId are bound together.
- An ark link points to one image of the film. Links for different villages of the same
  case open different images; that is expected.
- The image number and the folio number of the book are independent. Note both.

## Pace and the Terms of Use

The FamilySearch Terms of Use (https://www.familysearch.org/en/legal/terms, Code of Conduct)
forbid using "any software, technology, or device to perform a bulk download, to scrape
content, or to otherwise harvest" without written permission, and a violation can cost the
right to use the site. The account at risk is the user's, and the research depends on it.
Work at the pace of a person reading: one search, one film, one image at a time. Never page
through a whole collection, download a film's images, or run a script over a film.

## Single lookups

A few answers are easier to read from the JSON the site itself loads than from the page.
Each is one request for one thing the user is looking at, from a familysearch.org tab where
the user is signed in (`fetch(url, {credentials:'include'})`, `accept: application/json`):

| Need | Route |
|---|---|
| DGS number of the image on screen | `POST /search/filmdatainfo/image-data` with `{type:'image-data', args:{imageURL:<ark>, state:{imageOrFilmUrl:<ark>, viewMode:'i', selectedImageIndex:-1}, locale:'en'}}` → `dgsNum` |
| Parish of one film | `/service/search/catalog/v3/search?count=20&q.filmNumber=<DGS>` → `metadataHit.metadata.creator` |

For indexed records, use Records → Search in the page, one query at a time, and read the
results as they come.

Notes:

- The place filters in record search re-rank results and do not filter them.
- In Russian indexes, a patronymic often stands in the surname field (Ivanov with 170 000
  hits). Cap such surnames, and search a real surname with and without the patronymic.
- The catalogue route answers only for films that have a catalogue record. Image groups
  uploaded later by archives' own cameras often have none and return zero hits; take
  their place and dates from the image group summary instead.
- The parish of a record comes from the film's catalogue entry. The place printed on an
  indexed record is often only the district or the country.

## Mapping a reel of many cases

Court and nobility files are often filmed in runs, dozens of cases per reel, and the
catalogue's "item N of M" is a hint. It was wrong twice on the same reel, both times by one
case. Map the reel by its divider cards:

1. Open the film in the image viewer and switch to the gallery (thumbnail grid) view.
2. A divider card (a white sheet shot on black, inverted) shows as an almost black
   thumbnail and takes two consecutive images. The user or Claude spots them by eye while
   scrolling the grid.
3. The image after a card is the case cover. Open each cover in turn and note the case
   name, dates and image range; together the covers give the map of the reel.

On Soviet-era covers, trust the case name, the dates and the page count. Distrust the
inventory and bundle fields, and when the case number is corrected, take the new number.
Inventories were renumbered, so an old number of one case can equal the new number of
another.

A film the viewer will not open for a signed-in user is usually restricted: viewable only at
FamilySearch centres or affiliate libraries. Confirm the restriction notice in the viewer
(signing out or a rate limit also blocks images), then respect it and label the case
accordingly.

## The FamilySearch tree

The shared tree is a secondary source: other users' conclusions, often merged on name and
date. Use it for leads. When the user edits the tree, prepare the change and let the user
review and save it; add a person to the shared tree only when a document anchors the link,
and never for a godparent or neighbour with no other tie to the family.
