# Structured logging basics

Logs are data. Emitting structured fields instead of interpolated sentences makes logs searchable, filterable, and safe to aggregate.

## Key practices

- Emit one JSON object per event with stable field names.
- Include a request identifier, route, status, and latency for every request.
- Use log levels consistently: debug for detail, info for lifecycle events, warn for recoverable problems, error for failures.
- Never log passwords, tokens, full card numbers, or unnecessary personal data.
- Sample high-volume debug logs instead of disabling them entirely.

## Why it matters

Structured logs turn an incident from a grep exercise into a set of precise queries.

