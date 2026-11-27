# The test pyramid in practice

Fast unit tests should cover most behavior, integration tests should cover boundaries, and end-to-end tests should cover only critical journeys.

## Key practices

- Test behavior and public interfaces rather than private implementation details.
- Keep unit tests fast enough to run on every save.
- Use integration tests for database queries, serialization, and external adapters.
- Reserve end-to-end tests for the paths that must never break.
- Make every test deterministic; control time, randomness, and network access.

## Why it matters

The pyramid keeps feedback fast while still catching the integration failures that unit tests cannot see.

