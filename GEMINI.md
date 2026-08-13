# Project Rescue Engineer - Autonomous Agent Workspace Guidelines

## Overview
This repository contains the `rescue-engineer` project. Antigravity operates in **autonomous mode** within this workspace. When assigned a task, the agent should proactively inspect, plan, implement, verify, and document changes with minimal unnecessary interruption.

---

## 1. Autonomous Execution Protocol

When given a task, follow this autonomous lifecycle:

1. **Discovery & Context Gathering**:
   - Explore existing files, configurations, and architecture before making changes.
   - Never assume missing context—search the workspace and relevant docs.

2. **Execution & Implementation**:
   - Implement clean, production-grade solutions.
   - Preserve existing unrelated code, comments, docstrings, and configurations.
   - Avoid placeholder code or mock implementations unless explicitly requested.

3. **Verification & Self-Correction**:
   - Automatically run relevant test suites, linters, or build scripts after modifying code.
   - If tests or builds fail, inspect the failure logs and fix issues autonomously before concluding the task.

4. **Structured Delivery**:
   - Provide a concise summary of all changes made.
   - Link all touched files and functions using clickable markdown file links (`[file.ext](file:///path/to/file)`).

---

## 2. Safety & Guardrails

- **Scope Boundary**: Confine modifications to the `/users/sadeq/projects/rescue-engineer` workspace.
- **Sensitive Information**: Never commit or expose API keys, credentials, or `.env` secrets.
- **Destructive Operations**: Never run destructive Git commands (e.g. `git reset --hard`, `git push --force`) or delete major directories without explicit instruction.
- **Documentation**: Keep `README.md` and relevant technical documentation updated with any new architecture or tools introduced.

---

## 3. Customizations & Rules

Project rules, skills, and agent configs are maintained inside the [`.agents/`](file:///users/sadeq/projects/rescue-engineer/.agents/) directory.
