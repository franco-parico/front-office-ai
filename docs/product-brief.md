# Product Brief

## Summary

Front Office AI is a fantasy-football draft assistant that combines trusted rankings with league rules, roster construction, keeper economics, positional scarcity, and live draft context.

The product is currently in MVP validation with one design partner: a Yahoo Fantasy Football manager in a 12-team standard-scoring keeper league.

## Customer problem

Rankings describe general market value. A manager's decision occurs inside a specific league and a specific moment.

During a draft, the manager must understand:

- Which ranked players remain available
- Which starting positions still need to be filled
- What every other team may select
- Which positional tiers are about to disappear
- How many picks occur before the manager's next turn
- Whether a player's upside creates keeper value

Existing tools distribute these inputs across ranking sheets, league platforms, draft rooms, and the manager's own notes.

## Product hypothesis

If Front Office AI maintains the manager's league and draft context, then it can turn a generic ranking into timely, explainable options and help the manager make faster, more confident decisions.

## Jobs to be done

### Before the draft

> Help me understand how my league settings and keepers should change my strategy.

### During the draft

> Help me identify the best available options before my clock expires.

### After each pick

> Update the board and explain how the decision landscape changed.

## Initial design partner

**Lazy Sundays**

| Setting | Value |
|---|---|
| Teams | 12 |
| Scoring | Standard, no PPR |
| Starters | 1 QB, 3 WR, 2 RB, 1 TE, 1 K, 1 D/ST |
| Flex | None |
| Keeper limit | Two consecutive years |
| Keeper cost | One round earlier than the previous draft round |

The configuration creates meaningful demand at wide receiver, distinct roster construction without a flex position, and an explicit tradeoff between immediate value and future keeper upside.

## MVP experience

A manager can:

1. Configure the league and keeper rules.
2. Import a current ranking set.
3. Enter or synchronize completed picks.
4. See the available player board.
5. Track team rosters.
6. Receive three recommended players.
7. Understand the reason and tradeoff behind each option.
8. Override the recommendation.
9. Correct or undo draft-state errors.

## Recommendation inputs

- Overall rank
- Position rank and tier
- Open starting slots
- Existing roster
- Position scarcity
- Tier drop before the next turn
- Picks until the manager's next selection
- Player upside
- Keeper cost and potential

The first model will be deterministic and explainable. Future AI behavior must demonstrate improvement over this baseline.

## Success measures

### Usability

- A pick can be entered or synchronized in under two seconds.
- Recommendations update before the next decision is required.
- A mock draft can be completed without a separate spreadsheet.
- Corrections do not corrupt draft state.

### Recommendation quality

- Drafted players never appear as available.
- Recommendations fit the league's open roster requirements.
- Material tier changes are identified.
- Keeper value is reflected when relevant.
- Explanations are understandable without examining the underlying formula.

### Customer value

- The manager reports greater confidence in difficult picks.
- The manager makes decisions before the draft clock expires.
- Advice changes at least some choices compared with rankings alone.
- The manager understands why advice was accepted or rejected.
- The manager chooses to use the product for another draft.

## Open questions

- Does Yahoo expose completed picks during an active draft?
- Is manual entry acceptable for the initial experience?
- Which recommendation factors actually change decisions?
- How should future keeper value be balanced against immediate value?
- How much explanation is useful during a timed decision?
- When is a recommendation meaningfully better than a sorted ranking list?

## Current risks

| Risk | Response |
|---|---|
| Yahoo access is delayed or rejected | Continue validating the manual experience |
| Yahoo draft data is not live | Use Yahoo for setup and manual entry for picks |
| Recommendations resemble rankings | Add roster, scarcity, tier, turn, and keeper context |
| Users distrust the output | Make reasoning and tradeoffs visible |
| Scope expands prematurely | Require customer evidence before adding complexity |

## Out of scope

- Automated drafting
- Roster and transaction changes
- In-season lineup, waiver, and trade recommendations
- A second fantasy platform
- Multiple ranking providers
- News scraping
- Advanced identity-management workflows
- Opaque AI-generated rankings
