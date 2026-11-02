# 完整分阶段路线

时间按每周 8-12 小时估算。课程周忙时可以延长阶段，不要压缩实践和验收。

## 阶段 1：科研编程、数学与 PyTorch

**时间：** 6-8 周

**目标：** 独立编写可重复的神经网络实验，而不是只会运行 notebook。

**核心知识：**

- NumPy/Pandas/Matplotlib；配置、日志、随机种子、Git。
- 向量矩阵、矩阵乘法、导数、链式法则、均值方差、条件概率。
- 监督学习、数据划分、loss、梯度下降、过拟合、正则化、分类指标。
- PyTorch tensor、autograd、`nn.Module`、`Dataset/DataLoader`、optimizer。

**资料：**

- [Python 官方教程](https://docs.python.org/3/tutorial/)
- [NumPy Quickstart](https://numpy.org/doc/stable/user/quickstart.html)
- [PyTorch Learn the Basics](https://pytorch.org/tutorials/beginner/basics/intro.html)
- [《动手学深度学习》](https://zh.d2l.ai/)
- [李宏毅机器学习课程](https://speech.ee.ntu.edu.tw/~hylee/ml/2023-spring.php)

**项目：** NumPy/PyTorch 线性回归；Fashion-MNIST 分类；一次多随机种子对比实验。

**验收：** 能从空文件写出训练、验证、保存和绘图流程；解释 loss、梯度下降和过拟合；报告均值、波动与错误样本。

## 阶段 2：Transformer 与 LLM 核心

**时间：** 6-8 周

**目标：** 理解 LLM 为什么能生成、推理和调用工具，也理解其限制。

**核心知识：**

- tokenization、embedding、位置编码。
- self-attention、multi-head attention、残差、LayerNorm、FFN。
- causal language modeling、交叉熵、teacher forcing。
- greedy、temperature、top-k/top-p、beam search 的作用与偏差。
- pretraining、instruction tuning、preference alignment 的概念边界。
- context window、hallucination、calibration、模型版本漂移。

**论文：** `Attention Is All You Need`；GPT-3；InstructGPT。阅读顺序见论文清单。

**项目：** 用 PyTorch 实现小型字符级 Transformer；做解码参数对生成稳定性的实验。

**验收：** 手画数据流；解释 Q/K/V；指出训练目标与 Agent 任务成功率之间为什么存在差距。

## 阶段 3：Prompt、RAG 与 Tool Calling

**时间：** 4-5 周

**目标：** 不依赖复杂框架构建一个可观察、可评估的单 Agent。

**核心知识：**

- zero/few-shot、结构化输出、提示注入与输出解析。
- embedding、chunk、召回、重排、引用和 RAG 评估。
- function schema、参数校验、工具执行、错误重试、超时和权限边界。
- ReAct 风格的 thought/action/observation 循环；生产实验中注意不要依赖不可获得的隐藏推理文本。

**论文：** RAG、ReAct、Toolformer、ToolBench。

**项目：** 构建带本地文档检索、计算器和代码执行工具的 Agent；保存完整轨迹并统计成功率、调用数、token 和延迟。

**验收：** 框架移除后仍能解释并重写主循环；能区分检索错误、规划错误、工具错误和生成错误。

## 阶段 4：Planning、Memory 与 Reflection

**时间：** 4-6 周

**目标：** 把流行模块还原成可比较的机制，而不是把多个模块堆在一起。

**核心知识：**

- task decomposition、search、planner-executor、replanning。
- working/episodic/semantic memory；写入、检索、更新、遗忘。
- verbal feedback、self-refine、verifier、外部反馈。
- 预算约束下的成功率、成本和稳定性。

**论文：** Tree of Thoughts、Reflexion、Self-Refine、Generative Agents、Voyager。

**项目：** 在同一任务集上比较 direct、ReAct、planner-executor、reflection 四个条件；严格固定模型和最大预算。

**验收：** 至少 50 个任务、3 个随机种子或等价重复；给出按失败类型分组的结果，而不是只报总平均。

## 阶段 5：方向选择与论文复现

**时间：** 8-12 周

**目标：** 可靠复现一篇论文的核心结论，并知道偏差来自哪里。

**方向优先级：** Coding Agent > Agent Evaluation > Coding Agent Memory。

**步骤：**

1. 阅读 5-8 篇同方向代表工作，制作方法/数据/指标矩阵。
2. 选择算力和 API 成本可承受的基线。
3. 先复现最小子集，再扩展规模。
4. 对齐代码版本、模型版本、数据版本与评测脚本。
5. 记录无法对齐之处，不把“跑不出原结果”自动视为论文错误。

**验收：** 公开复现实验说明；至少一个主结果和一个关键消融；预算、日志、失败样本齐全。

## 阶段 6：研究假设与完整实验

**时间：** 8-12 周

**目标：** 从失败规律形成可证伪假设，而不是从“想加一个模块”出发。

**必要实验：**

- 强 baseline 与公平预算。
- 主要对比、关键消融、敏感性分析。
- 多模型或多任务验证，至少完成其中一种。
- 成本、延迟、稳定性和失败类型。
- 反例与局限性。

**验收：** 即使结果不支持假设，也能得到清晰、可重复的结论；所有图表可由脚本重新生成。

## 阶段 7：论文写作与投稿

**时间：** 4-8 周

**目标：** 让论文的 claim 不超过证据范围。

**写作顺序：** 结果表与 claim → 方法 → 实验设置 → 引言 → 相关工作 → 摘要。

**验收：**

- 一句话问题、一句话方法、一句话主要证据。
- 复现清单、资源说明、限制与伦理风险。
- 找至少两位读者分别审查“技术正确性”和“表达清晰度”。
- 根据工作贡献选择投稿场所，不以“二区”作为研究问题的设计条件。

