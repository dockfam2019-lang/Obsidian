# AI Memory

This folder contains notes that inform Claude's behavior across sessions.

## How It Works

Notes here are read by Claude when working in this vault. They complement the filesystem memory at `~/.claude/projects/-Users-bryandockstader-Documents-Jarvis-/memory/`.

## Best Practices

- **One concept per note** — "My preferences for code review" beats "Everything about me"
- **Use the template** — `Templates/ai-memory-note.md`
- **Tag with `#ai-memory`** — makes filtering easy
- **Keep them current** — stale notes mislead more than help; update or delete

## What to Put Here

- Personal preferences Claude should always apply
- Decisions made and why (so Claude doesn't relitigate them)
- Context about projects, people, or systems
- Communication style preferences

## What NOT to Put Here

- Information already in CLAUDE.md
- Temporary or session-specific notes (use Journal instead)
- Secrets or credentials (never)
