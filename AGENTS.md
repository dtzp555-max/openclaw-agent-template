# AGENTS

This file describes the OpenClaw workspace and the agents operating within it. It follows the standard OpenClaw AGENTS.md format.

---

## Workspace

| Field           | Value                        |
|-----------------|------------------------------|
| **Name**        | [WORKSPACE_NAME]             |
| **Purpose**     | [WORKSPACE_PURPOSE]          |
| **Owner**       | [USER_NAME]                  |
| **Created**     | [CREATION_DATE]              |

<!-- CUSTOMIZE: Fill in workspace details -->
<!-- Purpose example: "Personal productivity and side project development" -->
<!-- Purpose example: "Backend API development for Acme Corp" -->

---

## Agents in This Workspace

<!-- CUSTOMIZE: List all agents in this workspace -->
<!-- Each agent gets its own section below -->

### [AGENT_NAME]

| Field          | Value                              |
|----------------|------------------------------------|
| **Emoji**      | [AGENT_EMOJI]                      |
| **Creature**   | [AGENT_CREATURE]                   |
| **Role**       | [AGENT_ROLE]                       |
| **Config Dir** | `[PATH_TO_AGENT_CONFIG]`           |
| **Status**     | Active                             |

**Description:**
> [AGENT_DESCRIPTION]

**Capabilities:**
- [CAPABILITY_1]
- [CAPABILITY_2]
- [CAPABILITY_3]

**Limitations / Out of scope:**
- [LIMITATION_1]
- [LIMITATION_2]

---

<!-- OPTIONAL: Add more agents as needed -->
<!--
### [SECOND_AGENT_NAME]

| Field          | Value              |
|----------------|--------------------|
| **Emoji**      | [EMOJI]            |
| **Role**       | [ROLE]             |
| **Status**     | Active             |

**Description:**
> [DESCRIPTION]
-->

---

## Workspace Rules

<!-- CUSTOMIZE: Rules that apply to ALL agents in this workspace -->

1. **No force-push to main** — always use PRs or get explicit user approval.
2. **Update state on task completion** — write to `memory/CURRENT_STATE.md` when done.
3. **Announce blockers immediately** — don't silently stall; surface issues as soon as they appear.
4. **[WORKSPACE_RULE_4]** — [describe the rule]
5. **[WORKSPACE_RULE_5]** — [describe the rule]

---

## Shared Resources

<!-- CUSTOMIZE: Tools, services, or files shared across agents -->

| Resource          | Type           | Description                        |
|-------------------|----------------|------------------------------------|
| [RESOURCE_1]      | [TYPE]         | [DESCRIPTION]                      |
| [RESOURCE_2]      | [TYPE]         | [DESCRIPTION]                      |

<!-- Examples:
| GitHub repo       | Version control | Main codebase at github.com/org/repo |
| Linear workspace  | Issue tracking  | Project management and bug tracking  |
| Slack #dev        | Communication   | Team async updates                   |
-->

---

## Agent Handoff Protocol

When one agent passes work to another:

1. Update `memory/CURRENT_STATE.md` with current progress
2. Write a handoff note in `MEMORY.md` tagged with `[HANDOFF]`
3. Notify the user of the handoff

<!-- CUSTOMIZE: Add workspace-specific handoff rules if needed -->
