# 从软件工程本科生到 LLM Agent 研究者

这是一条以科研能力为目标的 12-15 个月学习路线。它不以“会调用 Agent 框架”为终点，而以能够独立阅读论文、复现实验、提出可证伪假设并完成论文初稿为终点。

## 当前起点

- 大二，软件工程方向，有 C++、算法竞赛和数据结构算法基础。
- 能使用 Python，但数学、机器学习、深度学习尚处于入门阶段。
- 研究兴趣优先考虑 Coding Agent，其次是 Agent Evaluation 与 Agent Memory。
- 时间不固定，因此按每周 8-12 小时、6 个可移动学习单元规划。
- 目标是大三阶段形成可投稿成果；投稿层级由工作质量决定，不用期刊分区倒推选题。

## 使用方法

1. 先读 [能力地图与取舍](docs/00-assessment.md)。
2. 按 [完整路线图](docs/01-roadmap.md) 推进，不要同时学习多个阶段。
3. 从 [第一个月计划](plans/month-01/README.md) 开始，每完成一周填写 `progress/` 记录。
4. 第 3 个月开始使用 [论文阅读清单](docs/04-paper-list.md) 和 [论文笔记模板](templates/paper-note.md)。
5. 第 6 个月前后依据验收结果决定 Coding Agent、Evaluation 或 Memory 的具体选题。
6. 每个阶段只有达到验收标准后才进入下一阶段；“看完课程”不算完成。

## 路线总览

| 阶段 | 时间 | 主要产出 |
|---|---:|---|
| 1. 科研编程、数学与 PyTorch | 第 1-2 月 | 可复现的分类实验与实验报告 |
| 2. Transformer 与 LLM | 第 3-4 月 | 小型 Transformer；能解释推理与上下文机制 |
| 3. Prompt、RAG、Tool Calling | 第 5 月 | 不依赖复杂框架的单 Agent |
| 4. Planning、Memory、Reflection | 第 6 月 | 机制对比实验与失败案例分析 |
| 5. 定向阅读与基线复现 | 第 7-9 月 | 一个公开基线的可靠复现 |
| 6. 研究假设与完整实验 | 第 10-12 月 | 对比、消融、成本与失败分析 |
| 7. 论文与投稿 | 第 13-15 月 | 论文初稿、复现实验包和投稿决策 |

详细的 3、6、12 个月里程碑见 [时间规划](docs/02-timeline.md)。

## 三条研究主线

1. **Coding Agent（首选）**：代码任务有编译器和测试反馈，与你的算法和软件工程背景匹配，也容易构造客观指标。
2. **Agent Evaluation**：研究稳定性、成本、错误恢复和评测可信度；算力要求相对低，最适合训练严谨实验能力。
3. **Agent Memory**：研究保存什么、何时检索、如何遗忘，以及记忆是否真正改善长期决策；可与 Coding Agent 结合。

暂不优先 Multi-Agent 和复杂强化学习。原因不是它们不重要，而是变量多、成本高，初学者很难把机制收益与额外 token、额外调用或 Prompt 差异区分开。

## 仓库导航

- [能力地图与知识取舍](docs/00-assessment.md)
- [完整分阶段路线](docs/01-roadmap.md)
- [3/6/12 个月里程碑](docs/02-timeline.md)
- [研究方向分析](docs/03-directions.md)
- [代表论文与阅读顺序](docs/04-paper-list.md)
- [论文阅读与复现方法](docs/05-reading-reproduction.md)
- [从问题到投稿](docs/06-research-to-paper.md)
- [算力、API 与低成本策略](docs/07-resources-compute.md)
- [第一个月逐周计划](plans/month-01/README.md)
- [第 2-3 月计划](plans/months-02-03/README.md)
- [第 4-12 月计划](plans/months-04-12/README.md)
- [实践项目阶梯](projects/README.md)
- [论文笔记模板](templates/paper-note.md)
- [实验记录模板](templates/experiment-log.md)
- [每周复盘模板](templates/weekly-review.md)

## 执行原则

- 先解释直觉，再学习公式和实现。
- 每项知识都必须对应一个 Agent 中的作用或一个实验能力。
- 每周至少一半时间用于写代码、做实验或分析结果。
- 任何结果都记录模型版本、数据版本、随机种子、预算和失败案例。
- 简单改 Prompt、换模型或调参数不是研究创新，除非它用于验证一个更一般、可复现的科学问题。

