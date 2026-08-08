---
name: phaser
description: >
  Generates a self-contained Phaser execution document (.phaser.md) that breaks a task down into a sequence of prompts.
  Trigger on "create a solution doc", "solve this with phaser", or when asked to plan a phased task.
---

# Phaser

A workflow where tasks are broken down into a sequence of prompts stored in an independent, self-contained markdown file (a "phase file"). The phase file is saved in the project's `phaser/` directory.

The phase file contains its own execution instructions, making it independent of any external state machines or modes. Any AI assistant reading the phase file can execute it sequentially based on the embedded rules.

## Goal

When triggered, your goal is to analyze the user's task and generate a complete, self-contained phase file (`phaser/<kebab-style-description>.phaser.md`). Do not attempt to execute the code or solve the task directly; instead, write the sequence of prompts needed to solve it.

## Phase File Generation Rules

1. **Directory Location**: All phase files MUST be written to the `phaser/` directory at the root of the project workspace. Create this directory if it is missing.
2. **File Naming**: Use kebab-case for the file name (e.g., `phaser/add-user-auth.phaser.md`).
3. **Template**: You MUST generate the file using the exact structure and rules defined in the "Phase File Template" section below.
4. **Prompts**: Break the user's task into distinct, logical prompts. Each prompt must clearly explain what needs to be done in that step.
5. **Gates**: Assign one of the following gates to each prompt:
   - `STOP & COMMIT`: The execution must pause after this prompt to allow the user to review and commit changes.
   - `NEEDS CLARIFICATION`: The execution must pause to ask the user a question before proceeding.
   - `NONE`: Execution can proceed immediately to the next prompt.

---

## Phase File Template

Use the following template for the generated phase file. The generated file MUST include the "Instructions for AI Execution" preamble exactly as written so the executing agent understands the rules.

```markdown
# Phase: <Short Title>

## Task Description
<A clear description of the overall task this phase file will accomplish.>

## Instructions for AI Execution
This is a self-contained phase file. If you are an AI assistant tasked with executing this file, you must follow these rules strictly:
1. **Sequential Execution**: Execute the prompts under `## Prompts to Execute` in numerical order. Skip prompts that already have an `***After Action***` section beneath them.
2. **After Action**: Immediately after successfully executing a prompt, append an `***After Action***` block directly beneath the prompt. This block should contain explanations of the work done, changes made, and any documentation instructions.
3. **Respect the Gate**: After writing the `***After Action***` block, look at the `Gate` defined for that prompt:
   - `STOP & COMMIT`: Stop execution, suggest a commit command to the user, and wait for them to confirm the commit before running the next prompt.
   - `NEEDS CLARIFICATION`: Stop execution and ask the user for the needed input.
   - `NONE`: Proceed to the next prompt.
4. **Final Documentation Evaluation**: Once all prompts have been executed (all have an `***After Action***` block), evaluate all the after-actions. If warranted, generate or update project documentation in the `./docs/` directory summarizing the completed work.

## Prompts to Execute

### 1. <Title of Step 1>
**Prompt:** <Detailed instructions on what needs to be accomplished in this step. e.g., "Create the initial database schema in `schema.sql` based on the user data model...">
**Gate:** <STOP & COMMIT | NEEDS CLARIFICATION | NONE>

<!-- During execution, the ***After Action*** block will be injected here -->

### 2. <Title of Step 2>
**Prompt:** <Detailed instructions for step 2...>
**Gate:** <STOP & COMMIT | NEEDS CLARIFICATION | NONE>

<!-- Add as many numbered prompts as necessary to complete the task -->

## Final Step: Documentation
Once all prompts above have been executed and have their corresponding `***After Action***` blocks, evaluate the accumulated work and create/update documentation in `./docs/` if warranted.
```
