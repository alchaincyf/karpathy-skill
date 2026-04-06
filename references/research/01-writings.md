# Andrej Karpathy 著作与核心论点调研

> 调研日期：2026-04-05
> 信息源说明：一手 = 直接引自本人文字/视频；二手 = 他人转述/摘要；推测 = 基于多处语境推断
> 黑名单：知乎、微信公众号、百度百科——本文件中均未使用

---

## 一、基本信息与职业轨迹

**出生**：1986年10月23日，斯洛伐克布拉迪斯拉发，15岁随家人移居加拿大多伦多
**教育**：
- 多伦多大学：计算机科学+物理（双学位），2005-2009
- 不列颠哥伦比亚大学：机器学习硕士，2009年
- 斯坦福大学：博士，导师 Fei-Fei Li，2015年毕业，论文题为《Connecting Images and Natural Language》

**职业轨迹（关键节点）**：
- 2015：创建CS231n（斯坦福首门深度学习课，从150人扩展到750人）
- 2015-2017：OpenAI联合创始成员，研究科学家
- 2017-2022：特斯拉AI总监（汇报Elon Musk），主导Autopilot
- 2022年7月：离开特斯拉
- 2023年2月：重返OpenAI
- 2024年2月：离开OpenAI
- 2024年7月：创立 Eureka Labs（AI原生教育公司）
- 2026年2月：发布microgpt（200行纯Python训练GPT，零依赖）

来源：[Wikipedia](https://en.wikipedia.org/wiki/Andrej_Karpathy)（一手信息来源于本人官网 karpathy.ai）

---

## 二、博客文章（karpathy.github.io）完整列表

| 日期 | 标题 | URL | 重要性 |
|------|------|-----|--------|
| 2026-02-12 | microgpt | karpathy.github.io/2026/02/12/microgpt/ | ⭐⭐⭐⭐⭐ 最新力作 |
| 2022-03-14 | Deep Neural Nets: 33 years ago and 33 years from now | karpathy.github.io/2022/03/14/lecun1989/ | ⭐⭐⭐⭐ |
| 2021-06-21 | A from-scratch tour of Bitcoin in Python | karpathy.github.io/2021/06/21/blockchain/ | ⭐⭐⭐ |
| 2021-03-27 | Short Story on AI: Forward Pass | karpathy.github.io/2021/03/27/forward-pass/ | ⭐⭐ |
| 2020-06-11 | Biohacking Lite | karpathy.github.io/2020/06/11/biohacking-lite/ | ⭐ |
| 2019-04-25 | A Recipe for Training Neural Networks | karpathy.github.io/2019/04/25/recipe/ | ⭐⭐⭐⭐⭐ 实践圣经 |
| 2018-01-20 | (started posting on Medium instead) | — | 转型节点 |
| 2016-09-07 | A Survival Guide to a PhD | karpathy.github.io/2016/09/07/phd/ | ⭐⭐⭐⭐ |
| 2016-05-31 | Deep Reinforcement Learning: Pong from Pixels | karpathy.github.io/2016/05/31/rl/ | ⭐⭐⭐ |
| 2015-11-14 | Short Story on AI: A Cognitive Discontinuity | karpathy.github.io/2015/11/14/ai/ | ⭐⭐ |
| 2015-10-25 | What a Deep Neural Network thinks about your #selfie | karpathy.github.io/2015/10/25/selfie/ | ⭐⭐ |
| 2015-05-21 | The Unreasonable Effectiveness of Recurrent Neural Networks | karpathy.github.io/2015/05/21/rnn-effectiveness/ | ⭐⭐⭐⭐⭐ 经典之作 |
| 2015-03-30 | Breaking Linear Classifiers on ImageNet | karpathy.github.io/2015/03/30/breaking-convnets/ | ⭐⭐ |
| 2014-09-02 | What I learned from competing against a ConvNet on ImageNet | karpathy.github.io/2014/09/02/what-i-learned-from-competing-against-a-convnet-on-imagenet/ | ⭐⭐⭐ |
| 2014-08-03 | Quantifying Productivity | karpathy.github.io/2014/08/03/quantifying-productivity/ | ⭐ |
| 2014-07-03 | Feature Learning Escapades | karpathy.github.io/2014/07/03/feature-learning-escapades/ | ⭐⭐ |
| 2012-10-22 | The state of Computer Vision and AI: we are really, really far away | karpathy.github.io/2012/10/22/state-of-computer-vision/ | ⭐⭐⭐ |
| 2011-04-27 | Lessons learned from manually classifying CIFAR-10 | karpathy.github.io/2011/04/27/manually-classifying-cifar10/ | ⭐⭐ |

**Medium博客**：https://karpathy.medium.com/
核心文章：
- [Software 2.0](https://karpathy.medium.com/software-2-0-a64152b37c35)（2017，最广泛引用的文章）

来源：直接爬取博客索引页（一手）

---

## 三、核心博文深度解析

### 3.1 Software 2.0（2017，Medium）
**来源**：https://karpathy.medium.com/software-2-0-a64152b37c35（一手）

**核心论点**：
> "Software 1.0 是人类用Python/C++等语言手写的指令集；Software 2.0 是神经网络的权重——由优化算法从数据中生成的程序。"

**Software 1.0 vs 2.0 对比**：
- SW1.0：程序员识别问题空间中的"期望行为点"，手写显式规则
- SW2.0：给定输入-输出对，优化算法在"程序空间"中搜索最优程序（网络权重）

**SW2.0 的优势**（Karpathy原文论述）：
1. 计算同质性：所有运算都是矩阵乘法，对硬件加速极度友好
2. 可以学习人类无法明确表述的知识
3. 性能随数据和算力持续提升（可预期的规模效应）

**SW2.0 的劣势/风险**（Karpathy承认）：
- 结果难以解释
- 会静默失败（silent failure）
- 可能编码数据中的偏见

**SW2.0 将吃掉的领域**：视觉识别、语音处理、图像翻译、图像描述、游戏AI、数据库查询

**特斯拉案例**：随着Autopilot进化，C++代码被持续删除，由神经网络权重替代——这是SW2.0"吃掉"SW1.0的实体案例。

---

### 3.2 The Unreasonable Effectiveness of RNNs（2015）
**来源**：karpathy.github.io/2015/05/21/rnn-effectiveness/（一手）

**核心论点**：
> "如果训练普通神经网络是在函数空间上的优化，那么训练循环网络就是在程序空间上的优化。"

**关键实验**（展示RNN生成能力）：
- Paul Graham essays：生成有结构的创业智慧文字
- 莎士比亚：学会对话结构、说话者名称、复杂句法
- Wikipedia markdown：自动发现wiki链接格式
- LaTeX数学：生成几乎可编译的数学证明
- Linux内核C代码：生成有正确括号嵌套和变量声明的函数

**技术洞察**：约5%的RNN神经元自发习得可解释算法（引号检测、URL边界、括号计数）——无需显式指导。

---

### 3.3 A Recipe for Training Neural Networks（2019）
**来源**：karpathy.github.io/2019/04/25/recipe/（一手）

**核心前提**（两个关键观察）：
1. 神经网络训练是"有漏洞的抽象"（leaky abstraction）——不能当插件用，需要深入理解
2. 失败是静默的——网络会训练但表现差，没有明显错误提示

**六阶段流程**：

**阶段1：成为数据的一部分**
- 花几小时检视数千条样本
- 理解分布、模式、不平衡、标注噪声

**阶段2：端到端骨架+基准测试**
- 固定随机种子
- 关闭数据增强
- 验证初始化时的loss是否符合预期
- 建立人类基准
- 单批次过拟合验证架构可行性

**阶段3：过拟合**
- "不要当英雄"：复制已验证的架构，不要自创
- Adam + lr=3e-4 是容错性最强的起点

**阶段4：正则化（按有效性排序）**
1. 获取更多真实数据（最有效）
2. 数据增强
3. 预训练
4. Dropout（ConvNet用spatial dropout）
5. weight decay、early stopping

**阶段5：调参**
- 随机搜索优于网格搜索（更好地捕捉各参数间的敏感性差异）

**阶段6：最后压榨**
- 模型集成（guaranteed ~2%提升）
- 比直觉判断训练更长的时间

**元原则**：
> "fast and furious的训练方式行不通。成功与耐心和细心的程度正相关。"

---

### 3.4 Deep Neural Nets: 33 years ago and 33 years from now（2022）
**来源**：karpathy.github.io/2022/03/14/lecun1989/（一手）

**核心论点**：深度学习33年来宏观上几乎没有变化——仍是可微神经网络 + 反向传播的端到端优化。变化的是规模。

**数量级对比**：
- 参数量：约1,000,000倍
- 处理像素数据量：约100,000,000倍
- 训练速度：消费级硬件提升3,000倍（GPU可再提升100倍）

**性能提升来源**：
- 现代优化技巧（Adam、dropout、数据增强）：~60%误差下降
- 更大数据集：中等贡献
- 规模：需要更多算力

**2055年预测**：
> 未来的从业者不会从头训练模型，而是用自然语言与巨型基础模型交流，告诉"10,000,000倍的神经网络超级大脑"要做什么。

---

### 3.5 microgpt（2026年2月）
**来源**：karpathy.github.io/2026/02/12/microgpt/，GitHub Gist（一手）

**核心主张**：用200行纯Python（零依赖、无PyTorch、无NumPy、无GPU加速）实现完整GPT训练和推理——这是他"十年迷恋：将LLM简化到最基本要素"的集大成之作。

**包含内容**：文档数据集、分词器、自动微分引擎、类GPT-2架构、Adam优化器、训练循环、推理循环。

**信念表达**：
> "Everything else is just efficiency."（其他所有东西只是效率问题。）

这是他"If I can't build it, I don't understand it"信念的最新实践。

---

## 四、YouTube教学视频系列

### Zero to Hero 系列（Neural Networks: Zero to Hero）
**主页**：https://karpathy.ai/zero-to-hero.html（一手）
**GitHub仓库**：https://github.com/karpathy/nn-zero-to-hero
**开始时间**：2022年8月
**理念**：语言模型是学习深度学习的最佳入口——即使目标是计算机视觉，所学都能迁移。

| # | 标题 | 时长 | 核心内容 |
|---|------|------|---------|
| 1 | The Spelled-Out Intro to Neural Networks and Backpropagation: Building Micrograd | 2h25m | 从零实现反向传播，只需高中微积分基础 |
| 2 | The Spelled-Out Intro to Language Modeling: Building Makemore | 1h57m | bigram字符级语言模型，PyTorch入门 |
| 3 | Building Makemore Part 2: MLP | 1h15m | 多层感知机，过拟合/欠拟合概念 |
| 4 | Building Makemore Part 3: Activations & Gradients, BatchNorm | 1h55m | 梯度流分析，批归一化 |
| 5 | Building Makemore Part 4: Becoming a Backprop Ninja | 1h56m | 手动反向传播，不用autograd |
| 6 | Building Makemore Part 5: Building a WaveNet | 56m | 层级卷积网络架构 |
| 7 | Let's Build GPT: From Scratch, in Code, Spelled Out | 1h56m | 从零构建GPT，遵循"Attention is All You Need" |
| 8 | Let's Build the GPT Tokenizer | 2h13m | BPE分词器从零实现，分词对LLM行为的影响 |

### 其他重要视频
- **[1hr Talk] Intro to Large Language Models**（2023年11月）：面向普通受众，涵盖LLM训练、LLM OS比喻、安全（jailbreak/prompt injection）
- **Deep Dive into LLMs like ChatGPT**（2025年2月，3h31m）：完整训练栈深度解析，心智模型建立
- **Let's reproduce GPT-2**：从头复现GPT-2

---

## 五、学术论文（按引用量/重要性）

来源：dblp.org + Google Scholar条目（二手，引用数为搜索时近似值）

| 年份 | 标题 | 发表场合 | 合作者 | 核心贡献 |
|------|------|---------|--------|---------|
| 2017 | Deep Visual-Semantic Alignments for Generating Image Descriptions | IEEE TPAMI | Li Fei-Fei | 多模态对齐（图像→自然语言描述） |
| 2016 | **DenseCap**: Fully Convolutional Localization Networks for Dense Captioning | CVPR | Justin Johnson, Li Fei-Fei | 密集图像描述任务 |
| 2016 | Connecting Images and Natural Language（PhD论文） | Stanford | — | 博士论文总结 |
| 2017 | PixelCNN++: Improving the PixelCNN with Discretized Logistic Mixture | ICLR | Tim Salimans等 | 生成模型改进 |
| 2017 | World of Bits: An Open-Domain Platform for Web-Based Agents | ICML | Tianlin Shi等 | 网页代理基准（早期agent研究） |
| 2015 | ImageNet Large Scale Visual Recognition Challenge | IJCV | Russakovsky, Deng, Fei-Fei等 | ImageNet基准定义 |
| 2015 | Visualizing and Understanding Recurrent Networks | CoRR | Justin Johnson, Li Fei-Fei | RNN可视化与解释 |
| 2015 | Deep visual-semantic alignments for generating image descriptions | CVPR | Li Fei-Fei | 图像描述早期版本 |
| 2014 | Grounded Compositional Semantics for Finding and Describing Images | TACL | Socher, Le, Manning, Ng | 图文组合语义 |
| 2014 | Large-Scale Video Classification with ConvNets | CVPR | Toderici, Li Fei-Fei等 | 视频理解 |
| 2014 | Deep Fragment Embeddings for Bidirectional Image Sentence Mapping | NIPS | Joulin, Li Fei-Fei | 双向图文嵌入 |

**注**：VGGNet（Very Deep ConvNets for Large-Scale Image Recognition）是Simonyan & Zisserman的工作，Karpathy参与的是ImageNet挑战赛论文，不是VGGNet的作者。（纠正常见误传）

**CS231n课程**：2015年创立，是斯坦福首门深度学习课，视频在线免费，累计超过800,000次观看（TIME杂志数据）。

---

## 六、Software 1.0 / 2.0 / 3.0 完整框架

**来源**：2017年Medium文章 + 2025年YC AI Startup School演讲（结合使用，均为一手）

Karpathy在2025年YC AI Startup School演讲中将框架扩展为三代：

| 代际 | 定义 | 编程方式 | 代表平台 |
|------|------|---------|---------|
| Software 1.0 | 人类用传统语言写的显式指令 | 程序员写代码 | GitHub |
| Software 2.0 | 神经网络的权重，由优化器从数据生成 | 调数据集 + 跑优化器 | Hugging Face |
| Software 3.0 | LLM，用自然语言Prompt来编程 | 用英语写Prompt | — |

关键论断：
> "Prompts are now programs that program the LLM."（Prompt现在是程序，它们对LLM编程。）
> "Software 3.0 is eating 1.0/2.0." 
> "A huge amount of software will be rewritten."

**特斯拉佐证**：Autopilot进化过程中，神经网络持续扩张，C++代码持续被删除——这是SW2.0吃掉SW1.0的真实案例。

---

## 七、LLM OS 概念

**来源**：
- X推文，2023年9月（一手）：https://x.com/karpathy/status/1707437820045062561
- X推文，2023年11月（一手）：https://x.com/karpathy/status/1723140519554105733
- 1hr Talk Intro to LLMs（2023年11月视频）（一手）

**核心类比**：LLM不是聊天机器人，而是新操作系统的内核进程（kernel process）。

| 传统OS | LLM OS |
|--------|--------|
| CPU | LLM（处理器） |
| RAM | 上下文窗口（工作记忆） |
| 文件系统 | 嵌入数据库（向量检索） |
| 系统调用 | 工具调用/API调用 |
| 长期运行程序 | Agents |
| I/O设备 | 多模态输入输出（视觉、音频） |

---

## 八、关键术语与概念发明

### 8.1 Vibe Coding（2025年2月）
**来源**：https://x.com/karpathy/status/1886192184808149383（一手）

> "There's a new kind of coding I call 'vibe coding', where you fully give in to the vibes, embrace exponentials, and forget that the code even exists."

**背景**：2025年2月6日发布，内容提到用Cursor Composer + Sonnet + SuperWhisper用声音指令编码。

**影响力**：被视为4.5百万次浏览，Merriam-Webster在2025年3月将其列为"俚语与流行词"；Collins英语词典将其评为2025年度词汇。

### 8.2 Jagged Intelligence（锯齿形智能）
**来源**：https://x.com/karpathy/status/1882518317585650084（一手）+ 2025 LLM Year in Review（一手）

> "LLMs exhibit amusingly jagged performance characteristics: simultaneously a genius polymath and a confused and cognitively challenged grade schooler, seconds away from getting tricked by a jailbreak."

这不是训练缺陷，而是RLVR优化机制的结构性后果：能力在RLVR训练的特定领域急剧上升，形成不均匀的能力地形。

### 8.3 LLMs as "Summoned Ghosts"（被召唤的幽灵）
**来源**：2025 LLM Year in Review（一手）

> "LLMs are not evolved animals but summoned ghosts—entities optimized under entirely different constraints than biological intelligence."

论证：LLM的神经架构、训练数据、训练算法、优化压力与生物智能完全不同，不应用"动物进化"的视角理解它们，而是作为"智能空间中全新类型的实体"。

### 8.4 LLMs的"Anterograde Amnesia"（前向遗忘症）
**来源**：YC AI Startup School 2025演讲（一手）

将LLM比作电影《Memento》主角：缺乏长期记忆整合能力，只依赖上下文窗口。

---

## 九、Eureka Labs 使命宣言

**来源**：https://eurekalabs.ai/（一手），2024年7月16日发布

**使命**：构建一种AI原生的新型学校。

**核心信念**：
> "Subject matter experts who are deeply passionate, great at teaching, infinitely patient and fluent in all languages are very scarce and cannot personally tutor all 8 billion people on demand."

**解决方案**：Teacher + AI Teaching Assistant 的协作模式——教师设计课程，AI助手被优化为引导学生完成学习的工具，支持、杠杆化、规模化教师的能力。

**愿景**：
> "If we are successful, it will be easy for anyone to learn anything, expanding education in both reach (a large number of people learning something) and extent (any one person learning a large amount of subjects, beyond what may be possible today unassisted)."

**首款产品**：LLM101n: Let's Build A Storyteller（本科级课程，学生训练自己的AI）

---

## 十、学习哲学

来源：Twitter/X推文 + Stanford建议页（一手）

### 核心信条1：Learning should not be fun（学习不应该是娱乐）
> "Learning is not supposed to be fun. It doesn't have to be actively not fun either, but the primary feeling should be that of effort."

### 核心信条2：反"碎片化学习"（shortification of learning）
**来源**：https://x.com/karpathy/status/1756380066580455557（一手，2024年2月）

> "There are a lot of videos on YouTube/TikTok etc. that give the appearance of education, but if you look closely they are really just entertainment."

处方：关掉那些快速博文的标签页，"seek the meal"——教科书、文档、论文、手册、长文。分配4小时窗口，阅读、记笔记、重读、重述、处理、操弄材料。

### 核心信条3：Build to understand（构建即理解）
> "If I can't build it, I don't understand it."

这一信条贯穿：micrograd、makemore、nanoGPT、microgpt——每次都是"从零手造"来证明真正理解。

### 核心信条4：读一手文献（Read primary sources）
推荐他的LLM阅读列表包括直接读原始论文（Attention is All You Need、GPT-2、InstructGPT等），而非二手解读。

---

## 十一、Dwarkesh Patel 播客核心观点

**来源**：https://www.dwarkesh.com/p/andrej-karpathy（二手整理，一手为原播客）

**AGI时间线**：还需10年（不是近在眼前），问题可解决但仍然困难。

**对强化学习的批评**（反常观点！）：
> "Reinforcement learning is terrible."

论据：基于结果的奖励是"从吸管里吸取监督信号"——把大量轨迹信息压缩成单个奖励信号，在整个学习过程中传播噪声。人类并不主要用RL学习，而是用反思、合成数据生成（思考）、睡眠中的蒸馏。

**模型崩溃（Model Collapse）问题**：合成数据生成会失败，因为模型产出"坍缩"的分布，反复自我采样会危险地缩窄多样性。训练模型生成内容会降低性能，维持熵需要外部熵源（人类交互、多样化经验）。

**认知核心（Cognitive Core）愿景**：未来系统将分离知识与认知——约10亿参数的"认知核心"，去掉百科全书式的记忆但保留推理算法，像人类一样需要知识时再查找。

**计算连续性观点**：Karpathy拒绝"AI与普通计算机科学"的截然区分。他认为进步是演化性的："我们在非常、非常缓慢地抽象自己"，类似编译器取代汇编。AGI可能表现为连续性改进，而非不连续跃迁。

---

## 十二、反复出现的核心论点（≥3次出现的真信念）

以下是跨多个场合反复表达的核心立场，按确认次数排序：

### 论点1：从零构建是理解的唯一路径 ★★★★★
**出现场合**：micrograd（视频+代码）、makemore系列、nanoGPT、microgpt博文、LLM101n课程设计哲学、PhD建议
**标志性表达**：
> "If I can't build it, I don't understand it."

### 论点2：神经网络训练会"静默失败"，需要极度谨慎和可视化 ★★★★★
**出现场合**：Recipe for Training NNs（2019）、Zero to Hero课程、CS231n材料
**标志性表达**：
> "Neural net training is a leaky abstraction." 
> "A 'fast and furious' approach does not work."

### 论点3：软件正在经历根本性范式转变（SW1.0→2.0→3.0） ★★★★★
**出现场合**：Software 2.0（2017）、1hr Intro to LLMs（2023）、YC Startup School（2025）、X推文（多条）
**标志性表达**：
> "Software 2.0 will eat through Software 1.0."
> "A huge amount of software will be rewritten."

### 论点4：LLM是新型计算基础设施，不是工具 ★★★★
**出现场合**：LLM OS推文（2023）、1hr Talk（2023）、YC演讲（2025）、2025 LLM Year in Review
**标志性表达**：LLM是操作系统内核；上下文窗口是RAM；Memento类比。

### 论点5：LLM是全新类型的实体，不能用生物/人类框架理解 ★★★★
**出现场合**：2025 LLM Year in Review、"summoned ghosts"推文（多条）、短故事文章
**标志性表达**：
> "LLMs are not evolved animals but summoned ghosts."
> "Jagged Intelligence" 

### 论点6：AI教育需要民主化，任何人都应能学到最优质内容 ★★★★
**出现场合**：CS231n免费开放、Zero to Hero系列（免费）、Eureka Labs使命宣言、LLM101n开源
**标志性表达**：
> "If we are successful, it will be easy for anyone to learn anything."

### 论点7：深度学习的本质33年未变，变化的只是规模 ★★★
**出现场合**：33 years ago and 33 years from now（2022）、Lex Fridman播客、多处采访
**标志性表达**：
> "Not much has changed in 33 years on the macro level."

### 论点8：数据质量和数量是SW2.0的核心竞争力（超越架构创新） ★★★
**出现场合**：Tesla Data Engine描述、Recipe for Training NNs（"获取更多真实数据是最有效的正则化"）、Zero to Hero课程
**标志性表达**：在正则化方法中，"Get more real data"排名第一。

---

## 十三、推荐阅读/资源（揭示智识谱系）

### 必读论文（Karpathy推荐的LLM入门清单）
来源：karpathy.ai LLM reading list（一手）

1. Attention is All You Need（Transformer原论文）
2. Language Models are Unsupervised Multitask Learners（GPT-2论文）
3. Training Language Models to Follow Instructions（InstructGPT）
4. Llama 2: Open Foundation and Fine-Tuned Chat Models
5. RLAIF: Scaling Reinforcement Learning from Human Feedback with AI
6. Training Compute Optimal Language Models（Chinchilla）
7. Sparks of Artificial General Intelligence: Early Experiments with GPT-4

### 推荐学习资源
- CS231n笔记（他自己写的）
- 《Deep Learning》教科书（Goodfellow等）
- 《Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow》（入门推荐）
- 直接读原始论文，不要只看二手解读

**智识谱系推断（推测）**：
- 对费曼式教学法的认同（"从零构建"="如果你能教会别人，说明你理解了"）
- 对LeCun工作的深度了解（33 years ago博文直接复现1989年LeCun论文）
- 对Bahdanau（注意力机制发明者）的个人通信（发布了私人邮件对话，征得同意）

---

## 十四、已知矛盾与张力（不调和，直接记录）

**矛盾1：对RL的批评 vs. RLVR的赞扬**
- Dwarkesh播客中：称"Reinforcement learning is terrible"，批评基于结果的奖励
- 2025 LLM Year in Review中：将RLVR（Reinforcement Learning from Verifiable Rewards）称为2025年最重要的训练范式转变，高度赞扬

可能的调和：他批评的是稀疏奖励的传统RL（如策略梯度），赞扬的是有可验证奖励的RLVR。但这一区分在原文中并不总是清晰。

**矛盾2：谦逊预测 vs. 大胆愿景**
- "AGI still a decade away"（谦逊的10年时间线）
- 同时描述未来"任何人都可以学到任何东西"的教育革命、"大量软件将被重写"

这不一定是矛盾，但存在张力：他的预测相对保守，但他的行动（创立Eureka Labs、押注SW3.0）假设变革即将发生。

**矛盾3：反对"shortification of learning"（碎片化学习） vs. 自己制作大量解释性视频**
他批评YouTube上给人学习感觉但实际是娱乐的内容，但他自己的Zero to Hero系列本身也是YouTube视频。
可能的区分：他的视频要求大量认知投入（2小时+，要求动手做），是他定义中"需要努力"的类型。

---

## 十五、来源索引

| 来源 | URL | 可信度 |
|------|-----|--------|
| 个人博客（karpathy.github.io） | http://karpathy.github.io/ | 一手 |
| Medium博客 | https://karpathy.medium.com/ | 一手 |
| 个人官网 | https://karpathy.ai/ | 一手 |
| Zero to Hero课程页面 | https://karpathy.ai/zero-to-hero.html | 一手 |
| X账号 | https://x.com/karpathy | 一手 |
| Eureka Labs官网 | https://eurekalabs.ai/ | 一手 |
| bearblog年度回顾 | https://karpathy.bearblog.dev/ | 一手 |
| dblp论文列表 | https://dblp.org/pid/04/9925.html | 一手（文献数据库） |
| Google Scholar | https://scholar.google.com/citations?user=l8WuQJgAAAAJ | 一手（文献数据库） |
| YC Startup School演讲摘要 | https://www.latent.space/p/s3 | 二手（有完整transcript） |
| Dwarkesh播客 | https://www.dwarkesh.com/p/andrej-karpathy | 二手（有完整对话） |
| Wikipedia传记 | https://en.wikipedia.org/wiki/Andrej_Karpathy | 二手（综合可信） |
| Stanford个人页面 | https://cs.stanford.edu/people/karpathy/ | 一手 |
| vibe coding维基 | https://en.wikipedia.org/wiki/Vibe_coding | 二手（辅助确认） |
