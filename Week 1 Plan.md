# Week 1 学习计划：AI × Web3 基础入门

> 目标：从"模型是什么 / 链是什么"出发，跑通一次 AI 实践、一次测试网交互，并完成一个最小交叉实验。建立权限、安全、人工确认与失败恢复意识。

---

## 一、个人学习计划

### 第 0 步：定位自己

先判断基础：偏 AI / 偏 Web3 / 两边都刚入门。**优先补短板** —— Web3 背景先补 AI，AI 背景先补 Web3。

### 学习节奏（建议 5–7 天）

| 阶段 | 内容 | 产出 |
|---|---|---|
| Day 1–2 | 模块 A：LLM → Prompt → Workflow → Agent 认知 | 跑通第一个 LLM API 请求 |
| Day 3 | 补短板方向的基础（Web3 链上操作链概念） | 概念笔记 |
| Day 4 | 测试网 / 合约交互实践 | 一次测试网交易 + 区块浏览器验证记录 |
| Day 5 | 最小交叉实验：AI 输出 → 人工复核 → 钱包确认 → 链上执行 → 验证 | 一条完整流程记录 |
| Day 6–7 | 整理概念说明 + 过程记录，准备 Week 2 共同语言 | 复盘文档 |

### 核心原则

- 至少完成**两个方向的最小实践**（一个 AI 工具任务 + 一个测试网/合约任务）。
- 交叉实验必须把 **AI 输出、人工复核、钱包确认、链上执行、验证记录** 放进同一条流程。
- 复杂度和风险越高，越要警惕过度 agent 化。

---

## 二、关键概念解释

### LLM 的本质

基于上下文进行概率生成 —— 给定文本，预测最合理的下一个 token 序列。擅长语言理解、代码生成、推理；不擅长精确事实记忆、确定性计算、跨会话状态保持。

### 四个控制层面

| 层面 | 作用 |
|---|---|
| 上下文窗口 | "工作内存"，控制模型能看到多少信息 |
| 系统指令 | 设置身份、语气和边界 |
| 提示词 | 传递当前任务意图 |
| 工具调用 | 让模型从"说话"变为"做事" |

### Prompt → Workflow → Agent 的边界

- **Prompt**：让模型回答，决策在人。
- **Workflow**：预定义任务流程，模型是其中一个节点，路径固定。
- **Agent**：模型自主规划、动态调用工具、跨轮管理状态。

三者的失控风险和可调试性完全不同。

### AI 输出必须验证的五类风险

1. **事实错误** —— 自信编造，关键事实须外部核实。
2. **引用错误** —— 编造论文/链接/数据来源，不信任模型给的链接。
3. **推理漂移** —— 长上下文逻辑链断裂，需分段验证。
4. **执行越权** —— agent 超出授权，须设 guardrails 与 human-in-the-loop。
5. **工具误用** —— 调错工具或参数，须用 tracing 监控。

### Agent 核心技术组件

状态管理（多节点共享 State）、长期记忆（跨 session 召回）、MCP（统一连接协议）、Skills（可复用高层指令集）、Tool Calling（结构化请求）、Tracing（可视化执行链）、Guardrails（输入输出验证）、Handoff（控制权移交）、错误恢复（重试/回退/人工介入）。

### 什么时候真的需要 Agent？

需要 agent：目标开放式、需多工具协作、中间结果决定下一步、需跨会话记忆。
更适合简单方案：一次性问答用 Prompt、流程固定用脚本、高合规用人工审核、数据确定性高用数据库查询。

### Web3 链上操作链

账户 → 钱包 → 签名 → 交易 → Gas → 合约 → 测试网 → 区块浏览器，构成一条完整的链上操作链。每一步都需理解"谁在授权、谁在执行、如何验证"。

---

## 三、待完成 Checklist

### 模块 A — AI 基础

- [ ] 看完 *What is a Large Language Model?* 与 Hugging Face LLM Course Ch.1
- [ ] 用 OpenAI / Anthropic / GLM 任一官方 Quick Start 跑通第一个 API 请求
- [ ] 能说清 model / messages / temperature / max_tokens 的作用
- [ ] 用 Claude Code / Codex CLI / Cursor 完成一个小任务
- [ ] 能用自己的话区分 Prompt / Workflow / Agent
- [ ] 读完 Microsoft《AI Agents for Beginners》并理解 agent 组件

### Web3 基础

- [ ] 理解账户 / 钱包 / 签名 / 交易 / Gas / 合约关系
- [ ] 在测试网完成一次交易
- [ ] 在区块浏览器查到该交易并截图存档

### 最小交叉实验

- [ ] 设计一条 "AI 输出 → 人工复核 → 钱包确认 → 链上执行 → 验证" 流程
- [ ] 实际跑通并记录每一步
- [ ] 标注流程中的 guardrail 与人工确认点

### 复盘

- [ ] 整理一份概念说明文档
- [ ] 整理一份过程记录（含失败与恢复）
- [ ] 列出 Week 2 想深入的交叉方向（支付/身份/权限/安全隐私/治理协作）

---

## 四、不懂问题清单（待解答）

> 在学习过程中遇到不确定的点，记录在此，逐条标注状态。

| # | 问题 | 所属模块 | 状态 |
|---|---|---|---|
| 1 | temperature 与 max_tokens 具体如何影响输出？ | AI 基础 | 待解答 |
| 2 | MCP 协议与普通 Tool Calling 的本质区别？ | Agent | 待解答 |
| 3 | 如何判断一个任务"该用 workflow 还是 agent"？ | Agent | 待解答 |
| 4 | 测试网的币从哪里获取（faucet 流程）？ | Web3 | 待解答 |
| 5 | Gas 费如何估算，签名失败如何恢复？ | Web3 | 待解答 |
| 6 | 交叉实验中"人工确认点"应该设在哪几步？ | 交叉 | 待解答 |
| 7 | 如何为 agent 设计有效的 guardrails？ | 安全 | 待解答 |
| 8 | *（自行补充）* | | |

---

## 五、推荐学习入口

- What is a Large Language Model?（视频）
- Hugging Face LLM Course — Chapter 1
- Anthropic: Building with the Claude API
- Z.ai API 开发者文档 / Coding Plan
- Claude Code 101
- Microsoft《AI Agents for Beginners》
- OpenAI Agents SDK Intro / LangGraph Overview / Hermes Agent Docs

---

*建立共同语言，是为了让 Week 2 的交叉探索走得更远。*
