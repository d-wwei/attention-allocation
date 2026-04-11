# Install — Claude Code

> **Recommended**: Run `./install.sh` from the repo root for automated installation with dual-mode support (@ reference + inline fallback).
> The manual steps below are for reference or troubleshooting.

## Quick install

```bash
# 1. Inject core rules into CLAUDE.md (direct content injection — works on all versions)
cat cognitive-protocol.md >> ~/.claude/CLAUDE.md
```

## What gets loaded where

| File | Destination | Purpose |
|---|---|---|
| `cognitive-protocol.md` | `~/.claude/CLAUDE.md` (appended) | Always-on core rules (~30 lines) |
| `SKILL.md` | `~/.claude/skills/attention-allocation/SKILL.md` | Full reference (loaded on demand) |
| `anti-patterns.md` | `~/.claude/skills/attention-allocation/anti-patterns.md` | Detailed anti-pattern guide |
| `examples.md` | `~/.claude/skills/attention-allocation/examples.md` | Before/after reference |

## Full install (with skill files)

```bash
# 1. Core rules (inject directly into CLAUDE.md)
cat cognitive-protocol.md >> ~/.claude/CLAUDE.md

# 2. Skill files
mkdir -p ~/.claude/skills/attention-allocation
cp SKILL.md ~/.claude/skills/attention-allocation/
cp anti-patterns.md ~/.claude/skills/attention-allocation/
cp examples.md ~/.claude/skills/attention-allocation/

# 3. (Core rules already injected in step 1)
```

## Verify

Ask Claude Code: "What are the attention allocation cognitive rules you're following?" It should list the five sections from `cognitive-protocol.md`: find the bottleneck first, filter by signal not volume, concentrate force, map before acting, calibrate don't fixate.

## Stacking with First Principles

If First Principles is already injected into `CLAUDE.md`, no changes needed. Both protocols load independently. First Principles governs reasoning input quality; Attention Allocation governs where to focus cognitive effort. No conflicts.

## Uninstall

```bash
# Remove the Attention Allocation section from ~/.claude/CLAUDE.md (search for "# Attention Allocation — Cognitive Protocol" header)
rm -rf ~/.claude/skills/attention-allocation
```
