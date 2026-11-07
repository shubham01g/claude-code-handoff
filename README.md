# HANDOFF: Claude never forgets your project again

You commented "HANDOFF," so here's the setup.

Claude forgets everything the moment you clear the chat. Long sessions fill up the context, and that's exactly where the important stuff gets lost.

`/session-handoff` fixes that. Before you clear, run one command and Claude writes a structured summary of the whole session. Paste it into a fresh chat and it picks up exactly where you left off.

## What the summary covers

- **Where it started:** the goal of the session
- **Decisions locked:** what we decided and why
- **What shipped:** every change, with file paths
- **Key files:** what the next session should read first
- **Running state:** background processes, servers, open branches
- **How to verify:** commands that prove things still work
- **Deferred + open questions:** what's not done yet
- **Pick up here:** the exact next step

It's written for the next Claude, not for you, so it's dense and precise. It stays in the chat and never writes a file.

## Setup

1. Copy [`.claude/skills/session-handoff/`](.claude/skills/session-handoff/) into `~/.claude/skills/session-handoff/`. That's one file: `SKILL.md`.
2. Restart Claude Code.

Or paste this into Claude Code:

```
Install the session-handoff skill from
https://github.com/shubham01g/claude-code-handoff/tree/main/.claude/skills/session-handoff
into ~/.claude/skills so it works in every project.
```

## How to use it

1. When a session gets long, or before you `/clear`, type:
   ```
   /session-handoff
   ```
2. Copy the summary.
3. `/clear`, paste the summary into the new chat, and keep going.

## Why not just `/compact`?

`/compact` squeezes the chat, and you don't control what survives. The handoff is a checklist, so decisions, file paths and "what's still running" never get dropped. A fresh session with a clean summary also works better than a crowded one.

It's a boring skill, but it's the one I'd miss the most.

---

Made by [@shubham_gunjal_ai](https://instagram.com/shubham_gunjal_ai)
