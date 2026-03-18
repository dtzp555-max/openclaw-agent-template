# OpenClaw Agent Template

A starter kit for creating a new OpenClaw agent in 5 minutes.

## What's This?

When you set up OpenClaw, you need a workspace with a bunch of files that define your agent's identity, memory, and behavior. This template gives you a clean starting point.

## Quick Start

```bash
# 1. Clone this repo
git clone https://github.com/dtzp555-max/openclaw-agent-template my-agent
cd my-agent

# 2. Copy files to your agent workspace
cp -r . ~/.openclaw/workspaces/my-agent/

# 3. Edit the placeholder files
#    - IDENTITY.md  → your agent's name, vibe, emoji
#    - USER.md      → info about the person the agent helps
#    - SOUL.md      → behavioral guidelines (customize or leave as-is)

# 4. Register the agent in openclaw.json and reload gateway
openclaw gateway reload
```

## Files

| File | Purpose |
|---|---|
| `SOUL.md` | Agent's behavioral DNA — persona, tone, continuity rules |
| `IDENTITY.md` | Name, creature type, vibe, emoji |
| `USER.md` | Info about the human the agent is helping |
| `AGENTS.md` | Workspace rules (session startup, memory, safety) |
| `MEMORY.md` | Long-term curated memory (persists across sessions) |
| `TOOLS.md` | Notes on local tools and setup specifics |
| `memory/CURRENT_STATE.md` | Short-term task state (In Flight / Blocked / Next) |

## FAQ

**How is this different from just creating files manually?**
It's not — this just saves you 20 minutes of copy-pasting from docs.

**Do I need all these files?**
`SOUL.md` is the most important. The others are optional but help the agent stay focused.

**How do I add a Telegram bot?**
Get a bot token from [@BotFather](https://t.me/BotFather), then add it to your `openclaw.json` under `accounts`.
