---
name: simplicity-coupling
description: Version 1.1.0. Use to detect over-engineering, unnecessary components, premature distribution, and organizational or runtime coupling.
license: MIT
---

# Architecture simplicity and coupling — 1.1.0

## Apply when

Always. Use after the other skills to challenge whether identified mechanisms and boundaries are justified.

## Required context

Option components, responsibilities, deployment units, data ownership, team ownership, change cadence, existing estate, delivery constraints, and operational maturity.

## Clarify

Ask what can be reused, which parts change independently, who operates each boundary, what complexity the organization can sustain, and which decisions can safely be deferred.

## Deterministic checks

- Require a requirement, risk, or ownership rationale for every component and boundary.
- Identify deployment, data, temporal, contract, vendor, and team coupling.
- Flag premature distribution, duplicate capabilities, excessive technology variety, and coordination-heavy ownership.
- Compare the proposed operational burden with team capacity and maturity.
- Include minimal-change and defer/do-nothing options when credible; do not penalize simplicity merely for lacking novelty.

## Research

Research is rarely necessary. Verify product lock-in, portability, or end-of-support claims when they materially affect coupling.

## Output

Produce a complexity budget, coupling map, removal or consolidation opportunities, reversibility assessment, and standard findings.
