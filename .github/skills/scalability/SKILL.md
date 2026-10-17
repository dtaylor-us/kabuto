---
name: scalability
description: Version 1.1.0. Use for demand, capacity, latency, throughput, concurrency, growth, and performance tradeoffs.
license: MIT
---

# Scalability and performance — 1.1.0

## Apply when

Use when load, latency, throughput, concurrency, data volume, growth, burst behavior, or performance isolation can affect the decision.

## Required context

Normal and peak demand, workload shape, concurrency, growth horizon, latency percentiles, throughput targets, data volume, payload sizes, and measurement method.

## Clarify

Ask which user journeys are latency-sensitive, what peak and burst profiles look like, what growth period applies, and which measurements support the forecast.

## Deterministic checks

- Flag unbounded, unitless, or implausible scale assumptions.
- Check end-to-end latency budgets rather than isolated component latency.
- Identify hot keys, shared bottlenecks, contention, fan-out, queue growth, backpressure, and noisy-neighbor risk.
- Check horizontal scaling assumptions, state placement, caching correctness, and load-test coverage.
- Require capacity thresholds and a response plan.

## Research

Verify quotas, limits, supported scale, and performance-sensitive compatibility using official documentation current to the retrieval date.

## Output

Produce a demand model, bottleneck hypotheses, capacity-test plan, uncertainty ranges, and standard findings.
