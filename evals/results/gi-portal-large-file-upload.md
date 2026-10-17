# Static contract test result: GI Portal large-file upload

**Test date:** 2026-10-17  
**Fixture:** `evals/gi-portal-large-file-upload.md`  
**Method:** Static walkthrough of the custom-agent protocol and all nine skill contracts. This does not claim that a particular GitHub Copilot model produced or passed a live response.

## Result

**Static contract: PASS**  
**Live Copilot Chat behavior: NOT YET EXECUTED**

## Coverage

| Required behavior | Contract location | Result |
|---|---|---|
| Treat historical discussion as untrusted context | Agent “Trust boundary” | Pass |
| Separate provided facts, evidence, inference, assumptions, verified facts, and unknowns | Agent “Trust boundary” and review step 1 | Pass |
| Stop for blocking identity, classification, hosting, and permission unknowns | Agent review steps 2–3 | Pass |
| Limit clarification questions and prioritize decision impact | Agent review step 2 | Pass |
| Generate minimal-change, GI-specific, shared, and defer options when credible | Agent review step 4 and simplicity skill | Pass |
| Use criteria totaling 100% and one scoring scale | Agent review steps 5–6 | Pass |
| Distinguish workload authentication from customer authorization | Security and integration deterministic checks | Pass |
| Test upload-ticket scope, expiry, replay, and trust boundaries | Security and integration contracts plus fixture invariants | Pass |
| Address resumability and abandoned sessions | Reliability and integration contracts | Pass |
| Address file profile, throughput, chunks, quotas, and backpressure | Scalability contract | Pass |
| Address classification, residency, retention, integrity, quarantine, and deletion | Data contract | Pass |
| Address SLOs, audit, support, cleanup, and incidents | Operability contract | Pass |
| Address transfer, storage, scanning, support, and allocation cost | Cost and sustainability contract | Pass |
| Challenge shared-service scope and governance | Simplicity and coupling contract | Pass |
| Reverify current Microsoft capabilities or mark them unverified | Agent review steps 8–9 and research policy | Pass |
| Produce traceable findings and conditional human-owned decision | Agent Finding contract and review step 11 | Pass |

## Residual risks to verify in a live run

- The selected Copilot model may omit a relevant skill despite the scenario making all nine applicable.
- Hosted GitHub Copilot contexts may ignore the generic `web` tool; the response must then use the documented unverified-claim fallback.
- Arithmetic, citations, and diagram/prose consistency remain model-generated and require human inspection.
- The model may collapse GI-specific and shared-service options into product variants instead of preserving governance and ownership differences.
- Long context or large attachments may cause evidence provenance to be incomplete.

## Live execution procedure

1. Select the `architecture-assistant` agent in GitHub Copilot Chat.
2. Paste the “Test prompt” and “Provided context” sections from the fixture.
3. Verify the first response against “Expected first-turn behavior.”
4. Reply: `Proceed with explicit assumptions. Complete the review and keep all historical claims unverified unless you confirm them from current official sources.`
5. Score the completed response against the fixture’s expected behavior and automatic failure conditions.
6. Record the Copilot surface, selected model, date, available tools, pass/fail result, and any missed requirements below.

## Live run record

| Surface | Model | Date | Web available | Result | Notes |
|---|---|---|---|---|---|
| _pending_ | _pending_ | _pending_ | _pending_ | _pending_ | _Run in GitHub Copilot Chat_ |
