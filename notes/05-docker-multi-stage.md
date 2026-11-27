# Smaller Docker images with multi-stage builds

Build dependencies and runtime dependencies are usually different. Multi-stage builds keep compilers and package caches out of the final image.

## Key practices

- Use a build stage with the full toolchain and a separate runtime stage with only the artifact.
- Prefer slim or distroless base images when the application supports them.
- Run the container as a non-root user.
- Pin base image tags instead of relying on latest.
- Copy dependency manifests first so layer caching can skip unchanged installs.

## Why it matters

Smaller images pull faster, expose fewer packages, and reduce the blast radius of a compromised container.

