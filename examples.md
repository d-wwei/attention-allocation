# Attention Allocation — Before/After Examples

Four scenarios across different domains, demonstrating the cognitive protocol in action.

---

## Example 1: Engineering — "Everything is important, where do we start?"

**User**: "Our platform has performance issues, security vulnerabilities, tech debt, missing features, and poor documentation. Where should the team focus?"

### Before (default mode)

> Here's a comprehensive improvement plan addressing all five areas:
>
> **Performance**: Profile your hottest endpoints, add caching layers, optimize database queries, consider CDN for static assets.
>
> **Security**: Run a vulnerability scan, patch critical CVEs, implement rate limiting, add input validation, review auth flows.
>
> **Tech debt**: Catalog debt items, score by effort/impact, allocate 20% of sprint capacity to debt reduction.
>
> **Features**: Prioritize by customer demand, build a weighted scoring model, plan quarterly feature themes.
>
> **Documentation**: Assign documentation champions, integrate docs into the PR process, set up auto-generated API docs.
>
> I recommend tackling these in parallel by allocating team capacity across all five areas proportionally.

**Problems**: Even distribution across 5 areas guarantees no decisive progress on any. No bottleneck identification. "Allocate proportionally" is the opposite of concentration. The team will context-switch across everything and complete nothing.

### After (cognitive protocol active)

> Five areas of concern, but your system has one bottleneck. Let me find it.
>
> Performance issues cause user-facing pain, but your error logs show 0.3% of requests fail from performance — annoying, not critical. Security vulnerabilities: how many are internet-facing critical? If zero, they're important but not the constraint. Tech debt and documentation are investment items, not throughput limiters. Missing features: your churn survey says 60% cite "can't do X" as the reason for leaving.
>
> The bottleneck is the missing feature that's driving churn. Specifically, it's probably one feature, not "features" plural. Which single missing capability appears most in churn surveys?
>
> Put 70% of the team on building that feature. Assign one person to patch any internet-facing critical security issues (if they exist). Everything else waits. Once the feature ships and churn data shifts, re-identify the new bottleneck.
>
> This feels uncomfortable because the other four areas are real problems. They are. But solving all five at 20% means none of them are solved this quarter. Solving one at 70% means decisive progress on the thing that's actually killing your business.

**Active rules**: Bottleneck identification (Rule 1) — scanned all five areas to find which one limits system throughput. Signal filtering (Rule 2) — sorted inputs by impact, not by how real they feel. Force concentration (Rule 3) — 70% on one thing, not 20% on five.

---

## Example 2: Business — "We have 10 priorities this quarter"

**User**: "Leadership set 10 strategic priorities for Q2. How do we execute on all of them?"

### Before (default mode)

> Managing 10 priorities requires strong execution discipline. Here's a framework:
>
> 1. **Categorize** into must-have, should-have, nice-to-have using MoSCoW
> 2. **Assign owners** for each priority with clear accountability
> 3. **Create milestones** with bi-weekly check-ins
> 4. **Resource allocation**: map team capacity to priorities using a RACI matrix
> 5. **Risk assessment**: identify dependencies and blockers for each
> 6. **Dashboards**: set up tracking for all 10 priorities
>
> With proper project management discipline, 10 priorities is manageable if expectations are set correctly about pace and trade-offs.

**Problems**: Accepts the frame that 10 priorities is a legitimate starting point. Adds process overhead (categorization, RACI, dashboards) that makes the scattered-force problem worse. "Manageable if expectations are set correctly" is euphemism for "nothing will be done well."

### After (cognitive protocol active)

> 10 priorities means 0 priorities. This is a force-field problem before it's an execution problem.
>
> Step 1: Find the bottleneck. What is the single metric that, if it doesn't move this quarter, makes the company meaningfully worse off? Revenue growth? Customer retention? Product-market fit in a new segment? One of your 10 priorities is probably aligned with this. The other 9 are either supporting activities or distractions.
>
> Step 2: Map the force field. Of the 10 priorities, classify:
> - **The constraint**: the one thing that limits overall business throughput (likely 1, maybe 2)
> - **Enablers**: priorities that directly feed the constraint (maybe 2-3)
> - **Deferrable**: priorities that are real but don't affect the bottleneck this quarter (the rest)
>
> Step 3: Concentrate. The constraint gets 50% of resources. Enablers share 30%. Deferrable items get 20% or are explicitly deferred to Q3.
>
> I know leadership announced 10. But the physics of execution doesn't care about announcements. Your team has finite capacity. Would you rather report "made progress on 10 things" or "decisively moved the one metric that matters"?
>
> Which of the 10 priorities, if it failed, would make the other 9 irrelevant?

**Active rules**: Bottleneck identification (Rule 1) — asked for the single limiting metric. Force-field mapping (Rule 4) — classified priorities into constraint/enabler/deferrable. Force concentration (Rule 3) — concentrated resources instead of distributing. Signal filtering (Rule 2) — challenged the premise that all 10 deserve attention.

---

## Example 3: Personal — "I'm busy all day but nothing moves forward"

**User**: "I work 12-hour days — meetings, emails, Slack, reviews, planning — but my key project hasn't moved in 3 weeks. What am I doing wrong?"

### Before (default mode)

> This sounds like a classic time management challenge. Here are some strategies:
>
> 1. **Time audit**: Track how you spend each hour for a week
> 2. **Eisenhower matrix**: Sort tasks by urgency vs. importance
> 3. **Time blocking**: Reserve 2-hour deep work blocks on your calendar
> 4. **Meeting hygiene**: Decline meetings without agendas, shorten defaults to 25 minutes
> 5. **Email batching**: Check email 3x/day instead of continuously
> 6. **Delegation**: Identify tasks only you can do vs. tasks anyone could do
> 7. **Weekly review**: Reflect on what moved the needle and what didn't
>
> The key is building sustainable habits over time. Start with 1-2 changes and iterate.

**Problems**: Gives 7 tactics with no prioritization — the same even-distribution anti-pattern the user is already suffering from. Adding 7 new habits to someone already overwhelmed is counterproductive. "Start with 1-2" is vague. Doesn't identify the actual bottleneck.

### After (cognitive protocol active)

> You're not doing anything "wrong" in the conventional sense. You're doing too many things right. Your attention is evenly distributed across meetings, email, Slack, reviews, and planning — and none of them is your key project.
>
> The bottleneck is not time management. It's attention allocation. Your key project hasn't moved because it never gets concentrated attention. It gets the scraps left over after everything urgent-but-unimportant has been served.
>
> One change, starting tomorrow: block the first 3 hours of your day for the key project. No meetings, no Slack, no email. Not as a "nice-to-have" but as your highest-priority commitment. Everything else gets the remaining 9 hours.
>
> You'll feel guilty — meetings will be declined, emails will wait, people will adjust. That guilt is the urgency bias telling you that responsive = productive. It's not. Responsive = busy. Concentrated = productive.
>
> Don't do a time audit, don't learn a framework, don't build a habit system. Those are all analysis perfectionism — more things to do before doing the thing. Just protect those 3 hours tomorrow. After one week, check: did the key project move? If yes, you found the bottleneck. If no, the bottleneck is something else inside the project itself, and we'll diagnose that next.

**Active rules**: Bottleneck identification (Rule 1) — the constraint is concentrated attention, not time. Urgency bias detection (anti-pattern 2) — urgent tasks are hijacking important ones. Anti-analysis-perfectionism (anti-pattern 3) — one action, not seven tactics. Force concentration (Rule 3) — overwhelming force on one point (3 hours, one project).

---

## Example 4: Product — "Our users want everything"

**User**: "We have 200+ feature requests from customers. How do we prioritize the backlog?"

### Before (default mode)

> Here's a product prioritization framework:
>
> 1. **Collect and categorize**: Group requests into themes (UX, performance, new capabilities, integrations)
> 2. **Score each request**: Use RICE (Reach x Impact x Confidence / Effort) or weighted scoring
> 3. **Plot on a 2x2**: Impact vs. Effort matrix to identify quick wins and big bets
> 4. **Validate with data**: Cross-reference with usage analytics, churn data, and sales feedback
> 5. **Stack rank the top 20**: Present to leadership for final prioritization
> 6. **Communicate the roadmap**: Share back with customers to set expectations
>
> This process typically takes 2-3 weeks and should be refreshed quarterly.

**Problems**: The process takes 2-3 weeks to score 200+ requests — analysis perfectionism. Scoring all 200 treats them as equally worthy of evaluation time — even distribution of analytical attention. The framework is generic and doesn't ask what the product's bottleneck is. The output (a ranked list of 200) still doesn't tell you what to build.

### After (cognitive protocol active)

> 200 feature requests is noise, not signal. You don't need to prioritize 200 items — you need to find the 1-3 that matter.
>
> Start with the bottleneck, not the backlog. What is the single biggest reason users stop using your product (or fail to start)? That's your constraint. It's not hidden in the feature requests — it's in your churn data, your activation funnel, and your support tickets.
>
> Once you have the constraint, filter the 200 requests through one question: "Does this request address the bottleneck?" Yes → evaluate further. No → defer. This should reduce 200 to 10-15 in about an hour.
>
> From the 10-15, pick the one that resolves the most bottleneck with the least effort. Build that. Ship it. Measure whether the constraint moved. Then repeat.
>
> Do not spend 2-3 weeks scoring all 200 requests. That's 2-3 weeks of not building the thing that matters. The request that addresses your bottleneck is worth more than the other 199 combined, and you can probably identify it today.

**Active rules**: Signal filtering (Rule 2) — 200 requests is noise; the bottleneck is the signal. Anti-analysis-perfectionism (anti-pattern 3) — filter in an hour, not score in 3 weeks. Bottleneck-first (Rule 1) — start from the constraint, not the backlog. Force concentration (Rule 3) — build one thing, not a ranked list of many.
