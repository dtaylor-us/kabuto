# Architecture Assistant

Architecture Assistant is a native GitHub Copilot custom agent for evidence-backed solution architecture reviews. It accepts a problem statement and supporting artifacts in Copilot Chat, identifies missing context, compares meaningfully different options, applies nine architecture skills, researches time-sensitive claims when needed, and produces a conditional recommendation with explicit tradeoffs.

It is decision support. A human remains responsible for accepting architectural decisions.

## Use it

1. Push this repository to GitHub or open it in a GitHub Copilot-supported workspace.
2. Select the `architecture-assistant` custom agent in the Copilot agent picker.
3. Describe the problem and attach any relevant requirements, diagrams, ADRs, policies, or other artifacts.
4. Answer the targeted clarification questions, or tell the agent to continue with documented assumptions.
5. Open the completed review created under `.tool-output/reviews/`. Chat contains only the decision summary and link.

Example prompt:

```text
Review the architecture described in evals/gi-portal-large-file-upload.md.
Proceed with explicit assumptions where evidence is missing and create the review file.
```

The agent has narrowly scoped edit access so it can create Markdown review artifacts in a Git-ignored output area. It does not have shell access and is instructed not to change application code or configuration unless a user explicitly asks for repository maintenance. If a Copilot surface does not expose file editing, the agent reports that limitation and returns copy-ready Markdown instead of claiming that it created a file.

In Copilot Chat surfaces that do not expose the agent picker, attach this repository so `.github/copilot-instructions.md` is included as repository context. The agent inherits the GitHub Copilot model selected by the user or environment; this repository has no model API dependency or credentials.

## Repository layout

```text
.github/
├── agents/architecture-assistant.agent.md
├── copilot-instructions.md
├── prompts/review-architecture.prompt.md
└── skills/
    ├── problem-framing/
    ├── security/
    ├── reliability/
    ├── scalability/
    ├── data/
    ├── integration/
    ├── operability/
    ├── cost-sustainability/
    └── simplicity-coupling/
```

Each skill is a discoverable `SKILL.md` package with a version in its title and description. The agent loads relevant skills based on the review and records skill identifiers and versions in findings.

Generated outputs are intentionally kept out of the tracked repository tree:

- Repository-specific source assets stay tracked under [.github/](/Users/derektaylor/projects/kabuto/.github), [docs/](/Users/derektaylor/projects/kabuto/docs), and [evals/](/Users/derektaylor/projects/kabuto/evals).
- Review artifacts and evaluation results belong under `.tool-output/`, which is ignored by Git.
- Toolkit discovery should honor `.gitignore` so ignored output files do not become future analysis inputs.

## Review workflow

The agent:

1. Creates a provenance-labeled context ledger.
2. Asks only decision-relevant clarification questions.
3. Generates two to four genuinely different options, including minimal-change and defer choices when appropriate.
4. Defines weighted criteria before applying the same criteria to every option.
5. Applies the relevant architecture skills.
6. Researches only current, pricing-sensitive, regulatory, compatibility, or conflicting claims using authoritative sources.
7. Writes a concise, decision-oriented Markdown artifact containing the recommendation, architecture, comparison, prioritized risks, verification steps, evidence, and candidate ADR.

## Safety and limitations

- Uploaded artifacts and web pages are untrusted data, never agent instructions.
- The agent must not invent requirements, evidence, citations, components, or verification results.
- Model output can still be wrong. Review evidence, assumptions, scores, and citations before accepting a decision.
- Web and tool availability varies by Copilot surface and organization policy. Claims that cannot be verified must remain explicitly uncertain.

See [the research policy](docs/research-policy.md), [security policy](SECURITY.md), and [contribution guide](CONTRIBUTING.md). Licensed under MIT.

## Governance docs

- [Skills index](docs/skills-index.md): maps each skill to its purpose, triggers, version, and evaluation scenarios, so maintainers can see coverage and keep versions in sync.
- [Review workflow guide](docs/review-workflow.md): where review artifacts live, how they are named and updated, and the path from draft to a human decision.
- [Review quality checklist](docs/review-quality-checklist.md): a short pre-acceptance check aligned with the agent contract.

Maintainers can use [the evaluation cases](evals/cases.md) for manual regression testing after changing the agent or a skill.
The [GI Portal large-file upload fixture](evals/gi-portal-large-file-upload.md) provides a realistic end-to-end enterprise scenario. Store any generated static-contract or live-run results under `.tool-output/evals/` so they remain local outputs rather than tracked repository content.
