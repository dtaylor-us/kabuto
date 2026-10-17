---
name: data
description: Version 1.1.0. Use for data ownership, models, consistency, lifecycle, residency, governance, migration, and diagram consistency.
license: MIT
---

# Data architecture and governance — 1.1.0

## Apply when

Use whenever a design creates, reads, transforms, transfers, retains, or deletes data.

## Required context

Data domains, systems of record, ownership, classification, lifecycle, residency, consumers, consistency needs, volumes, and migration state.

## Clarify

Ask who owns each data domain, which source is authoritative, what consistency is required, where data may reside, how long it is retained, and how deletion is proven.

## Deterministic checks

- Flag data without an owner, classification, authoritative source, retention rule, or deletion path.
- Check lineage, consent or purpose boundaries, residency, schema evolution, quality controls, backup, restore, and auditability.
- Identify uncontrolled copies, dual writes, ambiguous consistency, irreversible migration, and analytics access to operational data.
- Compare every store and flow in diagrams with the written description; report mismatches.
- Do not invent entities or infer governance approval.

## Research

Verify regulations, standards, residency behavior, retention features, and current storage semantics only when applicable. Prefer regulators, standards bodies, and official product documentation.

## Output

Produce a data ownership and lifecycle view, consistency decisions, migration safeguards, unresolved governance questions, and standard findings.
