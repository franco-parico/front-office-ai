# Product Roadmap

The roadmap is organized around customer and product risk rather than feature volume.

## Phase 1 — Ranking data foundation

**Status:** Complete

**Question:** Can the product safely ingest and preserve an external ranking board?

Delivered:

- File inspection and validation
- Versioned ranking snapshots
- Source-specific names, teams, and positions
- Multi-position support
- Duplicate detection
- Data-quality reporting
- Queryable ranking boards

## Phase 2 — Manual draft room

**Status:** Next

**Question:** Can one manager complete a draft with Front Office AI as the primary decision surface?

Planned:

- Lazy Sundays configuration
- Keeper players and round costs
- Ordered draft picks
- Player availability
- Team rosters
- Undo and correction

## Phase 3 — Explainable recommendations

**Status:** Planned

**Question:** Does league and draft context create advice that is more useful than a sorted ranking?

Planned:

- Three-player shortlist
- Roster-need model
- Position scarcity
- Tier-drop detection
- Turn-distance logic
- Upside and keeper value
- Plain-language reasons

## Phase 4 — Yahoo connectivity

**Status:** Awaiting API approval

**Question:** Can Yahoo reliably remove manual setup and draft-state entry?

Planned:

- OAuth authorization
- League discovery
- League settings
- User-team identification
- Player and roster retrieval
- Live draft-result latency test

The outcome may be full synchronization or a hybrid workflow.

## Phase 5 — Simulation and evaluation

**Status:** Planned

**Question:** Can the product measure and improve recommendation quality?

Planned:

- Mock-draft replay
- Strategy comparison
- Accepted and rejected recommendation events
- Roster-outcome measures
- Failure-mode review
