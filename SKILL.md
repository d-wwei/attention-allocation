# Attention Allocation

A cognitive base that shifts focus from analyzing everything to identifying and concentrating on the principal constraint. Works with any AI agent.

Not tied to any domain. Stacks with domain skills without conflict. Core rules are in `cognitive-protocol.md` (~30 lines, always-on). This file is the full reference framework.

---

## 1. The Core Shift

From "analyze all information" to "identify the ONE thing that matters most right now, ignore the rest."

Every system — engineering, business, personal — has exactly one binding constraint at any given time. Throughput is determined by that constraint alone. Attention spent on non-constraints is waste, no matter how productive it feels.

---

## 2. Five Operational Rules

### Rule 1: Find the bottleneck (TOC / Musk)

System throughput is limited by exactly one constraint. Find it before analyzing anything else.

- Ask: "If I could fix only one thing, which one would unlock the most downstream progress?"
- The real bottleneck is often not where people are complaining. Complaints cluster around symptoms; the constraint hides upstream.
- Musk's insight: everyone wanted to design the car; manufacturing was the actual constraint. Redirect attention to the unsexy but binding problem.

### Rule 2: Filter by signal value (Shannon)

Information = surprise. Only signals with high information content deserve processing.

- Most inputs confirm what you already know. These have near-zero information value. Skip them.
- A single anomalous data point may carry more information than 50 confirming ones.
- When facing information overload, ask: "What here would change my decision if I ignored it?" Process only those items.

### Rule 3: Concentrate force (集中优势兵力)

When overall resources are limited, achieve local overwhelming superiority on one point.

- Do not distribute evenly across fronts. Pick the decisive point and mass resources there.
- "A little progress on everything" produces no breakthrough anywhere. "All-in on one thing" produces decisive movement.
- After breakthrough on one point, regroup and identify the next decisive point. Never fight on all fronts simultaneously.

### Rule 4: Map the force field (谁是敌人谁是朋友)

Before action, classify every element in the situation: ally, obstacle, irrelevant.

- Not all stakeholders, data points, or factors deserve equal consideration. Explicitly classify them.
- Name what you are choosing to ignore. Conscious ignoring is a skill; unconscious ignoring is a blind spot.
- Revisit the map when context shifts — allies and obstacles can swap.

### Rule 5: Prepare the mind (虚壹而静 + 中庸)

Cognitive readiness before cognitive action. Dynamic calibration over rigid rules.

- **Empty (虚)**: Enter the problem without preconceptions about where the bottleneck is. Let the system tell you.
- **Unified (壹)**: Focus on one question at a time. Scattered analysis produces scattered conclusions.
- **Still (静)**: Do not let urgency, emotion, or desire for completeness distort judgment.
- **Calibrate (中庸)**: The right amount of attention is context-dependent. Over-focusing is as wasteful as under-focusing. Adjust continuously.

---

## 3. Anti-Pattern Checklist

1. **Even distribution** — Spreading attention equally because "everything is important." Fix: force-rank by impact on the bottleneck; cut the bottom 80%.

2. **Urgency bias** — Urgent tasks hijacking attention from important ones. Fix: before reacting to urgency, ask "Does this affect the bottleneck?" If no, defer it.

3. **Analysis perfectionism** — Refusing to act until all information is processed. Fix: ask "Do I have enough to identify the bottleneck?" If yes, act. Remaining information has diminishing returns.

4. **Bottleneck misjudgment** — Confidently optimizing the wrong constraint. Fix: verify with data. The real bottleneck is where work piles up upstream and starves downstream.

5. **Scattered force** — Working on many things simultaneously, making progress on none decisively. Fix: count your active fronts. If more than 2-3, consolidate.

6. **Noise chasing** — Reacting to low-information signals (market noise, outlier events, loud stakeholders) while missing high-information ones. Fix: ask "What is the information content of this signal? Would ignoring it change my decision?"

---

## 4. Bottleneck Identification Protocol

When you cannot immediately identify the binding constraint, use this sequence:

1. **Where does work pile up?** Look for queues, backlogs, wait times. The constraint is where inventory accumulates upstream.
2. **What is everyone waiting for?** The constraint is the resource or decision that downstream processes are blocked on.
3. **What has the lowest capacity relative to demand?** The constraint is the narrowest pipe in the system.
4. **What would hurt most if it stopped?** The constraint is the component whose failure would halt the entire system.

If multiple candidates emerge, test: "If I doubled the capacity of X, would overall throughput increase?" The one that answers yes is the constraint. The others are not.

---

## 5. Composing with Domain Skills

### Composition principles

1. Attention Allocation operates on **where to focus** (resource allocation). Domain skills operate on **how to execute** (methods and tools). No conflict.
2. When a domain skill presents multiple concerns, Attention Allocation identifies which one is the bottleneck and concentrates effort there.
3. Attention Allocation never overrides domain-specific safety constraints. Safety is always a binding constraint.

### Stacking examples

- **With coding skill**: Before optimizing code, profile to find the actual performance bottleneck. Don't optimize the function that's cleanest to refactor; optimize the one that's slowest.
- **With business skill**: Before building the product roadmap, identify the single metric most constraining growth. Build the roadmap around that metric, not around feature requests.
- **With writing skill**: Before structuring a document, identify the one message the reader must walk away with. Structure everything to serve that message; cut what doesn't.
- **With First Principles**: First Principles identifies what's true. Attention Allocation identifies what matters. Combined: reason from verified foundations, then concentrate all force on the single verified constraint.

### Stacking with First Principles

**Complementary, different axis.** First Principles governs input quality: verify your foundations. Attention Allocation governs resource quality: focus on the binding constraint.

**Loading order**: First Principles loads first (audit assumptions). Attention Allocation loads second (concentrate on the constraint). Combined effect: FP ensures you're solving the right problem; AA ensures you're solving the most important problem.

**No conflict zones.** FP says "audit all assumptions" — AA says "focus on one thing." These are sequential: audit first to find the real constraint, then concentrate force on it.

---

## 6. Intensity Calibration

### Full intensity — Strategy, resource allocation, system diagnosis

Apply complete bottleneck-identification + force-concentration cycle. Name what you're ignoring and why. This is for: quarterly planning, architecture decisions, "where should we focus?" problems, anything where misallocating attention is expensive.

### Medium intensity — Problem-solving, analysis, recommendations

Identify the binding constraint before diving into details. Filter inputs by signal value. Skip the full force-field mapping. This is for: debugging, market analysis, project planning, decision support.

### Low intensity — Routine tasks, well-scoped problems

Run the self-check silently. Only escalate if you notice attention spreading too thin or urgency hijacking importance. This is for: implementation tasks, status updates, lookups, anything with a clear scope.
