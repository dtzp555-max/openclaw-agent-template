# openclaw-agent-template

A minimal, opinionated starter kit for creating OpenClaw agents — drop it into any workspace and your agent has identity, memory, and operating rules from day one.

---

## Quick Start

```bash
# 1. Clone this template
git clone https://github.com/dtzp555-max/openclaw-agent-template.git my-agent
cd my-agent

# 2. Copy the files into your workspace's agent config directory
cp -r . /path/to/your/workspace/.openclaw/agent/

# 3. Reload your OpenClaw gateway to pick up the new config
openclaw reload   # or restart your Claude Code session
```

Then open `IDENTITY.md` and replace the `[PLACEHOLDERS]` with your agent's actual name, emoji, and vibe.

---

## Files

| File | Purpose |
|------|---------|
| `SOUL.md` | Core behavior contract — message prefix rules, principles, continuity recovery |
| `IDENTITY.md` | Who the agent is — name, emoji, creature, vibe, specializations |
| `USER.md` | Who the agent serves — working style, expertise, preferences |
| `AGENTS.md` | Workspace rules — session startup, memory policy, safety guardrails |
| `TOOLS.md` | Available tools and usage guidelines |
| `MEMORY.md` | Long-term memory — decisions, context, learnings across sessions |
| `memory/CURRENT_STATE.md` | Short-term state — what's in flight, blocked, or next |

---

## FAQ

**Q: Do I need all these files?**
Start with `SOUL.md`, `IDENTITY.md`, and `memory/CURRENT_STATE.md` — those three give you identity and continuity. Add the rest as your needs grow.

**Q: How does the agent pick up changes to these files?**
The agent reads them at session start. Edit a file and start a new session (or ask the agent to re-read it) for changes to take effect.

**Q: Can I use this with a non-OpenClaw Claude Code setup?**
Yes. The files are plain markdown. Point your `CLAUDE.md` at them with `@SOUL.md`, `@IDENTITY.md`, etc., and they work as regular context files.
