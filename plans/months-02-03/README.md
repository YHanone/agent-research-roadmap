# 第 2-3 月：深度学习基础与 Transformer 入门

## 第 2 月：把实验代码工程化

### 第 5 周：神经网络机制

- 激活函数、参数初始化、batch、epoch。
- 用 hooks 或日志观察梯度与激活。
- 项目：比较 ReLU 与另一种激活，分析收敛而非只看最终准确率。

### 第 6 周：优化与泛化

- SGD/Adam、学习率调度、正则化。
- 项目：在固定预算下比较优化器，至少 3 个随机种子。

### 第 7 周：概率与统计最小集合

- 随机变量、条件概率、期望、方差、抽样。
- 均值、标准差、置信区间的直觉；不要把标准差当置信区间。
- 项目：bootstrap 一个指标区间，观察小样本不稳定性。

### 第 8 周：工程化验收

- 命令行配置、日志、checkpoint、测试、结果脚本。
- 完成阶段 1 报告，提交代码审查。

**第 2 月验收：** 从空目录搭建训练项目；实验可重复；能解释数据泄漏、过拟合和随机波动。

## 第 3 月：Transformer 入门

### 第 9 周：文本表示

- tokenization、词表、embedding、序列 batch、mask。
- 实现简单 tokenizer 或分析现成 tokenizer，不深入训练 tokenizer 算法。

### 第 10 周：Attention 直觉与实现

- Q/K/V、scaled dot-product attention、mask。
- 用 PyTorch 手写单头 self-attention，并对所有 tensor 标注 shape。

### 第 11 周：Transformer Block

- multi-head、残差、LayerNorm、FFN、causal mask。
- 组装一个 block；用小输入检查输出和 mask。

### 第 12 周：论文与小模型

- 阅读 `Attention Is All You Need`：问题、架构、实验三条线。
- 训练字符级小语言模型或最小 GPT。
- 改变 temperature，观察生成多样性和正确性不能等同。

**第 3 月验收：**

- 画出一个 token 经过 Transformer 的数据流。
- 解释 attention 为什么适合在上下文中聚合信息。
- 解释语言模型训练目标为什么不等于 Agent 任务成功。
- 完成第一篇标准论文笔记。

