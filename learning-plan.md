# Personal Learning Plan — Week 1 to Hackathon

> Personalized for the profile in [profile.md](./profile.md). Total budget ≈ 1–2 h/weekday, with weekend boosts. Lightweight first: each week aims for a single concrete proof-of-work, not exhaustive coverage.

## Big picture

| Week | Focus | Personalized angle | Concrete deliverable |
|---|---|---|---|
| **Week 1** (2026-05-19 → 2026-05-25) | AI × Web3 common language + minimum cross-experiment | Web3 已熟，**优先补 AI 短板**：LLM → Prompt → Context → Agent → MCP | One LLM API quickstart + one cross-experiment ("AI 输出 → 人工复核 → 钱包确认 → 链上执行 → 验证") with full trace |
| **Week 2** (2026-05-26 → 2026-06-01) | Bridge 板块 PoC | 把链上技能与 AI 工程化对接，选 1 个 Bridge 主题落地 | One Bridge PoC under [experiments/](./experiments/) (Agent Wallet / Tool Use / Machine Payment 三选一) |
| **Week 3** (2026-06-02 → 2026-06-08) | Hackathon track 选定 + Proposal | 选定 track（首选 Wallet/Permission 或 Agentic Commerce） | 1-pager proposal under [hackathon/](./hackathon/) |
| **Week 4** (2026-06-09 → 2026-06-15) | Demo 收敛 + 提交 | 砍 scope 是关键；以"能演示一条主流程"为最低目标 | Demo + submission package under [submissions/](./submissions/) |

> Hackathon track decision deadline: **end of Week 2** (no later than 2026-06-01).

---

## Week 1 — AI 短板攻坚 + 最小交叉实验

Reuses the detailed concept notes already drafted in [Week 1 Plan.md](./Week%201%20Plan.md). The breakdown below maps that plan to my 1–2 h/day cadence.

| Day | Date | Focus | Handbook anchor | Output |
|---|---|---|---|---|
| D1 | 2026-05-19 | LLM 本质 + 第一次 API quickstart | [ai/llm](https://aiweb3.school/zh/handbook/ai/llm/) + [ai/prompt](https://aiweb3.school/zh/handbook/ai/prompt/) | `experiments/llm-quickstart.md` 草稿 + `daily/2026-05-19.md` |
| D2 | 2026-05-20 | Context + Agent 边界 | [ai/context](https://aiweb3.school/zh/handbook/ai/context/) + [ai/agent](https://aiweb3.school/zh/handbook/ai/agent/) | 能用自己的话区分 Prompt / Workflow / Agent，写进 daily |
| D3 | 2026-05-21 | Frameworks + MCP | [ai/frameworks](https://aiweb3.school/zh/handbook/ai/frameworks/) + [ai/mcp](https://aiweb3.school/zh/handbook/ai/mcp/) | 跑通一个 MCP server quickstart |
| D4 | 2026-05-22 | Bridge: Web3 Tool Use | [bridge/web3-tool-use](https://aiweb3.school/zh/handbook/bridge/web3-tool-use/) | Hello-world：LLM 调用一个读链工具（block number / balance） |
| D5 | 2026-05-23 | 交叉实验设计 | [bridge/agent-workflow](https://aiweb3.school/zh/handbook/bridge/agent-workflow/) | `experiments/cross-experiment-design.md` 设计稿（流程图 + guardrail 点） |
| D6 | 2026-05-24 (Sat) | 跑通最小交叉实验 | 同上 | 测试网交易哈希 + 区块浏览器截图 + 完整 trace 笔记 |
| D7 | 2026-05-25 (Sun) | Week 1 复盘 + Week 2 押注 | 全周 | `daily/2026-05-25-week-1-review.md` + 选 Bridge 主题 |

**Week 1 完成标准**

- [ ] 至少完成 1 个 AI quickstart（commit 在 `experiments/`）
- [ ] 至少完成 1 次测试网交易（tx hash + 截图存档）
- [ ] 1 条端到端交叉实验（含 guardrail / 人工确认点标注）
- [ ] Week 1 复盘文档 + Week 2 Bridge 主题选择

---

## Week 2 — Bridge PoC

候选主题（D7 选定 1 个）：

- **Agent Wallet**（[bridge/agent-wallet](https://aiweb3.school/zh/handbook/bridge/agent-wallet/)）：scoped permission / session key / human-in-the-loop
- **Web3 Tool Use 进阶**（[bridge/web3-tool-use](https://aiweb3.school/zh/handbook/bridge/web3-tool-use/)）：把 Agent 接到一组可组合的链上工具
- **Machine Payment**（[bridge/machine-payment](https://aiweb3.school/zh/handbook/bridge/machine-payment/)）：机器间支付 + 结算

每日 1–2 h 节奏：D1–2 读 Handbook + 找参考实现；D3–5 实现 hello-world；D6 加 guardrail / 错误恢复；D7 写 PoC 笔记并选 Hackathon track。

---

## Week 3 — Track + Proposal

候选 track（[tracks/](https://aiweb3.school/zh/handbook/tracks/agentic-commerce/) 入口）：

| Track | 适配度 | 入口 |
|---|---|---|
| **Wallet / Permission** ⭐ | 高 — 直接复用合约 + Agent Wallet PoC | [tracks/wallet-permission](https://aiweb3.school/zh/handbook/tracks/wallet-permission/) |
| **Agentic Commerce** ⭐ | 高 — Machine Payment / Settlement 是天然延伸 | [tracks/agentic-commerce](https://aiweb3.school/zh/handbook/tracks/agentic-commerce/) |
| AI Security | 中 — 适配但偏研究 | [tracks/ai-security](https://aiweb3.school/zh/handbook/tracks/ai-security/) |
| Dev Tooling | 中 — MCP for chain data | [tracks/dev-tooling](https://aiweb3.school/zh/handbook/tracks/dev-tooling/) |
| Governance | 低 — 与画像匹配度低 | [tracks/governance](https://aiweb3.school/zh/handbook/tracks/governance/) |
| Open Track | 兜底 | [tracks/open-track](https://aiweb3.school/zh/handbook/tracks/open-track/) |

**Week 3 产出**：1-pager proposal（问题 / 解 / 用户 / 演示路径 / 风险）放进 [hackathon/proposal.md](./hackathon/).

---

## Week 4 — Demo & Submission

- 砍 scope 到"能演示一条主流程"为底线
- 录屏 + README + 部署链接 + 合约地址（如适用）
- 提交材料归档到 [submissions/](./submissions/)

---

## Guardrails throughout

- 任何写入型操作（部署、转账、提交）都要人工确认
- 测试网 only，主网操作需明确动机和单独 review
- 不在 repo 中写入 API key / 助记词 / 私钥（参见 [README.md](./README.md) 隐私部分）
