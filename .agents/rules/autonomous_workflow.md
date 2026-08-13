# Autonomous Workflow Rules

## Objective
Enable autonomous problem solving, task completion, and end-to-end verification within the workspace.

## Core Rules

1. **End-to-End Task Ownership**:
   - When a task is assigned, own the full problem from diagnosis to working solution.
   - Do not stop halfway or ask for manual steps that can be automated (such as installing packages, running builds, or executing tests).

2. **Self-Healing & Diagnostics**:
   - When encountering build, compiler, runtime, or test errors, analyze the stack trace immediately.
   - Edit the appropriate files and re-test until the pipeline passes.

3. **Subagent Delegation**:
   - For complex, multi-part tasks, spawn specialized subagents (e.g., `research`) to investigate parallel components or deep documentation without cluttering the main conversation context.

4. **Transparent Artifacts**:
   - Use structured artifacts for extensive architectural reports, system diagrams, or comprehensive test matrices.
