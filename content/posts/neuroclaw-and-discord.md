---
title: "NeuroClaw + Discord — Your AI Team in Your Server"
date: 2026-05-17
draft: false
tags: ["discord", "bots", "integration", "neuroclaw", "agents"]
description: "How NeuroClaw integrates with Discord — routing messages to agents, channel-specific configs, and voice support."
---

NeuroClaw lives where you work. For many teams and individuals, that means Discord. NeuroClaw's Discord integration brings the full agent ecosystem directly into your servers.

## How It Works

NeuroClaw supports multiple Discord bots simultaneously. Each bot connects to the Discord gateway and stays online as a persistent presence in your server.

When you @mention a bot in a channel, the message is routed to the appropriate NeuroClaw agent, who processes it and responds — just like any other conversation, but inside Discord.

## Channel Routing

One of the most powerful features of the Discord integration is **per-channel agent routing**.

You can map specific channels to specific agents:

- `#code-help` → routes to Jarvis
- `#research` → routes to Tim  
- `#publishing` → routes to Mio
- `#ops` → routes to Oracle

When a user mentions the bot in a mapped channel, it automatically goes to the right agent — no need to specify who you want every time.

Channels without an explicit mapping fall back to the bot's default agent (typically Alfred, who can route further).

## Auto-Reply Mode

For private servers where it's just you and the bot, NeuroClaw supports **auto-reply mode** — the bot responds to every non-bot message in the server without requiring an @mention. This makes it feel much more natural for personal use.

Auto-reply is configurable per-guild, so you can enable it on your private server while keeping @mention-only behavior on shared community servers.

## Voice Responses

NeuroClaw supports text-to-speech responses through Discord. When voice is enabled, agents respond with both a text message and an attached `.mp3` audio file synthesized from their response.

Voice can be configured per-agent (each agent gets their own voice and TTS provider) and per-user (if a specific user prefers text-only responses, that preference is saved and respected automatically).

Supported TTS providers:
- **VoidAI** — fast, supports alloy/echo/fable/onyx/nova/shimmer voices
- **ElevenLabs** — high quality, supports custom and cloned voices

## Emoji Reactions

Agents can react to Discord messages with emoji — a lightweight way to acknowledge, agree, or express something without sending a full text reply. This makes conversations feel more natural and less bot-like.

## The Practical Result

With the Discord integration fully configured, NeuroClaw becomes a constant presence in your workflow. You can check in with your research agent during a meeting, ask for a code review while you're in a voice call, or get a quick infrastructure update without switching applications.

Your AI team, where your human team already is.
