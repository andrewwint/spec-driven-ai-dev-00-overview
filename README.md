# Spec-Driven AI Development

> **"Manage the LLM's context window like you manage your own attention."**

A hands-on 5-course series for engineers, product managers, and technology leaders adopting AI skills, open standards like AgentSkills.io, and LLM workflows in real production environments.

[![Course 1](https://img.shields.io/badge/Course%201-Foundations-blue)](https://github.com/andrewwint/spec-driven-ai-dev-01-foundations)
[![Course 2](https://img.shields.io/badge/Course%202-Data%20Platform-green)](https://github.com/andrewwint/spec-driven-ai-dev-02-data-platform)
[![Course 3](https://img.shields.io/badge/Course%203-ML%20Pipelines-orange)](https://github.com/andrewwint/spec-driven-ai-dev-03-ml-pipelines)
[![Course 4](https://img.shields.io/badge/Course%204-API%20%26%20Agents-red)](https://github.com/andrewwint/spec-driven-ai-dev-04-api-agents)
[![Course 5](https://img.shields.io/badge/Course%205-DevOps-purple)](https://github.com/andrewwint/spec-driven-ai-dev-05-devops)

---

# TL;DR for Engineering Leaders

Spec-Driven AI Development provides a disciplined way to use **AI skills and open standards safely inside production software delivery**.

Teams follow **specs → specialized agents → automated gates → human review** instead of ad-hoc prompting.

Typical outcomes:

- **20–40% reduction in repetitive coding and research time**
- fewer defects from hallucinated output
- faster onboarding
- standardized, auditable AI usage aligned with CI/CD and compliance

**AI becomes a productivity multiplier — not technical debt.**

---

## Executive Summary

![Image](https://miro.medium.com/1%2AD2PhsXB2eS0VvDKFC482CA.png)
_Example Agent Development Lifecycle (ADLC) you could have for your organization._

### What is this?

A practical framework and course series that teaches teams how to integrate AI agents directly into the Software Development Life Cycle (SDLC) safely and predictably.

This is not about replacing engineers. It's about increasing engineering leverage while maintaining the same standards for **reliability**, **testing**, **governance**, and **accountability**.

### The Approach

- **Instead of:** "Prompt and hope"
- **We use:** Specs → Agents → Deterministic Gates → Human Review

### Business Impact

| Metric           | Impact | Description                                                        |
| :--------------- | :----- | :----------------------------------------------------------------- |
| **Productivity** | High   | Faster scaffolding, automated research, quicker prototyping.       |
| **Quality**      | High   | Smaller scoped tasks, fewer hallucinations, automated tests/gates. |
| **Risk**         | Low    | Audit trails, reproducible workflows, SOC2/ISO compatible.         |

### Example ROI (Conservative)

**For a team of 6 engineers:**

- **Research & Docs:** 3–5 hrs saved/week
- **Boilerplate/Scaffolding:** 3–6 hrs saved/week
- **Rework Reduction:** 2–4 hrs saved/week
- **Total:** **≈ 8–15 hrs saved per engineer per week**

**[📊 See detailed ROI analysis →](docs/roi-analysis.md)** — includes solo developer vs. team comparisons, division of labor, collaboration patterns, and how to measure your own ROI.

---

## ⚡ Quick Start (5 Minutes)

See the workflow immediately.

```bash
git clone https://github.com/andrewwint/spec-driven-ai-dev-01-foundations
cd spec-driven-ai-dev-01-foundations
uv pip install -r requirements.txt
code .
```

**Then:**

1. Write a small spec.
2. Ask the **Advisor Agent** for guidance.
3. Generate a solution.
4. Review output with gates.

### Responsibility Swimlane

**Humans own the bookends.** AI assists in the middle.

| Phase         | Human Engineer  | Research Agent | Build Agents   | Review Agents |
| ------------- | --------------- | -------------- | -------------- | ------------- |
| **Discovery** | ✅ Write spec   | Gather docs    |                |               |
| **Planning**  | Approve design  | Summaries      | Draft skeleton |               |
| **Build**     | Guide direction |                | Generate code  |               |
| **Validate**  | Inspect output  |                |                | Tests/gates   |
| **Deploy**    | ✅ Own release  |                |                |               |

> AI doesn't replace judgment. It amplifies your capacity to exercise judgment.

---

## Core Concepts

### Progressive Disclosure

Don't dump all instructions upfront. Deliver context to agents **when it's relevant**:

| Method                 | Example                                         |
| ---------------------- | ----------------------------------------------- |
| **Decided to be read** | Advisor says "read docs/patterns/X.md for this" |
| **Discovered**         | Agent learns conventions from existing code     |
| **Triggered**          | Pre-commit hooks fire validation instructions   |
| **Given in feedback**  | Test failures guide the fix                     |

> _See: [Delivering Instructions to AI Models](https://blog.huikang.dev/2025/10/20/delivering-ai-instructions.html)_

### The DARE Model

A decision framework for balancing AI and deterministic tooling:

| Letter | Principle                | Question                                            |
| ------ | ------------------------ | --------------------------------------------------- |
| **D**  | **Deterministic First**  | Can this be a script, regex, or rule? Don't use AI. |
| **A**  | **AI for Ambiguity**     | Does this require judgment or generation? Use AI.   |
| **R**  | **Review at Boundaries** | Where should humans checkpoint?                     |
| **E**  | **Escalate on Failure**  | What triggers handoff? Define limits.               |

### The Advisor Pattern

Some agents don't generate code. They **guide**:

- Summarize documentation.
- Explain domain concepts.
- Suggest architectural patterns.

> _Think: A senior teammate giving direction, not auto-piloting your keyboard._

### Model Tier Selection

Use the **cheapest model that can do the job**:

| Tier         | Use For                    | Examples                     |
| ------------ | -------------------------- | ---------------------------- |
| **Fast**     | Simple tasks, translations | Smallest available model     |
| **Balanced** | Code review, teaching      | Mid-tier reasoning model     |
| **Premium**  | Architecture decisions     | Most capable available model |

Model selection is a skill. Don't default to premium.

### 10x Your Google Fu (MCP)

Agents connect directly to documentation using the **Model Context Protocol (MCP)** to fetch official docs and compare options. Lookup time drops from minutes to seconds.

### Enterprise = Easy to Reason About

Enterprise doesn't mean complex. It means code that others can **understand and contribute to**:

| Anti-Pattern             | Enterprise Pattern                          |
| ------------------------ | ------------------------------------------- |
| One giant CDK stack      | Multi-stack: network, data, api, monitoring |
| 500-line workflow file   | Reusable workflow templates                 |
| Tribal knowledge         | Runbooks and playbooks                      |
| "It works on my machine" | Docker + consistent environments            |
| Long-lived credentials   | OIDC + short-lived tokens                   |

> _The test: "Can a new team member understand this in a day?"_

---

## 🎓 Capstone Outcomes

By the end of this series, you will have a **Production-Ready System**:

- ✅ **Agent-Assisted SDLC:** A repeatable lifecycle from idea → production.
- ✅ **Specialized Agents:** Research • Advisor • Planner • Builder • Reviewer • Historian.
- ✅ **Production Artifacts:** APIs, pipelines, models, CI/CD, monitoring.
- ✅ **Reusable Templates:** Specs, repo structure, guardrails, agent patterns.
- ✅ **Practical Judgment:** Knowing when **not** to use AI is as important as knowing when to use it.

---

## 📚 The Learning Path

| <div style="width: 200px;">Course</div> | Focus and Key Concept Introduced                                                   | Time |
| --------------------------------------- | ---------------------------------------------------------------------------------- | ---- |
| **1. Foundations**                      | Spec-driven workflow, DARE Model, Doer+Gate agents                                 | ~9h  |
| **2. Data Platform**                    | Pipelines + Advisors, **Advisor Pattern, Progressive Disclosure**                  | ~10h |
| **3. ML Pipelines**                     | Models + Eval Gates, Experiment Proposals, Evaluation Gates, 🏢 Enterprise Context | ~9h  |
| **4. API & Agents**                     | Services + MCP, **MCP Documentation Access** ("10x Google Fu")                     | ~9h  |
| **5. DevOps**                           | Deployment + Ops, Plan Before Apply, Compliance as Code                            | ~9h  |

**Total:** ~46 hours of content

### Patterns That Thread Through Every Course

| Pattern                    | Introduced | Continues Through |
| -------------------------- | ---------- | ----------------- |
| **Advisor Agent**          | Course 2   | 3, 4, 5           |
| **Progressive Disclosure** | Course 2   | 3, 4, 5           |
| **🏢 Enterprise Context**  | Course 3   | 4, 5              |
| **ROI Trade-off Analysis** | Course 2   | 3, 4, 5           |
| **Focused Proposals**      | Course 2   | 3, 4, 5           |

---

## 🛠️ Tooling

**We keep the stack open and standard:**

- **Editor:** VS Code or any editor with AI skill support
- **Standards:** [AgentSkills.io](https://agentskills.io) open standard (widely adopted, tool-agnostic)
- **Runtime:** Python 3.10+, Node 18+
- **Pkg Mgr:** uv (fast Python management)
- **No proprietary vendor lock-in required.**

#### Observability (Optional but Recommended)

| Tool                                                                                          | Purpose               | Why We Use It                                                                                                                              |
| :-------------------------------------------------------------------------------------------- | :-------------------- | :----------------------------------------------------------------------------------------------------------------------------------------- |
| **[Splitrail](https://marketplace.visualstudio.com/items?itemName=piebald.splitrail-vscode)** | Token & Cost Tracking | "Context is Attention." This tool visualizes exactly how much context (and money) you are consuming, helping you validate ROI assumptions. |

---

## 📁 Repository Structure

Each course follows the same repo layout:

```text
spec-driven-ai-dev-0X-[course-name]/
├── README.md                # Course overview & how to use
├── code/
│   ├── 01-[module-name]/    # Complete snapshot at Module 1
│   ├── 02-[module-name]/    # Complete snapshot at Module 2
│   └── ...                  # One folder per module
├── slides/                  # Course slides (if any)
└── attachments/             # Templates, cheat sheets, extras
```

Each `code/0X-*/` folder is a **complete, runnable project** at that module checkpoint. Browse on GitHub or clone and explore any module.

### Inside Each Module Snapshot

```text
code/0X-[module-name]/
├── README.md
├── CHANGELOG.md         # What shipped (Human owned)
├── HISTORY.md           # Persistent context (Agent owned)
├── AGENTS.md            # Agent definitions & strategy
├── src/                 # Application source code
└── skills/              # AgentSkills.io skill definitions
```

---

## Principles Over Tools

We teach underlying principles that **transfer to any tooling**:

| Our Approach      | Industry Standard  | Why We Choose Ours                |
| ----------------- | ------------------ | --------------------------------- |
| pandas → Lambda   | dbt + warehouse    | Same principles, simpler setup    |
| Python validation | Great Expectations | You understand what's happening   |
| Makefile triggers | Airflow DAGs       | Focus on logic, not orchestration |
| Flask             | FastAPI            | Patterns transfer                 |
| CDK               | Terraform          | Both are IaC thinking             |

When you're ready to adopt industry tools, you'll recognize the thinking.

---

## 🚀 Start Here

**[👉 Course 1: Foundations](https://github.com/andrewwint/spec-driven-ai-dev-01-foundations)**
