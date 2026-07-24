# Changelog

This project follows milestone-based releases while the product is in validation.

## Unreleased

### Planned

- Lazy Sundays league and keeper configuration
- Manual draft-state management
- Explainable recommendation baseline
- Mock-draft evaluation

## 0.1.0 — Ranking data foundation

### Added

- FantasyPros CSV inspection and validation
- Versioned ranking-set imports
- Canonical player and source-observation separation
- Multi-position eligibility
- Duplicate-file detection
- Conservative player matching
- Queryable data-quality issues
- CLI and REST API access
- Automated tests, linting, and type checking
- Public pre-launch product site

### Product decisions

- Begin with one customer and one league
- Use a user-provided FantasyPros export before pursuing more ranking providers
- Prioritize draft-state validation over deeper identity-management workflows
- Select Yahoo as the first planned league platform
- Retain manual entry as an MVP workflow and integration fallback
