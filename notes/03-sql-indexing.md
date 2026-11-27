# Indexing strategies for slow SQL queries

An index is only useful when it matches the way the query filters, joins, and sorts. Add indexes from measured query plans, not from intuition.

## Key practices

- Capture a baseline with EXPLAIN ANALYZE before changing anything.
- Index columns used in selective filters and join conditions.
- Column order in a composite index matters: put equality filters before range filters.
- Remove redundant indexes; every index adds write cost and storage.
- Re-check the plan after the change and watch for regressions in write-heavy paths.

## Why it matters

A small number of well-chosen indexes often removes the slowest queries without adding operational complexity.

