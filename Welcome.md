# Welcome to Your Second Brain

This is a personal wiki that Claude builds and maintains for you. You bring the sources — articles, notes, book chapters, anything — and Claude reads them, writes structured pages, and keeps everything cross-referenced and organized. The wiki grows richer every time you add something new or ask a question.

Think of it like this: you're the editor-in-chief. Claude is the staff writer who does all the filing.

---

## The Three Things You'll Do

### 1. Add a source (Ingest)

There are two ways to add something. Use whichever is easier in the moment.

---

**Option A — Save a file, then tell Claude to ingest it**

Use this when you have a markdown file ready — from Obsidian Web Clipper, a downloaded article, a note you wrote, etc.

1. Drop the file into `raw/articles/` (for things you found) or `raw/notes/` (for your own writing)
2. Open Claude Code and say:

> *"Ingest raw/articles/my-article.md"*

---

**Option B — Paste directly into the chat**

Use this when you don't want to bother saving a file first. Just paste whatever you have — an article you copied from the web, notes you jotted down, a transcript, a voice memo you typed up — and say:

> *"Add this to the wiki"*

or just paste it with no instructions at all. Claude will recognize it as content to ingest, save it as a properly formatted file in `raw/` automatically, and then process it.

---

Either way, Claude will then:
- Talk through the key ideas with you
- Write a summary page for that source
- Create or update pages for any people, places, or organizations mentioned
- Create or update pages for the key ideas and themes
- Flag anything that contradicts what's already in the wiki
- Update the index and activity log

One article might touch 10 different wiki pages. You don't have to do any of that — Claude handles all of it.

---

### 2. Ask a question (Query)

Once you've added a few sources, you can ask questions across everything in the wiki:

> *"What does the wiki say about how sleep affects memory consolidation?"*

> *"Compare the arguments from the three papers I added last week."*

> *"What are the open questions I haven't resolved yet?"*

Claude searches the wiki, synthesizes an answer, and cites the pages it drew from. If the answer is useful enough to keep, it gets filed as its own page in `wiki/queries/` so it doesn't disappear into chat history.

---

### 3. Write a diary entry

Tell Claude you want to log an entry:

> *"New diary entry"*

Claude will walk you through four quick sections — what happened, what's on your mind, anything you learned, and your mood. You don't have to answer all of them, and if you just want to dump a paragraph of thoughts, that works too:

> *"Log today — had a really frustrating meeting, can't stop thinking about whether I should switch roles. Read something interesting about decision fatigue."*

Claude will extract the structure from whatever you give it, save the entry to `raw/notes/diary/`, and update a page called [[diary-patterns]] that tracks themes and patterns across all your entries over time — recurring topics, mood trends, open questions you keep returning to, moments where something shifted.

### 5. Clean it up (Lint)

Every few weeks, ask Claude to do a health check:

> *"Lint the wiki"*

Claude will scan everything and report back:
- Pages that nothing else links to (orphans)
- Claims in one page that contradict another
- Concepts that are mentioned everywhere but never got their own page
- Stubs that are ready to be expanded if you add more sources
- Suggestions for what to read next based on the gaps it sees

---

## Where Everything Lives

```
raw/          ← You put source files here. Claude reads them but never changes them.
  articles/   ← Articles, papers, web clips
  notes/      ← Your own writing, journal entries
  data/       ← Spreadsheets, exports, structured info

wiki/         ← Claude writes everything here. You just read it.
  index.md    ← The full catalog of every page in the wiki
  log.md      ← A running record of every ingest, query, and update
  overview.md ← Claude's evolving synthesis of everything — the "so what"
  sources/    ← One page per source you've ingested
  entities/   ← Pages for people, places, organizations
  concepts/   ← Pages for ideas, themes, frameworks
  queries/    ← Answers to questions you've asked that are worth keeping
```

---

## A Concrete Example

Say you're building a wiki about nutrition and longevity. Here's what a session might look like:

**You:** Save `attia-outlive-chapter3.md` into `raw/articles/`. Open Claude Code and say: *"Ingest attia-outlive-chapter3.md"*

**Claude:** Reads the chapter, discusses the main claims with you, then creates `wiki/sources/attia-outlive-chapter3.md`, updates `wiki/entities/peter-attia.md`, creates `wiki/concepts/zone-2-training.md` and `wiki/concepts/vo2-max.md`, notes that the claim about fasting contradicts something from a previous source, and updates the index and log.

**Later, you ask:** *"What does the wiki say about the relationship between VO2 max and lifespan?"*

**Claude:** Searches the index, reads the relevant pages, synthesizes an answer citing three sources, and offers to file it as `wiki/queries/vo2-max-and-lifespan.md`.

**A month later:** *"Lint the wiki"* — Claude finds that `wiki/concepts/zone-2-training.md` is a stub that could be expanded, that two sources disagree on optimal protein intake, and suggests you look for research on muscle protein synthesis to fill a gap.

---

## Tips for Getting Good Results

**Getting sources in:** The easiest flow is the [Obsidian Web Clipper](https://obsidian.md/clipper) browser extension — it converts any webpage to markdown in one click and saves it straight to your vault. Then just point Claude at the file.

**Exploring the wiki:** Obsidian's **Graph View** (left sidebar icon) shows you a visual map of everything and how it connects. Pages with many connections are your knowledge hubs. Isolated dots are candidates for the next lint pass.

**Don't lose good answers:** When Claude gives you a synthesis you find valuable, say *"File that as a query page."* Otherwise it disappears when the conversation ends.

**Let it compound:** The wiki gets more useful the more you add. The first few sources feel slow — by the time you have 20 or 30, Claude can start drawing connections you hadn't thought to make yourself.

---

## The Files Claude Uses Internally

You don't need to read these, but they're here:
- [[index]] — Claude reads this at the start of every session to know what's in the wiki
- [[log]] — the full history of everything that's happened
- `CLAUDE.md` — the rules Claude follows (you can read it if you're curious how the system works)
