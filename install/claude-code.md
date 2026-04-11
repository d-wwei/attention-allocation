# Install — Claude Code

## Quick install

```bash
# 1. Copy cognitive protocol to Claude's config
cp cognitive-protocol.md ~/.claude/attention-allocation.md

# 2. Add reference in CLAUDE.md
echo '@~/.claude/attention-allocation.md' >> ~/.claude/CLAUDE.md
```

## What gets loaded where

| File | Destination | Purpose |
|---|---|---|
| `cognitive-protocol.md` | `~/.claude/attention-allocation.md` | Always-on core rules (~30 lines) |
| `SKILL.md` | `~/.claude/skills/attention-allocation/SKILL.md` | Full reference (loaded on demand) |
| `anti-patterns.md` | `~/.claude/skills/attention-allocation/anti-patterns.md` | Detailed anti-pattern guide |
| `examples.md` | `~/.claude/skills/attention-allocation/examples.md` | Before/after reference |

## Full install (with skill files)

```bash
# 1. Core rules
cp cognitive-protocol.md ~/.claude/attention-allocation.md

# 2. Skill files
mkdir -p ~/.claude/skills/attention-allocation
cp SKILL.md ~/.claude/skills/attention-allocation/
cp anti-patterns.md ~/.claude/skills/attention-allocation/
cp examples.md ~/.claude/skills/attention-allocation/

# 3. Register in CLAUDE.md
echo '@~/.claude/attention-allocation.md' >> ~/.claude/CLAUDE.md
```

## Verify

Ask Claude Code: "What are the attention allocation cognitive rules you're following?" It should list the five sections from `cognitive-protocol.md`: find the bottleneck first, filter by signal not volume, concentrate force, map before acting, calibrate don't fixate.

## Stacking with First Principles

If `~/.claude/first-principles.md` is already referenced in `CLAUDE.md`, no changes needed. Both protocols load independently. First Principles governs reasoning input quality; Attention Allocation governs where to focus cognitive effort. No conflicts.

## Uninstall

```bash
rm ~/.claude/attention-allocation.md
rm -rf ~/.claude/skills/attention-allocation
# Remove the @~/.claude/attention-allocation.md line from ~/.claude/CLAUDE.md
```
