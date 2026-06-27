---
name: github-harness-workflow
description: Use when planning, executing, or reviewing work through GitHub Discussion, issue, PR, and evidence comments.
---

# GitHub Harness Workflow

Run AI work through GitHub surfaces instead of long chat.

## When To Use

Use this Skill when:

- starting a new project task;
- turning a loose request into work;
- splitting a Discussion into issues;
- completing an issue;
- deciding whether to close or continue.

## Inputs

- Demand Discussion, issue, PR, or user request.
- Existing repo files and relevant comments.
- Acceptance criteria or human review expectation.

## Flow

1. **Locate the source**
   - If there is a Discussion, read it first.
   - If there is an issue, read its goal, scope, acceptance, and comments.
   - If there is no durable source, ask to create a demand Discussion or task issue.

2. **Confirm the demand**
   - Identify target user, first version goal, in scope, out of scope, acceptance, and open questions.
   - If working inside a Discussion, write a demand confirmation commit.

3. **Split execution**
   - Convert confirmed demand into one or more task issues.
   - Each issue must be executable and reviewable.

4. **Execute one task**
   - Work only inside the issue scope.
   - If scope changes, stop and return to Discussion or split a new issue.

5. **Provide evidence**
   - Write an evidence comment.
   - Include changed files, PR, screenshots, command output, or links as appropriate.

6. **Recommend next step**
   - `close`: acceptance met and evidence is reviewable.
   - `continue`: same issue needs more work.
   - `split`: new task is needed.
   - `return-to-discussion`: requirements changed.

## Output Contract

Every work cycle should leave one of these:

- demand confirmation commit;
- task issue;
- PR description;
- evidence comment;
- review checklist result.

## Do Not

- Start implementation from a vague chat request when no durable source exists.
- Close an issue without evidence.
- Treat a Discussion as an execution task.
- Hide missing requirements inside a confident summary.
