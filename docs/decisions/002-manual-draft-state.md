# Decision 002: Keep manual draft-state entry in the MVP

**Status:** Accepted  
**Date:** July 2026

## Context

The product has not yet established that Yahoo exposes draft picks with enough speed and reliability for live recommendations. Making the product dependent on automatic synchronization would prevent validation of the core customer value.

## Decision

The MVP will include manual entry, correction, and undo for completed draft picks.

Yahoo synchronization, if viable, will produce the same internal draft-state model.

## Why

- It allows recommendation testing before platform approval.
- It provides a fallback during API delay or failure.
- It establishes a baseline for measuring integration value.
- It keeps the recommendation experience independent of one platform.

## Consequences

- The first experience requires some user effort.
- Pick entry must be extremely fast.
- Corrections and undo are essential, not edge cases.
- Automatic synchronization must coexist with manual state rather than replace it.
