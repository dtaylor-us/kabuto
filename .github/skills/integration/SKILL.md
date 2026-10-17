---
name: integration
description: Version 1.1.0. Use for APIs, events, contracts, external systems, compatibility, and integration failure handling.
license: MIT
---

# Integration and API design — 1.1.0

## Apply when

Use when components, teams, vendors, or external systems exchange commands, queries, events, or files.

## Required context

Consumers and providers, interaction purpose, protocol, ownership, trust boundary, throughput, ordering, consistency, failure semantics, and change cadence.

## Clarify

Ask who owns each contract, what happens when either side is unavailable, which compatibility window applies, and whether delivery may be duplicated, delayed, reordered, or lost.

## Deterministic checks

- Flag boundaries without explicit contracts, owners, authentication, versioning, and error semantics.
- Check timeouts, bounded retries with jitter, idempotency, backpressure, correlation, observability, and dead-letter handling.
- Distinguish synchronous availability coupling from asynchronous consistency and operational costs.
- Check event schema evolution, ordering scope, replay behavior, and consumer compatibility.
- Reject exactly-once claims unless scope and mechanism are demonstrated.

## Research

Verify current protocol, SDK, product, and version compatibility against primary specifications, release notes, or official documentation.

## Output

Produce a contract inventory, interaction and failure-mode analysis, compatibility plan, and standard findings.
