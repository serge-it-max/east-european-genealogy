# How the agent works on long research

## Bot checks, logins, paid access

- Never solve a CAPTCHA or a bot check, never use a solver, a proxy or a changed browser
  fingerprint, never enter a password.
- When a site shows a check or a login wall, open the page in the user's browser, tell the
  user which tab and what to pass, wait, and continue the search right after. Never write
  the source off as "blocked" without asking.
- Respect restricted films and reading-room-only units: label them `[offline]` with the
  reason, and look for another copy that is openly published.
- Do not draft letters to archives or researchers unless the user asks for them. Many
  users research online only; record what is offline and move on.

## Background agents

- A background agent that reads many files or scans must **create its notes file first**
  and **append after each finished unit** (a case, a page range, a search term). An agent
  that writes only at the end leaves nothing when it is stopped. Four agents once read
  about 500 pages for an hour and left nothing on disk.
- Closing the session usually ends the agents. Say so before launching long ones.
- Give each agent the rules it needs in its prompt: lists first, observation over
  conclusion, leads with availability labels, no CAPTCHA solving, the user's banned
  sources. An agent does not inherit them.
- Ask agents to resolve identity questions from documents and the family context, and to
  return leads, never lists of questions for the user.
- **Grep first, read second.** A sweep over many research files should search for markers
  ("not checked", "next steps", a shelfmark) and read only the sections found. Cyrillic
  costs roughly one token per two or three letters; one audit sent eight agents to read
  half a megabyte each and spent about two million tokens. Tell the user the rough cost
  before a large fan-out.

## Secondary sources and AI answers

- Search-engine AI summaries and chatbot answers are never a source. Open the primary
  source; drop a claim you cannot find there, and say you dropped it.
- A forum post, an online tree or a published genealogy is a lead to the documents it
  cites.

## Text and tools

- **Mixed scripts.** Generated text slips Latin letters into Cyrillic words («Anan» +
  «ьевский») and Polish letters into Cyrillic («Висłоцким»). After writing a file or a
  database note with Cyrillic, search it for `[а-яё][a-ząćęłńóśźż]|[a-ząćęłńóśźż][а-яё]`.
  It catches what an eye misses.
- **Windows shells corrupt non-ASCII arguments.** On Git Bash for Windows, Cyrillic passed
  as a command-line argument (for example `psql -c "…"`) arrives as garbage, and the error
  looks like a database encoding bug. Pass such text through a file or standard input, or
  through a script with parameters.
- **Bracket classes miss multibyte letters.** `grep "jami[nń]sk"` in some locales misses
  «Jamińska». Use alternation `(n|ń)` with a UTF-8 locale, or a search tool built on
  ripgrep, or Python `re`. Before trusting an old "0 hits" on a Polish or Ukrainian
  surname, check how it was searched.
- **Keep quotes in the original.** Names of people and places and quotes from sources stay
  in the source's script and spelling. Never transliterate them in notes: transliteration is
  where hybrid misspellings come from.
- **Paths to the user's files** in reports are absolute, so the user can open them.
