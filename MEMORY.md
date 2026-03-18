# MEMORY

Long-term memory for [AGENT_NAME]. This file accumulates important decisions, context, and learnings across sessions.

The agent reads this at the start of sessions (or when recovering context) to restore continuity.

---

## How to Use This File

- **Add entries** when something important is decided, discovered, or learned
- **Tag entries** with `[DECISION]`, `[CONTEXT]`, `[LEARNING]`, `[HANDOFF]`, or `[WATCH]`
- **Date entries** so they can be evaluated for freshness
- **Remove stale entries** — outdated memory is worse than no memory
- **Keep it scannable** — use headers and bullets, not paragraphs

---

## Decisions

<!-- Record important decisions made during the project -->
<!-- Format: ### [DATE] [DECISION] Topic -->
<!-- Example:
### 2024-01-15 [DECISION] Auth strategy
Went with JWT over sessions. Reason: stateless, easier to scale across multiple services.
Revisit if we ever need server-side session invalidation.
-->

_No decisions recorded yet._

---

## Context

<!-- Background info the agent needs to operate effectively -->
<!-- Things that aren't obvious from reading the code -->
<!-- Example:
### [CONTEXT] Why the API uses v1 prefix everywhere
The v0 API is still live for legacy clients. All new work goes to v1. Never touch /v0 routes.
-->

_No context recorded yet._

---

## Learnings

<!-- Things discovered through trial and error -->
<!-- Example:
### [LEARNING] GitHub Actions cache
The cache key must include the lock file hash or the cache never invalidates properly.
Spent 2 hours debugging this — don't make the same mistake.
-->

_No learnings recorded yet._

---

## Watch List

<!-- Things to keep an eye on — potential issues, tech debt, upcoming changes -->
<!-- Example:
### [WATCH] Dependency: stripe SDK
Pinned to 12.x — v13 has breaking changes in webhook handling. Check before upgrading.
-->

_Nothing on the watch list._

---

## Handoffs

<!-- Notes left for other agents or for future sessions after a context gap -->
<!-- Example:
### 2024-01-20 [HANDOFF] From: Iggy → To: Next session
Left off mid-way through the auth refactor. PR #42 is open and passing CI.
Remaining: need to update the session middleware to use the new token format.
-->

_No handoffs recorded._
