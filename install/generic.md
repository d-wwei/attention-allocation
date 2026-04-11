# Install — Generic (Any Agent/Framework)

> **Recommended**: Run `./install.sh` from the repo root for automated installation. Supports Claude Code, Gemini CLI, Codex CLI, Cursor, OpenCode, and OpenClaw.
> The manual steps below are for reference or troubleshooting.

## Universal principle

Attention Allocation is a cognitive base — it changes how the agent allocates cognitive resources, not what tools it uses. Installation means injecting `cognitive-protocol.md` into the agent's always-on instructions (system prompt, rules file, or configuration).

## Platform mapping

| Platform | Where to inject | File to use |
|---|---|---|
| Claude Code | `~/.claude/attention-allocation.md` + ref in `CLAUDE.md` | `cognitive-protocol.md` |
| Codex | Prepend to `AGENTS.md` | `cognitive-protocol.md` |
| Gemini | `system_instruction` field | `cognitive-protocol.md` |
| Cursor | Prepend to `.cursorrules` | `cognitive-protocol.md` |
| ChatGPT | Custom Instructions -> system prompt | `cognitive-protocol.md` |
| LangChain | System message in chain | `cognitive-protocol.md` |
| AutoGPT / CrewAI | Agent system prompt | `cognitive-protocol.md` |
| Any other | Find the "always-on instructions" config and inject there | `cognitive-protocol.md` |

## Step by step

1. Locate your agent's system prompt or always-on rules file
2. Copy the contents of `cognitive-protocol.md` (~30 lines)
3. Paste it into the system prompt, BEFORE any domain-specific instructions
4. If using First Principles, place it first, then Attention Allocation

## File selection guide

| Need | File | Size |
|---|---|---|
| Minimal install (core rules only) | `cognitive-protocol.md` | ~30 lines |
| Full reference framework | + `SKILL.md` | ~160 lines |
| Anti-pattern detection | + `anti-patterns.md` | ~130 lines |
| Teaching examples | + `examples.md` | ~130 lines |

For most agents, `cognitive-protocol.md` alone is sufficient. The additional files are reference material for when the agent needs deeper guidance.

## Troubleshooting

- **Agent ignores the rules**: Move `cognitive-protocol.md` content to the beginning of the system prompt, not the end. Most models weight earlier instructions more heavily.
- **Agent still spreads attention evenly**: This is the hardest habit to break. Add the anti-pattern checklist from `SKILL.md` section 3 to reinforce the filtering behavior.
- **Rules conflict with domain instructions**: Attention Allocation should never conflict — it changes resource allocation, not output format. If conflict appears, the domain instruction likely assumes even distribution is desirable. That assumption is worth questioning.
- **Context window pressure**: `cognitive-protocol.md` is ~30 lines. If that's too much, something else in your prompt needs trimming first.
