# amposer-bootstrap

An interactive **ReAct-style bootstrap skill** for agents that helps you create a solid foundation for agents in a new (or existing) project.

It gathers goals, distills what is *foundational* for any new agent to know on first startup, forces verification of every distillation with the human, and then scaffolds the actual artifacts:

- `AGENTS.md` — the universal truths and onboarding checklist
- Project personas (e.g. Security Officer, Infrastructure Engineer, Platform Lead…)
- Starter skills for recurring high-value procedures

## What `/bootstrap` does

1. Runs a structured interactive loop (gather → distill → verify with you → decide → create).
2. Every major piece of distilled knowledge must be explicitly confirmed by you before it is treated as foundational.
3. Produces a minimal, high-leverage set of files so that future agents dropped into the project have immediate orientation, guardrails, and the right specialized roles/skills available.

Example use cases:
- Starting a new project and wanting agents to "just know" the important things from day one.
- Adding strong role separation (Security, SRE, Domain Expert, etc.) via personas.
- Capturing the critical procedures as reusable skills.

## Installation

Clone the repository:

```bash
git clone https://github.com/lonnylot/amposer-bootstrap.git
cd amposer-bootstrap
```

### For your user environment

Copy the `skills/` directory into your preferred skills location. For example:

```bash
# For .agents (recommended for portability)
cp -r skills/* ~/.agents/skills/

# Or for Grok-specific
cp -r skills/* ~/.grok/skills/
```

### For a specific project

Copy the `skills/` directory into your project's `.agents/skills/` or `.grok/skills/` directory.

The skill will then be available as `/bootstrap`.

## Usage

```bash
/bootstrap
/bootstrap Build a secure multi-tenant control plane for IoT devices
```

The optional argument provides initial seed context for the interactive bootstrap process.

## Project Structure

```
.
├── README.md
├── LICENSE
├── .gitignore
└── skills/
    └── bootstrap/
        ├── SKILL.md
        └── references/
            ├── agent-onboarding-snippet.md
            ├── persona-template.toml
            └── skill-template.md
```

When the skill runs, it reads the templates from the `references/` directory that sits next to `SKILL.md`.

The skill creates output artifacts using the portable `.agents/` convention (with `AGENTS.md` at the project root):

- `AGENTS.md`
- `.agents/personas/<role>.toml`
- `.agents/skills/<procedure>/SKILL.md`

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

*Modeled after the structure and documentation style of [amposer-project-management](https://github.com/lonnylot/amposer-project-management).*