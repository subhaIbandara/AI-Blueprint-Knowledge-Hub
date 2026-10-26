# Skills — Reusable AI Instructions

## What Are Skills?

Skills are reusable sets of instructions, knowledge, and guidelines that help AI assistants perform specific tasks consistently and effectively.

Instead of explaining the same requirements every time, we define them once in a skill and reuse them whenever needed.

A skill can include instructions, workflows, examples, reference materials, scripts, and validation rules that guide an AI assistant through a particular task.

## Why Are Skills Important?

Skills help us move beyond generic AI responses towards more consistent, context-aware, and task-specific assistance.

For QA engineers, skills can help AI assistants:

- Generate test cases from requirements and acceptance criteria.
- Create Playwright automation using existing project conventions.
- Review test code for quality, maintainability, and coverage.
- Analyse test failures and investigate potential root causes.
- Test AI applications for accuracy, hallucinations, and reliability.
- Follow established security rules and engineering standards.

Skills are also useful for software development, code reviews, documentation, AI agents, and other repeatable engineering workflows.

## How Do We Create a Skill?

We define each skill in a file named `SKILL.md`. This file contains the instructions that explain what the skill does, when to use it, and how the AI assistant should perform the task.

A well-structured skill typically includes:

| Component | Purpose |
|---|---|
| Name | A unique, descriptive identifier. |
| Description | What the skill does and when to use it. |
| Instructions | Steps and rules the AI should follow. |
| Core Principles | Standards that guide decisions. |
| Inputs and Context | Required information, files, and resources. |
| Expected Output | The expected result and its format. |
| Validation | How to verify correctness and quality. |
| Security Guardrails | Restrictions that prevent unsafe actions and protect sensitive information. |
| Examples and References | Supporting examples and documentation. |
| When to Use | Scenarios where the skill is applicable. |
| When Not to Use | Scenarios where the skill is not applicable. |

Not every skill needs every section. Adapt the structure to the task and keep the instructions clear, focused, and reusable.

## Recommended Skill Structure

A skill can start with a single `SKILL.md` file and grow when additional resources become necessary.

```text
skill-name/
├── SKILL.md
├── references/
│   └── supporting-docs.md
├── examples/
│   └── example.md
└── scripts/
    └── validation-script.py
```

- `SKILL.md` — Main skill instructions and metadata.
- `references/` — Supporting documentation and detailed guidance.
- `examples/` — Examples of expected inputs and outputs.
- `scripts/` — Optional scripts for automation and validation.

## Core Principles

### 1. Be Specific
Provide clear, actionable instructions, constraints, and expected outcomes.

### 2. Use Trusted Sources
Follow approved requirements, project documentation, API specifications, and existing code. For QA automation, never invent endpoints, selectors, test data, or expected behaviour.

### 3. Prevent Hallucinations
When information is missing or uncertain, state the limitation, request clarification when necessary, and never present assumptions as verified facts.

### 4. Validate the Output
Review generated results against requirements. Run appropriate checks and tests whenever possible and authorised.

### 5. Apply Security Guardrails
Protect credentials, tokens, personal information, and confidential code. Avoid unauthorised access and destructive actions.

### 6. Keep Skills Reusable
Separate general instructions from project-specific details so skills can be adapted to different projects.

### 7. Keep Skills Maintainable
Use clear instructions, version control, representative examples, and regular reviews to keep skills accurate and up to date.

## When Should We Use a Skill?

Use a skill when a task:

- Is repeated frequently.
- Requires a consistent workflow or output format.
- Needs specialised domain knowledge.
- Must follow project conventions or quality standards.
- Benefits from explicit validation and security rules.
- Can be reused across tasks or projects.

A skill may not be necessary for a simple, one-time question.

## Skills for QA and AI Engineering

This repository may include skills for:

- Test planning and test case generation.
- Playwright and API test automation.
- Test code review and debugging.
- CI/CD testing workflows.
- AI application testing and evaluation.
- Prompt engineering and structured outputs.
- AI agents, MCP, and tool integration.
- RAG evaluation and hallucination detection.
- AI security, reliability, and observability.

## Creating a Skill File

We write skills in Markdown (`.md`) format, usually using a file named `SKILL.md`. This file contains the instructions that guide an AI assistant in performing a specific task.

Before creating a skill, let's understand why we use Markdown and how to create and preview a Markdown file.

## Why Do We Write Skills in Markdown Format?

Markdown is simple, readable, and easy to maintain. It allows us to organise skill instructions using headings, lists, tables, code blocks, and examples.

Using Markdown makes skill instructions easy for humans to understand, easy to maintain in GitHub, and suitable for AI assistants to process.

## How to Create and Preview Markdown Files for Free

You can use [StackEdit](https://stackedit.io/app), a free, browser-based Markdown editor.

1. Open StackEdit.
2. Create a new Markdown document.
3. Write your content using Markdown syntax.
4. Preview the formatted document.
5. Export or download the file when needed.

You can also create and edit `.md` files directly in VS Code or GitHub.

**Example:** `SKILL.md` contains the instructions for a particular skill, while `README.md` explains the purpose and structure of your skills collection.


## Important Reminder

A skill guides an AI assistant; it does not guarantee correctness. Results still depend on the quality of the instructions, available context, source material, tools, and validation.

**The goal is to make AI-assisted work more consistent, traceable, secure, and reliable.**