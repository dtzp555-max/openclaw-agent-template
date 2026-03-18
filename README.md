# OpenClaw Agent Template

A starter kit for creating new OpenClaw agents. Get a fully configured agent running in under 5 minutes.

---

## Quick Start (3 Steps)

### Step 1 — Clone this template

```bash
# Copy the template files to your agent's workspace directory
cp -r openclaw-agent-template/ ~/.openclaw/projects/YOUR_AGENT_NAME/
```

Or if you're setting up inside an existing project:

```bash
# Copy just the agent config files into your project
cp openclaw-agent-template/{SOUL.md,IDENTITY.md,USER.md,AGENTS.md,TOOLS.md,MEMORY.md} your-project/
cp -r openclaw-agent-template/memory/ your-project/memory/
```

### Step 2 — Fill in the placeholders

Open each file and replace the `[PLACEHOLDER]` values with your agent's actual details:

| File | What to fill in |
|------|----------------|
| `IDENTITY.md` | Agent name, emoji, creature, vibe |
| `USER.md` | Your name, pronouns, timezone, preferences |
| `SOUL.md` | Personality description, workspace name |
| `AGENTS.md` | Workspace name, agent role, capabilities |
| `TOOLS.md` | Workspace-specific tools and restrictions |
| `MEMORY.md` | Leave empty — the agent will populate this |
| `memory/CURRENT_STATE.md` | Leave empty — the agent will populate this |

Search for `[` to find all placeholders across files:

```bash
grep -r "\[" . --include="*.md" -l
```

### Step 3 — Restart the gateway

```bash
openclaw gateway restart
# or via the OpenClaw app: Settings -> Gateway -> Restart
```

Your agent is ready. Open a new chat and it will introduce itself.

---

## File Reference

### `SOUL.md` — Behavioral DNA
Defines how the agent communicates and recovers from context loss. Contains:
- **Message prefix format** — the emoji + name pattern used in every message
- **Core truths** — non-negotiable facts the agent holds about itself
- **Vibe** — personality description that shapes tone
- **Continuity recovery protocol** — step-by-step instructions for re-orienting after a context gap

**Edit this when:** you want to change the agent's personality, communication style, or recovery behavior.

---

### `IDENTITY.md` — Who the Agent Is
Defines the agent's name, emoji, creature, role, and specializations.

**Edit this when:** the agent takes on new responsibilities or you want to update its self-description.

---

### `USER.md` — Who the Agent Serves
Tells the agent about the person it's working with — expertise level, preferences, timezone, and working style. This helps the agent calibrate its responses.

**Edit this when:** your working style changes, you want to add/remove preferences, or a new person starts working with the agent.

---

### `AGENTS.md` — Workspace Map
Describes the workspace and all agents operating within it. Follows the standard OpenClaw AGENTS.md format. Useful when multiple agents share a workspace.

**Edit this when:** you add a new agent, change workspace rules, or update shared resources.

---

### `TOOLS.md` — What the Agent Can Do
Documents tools available to the agent: built-in Claude Code tools, workspace-specific CLIs, MCP servers, and APIs. Also defines restricted actions that require user approval.

**Edit this when:** you add new tools to the workspace, change permissions, or want to restrict certain actions.

---

### `MEMORY.md` — Long-Term Memory
Accumulates important decisions, context, and learnings across sessions. The agent reads this when starting a new session or recovering context.

**Edit this when:** you want to manually add context or remove outdated entries. The agent will also write to this file automatically.

---

### `memory/CURRENT_STATE.md` — Right Now
Tracks what's in flight, what's blocked, what was recently finished, and what's planned next. The agent updates this at the end of every session.

**Edit this when:** you want to manually set the agent's initial task list or correct its understanding of current state.

---

## FAQ

**Q: Do I need all these files?**
A: `SOUL.md`, `IDENTITY.md`, and `USER.md` are the minimum for a working agent. The others improve reliability and multi-session continuity.

**Q: What are the `[PLACEHOLDER]` values?**
A: Bracketed ALL_CAPS values are placeholders you should replace. `<!-- comments -->` explain what goes there. Search for `[` to find them all.

**Q: Can I have multiple agents in one workspace?**
A: Yes. Add each agent to `AGENTS.md` and give each its own config directory. They'll share the workspace rules but have separate identities and memories.

**Q: How does the agent remember things between sessions?**
A: It reads `MEMORY.md` and `memory/CURRENT_STATE.md` at the start of each session. For this to work reliably, the agent needs to update `CURRENT_STATE.md` before each session ends.

**Q: What if the agent seems confused or off-character?**
A: Trigger continuity recovery manually by saying: "Re-read your SOUL.md and IDENTITY.md and re-orient." The agent will follow the recovery protocol defined in `SOUL.md`.

**Q: Can I add custom tools?**
A: Yes — document them in `TOOLS.md`. For MCP servers, configure them in Claude Code settings and reference them in `TOOLS.md` so the agent knows they exist and how to use them.

**Q: How do I update the agent's personality?**
A: Edit the `## Vibe` section in `SOUL.md`. Changes take effect in the next session.

---

## Template Version

`v1.0.0` — Initial release

---

## License

This template is provided as-is for use with OpenClaw. Modify freely.
