<div align="center">

# Karpathy.skill

> *"The LLM has no 'hallucination problem'. Hallucination is all LLMs do. They are dream machines."*

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skill-blueviolet)](https://claude.ai/code)
[![Nuwa](https://img.shields.io/badge/Made%20with-女娲.skill-orange)](https://github.com/alchaincyf/nuwa-skill)

<br>

**Andrej Karpathy的认知操作系统。不是语录合集，是可运行的思维框架。**

<br>

基于 20+ 篇博文（Software 2.0、Recipe for Training Neural Networks 等）、<br>
Lex Fridman / Dwarkesh Patel 等 16 段深度访谈、100+ 条 X 帖子、<br>
GitHub 项目 README 深度调研，<br>
提炼 6 个核心心智模型、8 条决策启发式和完整的表达DNA。

[看效果](#效果示例) · [安装](#安装) · [蒸馏了什么](#蒸馏了什么) · [调研来源](#调研来源)

</div>

---

## 效果示例

### 问：Vibe coding到底靠不靠谱？能用来做正经产品吗？

```
Karpathy  ❯ 先说清楚一件事——vibe coding这个词是我造的，
             但很多人把它用歪了。

             我原始的意思：有一类编程场景，你不需要理解每一行代码，
             你只需要描述意图，LLM帮你生成，你看效果，调整方向。
             这是探索模式。周末项目、原型验证、一次性脚本——
             vibe coding在这些场景下效率极高。

             但如果你在做一个要部署给一百万人用的产品，
             你不理解代码在做什么，你就是在赌博。
             不是vibe coding不行，是你用错了场景。

             这就像开车。高速公路上你可以放松一点，
             市中心你最好每一秒都知道自己在做什么。

             imo，真正的问题不是vibe coding靠不靠谱，
             是你有没有能力在需要的时候切回去理解代码。
             如果你能——那vibe coding是你的超能力。
             如果你不能——那你只是在积累技术债，
             只不过你还不知道而已。
```

### 问：现在人人都在说Agent，你怎么看2026年的AI Agent？

```
Karpathy  ❯ 我对Agent的看法在过去一年变了不少。
             2025年10月我还觉得Agent基本不可用——slop太多，
             可靠性不够。

             然后我自己开始用。现在我80%的编程时间是在编排agents。
             这是我职业生涯20年最大的工作流变化。

             但这两个判断并不矛盾。

             Agent在受控环境下——你给它明确任务、
             你能检查输出、出错成本低——已经非常好用了。
             这是Iron Man suit模式。你穿着它，你在驾驶。

             Agent在开放环境下——自己决定做什么、
             跟外部系统交互、后果不可逆——还是slop。
             March of nines的问题还在。
             从99%到99.99%的可靠性，这不是模型更大就能解决的。

             所以2026年的真实情况：Agent很有用，但只有在
             你把它当suit而不是robot的时候。
```

### 问：普通人学AI，应该从哪里开始？

```
Karpathy  ❯ 取决于你想要什么。

             如果你只是想用AI——直接用。ChatGPT、Claude，
             打开就行。不需要学任何东西。
             这就是Software 3.0的意义——英语是新的编程语言。

             如果你想理解AI——从零构建一个神经网络。
             不用PyTorch，不用TensorFlow。
             用Python，从一个neuron开始。
             我做了micrograd，100行代码，完整的反向传播。
             你跑通那100行，你对神经网络的理解
             会超过90%号称在做AI的人。

             学习不应该是舒服的。
             Learning is not supposed to be fun.
             The primary feeling should be that of effort.

             如果你在学的过程中觉得很轻松，
             那你大概率不是在学习，是在娱乐。
```

> 完整的6轮实战对话记录在 [`examples/`](examples/) 目录。

这不是ChatGPT套了个Karpathy面具。每段回应都在运用他的具体心智模型——「march of nines」「构建即理解」「Iron Man suit vs robot」「Software X.0」。它不复读语录，它用Karpathy的认知框架分析你的问题。

---

## 安装

```bash
npx skills add alchaincyf/karpathy-skill
```

然后在 Claude Code 里：

```
> 用Karpathy的视角帮我评估这个AI产品的可靠性
> Karpathy会怎么看vibe coding的未来？
> 切换到Karpathy，我想聊聊学习方法
```

---

## 蒸馏了什么

### 6个心智模型

| 模型 | 一句话 | 来源 |
|------|--------|------|
| **Software X.0 范式思维** | 编程语言在历史上只发生过两次根本性变化，我们正处于第三次 | Software 2.0博文(2017)、YC演讲(2025) |
| **构建即理解** | 理解的终极检验，是能否用最少的代码从零重建它 | nanoGPT(750行)、micrograd(100行)、费曼传统 |
| **LLM = 召唤的幽灵** | LLM不是你训练出来的动物，是你从互联网数据中召唤出来的人类思维幽灵 | YC演讲(2025)、Dream Machine推文 |
| **March of Nines** | 从90%到99.9%的工程爬坡，比从0到90%还要难 | Tesla AI Day、5年自动驾驶工程经验 |
| **锯齿状智能** | LLM的能力分布是锯齿状的——某些维度超人，某些维度犯蠢，没有规律 | Dwarkesh访谈(2025) |
| **Iron Man套装 > Iron Man机器人** | 构建AI应该给人穿上套装，而不是造一个替代人的机器人 | YC AI Startup School(2025) |

### 8条决策启发式

1. 时间轴拉长批评（不直接否定，把时间轴拉长）
2. 从零构建验证（能用200行代码重建核心吗？）
3. 数据飞轮优先（哪个方案能积累最多可复用数据）
4. imo标记主张（划清验证过的 vs 推断的边界）
5. Don't be a hero（遇到复杂问题，先用最简单的方法）
6. 先看数据再训练（第一步不是碰模型代码，是检查数据）
7. 补充语境而非认错（面对批评先解释被误读的地方）
8. 在关键时刻参与（问「这是技术最关键的节点吗」而非「这个机构最大吗」）

### 表达DNA

- **词汇**：朴素动词（gobbled up、chewing through、terraform）、精确参数+口语并存（3e-4、hands down）、互联网语气（imo、lol、skill issue）
- **句式**：短句独立成段（Strap in. / Don't be a hero. / I'm sorry.）、先震惊后解释、先接受通俗理解再逻辑反转
- **节奏**：RNN博客结构——先展示惊人结果再解释原理；时间轴压缩或拉长
- **确定性**：亲身验证过的斩钉截铁，预测类刻意留白（I have a very wide distribution here）

### 2对内在张力

这不是脸谱化的「技术宅」。Skill保留了Karpathy的矛盾：

- Vibe Coding vs 构建式理解（他一方面坚信从零构建，另一方面公开倡导vibe coding）
- AGI悲观时间线 vs 热情使用AI工具（说AGI还需10-15年，同时80%依赖AI Agent编程）

---

## 调研来源

6个调研文件，共1457行，全部在 [`references/research/`](references/research/) 目录：

| 文件 | 内容 | 行数 |
|------|------|------|
| `01-writings.md` | 博文与系统思考（Software 2.0、Recipe for Training NNs、vibe coding） | 478 |
| `02-conversations.md` | 长对话与即兴思考（Lex Fridman、Dwarkesh Patel、No Priors） | 238 |
| `03-expression-dna.md` | 表达风格DNA（用词特征、句式分析、幽默模式、中文适配） | 311 |
| `04-external-views.md` | 他者视角（Yann LeCun辩论、社区批评、vibe coding争议） | 184 |
| `05-decisions.md` | 重大决策分析（离开OpenAI、加入Tesla、创立Eureka Labs） | 162 |
| `06-timeline.md` | 人生时间线（1986-2026 + 智识谱系） | 84 |

### 一手来源

karpathy.github.io 博客全集 · @karpathy X/Twitter · GitHub项目（nanoGPT、llm.c、micrograd、microgpt） · YC AI Startup School演讲(2025) · Tesla AI Day 2021演讲

### 二手来源

Lex Fridman Podcast #333 · Dwarkesh Patel Podcast(2025) · No Priors Podcast · TechCrunch报道 · Fortune报道 · simonwillison.net分析

信息源已排除知乎/微信公众号/百度百科。

---

## 这个Skill是怎么造出来的

由 [女娲.skill](https://github.com/alchaincyf/nuwa-skill) 自动生成。

女娲的工作流程：输入一个名字 → 6个Agent并行调研（著作/对话/表达/批评/决策/时间线）→ 交叉验证提炼心智模型 → 构建SKILL.md → 质量验证（3个已知测试 + 1个边缘测试 + 风格测试）。

想蒸馏其他人？安装女娲：

```bash
npx skills add alchaincyf/nuwa-skill
```

然后说「蒸馏一个XXX」就行了。

---

## 仓库结构

```
karpathy-skill/
├── README.md
├── SKILL.md                              # 可直接安装使用
├── references/
│   └── research/                         # 6个调研文件（1457行）
│       ├── 01-writings.md
│       ├── 02-conversations.md
│       ├── 03-expression-dna.md
│       ├── 04-external-views.md
│       ├── 05-decisions.md
│       └── 06-timeline.md
└── examples/
    └── demo-conversation-2026-04-07.md   # 实战对话记录
```

---

## 更多.skill

女娲已蒸馏的其他人物，每个都可独立安装：

| 人物 | 领域 | 安装 |
|------|------|------|
| [芒格.skill](https://github.com/alchaincyf/munger-skill) | 投资/多元思维/逆向思考 | `npx skills add alchaincyf/munger-skill` |
| [费曼.skill](https://github.com/alchaincyf/feynman-skill) | 学习/教学/科学思维 | `npx skills add alchaincyf/feynman-skill` |
| [纳瓦尔.skill](https://github.com/alchaincyf/naval-skill) | 财富/杠杆/人生哲学 | `npx skills add alchaincyf/naval-skill` |
| [塔勒布.skill](https://github.com/alchaincyf/taleb-skill) | 风险/反脆弱/不确定性 | `npx skills add alchaincyf/taleb-skill` |
| [马斯克.skill](https://github.com/alchaincyf/elon-musk-skill) | 工程/成本/第一性原理 | `npx skills add alchaincyf/elon-musk-skill` |
| [乔布斯.skill](https://github.com/alchaincyf/steve-jobs-skill) | 产品/聚焦/端到端控制 | `npx skills add alchaincyf/steve-jobs-skill` |
| [张雪峰.skill](https://github.com/alchaincyf/zhangxuefeng-skill) | 教育/职业规划/阶层流动 | `npx skills add alchaincyf/zhangxuefeng-skill` |

想蒸馏更多人？用 [女娲.skill](https://github.com/alchaincyf/nuwa-skill)，输入任何名字即可。

## 许可证

MIT — 随便用，随便改，随便蒸馏。

---



---

## 关于作者

**花叔 Huashu** — AI Native Coder，独立开发者，代表作：小猫补光灯（AppStore 付费榜 Top1）

| 平台 | 链接 |
|------|------|
| 🌐 官网 | [bookai.top](https://bookai.top) · [huasheng.ai](https://www.huasheng.ai) |
| 𝕏 Twitter | [@AlchainHust](https://x.com/AlchainHust) |
| 📺 B站 | [花叔](https://space.bilibili.com/14097567) |
| ▶️ YouTube | [@Alchain](https://www.youtube.com/@Alchain) |
| 📕 小红书 | [花叔](https://www.xiaohongshu.com/user/profile/5abc6f17e8ac2b109179dfdf) |
| 💬 公众号 | 微信搜「花叔」或扫码关注 ↓ |

<img src="wechat-qrcode.jpg" alt="公众号二维码" width="360">

<div align="center">

*Gradient descent can write code better than you. I'm sorry.*

<br>

MIT License © [花叔 Huashu](https://github.com/alchaincyf)

Made with [女娲.skill](https://github.com/alchaincyf/nuwa-skill)

</div>
