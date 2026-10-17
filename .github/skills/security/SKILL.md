---
name: security
description: Version 1.1.0. Use when reviewing trust boundaries, sensitive data, identity, threats, abuse, compliance claims, or current security guidance.
license: MIT
---

# Security and threat analysis — 1.1.0

## Apply when

Use for every deployable design; deepen the review when identity, sensitive data, external access, privileged operations, or regulated obligations are present.

## Required context

Assets, actors, trust boundaries, data classifications, entry points, identity flows, deployment boundary, threat actors, and control owners.

## Clarify

Ask what data is sensitive, who may access it, which identities and trust boundaries exist, which threats are credible, and which obligations have been confirmed by accountable experts.

## Deterministic checks

- Flag sensitive data without access, encryption, retention, deletion, audit, and incident requirements.
- Flag unauthenticated or over-privileged boundaries and missing service-to-service identity.
- Check secret handling, tenant isolation, supply-chain trust, abuse resistance, and security telemetry.
- Never infer compliance or claim that controls guarantee compliance.
- Require ownership and verification for every high-impact control.

## Research

Trigger for current vulnerabilities, security guidance, regulations, standards, and product control behavior. Prefer regulators, standards bodies, maintainers, and official vendor security documentation. Record version and date applicability.

## Output

Produce assets, trust boundaries, prioritized threat scenarios, control gaps, residual risk, and standard findings with executable verification steps.
