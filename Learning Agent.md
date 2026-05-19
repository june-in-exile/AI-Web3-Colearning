請參考：<https://ethpanda.notion.site/Learning-Agent-Markdown-355bbd63be8781229f7bd724c6f98212>

## 目标

- 做一个课程级 Markdown 配置文件，作为 learning agent 的启动上下文。
- 让学员不需要反复复制课程说明，而是把一个 URL 丢给 agent，就能开始持续学习、任务拆解、记录和复盘。
- 让 agent 能根据学员水平进行交互式追问，例如初级 / 中级 / 高级、已有 AI 或 Web3 基础、每周可投入时间、想做的方向。

## Markdown 文件建议包含

- 课程定位：AI × Web3 School 是什么、面向谁、希望学员最终获得什么。
- 课程内容大纲：Week 1–Week 4 / Hackathon 的主线、每周学习目标、模块和推荐材料。
- 挑战任务：learning agent 配置、GitHub repo、AI coding、Web3 测试网、最小交叉实验、方向扫描、Hackathon proposal。
- 关键时间点：开营、每周任务提交、checkpoint、Hackathon、Demo Day / Showcase 等。
- 交付标准：repo、README、commit、日志、截图、交易哈希、合约地址、demo、复盘笔记。
- 安全边界：私钥、助记词、API Key、签名、转账、部署、权限操作必须人工确认，不允许直接交给 agent。

## 交互式学习计划逻辑

1. 先问学员当前水平：初级 / 中级 / 高级。
2. 再问学员背景：更偏 AI、更偏 Web3、两边都刚入门，还是已有工程经验。
3. 再问每周可投入时间和目标：补基础、做 demo、研究方向、准备 Hackathon。
4. 根据回答生成个人 Week 1–Week 2 任务计划，并建议 repo 结构、每日任务和 proof-of-work。
5. 每次学习后要求 agent 追问：今天完成了什么、遇到什么问题、下一步需要补什么材料。

## 待完善

- [ ]  把最终 Markdown 文件正文写出来，并发布成一个可访问 URL，供学员直接丢给 Claude Code / Codex / Hermes。
