# Designing predictable REST error responses

Clients should be able to handle failures without parsing prose. A stable error shape is part of your public API contract.

## Key practices

- Return a machine-readable error code that never changes meaning.
- Include a human-readable message for developers, not for end users.
- Choose the HTTP status code that matches the semantic failure.
- Add a request identifier so support can trace the failure through logs.
- Document every error code alongside the endpoint that can return it.

## Why it matters

Consistent errors reduce client-side guesswork and make production incidents faster to diagnose.

