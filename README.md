# if-tree skill

**条件树协议：把未封口的问题收敛为可交付的确定结构。**

一套通用的结构化收敛协议。把人和 AI 之间的模糊对话，收敛为可无歧义实现的条件树文档。适用于任何 AI，适用于任何可顺序化的目标物——代码、论文、手册、剧本、模组、流程、架构……

> **English version follows below.** [Jump to English ↓](#if-tree-skill-1)

---

## 这套协议解决什么问题

你和 AI 之间的协作，核心瓶颈不在 AI 的能力，而在**你们之间的需求从未被结构化**。

你给 AI 的需求几乎永远是不完整的。你自己也不知道全部细节。AI 不会告诉你它不知道什么——它会猜，然后自信地产出一堆看似正确、实则建立在猜测上的内容。你发现不对，改一处，它又猜另一处。几轮之后，你在给一个不知道自己在干什么的系统擦屁股。

这不是 AI 不够聪明。这是人和 AI 之间缺少一套结构化的收敛协议。

**if-tree 从根源上解决这个问题。**

它不让 AI 猜。它要求：用户没说的标 ERROR，不猜不补。每一个条件分支必须闭合。每一个无法自主解决的问题必须暴露给人类，不允许静默吞掉。

结果是：你和 AI 之间的对话不再是无结构的自然语言碰撞，而是一棵持续生长、持续收敛的条件树。树上每个节点有精确地址。每个缺口有精确标记。每一轮对话都在填洞、闭合分支、推进收敛。当整棵树闭合时，目标物可以被无歧义地产出——无论那个目标物是代码、论文、手册还是任何其他东西。

**文档即结构，结构即程序，严格等价。**

---

## 目标物不只是代码

条件树最终收敛后交出的目标物，只要求一个特征：**可顺序化**——能被从头到尾线性地阅读、执行或交付。满足这个特征的一切都适用：

- **代码**：程序、脚本、配置、数据库结构、API 接口
- **文档**：论文、技术报告、用户手册、操作手册、规格说明书
- **创作**：剧本、模组、世界观设定、叙事结构
- **流程**：工作流、审批链、运维规程、应急预案
- **架构**：系统设计、产品架构、组织流程

条件树是这些目标物的**前置结构**。它在目标物成形之前，先把所有条件、分支、例外、边界、未知全部显影。目标物是结构在最终形式中的沉积。

---

## 5 分钟上手

### 1. 安装

将 `if-tree-skill-v5.md` 放入你使用的 AI 系统的 skill / system prompt / custom instructions 中。

- **Claude**：Project Knowledge 或 Custom Instructions
- **ChatGPT**：Custom Instructions 或 GPTs 的 Instructions
- **Gemini**：System Instructions
- **本地模型（Ollama / LM Studio 等）**：System Prompt

skill 不依赖任何特定 AI。它是纯协议，任何能理解自然语言的模型都能执行。

### 2. 开始使用

直接向 AI 描述你的需求。不需要说"请整理需求"。skill 收到需求描述即触发。

```
用户：我要做一个批量处理 Excel 文件的工具，读取指定列，
     清洗数据后输出到新文件。

AI：（自动输出结构化条件树，带节点地址、事实前提、
    数据校验、ERROR 标记、转人工机制）
```

```
用户：我要写一篇关于人机协作规格收敛的论文，
     包含理论框架、形式定义和工程验证三个部分。

AI：（自动输出结构化条件树，把论文的论证链、
    章节依赖、待补证明、待确认前提全部显影）
```

### 3. 迭代

对着条件树给反馈。引用节点地址修改。AI 先改文档，输出变更摘要，再产出目标物。不跳步。

---

## 核心机制

### 条件树 = 图灵完备的自然语言程序

条件分支（if-else）+ 循环（LOOP / FOREACH / BREAK / CONTINUE）= 图灵完备。每个叶节点必须同时具备触发条件、执行动作、输出或状态变化。三者缺一标 ERROR。

### ERROR 即停

用户没说的不猜。命中未知就停止推断，标记 ERROR，等待用户补充。这不是保守，这是对伪连续的主动防伪。AI 最危险的习惯是在不知道的时候继续流畅输出。

### 数据校验四步

不受控数据进入程序时，严格执行：信任分级 → 目标格式定义 → 清洗或拒绝 → 转人工。不允许静默丢弃、默认值、跳过不报。每一条异常都必须暴露给人类。

### 文档先于产出

修改反馈 → 定位节点 → 先改文档 → 输出变更摘要 → 再产出目标物。文档是唯一权威状态。目标物是结构在最终形式中的沉积。

### 可逆性自检

输出前模拟一个完全不了解需求的执行者，只看文档验证能否无歧义地产出完整目标物。不能 → 标 ERROR 或补全后重新自检。

---

## 为什么这不只是"更好的 prompt"

prompt engineering 优化的是单次输出质量。if-tree 改变的是人机协作的结构。

| | Prompt Engineering | if-tree |
|---|---|---|
| 作用点 | 单次输入 → 单次输出 | 多轮交互 → 持续收敛 |
| 对未知的处理 | AI 自行补全（猜） | ERROR 即停，暴露给人类 |
| 输出物 | 直接产出 | 结构化条件树文档 → 目标物 |
| 可审查性 | 低（需从产出物反推意图） | 高（文档即结构） |
| 复利 | 无（每次从零开始） | 有（文档持续积累、收敛） |

---

## 理论基础：灯式机

if-tree 不是一个恰好好用的工程技巧。它背后有完整的理论框架。

图灵机回答：什么叫可机械计算。  
冯诺伊曼机回答：怎样把可机械计算封装为可执行程序系统。  
**灯式机回答：一个未封口的问题，如何在现实时间中收敛为可交付的确定结构。**

三台机器各回答一个不同的根问题：**可计算、可执行、可审查**。灯式机处理的是第三个。它的主对象是冻结时间切片——条件树文档在当前轮下所承载的等价有效信息量。它的状态语言由四类对象组成：

- **洞**（hole）：位置已留出，内容尚未确认
- **节点**（node）：预期与现实一致，已闭合
- **错误**（error）：经现实比对，确认无投影
- **缝隙**（gap）：父层视角下，切片尚不能成立

灯式机的工作就是让洞塌缩为节点，让无投影位显影为错误，让缝隙消失——直到切片可交接。交接物可以是代码、文档、记忆，或下一轮灯式机的输入。

完整理论见 [`灯式机的自然哲学与数学原理.md`](灯式机的自然哲学与数学原理.md)。

---

## 复利效应

if-tree 的价值不是线性增长的。

第一份条件树建立后，后续的修改、扩展、重构都沿着树结构进行。定位节点 → 改文档 → 变更摘要 → 目标物跟进。维护成本从"在整片产出物表面找入口"压缩为"沿树深度定位入口"。

旧产出物可以反向 lift 回条件树。一旦这件事成立，历史积累从债务变成结构资本。

每一轮有效的文档更新都在压缩实现自由度：

$$\Omega_{t+1} \subsetneq \Omega_t$$

直到产出只剩下"如何优雅地实现"，而不再主要是"用户到底想要什么"。

---

## 仓库结构

```
if-tree-skill-v5.md                  ← skill 本体，安装这个文件
v5 主工作流.md                        ← 完整工作流条件树
IF-Tree Skill 的设计哲学与结构原理.md   ← if-tree 的设计哲学
灯式机的自然哲学与数学原理.md           ← 灯式机理论（当前版本）
CITATION.cff                          ← 引用信息
```

---

## 适用范围

**适用于任何可顺序化的目标物。** 只要最终产出能被从头到尾线性地阅读、执行或交付，if-tree 就能为它提供前置结构。

**不限定 AI：** Claude、ChatGPT、Gemini、DeepSeek、Qwen、本地模型——任何能理解自然语言指令的模型都能执行此协议。

**不限定产出形式：** 条件树是目标物的前置结构。最终沉积为代码、论文、手册、剧本还是流程规范，取决于你和 AI 的选择。

---

## FAQ

**Q：这和 PRD（产品需求文档）有什么区别？**  
A：PRD 是散文。散文不能被机械执行。条件树可以。条件树的每个节点有精确地址、精确的条件-动作-输出三元结构、精确的分支闭合。PRD 告诉你"大概要做什么"，条件树告诉你"精确到每一个 if-else 要做什么"。

**Q：只能用于写代码吗？**  
A：不。代码只是条件树可以收敛出的目标物之一。论文、手册、剧本、模组、工作流、架构设计——任何可顺序化的产出物都适用。灯式机理论的核心主张是：目标物只要求具有可顺序化特征，条件树就能为它提供前置结构。

**Q：需要学新语法吗？**  
A：不需要。条件树的语法就是自然语言加缩进。"如果……那么……否则……"。你已经会了。

**Q：小项目也需要吗？**  
A：越小的项目越能感受到立竿见影的效果——因为一棵十几个节点的条件树，几轮对话就能完全闭合，然后一次性产出完整目标物。

**Q：和 AI 的 system prompt 冲突吗？**  
A：不冲突。if-tree 是协议层，不覆盖 AI 的基础能力。它只在需求描述出现时激活。

---

## License

MIT

---

---

# if-tree skill

**Condition Tree Protocol: Converging Unsealed Problems into Deliverable Determinate Structures.**

A universal structural convergence protocol. Converges vague human-AI dialogue into unambiguous condition tree documents. Works with any AI, works for any linearizable deliverable — code, papers, manuals, scripts, modules, workflows, architectures…

---

## What Problem Does This Solve

The core bottleneck in human-AI collaboration is not AI's capability. It's that **the requirements between you and AI have never been structured**.

The requirements you give AI are almost never complete. You don't know every detail yourself. AI won't tell you what it doesn't know — it guesses, then confidently produces content built on those guesses. You spot something wrong, fix one part, and it guesses elsewhere. A few rounds in, you're cleaning up after a system that doesn't know what it's doing.

This isn't about AI being insufficiently intelligent. It's about the absence of a structured convergence protocol between human and AI.

**if-tree solves this problem at the root.**

It doesn't let AI guess. The rule: if the user didn't say it, mark it ERROR — no guessing, no filling in. Every conditional branch must close. Every problem the system can't solve on its own must be surfaced to a human — silent swallowing is forbidden.

The result: your conversation with AI is no longer an unstructured collision of natural language. It becomes a continuously growing, continuously converging condition tree. Every node has a precise address. Every gap has a precise marker. Every round of dialogue fills holes, closes branches, and pushes toward convergence. When the tree closes, the deliverable can be produced without ambiguity — whether that deliverable is code, a paper, a manual, or anything else.

**Document is structure. Structure is program. Strict equivalence.**

---

## The Deliverable Is Not Just Code

The deliverable produced when a condition tree converges requires only one property: **linearizability** — it can be read, executed, or delivered from start to finish. Everything that satisfies this property is in scope:

- **Code**: programs, scripts, configurations, database schemas, API interfaces
- **Documents**: papers, technical reports, user manuals, operation guides, specifications
- **Creative works**: screenplays, game modules, world-building, narrative structures
- **Processes**: workflows, approval chains, operations procedures, emergency protocols
- **Architectures**: system designs, product architectures, organizational processes

The condition tree is the **pre-structure** for all of these. Before the deliverable takes shape, the tree surfaces every condition, branch, exception, boundary, and unknown. The deliverable is the structure's sediment in its final form.

---

## Get Started in 5 Minutes

### 1. Install

Place `if-tree-skill-v5.md` into your AI system's skill / system prompt / custom instructions.

- **Claude**: Project Knowledge or Custom Instructions
- **ChatGPT**: Custom Instructions or GPTs Instructions
- **Gemini**: System Instructions
- **Local models (Ollama / LM Studio, etc.)**: System Prompt

The skill is AI-agnostic. It's a pure protocol — any model that understands natural language can execute it.

### 2. Start Using

Describe your requirements directly to the AI. No need to say "please structure my requirements." The skill triggers automatically upon receiving any requirement description.

```
User: I need a tool that batch-processes Excel files, reads 
      specific columns, cleans the data, and outputs to a new file.

AI:   (automatically outputs a structured condition tree with 
      node addresses, axioms, data validation, ERROR markers,
      and human escalation mechanisms)
```

```
User: I'm writing a paper on human-AI collaborative specification 
      convergence, with three parts: theoretical framework, formal 
      definitions, and engineering validation.

AI:   (automatically outputs a structured condition tree that 
      surfaces the argumentation chain, chapter dependencies, 
      unproven theorems, and unconfirmed premises)
```

### 3. Iterate

Give feedback against the condition tree. Reference node addresses for modifications. AI updates the document first, outputs a change summary, then produces the deliverable. No skipping steps.

---

## Core Mechanisms

### Condition Tree = Turing-Complete Natural Language Program

Conditional branches (if-else) + loops (LOOP / FOREACH / BREAK / CONTINUE) = Turing complete. Every leaf node must have: trigger condition + action + output or state change. Missing any of the three → ERROR.

### ERROR-and-Halt

If the user didn't specify it, don't guess. When the system hits an unknown, it halts inference, marks ERROR, and waits for user input. This isn't conservatism — it's active counterfeit prevention against pseudo-continuity. AI's most dangerous habit is continuing to produce fluent output when it doesn't know.

### Four-Step Data Validation

When uncontrolled data enters the program, execute strictly in order: trust classification → target format definition → clean or reject → escalate to human. No silent drops, no defaults, no skip-without-reporting. Every anomaly must be surfaced to a human.

### Document Before Deliverable

Modification feedback → locate node → update document first → output change summary → then produce deliverable. The document is the sole authoritative state. The deliverable is the structure's sediment in its final form.

### Reversibility Self-Check

Before output, simulate an executor who knows nothing about the requirements. Verify they can produce the complete deliverable from the document alone, without ambiguity. If not → mark ERROR or complete the gaps and re-check.

---

## Why This Isn't Just "Better Prompting"

Prompt engineering optimizes single-output quality. if-tree changes the structure of human-AI collaboration.

| | Prompt Engineering | if-tree |
|---|---|---|
| Scope | Single input → single output | Multi-turn → continuous convergence |
| Handling unknowns | AI fills in (guesses) | ERROR-and-halt, surface to human |
| Output | Direct production | Structured condition tree doc → deliverable |
| Auditability | Low (reverse-engineer intent from output) | High (document is structure) |
| Compound returns | None (start from scratch each time) | Yes (document accumulates, converges) |

---

## Theoretical Foundation: The Lamp Machine

if-tree is not an engineering trick that happens to work well. It has a complete theoretical framework behind it.

The Turing Machine answers: what is mechanically computable.  
The von Neumann Architecture answers: how to package mechanical computation into executable program systems.  
**The Lamp Machine answers: how an unsealed problem converges in real time into a deliverable determinate structure.**

Three machines, three distinct root questions: **computable, executable, auditable**. The Lamp Machine addresses the third. Its primary object is the frozen time slice — the equivalent effective information carried by a condition tree document at the current round. Its state language consists of four objects:

- **Hole**: position reserved, content not yet confirmed
- **Node**: prediction matches reality, closed
- **Error**: reality comparison confirms no valid projection
- **Gap**: from the parent level's perspective, the slice cannot yet stand

The Lamp Machine's work is to collapse holes into nodes, surface unprojectable positions as errors, and eliminate gaps — until the slice is ready for handoff. The handoff target can be code, a document, memory, or the next round's input to the Lamp Machine itself.

Full theory: [`灯式机的自然哲学与数学原理.md`](灯式机的自然哲学与数学原理.md)

---

## Compound Returns

if-tree's value does not grow linearly.

Once the first condition tree is built, all subsequent modifications, extensions, and refactors follow the tree structure. Locate node → update document → change summary → deliverable follows. Maintenance cost compresses from "searching across the entire output surface for an entry point" to "navigating tree depth to locate the entry point."

Legacy deliverables can be reverse-lifted back into condition trees. Once this works, historical accumulation transforms from debt into structural capital.

Every effective document update compresses implementation degrees of freedom:

$$\Omega_{t+1} \subsetneq \Omega_t$$

Until production is reduced to "how to implement elegantly" — no longer primarily "what does the user actually want."

---

## Repository Structure

```
if-tree-skill-v5.md                           ← Skill body — install this file
v5 主工作流.md                                  ← Complete workflow condition tree
IF-Tree Skill 的设计哲学与结构原理.md             ← Design philosophy of if-tree
灯式机的自然哲学与数学原理.md                      ← Lamp Machine theory (current)
CITATION.cff                                    ← Citation information
```

---

## Scope

**Applies to any linearizable deliverable.** As long as the final output can be read, executed, or delivered from start to finish, if-tree can provide its pre-structure.

**AI-agnostic:** Claude, ChatGPT, Gemini, DeepSeek, Qwen, local models — any model that understands natural language instructions can execute this protocol.

**Form-agnostic:** the condition tree is the deliverable's pre-structure. Whether it ultimately sediments into code, a paper, a manual, a screenplay, or a process specification is up to you and your AI.

---

## FAQ

**Q: How is this different from a PRD (Product Requirements Document)?**  
A: A PRD is prose. Prose cannot be mechanically executed. A condition tree can. Every node has a precise address, a precise condition-action-output triad, and precise branch closure. A PRD tells you "roughly what to build." A condition tree tells you "exactly what every if-else should do."

**Q: Is this only for writing code?**  
A: No. Code is just one of many deliverables a condition tree can converge toward. Papers, manuals, screenplays, game modules, workflows, architecture designs — any linearizable output is in scope. The Lamp Machine theory's core claim is: as long as the deliverable has the property of linearizability, the condition tree can provide its pre-structure.

**Q: Do I need to learn new syntax?**  
A: No. The condition tree's syntax is natural language plus indentation. "If… then… else…" You already know it.

**Q: Is this needed for small projects?**  
A: Small projects are where you feel the impact most immediately — a tree of ten-odd nodes can fully close in a few rounds of dialogue, then produce the complete deliverable in one shot.

**Q: Does it conflict with the AI's system prompt?**  
A: No. if-tree is a protocol layer. It doesn't override the AI's base capabilities. It activates only when a requirement description appears.

---

## Author

**Starlight** ([@starlight-yxat](https://github.com/starlight-yxat))

Independent researcher. Designer of if-tree skill. Originator of Lamp Machine theory.

---

## License

MIT
