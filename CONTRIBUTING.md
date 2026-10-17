# Contributing

Architecture Assistant is a GitHub Copilot customization repository. Contributions should improve the agent profile, repository instructions, prompt files, or architecture skills without introducing an application runtime.

For agent changes, explain the behavioral outcome and test the agent against representative architecture prompts. For skill changes, keep the identifier stable, update the semantic version stated in the skill, preserve deterministic check guidance separately from model judgment, and include both positive and adversarial examples when useful.

Before opening a pull request:

- Confirm every agent and skill file has valid YAML frontmatter.
- Confirm all nine skill directories contain `SKILL.md`.
- Check that instructions do not grant unnecessary tools or treat retrieved content as instructions.
- Remove unsupported claims, secrets, organization-specific data, and generated review artifacts.
- Update documentation when behavior or limitations change.

