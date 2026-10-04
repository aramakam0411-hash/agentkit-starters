---
name: workflow-to-agent
description: Turn a repeated real-world task into a bounded AI agent workflow with inputs, outputs, tool actions and a useful first trial. Use when someone wants to automate a task but the agent's job is still vague.
---

# Workflow to agent

Map the task as it happens today: what starts it, what information arrives, which decisions need judgment, and what useful result finishes it. Preserve the user's existing tools and constraints. Do not add several agents merely because a task has several steps.

Use [the workflow sheet](../../templates/agent-workflow.md). For each step, distinguish a deterministic operation, a reasoning decision and an external action. Use ordinary code or a form where judgment adds no value. Give the agent tools only for the required steps and define what it should do when an important input is missing.

Make the output contract concrete: required fields, evidence or source links when applicable, and the destination. For a research shortlist, the output might be three candidates with reasons and sources. For an enquiry assistant, it might be a draft response with missing details highlighted; it must not invent prices or availability.

Choose a first trial using sample or supplied permitted data. Define a normal input, an incomplete input and an expected outcome for each. If sending, booking or payment is part of the eventual task, keep the trial at the preview stage unless the actual action is already authorized. Leave that action's approval point explicit.

Produce the workflow, a usable agent instruction and the trial checklist. Report which integrations are real and which are simulated. A plausible diagram is a design, not proof that an automation runs; verify execution before describing it as live.
