# AuthorOS Skills Marketplace

> Install AI author skills on any coding agent. Write better books.

Pre-built skill packs for Claude Code, OpenCode, Codex, and Gemini CLI. Each pack contains the same core capabilities adapted to the agent's format.

## Available Skill Packs

| Pack | Agent | Format | Install |
|------|-------|--------|---------|
| `claude-code/` | Claude Code | `.claude/commands/*.md` | Copy to `.claude/commands/` |
| `opencode/` | OpenCode | TypeScript agents | Add to `src/agents/` |
| `codex/` | Codex (OpenAI) | `AGENTS.md` sections | Append to `AGENTS.md` |
| `gemini/` | Gemini CLI | `.gemini/*.md` | Copy to `.gemini/` |
| `cursor/` | Cursor | `.cursor/rules/*.md` | Copy to `.cursor/rules/` |

## Core Skills (included in every pack)

| Skill | What It Does |
|-------|-------------|
| `author` | Unified orchestrator (12 modes) |
| `story-architect` | Story structure, Arc cycle, beats |
| `character-psych` | Character Diamond, voice, motivation |
| `line-editor` | Prose polish, anti-slop, Seven-Pass |
| `memory-search` | Semantic vector search across manuscripts |
| `codex-link` | Auto-surface canon when character names appear |
| `describe` | Five sensory expansions per scene element |
| `draft-zero` | Full novella outline from single concept |
| `publish` | Export to epub/pdf/kindle/docx/web |

## Quick Install

### Claude Code
```bash
cp claude-code/*.md .claude/commands/
```

### OpenCode
```bash
cp opencode/agents/*.ts src/agents/
```

### Any Agent
The markdown files are portable. Copy them to your agent's command/skill directory.

## Multi-Agent Setup

Run multiple agents simultaneously sharing the same manuscript memory:

```bash
# Terminal 1: Claude Code (deep structure)
# Terminal 2: OpenCode (creative drafting)
# Terminal 3: Codex (research)
# Shared: memsearch-sqlite.py reads/writes same SQLite DB
```

## Arcanea Extension

For mythology-enhanced authoring with Ten Gates, Five Elements, Web3, and multiverse:
```bash
cp arcanea/*.md .claude/commands/  # Add Arcanea skills on top
```
