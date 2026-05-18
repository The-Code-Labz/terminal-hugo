---
title: "The Memory Stack — How NeuroClaw Remembers"
date: 2026-05-17
draft: false
tags: ["memory", "neurovault", "knowledge", "neuroclaw", "rag"]
description: "How NeuroClaw stores, retrieves, and reasons over persistent knowledge using NeuroVault and the memory stack."
---

One of the fundamental limitations of most AI systems is that they forget. Every conversation starts fresh, with no knowledge of what came before. NeuroClaw is built differently.

## The Problem With Stateless AI

When an AI system has no memory:
- Every session requires re-explaining context
- Preferences have to be repeated
- Insights discovered in one conversation disappear
- Work done yesterday is invisible today

This is fine for simple queries. For a system designed to be an ongoing operational partner, it's a serious limitation.

NeuroClaw solves this through the **memory stack**.

## NeuroVault — The Knowledge Layer

NeuroVault is NeuroClaw's primary long-term memory system. It's a structured knowledge store where agents can write, search, and retrieve notes across sessions.

Every entry in NeuroVault is typed:

| Type | Purpose |
|---|---|
| `semantic` | General knowledge and facts |
| `procedural` | Step-by-step instructions and workflows |
| `episodic` | Records of things that happened |
| `preference` | User preferences and stated choices |
| `insight` | Derived conclusions and analysis |
| `project` | Project-specific context |
| `session_summary` | Compressed summaries of past sessions |

When an agent learns something worth keeping — a workflow that worked, a preference you stated, a decision that was made — it writes a vault note. When you ask about something that might have prior context, the agent searches the vault before answering.

## The Memory Index

Alongside NeuroVault, NeuroClaw maintains a local memory index optimized for fast retrieval. The `search_memory` tool searches across both the index and NeuroVault simultaneously, returning the most relevant results ranked by salience, importance, and recency.

## Session Summaries

When a conversation gets long, agents can compress it — distilling the most important points into a `session_summary` vault note. This prevents context loss as sessions grow and ensures critical information isn't buried in old conversation logs.

## How It Works in Practice

1. You mention that you prefer a specific deployment strategy
2. The agent writes a `preference` note to NeuroVault
3. Three sessions later, you start a new deployment conversation
4. The agent searches memory before responding
5. It finds the preference note and applies it automatically

You don't have to repeat yourself. The system carries that knowledge forward.

## The Bigger Picture

The memory stack is what transforms NeuroClaw from a collection of AI tools into a system that actually *learns* how you work. Over time, it accumulates context — your preferences, your projects, your procedures, your history — and uses all of it to give better, more personalized responses.

Knowledge compounds. The longer you use it, the more it knows, and the more capable it becomes as a partner.
