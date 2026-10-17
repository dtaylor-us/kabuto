---
name: reliability
description: Version 1.1.0. Use for availability, failure modes, recovery objectives, disaster recovery, and dependency resilience.
license: MIT
---

# Reliability, availability, and disaster recovery — 1.1.0

## Apply when

Use when downtime, data loss, degraded dependencies, disaster recovery, or continuity matters.

## Required context

Availability target, RTO, RPO, durability target, critical journeys, dependencies, failure domains, maintenance model, and recovery ownership.

## Clarify

Ask which failures must be tolerated, how long degradation is acceptable, how much data may be lost, and when recovery was last exercised.

## Deterministic checks

- Flag missing or contradictory availability, RTO, RPO, and durability targets.
- Identify single points of failure and correlated failure domains.
- Check dependency timeouts, retries, backoff, circuit breaking, graceful degradation, capacity headroom, backup integrity, and restore testing.
- Distinguish configured redundancy from demonstrated recoverability.
- Check that recovery procedures have owners, frequencies, and measurable success criteria.

## Research

Verify current regional availability, service guarantees, replication semantics, and recovery limitations only when decision-relevant. Prefer official service and SLA documentation.

## Output

Produce a failure-mode table, recovery posture, untested assumptions, residual risks, and standard findings.
