# Measure before you optimize

Performance work without a baseline is guessing. Measure the current behavior, find the bottleneck, and verify that the change actually helped.

## Key practices

- Define the metric that matters: latency, throughput, memory, or cost.
- Capture a baseline under a workload that resembles production.
- Profile before changing code so you fix the real bottleneck.
- Change one variable at a time and re-run the same benchmark.
- Keep the benchmark in the repository so future changes can be compared.

## Why it matters

Measurement prevents wasted effort and protects against optimizations that make the common case slower.

