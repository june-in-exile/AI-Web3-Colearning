# 个人学习计划

## 学员画像

| 维度 | 自评 |
| --- | --- |
| AI 基础 | 有基础 — 用过聊天界面、调过 API；没系统做过 Agent / RAG / MCP |
| Web3 基础 | 熟悉 — 写过并部署过合约，熟一条链的开发栈 |
| 编程 | 能独立开发 |
| 目标 | **Hackathon 项目**（Week 4 拿出 demo / proposal） |
| 每日时间 | 1–2 小时（周末加量） |
| 输出语言 | 中英混合（中文为主，代码 / commit 英文） |

- **长板**：链上技能（合约、钱包、Dev Stack）
- **短板**：Agent 工程化（state / memory / tool calling / MCP / guardrails）、Agent 框架（LangGraph / OpenAI Agents SDK / Hermes）、Vibe Coding 工作流

## 总体节奏

| 阶段 | 日期 | 重点 | 交付物 |
| --- | --- | --- | --- |
| **Week 1** | 05-19 → 05-25 | 补 AI 短板 + 最小交叉实验 | 1 个 LLM API quickstart + 1 条 "AI → 人工 → 钱包 → 链上 → 验证" 端到端实验 |
| **Week 2** | 05-26 → 06-01 | Bridge 主题 PoC（选 1） | PoC 落进 `experiments/`；**周末锁定 Hackathon track** |
| **Week 3** | 06-02 → 06-08 | Track 选定 + 提案 | 1-pager proposal 落进 `hackathon/` |
| **Week 4** | 06-09 → 06-15 | Demo 收敛 + 提交 | Demo + 提交包归档进 `submissions/` |

## Week 1 详细排期（1–2h/天）

| Day | 日期 | 重点 | Handbook 锚点 | 产出 |
| --- | --- | --- | --- | --- |
| D1 | 05-19 | LLM 本质 + 第一次 API quickstart | [ai/llm](https://aiweb3.school/zh/handbook/ai/llm/) + [ai/prompt](https://aiweb3.school/zh/handbook/ai/prompt/) | `experiments/llm-quickstart.md` |
| D2 | 05-20 | Context + Agent 边界 | [ai/context](https://aiweb3.school/zh/handbook/ai/context/) + [ai/agent](https://aiweb3.school/zh/handbook/ai/agent/) | 用自己的话区分 Prompt / Workflow / Agent |
| D3 | 05-21 | Frameworks + MCP | [ai/frameworks](https://aiweb3.school/zh/handbook/ai/frameworks/) + [ai/mcp](https://aiweb3.school/zh/handbook/ai/mcp/) | 跑通 1 个 MCP server quickstart |
| D4 | 05-22 | Web3 工具调用 hello-world | [bridge/web3-tool-use](https://aiweb3.school/zh/handbook/bridge/web3-tool-use/) | LLM 调用一个读链工具 |
| D5 | 05-23 | 交叉实验设计 | [bridge/agent-workflow](https://aiweb3.school/zh/handbook/bridge/agent-workflow/) | `experiments/cross-experiment-design.md` |
| D6 | 05-24（六） | 跑通最小交叉实验 | 同上 | tx hash + 截图 + trace 笔记 |
| D7 | 05-25（日） | 复盘 + 选 Week 2 主题 | 全周回顾 | `daily/2026-05-25.md`（含周复盘） |

**Week 1 完成线**：① 1 个 AI quickstart commit；② 1 条测试网 tx + 截图；③ 1 条端到端交叉实验（标注 guardrail / 人工确认点）；④ 周复盘 + Week 2 选题。

## Hackathon track 候选（Week 2 末锁定 1 个）

| Track | 匹配度 | 入口 |
| --- | --- | --- |
| Wallet / Permission ⭐ | 高 — 直接复用合约 + Agent Wallet | [tracks/wallet-permission](https://aiweb3.school/zh/handbook/tracks/wallet-permission/) |
| Agentic Commerce ⭐ | 高 — Machine Payment / Settlement 是延伸 | [tracks/agentic-commerce](https://aiweb3.school/zh/handbook/tracks/agentic-commerce/) |
| AI Security | 中 — 偏研究 | [tracks/ai-security](https://aiweb3.school/zh/handbook/tracks/ai-security/) |
| Dev Tooling | 中 — MCP for chain data | [tracks/dev-tooling](https://aiweb3.school/zh/handbook/tracks/dev-tooling/) |
| Open Track | 兜底 | [tracks/open-track](https://aiweb3.school/zh/handbook/tracks/open-track/) |

## 不懂问题清单

> 学到哪记到哪。能解决就划掉；该反馈 Handbook 的标 `→ feedback`。

- [ ] `temperature` 与 `max_tokens` 如何影响输出？
- [ ] MCP 协议与普通 Tool Calling 的本质区别？
- [ ] 任务"该用 workflow 还是 agent"如何判断？
- [ ] 如何为 agent 设计有效 guardrails？
- [ ] 交叉实验中"人工确认点"设在哪几步？

## 安全护栏

- 任何写入型操作（部署、转账、提交）人工确认
- **测试网 only**；主网操作单独 review
- 不在 repo 写入 API key / 助记词 / 私钥
