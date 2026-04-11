# Attention Allocation Anti-Patterns

Detailed reference for detecting and fixing attention allocation failures across reasoning tasks.

---

## 1. Even Distribution

**Pattern**: Treating all inputs, factors, or priorities as equally deserving of analysis. The output is balanced, comprehensive, and useless — because it doesn't tell you where to focus.

**Detection**:
- The response addresses 5+ factors with roughly equal depth
- No factor is identified as more important than others
- Recommendations are "consider A, also consider B, don't forget C" without ranking
- The phrase "it depends" used as a conclusion rather than a starting point for constraint identification
- Equal-weight scoring matrices applied without questioning whether the weights are correct

**Fix**: Force-rank by impact on the binding constraint. The top item gets 70% of attention. The bottom 80% get named and explicitly deferred.

```
Bad: Let's analyze all 8 factors affecting your product launch: market timing, pricing, features, distribution, team readiness, competition, branding, and regulatory compliance. [proceeds to give equal paragraphs to each]

Good: Your product launch has one binding constraint: distribution. You have the product, the pricing, and the market timing — but no channel to reach customers at scale. Features, branding, and the other 5 factors are irrelevant until distribution is solved. Here's how to solve distribution: [concentrates entire response on this]
```

---

## 2. Urgency Bias

**Pattern**: Allowing urgent-but-unimportant demands to hijack attention from important-but-not-urgent work. The agent responds to whatever is loudest, most recent, or most emotionally charged — not what matters most.

**Detection**:
- Recommendations react to the most recent event rather than the structural situation
- "We need to address X immediately" without checking whether X affects the bottleneck
- Short-term fixes that don't touch the underlying constraint
- Fire-fighting mentality: every response is about putting out today's fire
- The user's stress level is driving prioritization rather than system analysis

**Fix**: Before reacting to urgency, ask: "Does this affect the binding constraint?" If no, it can wait. If yes, it's not just urgent — it's important. The distinction matters.

```
Bad: User says "Our biggest customer is threatening to leave!" Agent: "Here's a 5-step customer retention plan: immediate outreach, executive sponsor call, custom feature commitment, pricing adjustment, quarterly business review."

Good: "Before we react: is this customer's potential departure the bottleneck for your business? Your revenue concentration shows they're 8% of ARR. Meanwhile, your activation rate (the real bottleneck) means you're losing the equivalent of this customer every month in failed onboarding. Retain this customer with a 30-minute executive call, then redirect attention to activation — that's where the real revenue risk lives."
```

---

## 3. Analysis Perfectionism

**Pattern**: Refusing to identify the constraint or take action until all information has been processed. The agent keeps analyzing, requesting more data, and building more comprehensive models — while the actual bottleneck remains unaddressed.

**Detection**:
- "We need more data before we can decide" when the bottleneck is already identifiable
- Requesting information that won't change the ranking of constraints
- Building elaborate frameworks before identifying what they're optimizing for
- The analysis grows in scope rather than converging on a decision
- Equal effort spent on high-information and low-information inputs

**Fix**: Ask "Do I have enough information to identify the most likely bottleneck?" If yes, act on it. The cost of acting on an 80% likely bottleneck is almost always less than the cost of waiting for 95% certainty.

```
Bad: "To properly prioritize, I'll need: detailed user analytics for the past 6 months, customer interview transcripts, competitive analysis, engineering capacity estimates, revenue attribution by feature, and NPS breakdown by segment. Once I have all this, I can build a comprehensive prioritization framework."

Good: "Your support tickets show 40% are about onboarding confusion. Your funnel shows 60% drop-off at step 3. I don't need 6 months of analytics — the bottleneck is step 3 of onboarding. Let's fix that first. If I'm wrong, we'll see no improvement in 2 weeks and can re-examine. But waiting for perfect data costs more than testing the obvious hypothesis."
```

---

## 4. Bottleneck Misjudgment

**Pattern**: Confidently identifying and optimizing the wrong constraint. The agent picks the most visible, most discussed, or most familiar problem — which is often a symptom rather than the root constraint.

**Detection**:
- The identified "bottleneck" is where people are complaining (symptoms cluster), not where work is piling up (constraint location)
- Optimizing the identified constraint doesn't improve overall throughput
- The "bottleneck" is something the agent has seen before in similar situations (pattern-matching over analysis)
- No verification step: "If I doubled capacity here, would the whole system speed up?"
- Confusing a local optimization target with the global constraint

**Fix**: Verify with the throughput test: "If this constraint were removed, would the system's overall output increase?" If not, it's not the real bottleneck. Look for where work queues up and where downstream processes starve.

```
Bad: "Your engineering team is too slow. They're only shipping 2 features per quarter. Let's improve engineering velocity with better sprint planning, automated testing, and developer experience investment."

Good: "Your engineering team ships 2 features per quarter, but your product team has only validated 1 feature idea in the last quarter. Engineering isn't the bottleneck — they're actually ahead of validated demand. The constraint is product discovery. Doubling engineering speed would just produce more unvalidated features faster. Concentrate on discovery velocity first."
```

---

## 5. Scattered Force

**Pattern**: Working on many fronts simultaneously, making incremental progress everywhere but decisive progress nowhere. Resources are distributed "fairly" across all initiatives, ensuring none has enough to break through.

**Detection**:
- More than 3 active initiatives competing for the same resource pool
- Progress reports show "10% done" across 10 projects rather than "100% done" on 1
- "We can't choose, so we'll do a little of each" as an explicit or implicit strategy
- Team members context-switching across multiple priorities within the same week
- The phrase "we're making progress on all fronts" used as a positive signal

**Fix**: Count active fronts. If more than 2-3, consolidate. Pick the one with highest leverage on the bottleneck, resource it to completion, then move to the next. Sequential completion beats parallel incrementalism.

```
Bad: "Here's your Q2 plan: allocate 20% to platform stability, 20% to new features, 20% to technical debt, 20% to performance optimization, and 20% to developer experience. This balanced approach ensures all areas receive attention."

Good: "You have 5 initiatives and enough resources for 1.5 of them done well. Platform stability is the bottleneck — your 99.2% uptime is causing 3 enterprise deals to stall. Put 70% of resources on stability until you hit 99.9%. Put 30% on the one new feature tied to the biggest deal. The other 3 initiatives wait until Q3. Doing 5 things at 20% means finishing 0 things this quarter."
```

---

## 6. Noise Chasing

**Pattern**: Reacting to low-information signals (market fluctuations, outlier anecdotes, vocal minorities) while missing high-information signals (structural trends, systematic failures, silent attrition).

**Detection**:
- Recommendations shift based on the most recent data point rather than the trend
- A single customer complaint triggers a strategy change
- Market noise (daily/weekly fluctuations) treated as signal
- Anecdotes override aggregate data
- The loudest stakeholder's concern becomes the top priority regardless of its systemic importance

**Fix**: Before processing a signal, ask: "What is the information content here? Does this change my model of where the bottleneck is?" If the signal is consistent with what you already know (confirming noise), skip it. If it genuinely surprises you (new information), process it deeply.

```
Bad: "Your competitor just launched a new AI feature. We should immediately pivot our roadmap to include AI capabilities. Also, a customer on Twitter complained about your mobile app. And there's a new industry report showing blockchain adoption is rising. Let me analyze how all three affect your strategy."

Good: "Three signals came in. Let me filter: (1) Competitor AI feature — expected move, zero surprise, confirms existing trend. Low information value. (2) Twitter complaint — single anecdote, check if it represents a pattern. It doesn't — your mobile NPS is 72. Noise. (3) Industry blockchain report — irrelevant to your bottleneck (onboarding conversion). Noise. None of these signals change the bottleneck. Stay focused on onboarding."
```

---

## Quick Self-Check Sequence

When reviewing your output for attention allocation anti-patterns, scan in this order:

1. **Distribution** → Am I spreading attention evenly instead of concentrating?
2. **Urgency** → Am I reacting to what's loud instead of what matters?
3. **Completeness** → Am I waiting for perfect information instead of acting on the likely bottleneck?
4. **Accuracy** → Have I verified this is the real bottleneck, not just the obvious one?
5. **Concentration** → Am I recommending action on too many fronts simultaneously?
6. **Signal quality** → Am I processing noise, or only genuine information?
