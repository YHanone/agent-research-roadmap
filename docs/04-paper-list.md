# 代表论文与阅读顺序

本清单优先使用论文官方页面、会议页面、作者项目页和官方代码仓库。`无官方代码` 表示未列入可确认的作者官方实现，不用第三方仓库冒充。发表状态以表中链接为准，正式研究前应再次核对最新版本。

## A：建立 LLM 基础

| 优先级 | 论文 | 时间/发表 | 论文 | 官方代码 | 阅读目的 |
|---|---|---|---|---|---|
| A1 | Attention Is All You Need | 2017, NeurIPS | [论文](https://papers.nips.cc/paper/7181-attention-is-all-you-need) | 无官方代码 | 理解 Transformer 数据流，不要求记住全部公式 |
| A2 | Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks | 2020, NeurIPS | [论文](https://papers.nips.cc/paper/2020/hash/6b493230205f780e1bc26945df7481e5-Abstract.html) | [Transformers RAG 实现](https://github.com/huggingface/transformers/tree/main/src/transformers/models/rag) | 理解参数知识与外部检索的分工 |
| A3 | Training language models to follow instructions with human feedback | 2022, NeurIPS | [论文](https://papers.nips.cc/paper_files/paper/2022/hash/b1efde53be364a73914f58805a001731-Abstract-Conference.html) | 无完整官方训练代码 | 理解 instruction following 与偏好对齐 |

## B：Agent 核心机制

| 优先级 | 论文 | 时间/发表 | 论文 | 官方代码 | 阅读目的 |
|---|---|---|---|---|---|
| B1 | ReAct: Synergizing Reasoning and Acting in Language Models | 2023, ICLR | [OpenReview](https://openreview.net/forum?id=WE_vluYUL-X) | [ysymyth/ReAct](https://github.com/ysymyth/ReAct) | 最清晰的 reasoning-action-observation 基线之一 |
| B2 | Toolformer: Language Models Can Teach Themselves to Use Tools | 2023, NeurIPS | [论文](https://proceedings.neurips.cc/paper_files/paper/2023/hash/d842425e4bf79ba039352da0f658a906-Abstract-Conference.html) | 无官方代码 | 区分“推理时编排工具”和“训练模型学会工具” |
| B3 | Tree of Thoughts: Deliberate Problem Solving with Large Language Models | 2023, NeurIPS | [论文](https://proceedings.neurips.cc/paper_files/paper/2023/hash/271db9922b8d1f4dd7aaef84ed5ac703-Abstract-Conference.html) | [princeton-nlp/tree-of-thought-llm](https://github.com/princeton-nlp/tree-of-thought-llm) | 理解搜索、评价与计算预算的关系 |
| B4 | Reflexion: Language Agents with Verbal Reinforcement Learning | 2023, NeurIPS | [arXiv](https://arxiv.org/abs/2303.11366) | [noahshinn/reflexion](https://github.com/noahshinn/reflexion) | 研究语言反馈和 episodic memory |
| B5 | Self-Refine: Iterative Refinement with Self-Feedback | 2023, NeurIPS | [论文](https://proceedings.neurips.cc/paper_files/paper/2023/hash/91edff07232fb1b55a505a9e9f6c0ff3-Abstract-Conference.html) | [madaan/self-refine](https://github.com/madaan/self-refine) | 学会为迭代改进设置公平重采样基线 |
| B6 | Generative Agents: Interactive Simulacra of Human Behavior | 2023, UIST | [arXiv](https://arxiv.org/abs/2304.03442) | [joonspk-research/generative_agents](https://github.com/joonspk-research/generative_agents) | 理解记忆流、反思和长期行为；不把模拟效果等同真实智能 |
| B7 | Voyager: An Open-Ended Embodied Agent with Large Language Models | 2024, TMLR | [OpenReview](https://openreview.net/forum?id=ehfRiF0R3a) | [MineDojo/Voyager](https://github.com/MineDojo/Voyager) | 看 curriculum、skill library 和环境反馈如何结合 |

## C：评估、工具与环境

| 优先级 | 论文 | 时间/发表 | 论文 | 官方代码 | 阅读目的 |
|---|---|---|---|---|---|
| C1 | AgentBench: Evaluating LLMs as Agents | 2024, ICLR | [OpenReview](https://openreview.net/forum?id=zAdUB0aCTQ) | [THUDM/AgentBench](https://github.com/THUDM/AgentBench) | 理解多环境评估以及环境配置成本 |
| C2 | ToolLLM: Facilitating Large Language Models to Master 16000+ Real-world APIs | 2024, ICLR | [OpenReview](https://openreview.net/forum?id=dHng2O0Jjr) | [OpenBMB/ToolBench](https://github.com/OpenBMB/ToolBench) | 研究工具数据、检索与评测，不追求重跑完整训练 |
| C3 | WebArena: A Realistic Web Environment for Building Autonomous Agents | 2024, ICLR | [OpenReview](https://openreview.net/forum?id=oKn9c6ytLx) | [web-arena-x/webarena](https://github.com/web-arena-x/webarena) | 理解真实交互环境和状态型评测 |
| C4 | OSWorld: Benchmarking Multimodal Agents for Open-Ended Tasks in Real Computer Environments | 2024, NeurIPS Datasets and Benchmarks | [arXiv](https://arxiv.org/abs/2404.07972) | [xlang-ai/OSWorld](https://github.com/xlang-ai/OSWorld) | 了解 GUI Agent 的环境、评测与安全难点；初期不复现全套 |

## D：Coding Agent 主线

| 优先级 | 论文 | 时间/发表 | 论文 | 官方代码 | 阅读目的 |
|---|---|---|---|---|---|
| D1 | SWE-bench: Can Language Models Resolve Real-World GitHub Issues? | 2024, ICLR | [OpenReview](https://openreview.net/forum?id=VTF8yNQM66) | [SWE-bench/SWE-bench](https://github.com/SWE-bench/SWE-bench) | 先理解任务构建、测试型评测和污染风险 |
| D2 | SWE-agent: Agent-Computer Interfaces Enable Automated Software Engineering | 2024, NeurIPS | [arXiv](https://arxiv.org/abs/2405.15793) | [SWE-agent/SWE-agent](https://github.com/SWE-agent/SWE-agent) | 首选架构阅读：Agent-Computer Interface、轨迹和编辑反馈 |
| D3 | Agentless: Demystifying LLM-based Software Engineering Agents | 2025, PACMSE/FSE | [arXiv](https://arxiv.org/abs/2407.01489) | [OpenAutoCoder/Agentless](https://github.com/OpenAutoCoder/Agentless) | 检验复杂 Agent 是否必要，建立强而简单的 baseline |
| D4 | OpenHands: An Open Platform for AI Software Developers as Generalist Agents | 2024, arXiv 预印本 | [arXiv](https://arxiv.org/abs/2407.16741) | [All-Hands-AI/OpenHands](https://github.com/All-Hands-AI/OpenHands) | 了解开放式软件 Agent 平台；阅读时以版本号固定实现 |

## E：方向扩展，暂不作为首个复现

| 优先级 | 论文 | 时间/发表 | 论文 | 官方代码 | 阅读目的 |
|---|---|---|---|---|---|
| E1 | MetaGPT: Meta Programming for Multi-Agent Collaborative Framework | 2024, ICLR | [arXiv](https://arxiv.org/abs/2308.00352) | [FoundationAgents/MetaGPT](https://github.com/FoundationAgents/MetaGPT) | 分析角色与流程设计，同时检查相对单 Agent 的预算公平性 |
| E2 | ChatDev: Communicative Agents for Software Development | 2024, ACL | [arXiv](https://arxiv.org/abs/2307.07924) | [OpenBMB/ChatDev](https://github.com/OpenBMB/ChatDev) | 了解多 Agent 软件开发流程；不把演示质量当任务正确率 |
| E3 | MemGPT: Towards LLMs as Operating Systems | 2023, arXiv 预印本 | [arXiv](https://arxiv.org/abs/2310.08560) | [letta-ai/letta](https://github.com/letta-ai/letta) | 理解分层记忆与上下文管理；代码已持续演化，复现须固定版本 |
| E4 | ToolEmu: Identifying the Risks of LM Agents with an LM-Emulated Sandbox | 2023, arXiv 预印本 | [arXiv](https://arxiv.org/abs/2309.15817) | [ryoungj/ToolEmu](https://github.com/ryoungj/ToolEmu) | 从工具风险和模拟评测进入 Agent Safety |

## 推荐阅读顺序

1. 第 3-4 月：A1 → A2 → B1。
2. 第 5-6 月：B4 → C1 → D1。
3. Coding Agent 定向：D2 → D3 → D4。
4. Memory 定向：B4 → B6 → B7，然后回到 Coding Agent 场景设计实验。
5. Planning 定向：B3 → B1 → D2，重点检查预算公平。

## 每篇论文的最低产出

- 100 字以内的问题定义。
- 一张方法数据流图。
- 三条主要 claim 及其对应证据。
- 最强 baseline 和公平性判断。
- 两个失败模式或限制。
- 一个最便宜的复现切入点。

