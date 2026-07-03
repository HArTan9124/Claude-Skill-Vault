# 🧠 HarTan Labs — Claude Skills Vault

> **A curated, open-source collection of Claude skill prompts for every major software engineering role.**
> Drop any skill into your Claude project and get a focused, role-appropriate AI collaborator — not a generalist trying to do everything at once.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Skills](https://img.shields.io/badge/skills-21-brightgreen)](#-skill-hierarchy)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-orange.svg)](CONTRIBUTING.md)

---

## What Is This?

Each folder in this vault contains a single `SKILL.md` file — a structured Claude prompt that makes Claude behave like a seasoned professional in a specific role.

**Why role-specific skills?**

A generalist assistant tries to be everything: architect, debugger, writer, QA. Skills solve this by giving Claude a **clear job**, a **decision-making framework**, and explicit **guardrails** for that role only. The result is sharper, more consistent, and more actionable output.

---

## How to Use

### Claude Projects (Recommended)

1. Open [Claude.ai](https://claude.ai) and create or open a **Project**.
2. Go to **Project Instructions**.
3. Copy the full contents of any `SKILL.md` and paste it as the project's custom instructions.
4. Start a conversation — Claude will now behave as that role.

### Per-Conversation

1. Open a new Claude conversation.
2. Paste the full contents of a `SKILL.md` as your first message or system prompt.
3. Proceed with your task.

### Trigger Phrases

Each skill defines specific trigger phrases in its `description` frontmatter (e.g., `"as my backend engineer"`, `"review this code"`). Using these phrases keeps Claude in role even across long conversations.

---

## 🏗️ Skill Hierarchy

Skills are arranged from the **ground up** — the same way a real engineering organization is structured. Start at the bottom with infrastructure, build up through application code, and reach strategy and leadership at the top.

```
┌─────────────────────────────────────────────┐
│          TIER 7 — LEADERSHIP                │
│                   CEO                       │
├─────────────────────────────────────────────┤
│          TIER 6 — PLANNING & STRATEGY       │
│     Software Architect · Product Manager    │
│           Research Scientist                │
├─────────────────────────────────────────────┤
│          TIER 5 — COMMUNICATION             │
│             Technical Writer                │
├─────────────────────────────────────────────┤
│     TIER 4 — QUALITY & SAFETY               │
│  Security Engineer · Code Reviewer          │
│         QA Engineer                         │
├─────────────────────────────────────────────┤
│     TIER 3 — INTELLIGENCE LAYER             │
│     AI / ML Engineer · MLOps Engineer       │
├─────────────────────────────────────────────┤
│     TIER 2 — APPLICATION LAYER              │
│  Backend · Frontend · Mobile · Game Dev     │
├─────────────────────────────────────────────┤
│     TIER 1 — DATA LAYER                     │
│  Data Engineer · Database Administrator     │
├─────────────────────────────────────────────┤
│     TIER 0 — INFRASTRUCTURE LAYER           │
│  Embedded · Cloud · DevOps · Platform · SRE │
└─────────────────────────────────────────────┘
```

---

### Tier 0 — Infrastructure Layer

> The foundation everything else runs on: hardware, cloud, deployment pipelines, and reliability.

| Skill | Best Used For |
|---|---|
| [🔩 Embedded Engineer](embedded-engineer/SKILL.md) | Firmware, MCUs, RTOS, bare-metal C/C++, hardware interfaces |
| [☁️ Cloud Engineer](cloud-engineer/SKILL.md) | IaC, IAM, cloud resource provisioning, cost optimization |
| [⚙️ DevOps Engineer](devops/SKILL.md) | CI/CD pipelines, Docker, deployment automation, environment setup |
| [🏛️ Platform Engineer](platform-engineer/SKILL.md) | Internal developer platforms, golden paths, self-service tooling |
| [📡 Site Reliability Engineer](site-reliability-engineer/SKILL.md) | SLOs, alerting, incident response, runbooks, toil reduction |

---

### Tier 1 — Data Layer

> Where raw data is stored, moved, and shaped into something queryable and reliable.

| Skill | Best Used For |
|---|---|
| [🗄️ Database Administrator](database-administrator/SKILL.md) | Schema design, query tuning, migrations, indexing, backups |
| [🔀 Data Engineer](data-engineer/SKILL.md) | ETL pipelines, data warehouses, streaming, data quality |

---

### Tier 2 — Application Layer

> The code users and systems directly interact with, across every surface.

| Skill | Best Used For |
|---|---|
| [🖥️ Backend Engineer](backend-engineer/SKILL.md) | APIs, authentication, business logic, server-side code |
| [🎨 Frontend Engineer](frontend-engineer/SKILL.md) | UI components, state management, accessibility, client-side logic |
| [📱 Mobile Engineer](mobile-engineer/SKILL.md) | iOS, Android, Flutter, React Native, device APIs |
| [🎮 Game Developer](game-developer/SKILL.md) | Game loops, physics, rendering pipelines, game systems |

---

### Tier 3 — Intelligence Layer

> Building, deploying, and maintaining machine learning and AI capabilities.

| Skill | Best Used For |
|---|---|
| [🤖 AI / ML Engineer](ai-engineer/SKILL.md) | Model selection, ML pipelines, prompt engineering, LLM integration |
| [🚀 MLOps Engineer](mlops-engineer/SKILL.md) | Model deployment, drift monitoring, retraining pipelines, feature stores |

---

### Tier 4 — Quality & Safety

> The gate between code written and code trusted — correctness, security, and reliability.

| Skill | Best Used For |
|---|---|
| [🔐 Security Engineer](security-engineer/SKILL.md) | Threat modeling, vulnerability review, auth, secrets handling, hardening |
| [👁️ Code Reviewer](code-reviewer/SKILL.md) | PR reviews, bug hunting, security checks, pre-ship validation |
| [🧪 QA Engineer](qa-engineer/SKILL.md) | Test strategies, test case design, edge cases, test code |

---

### Tier 5 — Communication

> Turning technical work into knowledge that can be found, understood, and acted on.

| Skill | Best Used For |
|---|---|
| [✍️ Technical Writer](technical-writer/SKILL.md) | READMEs, API docs, guides, runbooks, changelogs |

---

### Tier 6 — Planning & Strategy

> Deciding what to build, how to structure it, and what the evidence says.

| Skill | Best Used For |
|---|---|
| [🏗️ Software Architect](software-architect/SKILL.md) | System design, architecture tradeoffs, tech stack selection |
| [📋 Product Manager](product-manager/SKILL.md) | Feature scoping, user stories, MVP definition, prioritization |
| [🔬 Research Scientist](research-scientist/SKILL.md) | Paper summaries, literature synthesis, method evaluation |

---

### Tier 7 — Leadership

> Direction, prioritization, and accountability across everything.

| Skill | Best Used For |
|---|---|
| [👔 CEO / Chief of Staff](ceo-skill/ceo/SKILL.md) | Prioritization, weekly reviews, scope cutting, decision quality |

---

## Skill Format

Every `SKILL.md` follows the same structure so they are easy to read, extend, and compare:

```markdown
---
name: role-name
description: >
  When to activate this skill and trigger phrases.
---

# Role Title

One-line identity statement.

## Core behaviors
Numbered list of the most important decision rules for this role.

## Output shape
What the response should always contain.

## Do NOT
Hard guardrails — what this role must never do.
```

---

## Design Principles

These skills were designed with three constraints in mind:

1. **Generalized, not project-specific.** No skill contains hardcoded project names, URLs, or company-specific logic. They work for any codebase and any team size.

2. **Role-contained.** Each skill stays in its lane. A backend engineer skill does not give frontend advice. A security engineer skill does not write application features. This prevents the "generalist drift" that makes AI assistants less useful over long sessions.

3. **Opinionated but honest.** Skills define strong defaults (e.g., "idempotency is non-negotiable" for data engineers) while explicitly surfacing tradeoffs. Claude should help you decide well, not just agree with you.

---

## Contributing

Contributions are welcome and encouraged. This vault grows better when more roles and disciplines are represented.

### Adding a New Skill

1. Fork this repository.
2. Create a new folder named after the role (lowercase, hyphenated): `my-new-role/`
3. Add a `SKILL.md` file following the [format above](#skill-format).
4. Make sure the skill:
   - Is **generalized** — no project-specific content
   - Is **role-contained** — covers only what that role would reasonably own
   - Has at least **3–5 core behaviors** and clear **Do NOT** guardrails
   - Includes **trigger phrases** in the `description` frontmatter
5. Open a Pull Request with a brief description of the role and why it fills a gap.

### Improving Existing Skills

If you find a skill too narrow, outdated, or missing a critical behavior, open an issue or PR with the proposed change and the reasoning behind it.

---

## License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

You are free to use, copy, modify, and distribute these skills in personal and commercial projects.

---

## Author

Built and maintained by **Harshit Tandon** ([@HarTan-Labs](https://github.com/HarTan-Labs)).

If this vault is useful to you, consider starring the repo or contributing a skill. Every role added makes this more useful for everyone.
# Claude-Skill-Vault
