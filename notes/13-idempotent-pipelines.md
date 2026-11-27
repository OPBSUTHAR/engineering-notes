# Building idempotent data pipelines

A pipeline that can safely run twice is easier to operate than one that requires perfect failure handling. Idempotency should be designed in, not bolted on.

## Key practices

- Derive deterministic keys for every record you write.
- Use upserts or merge operations instead of blind inserts.
- Track which batches have been processed and make retries skip completed work.
- Validate row counts and checksums at each stage.
- Test the pipeline by running the same input twice and comparing the output.

## Why it matters

Idempotent pipelines turn retries from a risk into a routine recovery step.

