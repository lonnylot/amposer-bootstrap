<!-- 
  AGENT ONBOARDING SNIPPET
  Include a short version of this near the top of the project's AGENTS.md (or as a separate AGENT-ONBOARDING.md that AGENTS.md links to).
  The goal: a brand-new agent (or a human pasting context for a new session) can read 1-2 screens and be useful + safe immediately.
-->

## New Agents & Bootstrapped Sessions — Start Here

1. **Internalize the Mission & Success Definition** (see top of this file).
2. **Read the "Core Domain Concepts & Invariants"** section. These are non-negotiable.
3. **Know the Information Architecture**: where truth lives (specific files, this AGENTS.md, the personas below, key skills, external systems).
4. **Adopt the right stance quickly**:
   - Use `/personas` (or the agents modal) to load relevant personas for the task.
   - Example: for anything touching security, auth, or data exposure, activate the `security-officer` (or equivalent) persona on subagents.
5. **Use the project's foundational skills** for repeatable work:
   - `/<primary-skill-1>`
   - `/<primary-skill-2>`
6. **Verify before you ship or advise**. Every significant output should be traceable to a verified step or explicit user confirmation.
7. **When in doubt, surface it**. A short "From the <Role> perspective: ..." note is often the highest-value contribution a new agent can make.

If this is your first time in the project, run the following before making changes:
- (Populated by the bootstrap process — e.g. "read the architecture overview at docs/architecture.md", "run `make dev` and confirm it comes up cleanly", "list the .grok/skills directory".)

After the first 10-15 minutes you should be able to answer:
- What is the single most important outcome this project is trying to achieve right now?
- What is the one thing we must never do?
- Where would you look first for the current state of X?

If you cannot answer those three questions, ask the user for clarification before proceeding.
