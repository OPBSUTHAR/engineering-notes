# Python virtual environments and pinned dependencies

Every Python project should run in an isolated environment with reproducible dependencies. That prevents "works on my machine" failures and makes CI match local development.

## Key practices

- Create a virtual environment per project and keep it out of version control.
- Pin direct dependencies and commit the lock file your tool produces.
- Separate development dependencies from runtime dependencies.
- Upgrade dependencies deliberately, then run the test suite before merging.
- Document the exact commands needed to recreate the environment.

## Why it matters

Reproducible environments turn dependency problems into rare, debuggable events instead of everyday surprises.

