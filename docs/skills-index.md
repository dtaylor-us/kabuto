# Skills index

Each skill lives in `.github/skills/<name>/SKILL.md`. Versions below must match the `description` and title in each `SKILL.md`; update this table whenever a skill changes. Scenarios refer to [evals/cases.md](../evals/cases.md) unless noted; the [GI Portal fixture](../evals/gi-portal-large-file-upload.md) exercises every skill.

| Skill | Purpose | Trigger conditions | Version | Evaluation scenarios |
|---|---|---|---|---|
| `problem-framing` | Test requirement completeness, contradictions, stakeholders, assumptions, and unknowns. | Always; runs before options are generated. | 1.1.0 | Incomplete context; Contradictory requirements; Correct deferral; Prompt injection |
| `security` | Trust boundaries, sensitive data, identity, threats, abuse, compliance claims. | Every deployable design; deeper when identity, sensitive data, or regulated obligations exist. | 1.1.0 | Sensitive-data exposure; Prompt injection |
| `reliability` | Availability, failure modes, recovery objectives, disaster recovery, dependency resilience. | Downtime, data loss, degraded dependencies, or continuity matters. | 1.1.0 | Missing recovery objectives; Single point of failure |
| `scalability` | Demand, capacity, latency, throughput, concurrency, growth. | Load, latency, volume, burst, or performance isolation can affect the decision. | 1.1.0 | Implausible scale |
| `data` | Ownership, models, consistency, lifecycle, residency, governance, diagram consistency. | Any design that creates, reads, transforms, transfers, retains, or deletes data. | 1.1.0 | Contradictory requirements; Diagram disagreement; Correct deferral |
| `integration` | APIs, events, contracts, external systems, compatibility, failure handling. | Components, teams, vendors, or external systems exchange commands, queries, events, or files. | 1.1.0 | Outdated evidence; Vendor bias |
| `operability` | Observability, SLOs, deployment, support, incident response, ownership. | Every production or business-critical capability. | 1.1.0 | Missing recovery objectives; Single point of failure |
| `cost-sustainability` | Budget, cost drivers, utilization, unit economics, resource efficiency. | Options materially differ in build cost, operating cost, licensing, consumption, or staffing. | 1.1.0 | Outdated evidence; Vendor bias |
| `simplicity-coupling` | Detect over-engineering, unnecessary components, premature distribution, coupling. | Always; runs after the other skills to challenge identified mechanisms. | 1.1.0 | Over-engineering |
