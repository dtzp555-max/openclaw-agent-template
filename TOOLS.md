# TOOLS

This file documents the tools available to this agent. The agent reads this to understand what it can do and how to use each tool correctly.

---

## Overview

<!-- CUSTOMIZE: Brief summary of this agent's tool access -->

[AGENT_NAME] has access to the following categories of tools:

- **[CATEGORY_1]** — [brief description]
- **[CATEGORY_2]** — [brief description]
- **[CATEGORY_3]** — [brief description]

---

## Built-in Claude Code Tools

These tools are always available via Claude Code:

| Tool       | Description                                      | Notes                          |
|------------|--------------------------------------------------|--------------------------------|
| `Read`     | Read file contents                               | Prefer over `cat`              |
| `Write`    | Create or overwrite files                        | Use `Edit` for small changes   |
| `Edit`     | Make targeted edits to existing files            | —                              |
| `Bash`     | Run shell commands                               | Use sparingly; prefer dedicated tools |
| `Glob`     | Find files by pattern                            | —                              |
| `Grep`     | Search file contents by regex                   | —                              |
| `WebFetch` | Fetch and summarize a URL                        | Read-only                      |
| `WebSearch`| Search the web                                  | —                              |
| `TodoWrite`| Manage task list for current session            | —                              |

---

## Workspace-Specific Tools

<!-- CUSTOMIZE: Add tools specific to this workspace -->

### [TOOL_NAME_1]

**Type:** [CLI / MCP / API / Script]
**Command / Invocation:** `[HOW_TO_USE]`

**What it does:**
> [DESCRIPTION]

**When to use:**
> [USE_CASE]

**Important notes:**
- [NOTE_1]
- [NOTE_2]

---

### [TOOL_NAME_2]

**Type:** [CLI / MCP / API / Script]
**Command / Invocation:** `[HOW_TO_USE]`

**What it does:**
> [DESCRIPTION]

**When to use:**
> [USE_CASE]

---

<!-- OPTIONAL EXAMPLES to help you fill this in:

### GitHub CLI (gh)

**Type:** CLI
**Command:** `gh pr create`, `gh issue view`, etc.

**What it does:**
> Interacts with GitHub — PRs, issues, releases, CI status.

**When to use:**
> Any time the user asks about PRs, issues, or CI without providing a URL.

**Important notes:**
- Always confirm before closing/merging PRs
- Use `gh pr view --json` for machine-readable output

---

### Linear MCP

**Type:** MCP
**Invocation:** Available via Claude Code MCP tools

**What it does:**
> Read and update Linear issues and projects.

**When to use:**
> When the user references a ticket number or asks to update issue status.

-->

---

## Tool Usage Guidelines

<!-- CUSTOMIZE: Rules for how this agent should use tools -->

1. **Prefer dedicated tools over Bash** — use `Read` not `cat`, `Grep` not `grep`.
2. **Confirm before destructive actions** — ask before deleting files, force-pushing, or closing issues.
3. **[GUIDELINE_3]** — [describe]
4. **[GUIDELINE_4]** — [describe]

---

## Restricted Actions

<!-- CUSTOMIZE: Things this agent should never do without explicit approval -->

This agent will NOT perform the following without explicit user confirmation:

- [ ] [RESTRICTED_ACTION_1] — e.g., "Push to main branch"
- [ ] [RESTRICTED_ACTION_2] — e.g., "Delete files outside the project directory"
- [ ] [RESTRICTED_ACTION_3] — e.g., "Make API calls that incur costs"
