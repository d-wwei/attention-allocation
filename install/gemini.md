# Install — Gemini

> **Recommended**: Run `./install.sh --agent=gemini-cli` from the repo root for automated installation.
> The manual steps below are for reference or troubleshooting.

## Method 1: system_instruction (API)

```python
import google.generativeai as genai

with open("cognitive-protocol.md") as f:
    attention_allocation_rules = f.read()

model = genai.GenerativeModel(
    model_name="gemini-2.0-flash",
    system_instruction=attention_allocation_rules
)
```

## Method 2: Google AI Studio

1. Open AI Studio -> System Instructions panel
2. Paste the contents of `cognitive-protocol.md`
3. Save as a preset for reuse

## Method 3: CLI / framework integration

If using a framework (LangChain, LlamaIndex, etc.), inject `cognitive-protocol.md` into the system message.

## What to include

- **Always**: `cognitive-protocol.md` — compact enough for any context budget
- **Optional**: Key sections from `SKILL.md` (operational rules, anti-pattern checklist) if context allows
- **Skip**: Install files, README, full examples

## Stacking with First Principles

Place First Principles first in the system instruction, then Attention Allocation. Both are concise enough to fit together without significant context cost.
