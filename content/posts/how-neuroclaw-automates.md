---
title: "How NeuroClaw Automates Your Workflow"
date: 2026-05-17
draft: false
tags: ["automation", "n8n", "jobs", "workflows", "neuroclaw"]
description: "A look at NeuroClaw's automation stack — scheduled jobs, n8n workflows, webhooks, and how they all connect."
---

One of NeuroClaw's most powerful capabilities isn't the agents themselves — it's the automation infrastructure underneath them. NeuroClaw is designed to keep working even when you're not watching.

## Three Layers of Automation

### 1. The Job Scheduler

NeuroClaw has a built-in job scheduler that supports several job types:

| Job Type | What it does |
|---|---|
| `agent_message` | Sends a message to any agent on a cron schedule |
| `outbound_webhook` | POSTs to an external URL at a defined interval |
| `shell_command` | Runs a shell command on the host |
| `n8n_workflow` | Triggers a specific n8n workflow with a payload |
| `kestra_flow` | Triggers a Kestra flow with inputs |

Every job is tracked in the system. You can list, update, pause, or delete jobs at any time. Jobs also support inbound webhook slugs — so external services can trigger them.

### 2. n8n Integration

NeuroClaw has native integration with n8n, a powerful open-source workflow automation platform. From within NeuroClaw, you can:

- List all n8n workflows
- Get the full JSON definition of any workflow
- Create and activate new workflows programmatically
- Trigger workflows with custom payloads

This means NeuroClaw agents can design, deploy, and trigger n8n automations — turning agent intelligence into persistent, scheduled behavior.

### 3. Kestra Flow Orchestration

For more complex, multi-step infrastructure pipelines, NeuroClaw integrates with Kestra. Mayumi Saegusa handles Kestra orchestration — managing flows that involve long-running operations, conditional branching, and infrastructure-level tasks.

## Practical Examples

**Daily intelligence briefing:** An `agent_message` job sends Tim (the research agent) a task every morning to pull recent developments in a specific domain and summarize them to NeuroVault.

**Webhook-triggered deploy:** An inbound webhook job listens for a signal from a CI system, then triggers a Kestra flow to deploy updated infrastructure.

**Scheduled content publishing:** A cron job messages Mio every week to check for draft posts ready to publish and push them to the Hugo site.

## Why This Matters

Most AI systems are reactive — they only act when you talk to them. NeuroClaw is also *proactive*. The automation layer is what makes it possible for the system to monitor, maintain, and execute work continuously — extending your capacity beyond the hours you're actively engaged.

The goal isn't just to answer questions. It's to keep things moving while you focus on what matters most.
