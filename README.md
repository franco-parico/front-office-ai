# Front Office AI

Front Office AI is a fantasy-football draft assistant that turns generic rankings into recommendations tailored to a manager's league, roster, keepers, and live draft.

> **Who should I consider drafting next—and why?**

## Why I'm building it

I got so good at using AI at work that I automated myself out of a job, so now I'm using AI for the one thing I truly give a shit about: fantasy football.

**Stage:** MVP validation  
**First customer:** Yahoo Fantasy Football manager  
**First use case:** Live draft decision support  
**Website:** [Front Office AI](https://front-office-ai-pilot.franco-parico.chatgpt.site)

## The problem

Fantasy managers have plenty of rankings and analysis, but still have to combine them with league rules, roster needs, positional scarcity, keeper value, and a moving draft board—often while the clock is running.

Front Office AI treats rankings as an input rather than the answer. The product's job is to maintain the relevant context, recommend three available players, and explain the tradeoff behind each option.

## Initial customer

The first experience is designed around **Lazy Sundays**, a 12-team, standard-scoring Yahoo keeper league with:

- 1 QB, 3 WR, 2 RB, 1 TE, 1 K, and 1 D/ST
- No flex position
- Two consecutive keeper years
- A keeper cost one round earlier than the player's previous draft round

This is the first design case, not the final market boundary.

## Product principles

- **Context over consensus.** Rankings start the conversation.
- **Explain the recommendation.** Advice should show its reasoning and tradeoffs.
- **Keep the manager in control.** Front Office AI advises; it does not draft.
- **Manual workflows are valid.** Integrations remove effort but should not define value.
- **Earn complexity.** Add sources, infrastructure, and AI when customer evidence warrants it.

## Progress

| Milestone | Status |
|---|---|
| Versioned ranking ingestion | Complete |
| Public product site | Complete |
| Yahoo API access application | Submitted |
| Manual draft room | Next |
| Explainable recommendation baseline | Planned |
| Yahoo connectivity | Awaiting access |
| Draft simulation and evaluation | Planned |

The ranking foundation has been validated against a real 2026 export: 500 rows received, 498 rankings imported, and two empty separator rows identified without silent data loss.

## Current product bet

The next milestone is a manual but intelligent draft room:

1. Configure the league and keepers.
2. Load a ranking snapshot.
3. Record completed picks.
4. Track player availability and every team's roster.
5. Recommend three players using value, need, scarcity, tiers, turn distance, upside, and keeper potential.
6. Explain each recommendation.
7. Record when the manager accepts or rejects the advice.

Yahoo should eventually automate league configuration and draft-state entry. The product must demonstrate value before that automation is available.

## Documentation

- [Product brief](docs/product-brief.md)
- [Roadmap](docs/roadmap.md)
- [Changelog](CHANGELOG.md)
- [Why Yahoo is the first platform](docs/decisions/001-yahoo-first.md)
- [Why the MVP keeps manual draft entry](docs/decisions/002-manual-draft-state.md)

## What this portfolio demonstrates

- Customer-driven discovery
- Hypothesis-led prioritization
- MVP scope management
- Data-product thinking
- Platform and integration strategy
- Explainable decision-support design
- Success-metric definition
- Product and engineering collaboration

## Disclaimer

Front Office AI is an independent, pre-launch product. Yahoo and FantasyPros are trademarks of their respective owners. Front Office AI is not affiliated with or endorsed by either company.
