---
name: <kebab-skill-name>
description: >
  <One or two sentence description of what the skill does. Include the main trigger phrases and the slash command form so the model can decide when to auto-invoke it. Example: "Perform a security-focused review of infrastructure changes. Use when the user asks for a security review, /security-review, or needs blast-radius analysis of a change.">
argument-hint: "<brief hint for the slash autocomplete, e.g. 'infra change description or PR link'>"
user-invocable: true
---

# <Human Readable Skill Name>

<One paragraph: what this skill is for and the outcome it produces.>

## When to Use

- Bullet list of concrete situations
- Include both explicit slash command cases and natural language triggers

## Core Rules (never violate)

- Rule 1 (most important)
- Rule 2
- ...

## Steps

1. **Preparation**  
   What to read or run first (use specific tool names: `read_file`, `run_terminal_command`, `grep`, `list_dir`, etc.).

2. **Execution**  
   The actual work. Be concrete about commands, file paths to write, and expected formats.

3. **Verification**  
   How the agent (and user) know the work is good. Explicit checks, tests, or review steps.

4. **Output**  
   What to write where (summary file, updated review file, PR description, etc.). Always include exact paths the caller supplied.

## Anti-Hallucination & Tool Discipline

- Every claim that you performed an action must be backed by a real tool call in the same turn or visible in history.
- After writing any file, read it back before declaring success.
- Prefer explicit paths passed in the prompt over guessing.

## Examples (optional but valuable)

```
 /<kebab-skill-name> <realistic example argument>
```

## Notes for Future Improvement

- Things the first version deliberately left as "later" (the bootstrapper can note these).
- Common patterns this skill should eventually learn from memory (if a memory system exists in the project).
