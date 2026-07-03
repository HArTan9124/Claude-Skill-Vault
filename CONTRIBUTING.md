# Contributing to HarTan Labs — Claude Skills Vault

Thank you for taking the time to contribute. Every skill added or improved makes this vault more useful for the community.

---

## Ways to Contribute

| Type | Description |
|---|---|
| **New skill** | Add a skill for a role not yet covered |
| **Improve an existing skill** | Fix inaccuracies, add missing behaviors, improve trigger phrases |
| **Bug report** | Open an issue if a skill produces consistently poor results |
| **Discussion** | Open an issue to propose a new role or discuss the skill format |

---

## Adding a New Skill

1. **Fork** this repository and create a new branch: `skill/your-role-name`
2. Create a new folder: `your-role-name/`
3. Add a `SKILL.md` inside it following this exact structure:

```markdown
---
name: your-role-name
description: >
  One paragraph: what this skill does, when to use it, and trigger phrases.
  Triggers on: "as my X", "specific phrase", "another phrase".
---

# Role Title

One-sentence identity statement. What this role cares about most.

## Core behaviors
1. **Behavior name.** Explanation of the principle and why it matters for this role.
2. **Behavior name.** ...
(3–6 behaviors recommended)

## Output shape
- What every response from this role should always contain.
- Keep this prescriptive and concrete.

## Do NOT
- Hard guardrail one.
- Hard guardrail two.
```

4. **Checklist before opening a PR:**
   - [ ] Skill is fully generalized — no project-specific content, URLs, or company names
   - [ ] Skill is role-contained — does not bleed into adjacent roles
   - [ ] Trigger phrases are natural and distinct from existing skills
   - [ ] `Do NOT` section has at least 2 meaningful guardrails
   - [ ] Folder name is lowercase and hyphenated

5. Open a **Pull Request** with:
   - The role name in the title
   - A 1–2 sentence description of what gap this fills

---

## Improving an Existing Skill

- Open an issue first if the change is significant (rewording a core behavior, adding/removing a guardrail).
- For small fixes (typos, clarity improvements), a direct PR is fine.
- Always explain *why* in the PR description — "this behavior was missing" is more useful than "updated skill."

---

## Code of Conduct

Be direct, constructive, and respectful. Critique the skill content, not the person who wrote it.
