# Decision 001: Yahoo is the first league platform

**Status:** Accepted  
**Date:** July 2026

## Context

The first design partner manages their primary fantasy league on Yahoo Sports. Supporting another platform first would optimize for hypothetical demand rather than the observed customer workflow.

## Decision

Yahoo Fantasy Sports will be the first planned league integration.

The initial integration will request read-only access and investigate:

- League discovery
- Scoring and roster settings
- Teams and rosters
- Player identifiers
- Draft results
- Live draft-result latency

## Why

- It serves the first real customer.
- It provides direct product-learning opportunities.
- It tests whether a platform integration materially improves the draft workflow.
- It avoids broad multi-platform abstraction before one integration is understood.

## Consequences

- Yahoo API approval and OAuth become external dependencies.
- Live draft-pick availability remains an unresolved risk.
- Manual workflows must remain available.
- Additional platforms are deferred until Yahoo produces meaningful learning.
