# Attention Allocation | 提纲挈领

A cognitive base that shifts AI agents from analyzing everything to identifying and concentrating on the principal constraint. Works with any LLM agent — Claude, GPT, Gemini, or custom frameworks.

让 AI agent 从"分析所有信息"转向"找到当前最重要的一件事，集中力量，忽略其余"。适用于任何 LLM agent — Claude、GPT、Gemini 或自定义框架。

---

## What it does | 它做什么

Most AI agents treat all inputs as equally worthy of analysis. They produce thorough, balanced, exhaustive responses that spread attention evenly across every factor — and in doing so, fail to identify what actually matters. Attention Allocation adds a reasoning layer that locates the single binding constraint, concentrates force on it, and deliberately ignores everything else until that constraint moves.

大多数 AI agent 把所有输入视为同等重要。它们产出全面、均衡、详尽的回答，把注意力平均分配到每个因素上——结果是无法识别什么才真正重要。注意力分配增加了一个推理层——定位唯一的约束瓶颈、集中力量突破它、在它移动之前刻意忽略其他一切。

### Before (default agent) | 安装前

> "We have 10 priorities this quarter — how do we resource them?"
>
> "Here's a weighted scoring matrix across all 10 priorities, factoring in business impact, effort, risk, and strategic alignment. I recommend distributing resources proportionally based on the composite score..."

### After (with Attention Allocation) | 安装后

> "10 priorities means 0 priorities. Your system has one bottleneck right now — the constraint that, if not resolved, makes all other progress irrelevant. Let me find it. Looking at your revenue pipeline: customer activation rate is 12%, but retention is 89%. Activation is the bottleneck. Put 70% of resources on activation. The other 9 'priorities' either feed into activation or can wait. Which do you want me to classify?"

---

## How it works | 工作原理

**One core cognitive shift** applied to every reasoning task:

一个核心认知转换，应用于每一个推理任务：

| Default mode | Target mode |
|---|---|
| Analyze all information 分析所有信息 | Identify the ONE thing that matters most, ignore the rest 找到最重要的一件事，忽略其余 |

**Five operational rules** that implement this shift:

五条操作规则，实现这个转换：

| Rule | Description |
|---|---|
| Find the bottleneck 找到瓶颈 | Every system's throughput is limited by exactly one constraint. Find it before analyzing anything else. |
| Measure signal, not volume 衡量信号而非数量 | Information value = surprise. Only high signal-to-noise inputs deserve processing time. |
| Concentrate force 集中兵力 | When overall resources are limited, achieve overwhelming superiority on one point rather than spreading thin. |
| Map the force field 绘制力场 | Before acting, identify who/what matters and who/what doesn't. Not all stakeholders, factors, or data points are equal. |
| Prepare the mind 虚壹而静 | Before judgment, empty preconceptions, unify focus, still disturbance. Cognitive readiness before cognitive action. |

**Six anti-patterns** that catch false attention allocation:

六个反模式，捕捉错误的注意力分配：

| Anti-pattern 反模式 | Description 描述 |
|---|---|
| Even distribution 均匀分配 | Giving equal attention to everything because "it all matters" 因为"都重要"而平均分配注意力 |
| Urgency bias 紧急偏误 | Urgent-but-unimportant steals attention from important-but-not-urgent 紧急但不重要的事抢走了重要但不紧急的注意力 |
| Analysis perfectionism 分析完美主义 | Wanting to process all information before deciding 想处理完所有信息再做决定 |
| Bottleneck misjudgment 瓶颈误判 | What you think is the bottleneck isn't the real one 你以为的瓶颈不是真正的瓶颈 |
| Scattered force 兵力分散 | Spreading resources across many fronts instead of concentrating 把资源分散到多条战线而不是集中 |
| Noise chasing 追逐噪声 | Reacting to low-information signals while missing high-information ones 对低信息量信号反应而错过高信息量信号 |

---

## Installation | 安装

### Claude Code
```bash
cp cognitive-protocol.md ~/.claude/attention-allocation.md
echo '@~/.claude/attention-allocation.md' >> ~/.claude/CLAUDE.md
```

### Codex
```bash
cat cognitive-protocol.md >> AGENTS.md
```

### Gemini
Paste `cognitive-protocol.md` into `system_instruction`.

将 `cognitive-protocol.md` 内容粘贴到 `system_instruction` 中。

### Cursor
```bash
cat cognitive-protocol.md >> .cursorrules
```

### Any agent | 任何 agent
Inject `cognitive-protocol.md` (~30 lines) into the system prompt. See [`install/generic.md`](install/generic.md) for details.

将 `cognitive-protocol.md`（约 30 行）注入系统提示词。详见 [`install/generic.md`](install/generic.md)。

---

## File structure | 文件结构

```
attention-allocation/
├── README.md                  ← You are here / 你在这里
├── cognitive-protocol.md      ← Core rules (~30 lines, always-on) / 核心规则（约 30 行，始终激活）
├── SKILL.md                   ← Full framework reference / 完整框架参考
├── anti-patterns.md           ← Detailed anti-pattern guide / 反模式详解
├── examples.md                ← Before/after scenarios / 前后对比示例
└── install/
    ├── claude-code.md         ← Claude Code installation / Claude Code 安装指南
    ├── codex.md               ← Codex installation / Codex 安装指南
    ├── gemini.md              ← Gemini installation / Gemini 安装指南
    └── generic.md             ← Universal guide / 通用安装指南
```

---

## Composability | 可组合性

Attention Allocation is a **cognitive base** — it changes how the agent allocates cognitive resources, not what it produces. It stacks cleanly with any domain skill (coding, design, writing, analysis) because it operates at a different layer.

注意力分配是一个**认知底座**——它改变 agent 分配认知资源的方式，而非产出内容。它与任何领域技能（编程、设计、写作、分析）无冲突地叠加，因为它运行在不同的层级。

### Relationship to other cognitive bases | 与其他认知底座的关系

| Layer 层级 | What it governs 管辖范围 | Example 示例 |
|---|---|---|
| [First Principles](https://github.com/d-wwei/first-principles) 第一性原理 | Input quality — what foundations to build on 输入质量 | "Audit assumptions before solving" 先审计假设 |
| Attention Allocation 注意力分配 | Resource quality — where to focus cognitive effort 资源质量 | "Find the one constraint that matters, ignore the rest" 找到那一个约束，忽略其余 |

Both load as always-on cognitive protocols. No conflicts. Combined: reason from verified foundations, then concentrate all force on the single point that matters most.

两者同时加载，始终激活，互不冲突。组合效果：从经过验证的基础出发推理，然后把所有力量集中在最重要的那一个点上。

---

## Theoretical foundation | 理论基础

Synthesized from converging insights across independent traditions:

- **TOC (Goldratt)**: System throughput is limited by exactly one bottleneck; optimizing non-bottlenecks is waste.
- **Information theory (Shannon)**: Information = surprise; only high signal-to-noise signals deserve processing.
- **Mao's 集中优势兵力**: When overall weaker, achieve local overwhelming superiority on one point, then move.
- **Mao's "谁是敌人谁是朋友"**: Before action, map the force field — who matters, who doesn't.
- **Xunzi's 虚壹而静**: Cognitive preparation — empty (no preconceptions), unified (focused), still (undisturbed).
- **Confucius' 中庸**: Dynamic calibration — the "right amount" moves with context, never static.
- **Musk**: "Manufacturing is the hard part" — redirect attention to the real bottleneck, not the glamorous one.

The cognitive protocol strips all theory and translates these ideas into executable instructions for any reasoning agent.

认知协议剥离了所有理论，将这些思想转译为任何推理 agent 可执行的指令。

---

## License

MIT

---

## All Cognitive Bases

Cognitive bases are meta-cognitive instruction sets that change HOW an agent thinks, not WHAT it does. Each one targets a different cognitive axis. Mix and match.

| Cognitive Base | What it changes |
|---|---|
| [First Principles](https://github.com/d-wwei/first-principles) | Reason from verified foundations, not inherited conventions |
| [Results-Driven](https://github.com/d-wwei/results-driven) | Require evidence for completion, not just activity |
| [Tacit Knowledge](https://github.com/d-wwei/tacit-knowledge) | Think like an experienced practitioner |
| [Bayesian Reasoning](https://github.com/d-wwei/bayesian-reasoning) | Calibrated probability thinking, not binary judgments |
| [Constraint as Catalyst](https://github.com/d-wwei/constraint-as-catalyst) | Turn constraints into innovation catalysts |
| [Conviction Override](https://github.com/d-wwei/conviction-override) | Override rational caution when obstacles are convention, not physics |
| [Cross-Domain Connector](https://github.com/d-wwei/cross-domain-connector) | Detect structural isomorphisms across disciplines |
| [Dialectical Thinking](https://github.com/d-wwei/dialectical-thinking) | Synthesize through contradictions (矛盾论) |
| [Double-Loop Learning](https://github.com/d-wwei/double-loop-learning) | Question the assumptions that produce errors |
| [Frame Auditing](https://github.com/d-wwei/frame-auditing) | Detect and transcend invisible analytical frames |
| [Interactive Cognition](https://github.com/d-wwei/interactive-cognition) | Model others' cognition and manage information flow |
| [Inversion Thinking](https://github.com/d-wwei/inversion-thinking) | Map failure modes first, then avoid them |
| [Motivation Audit](https://github.com/d-wwei/motivation-audit) | Audit motivational drivers before analysis (正心诚意) |
| [Non-Attachment](https://github.com/d-wwei/non-attachment) | Radical cognitive freedom — use frameworks without fusing |
| [Principled Action](https://github.com/d-wwei/principled-action) | Unify knowing and doing through practice-theory spirals (知行合一) |
| [Second-Order Thinking](https://github.com/d-wwei/second-order-thinking) | Trace consequences beyond first-order effects |
| [Systems Thinking](https://github.com/d-wwei/systems-thinking) | Feedback-driven structural analysis, not linear cause-effect |
| [Temporal Wisdom](https://github.com/d-wwei/temporal-wisdom) | Make time your ally — compound effects and phase awareness |
| [Cognitive Base Creator](https://github.com/d-wwei/cognitive-base-creator) | Generate new cognitive bases from any thinking framework |
