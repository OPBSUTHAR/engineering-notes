# Managing secrets in local development

Local secrets are still secrets. The goal is to keep them out of version control while making the project easy to start.

## Key practices

- Keep the real .env file out of Git and commit a .env.example with empty values.
- Store shared development secrets in a password manager or secret manager, not in chat.
- Use separate credentials for local development and production.
- Rotate a credential immediately if it is committed, even in a private repository.
- Add secret scanning to CI so accidental commits fail before merge.

## Why it matters

A leaked development credential is often enough to reach internal data or expensive third-party services.

