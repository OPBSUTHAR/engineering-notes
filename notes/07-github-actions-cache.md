# Caching dependencies in GitHub Actions

Most CI time is spent downloading and rebuilding dependencies. A correctly keyed cache can cut that time without changing the build.

## Key practices

- Cache the package manager directory, not the entire workspace.
- Key the cache on the lock file hash and the operating system.
- Restore the cache before installing dependencies, and let the install step update it.
- Never cache secrets, build outputs that contain credentials, or mutable global state.
- Check the cache hit rate in the workflow logs and adjust the key when it is low.

## Why it matters

Faster CI means faster reviews and fewer interrupted development cycles.

