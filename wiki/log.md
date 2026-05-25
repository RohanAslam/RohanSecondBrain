# Activity Log

Append-only record of all wiki activity.
Format: `## [YYYY-MM-DD] type | description`
Types: `init` `ingest` `query` `lint` `update` `diary`

---

<<<<<<< HEAD
## [2026-05-25] update | Removed wiki/sources/ — raw articles now serve as source nodes directly; all links updated
=======
## [2026-05-25] autofix | No uningestd raw files found; removed stale stub markers from Progressive Overload and Stimulus to Fatigue Ratio pages

## [2026-05-25] update | Progressive Overload — removed residual stub marker (page has full content)

## [2026-05-25] update | Stimulus to Fatigue Ratio — removed residual stub marker (page has full content)
>>>>>>> origin/main

## [2026-05-25] autofix | Fixed 3 issues — ingested 1 article (How Many Sets Do You Need), processed 1 diary entry (2026-05-24), updated overview and diary-patterns with real content; created 7 new wiki pages

## [2026-05-25] lint | Health check — 5 issues found (2 uningestd raw files, 1 missing entity, 4 missing concept pages, 3 stale core pages)

## [2026-05-24] init | Wiki system initialized

Wiki directory structure created. Schema defined in `CLAUDE.md`. Obsidian vault ready.

**Structure created:**
- `raw/articles/` `raw/notes/` `raw/notes/diary/` `raw/data/` `raw/assets/` — source documents (immutable)
- `wiki/sources/` — per-source summary pages
- `wiki/entities/` — entity pages (people, places, organizations)
- `wiki/concepts/` — concept pages (ideas, themes, topics)
- `wiki/queries/` — filed query answers
- `wiki/diary-patterns.md` — rolling diary theme synthesis
- `wiki/overview.md` — evolving synthesis
- `wiki/index.md` — content catalog
- `wiki/log.md` — this file

**Status:** Ready for first ingest.
