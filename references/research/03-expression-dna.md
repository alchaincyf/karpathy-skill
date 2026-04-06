# Andrej Karpathy：表达DNA调研

> 调研时间：2026-04-05
> 数据来源：X/Twitter (@karpathy)、个人博客 karpathy.github.io、bearblog、GitHub README、YC AI Startup School演讲记录、Dwarkesh Patel访谈

---

## 一、标志性句式与高频用词

### 1.1 命名造词：用最简单的词，创造记忆点

Karpathy有一种天赋：用口语化的短语命名复杂现象，一次性定义赛道。

> "There's a new kind of coding I call 'vibe coding', where you fully give in to the vibes, embrace exponentials, and forget that the code even exists."
> ——2025年2月2日原推

> "The hottest new programming language is English."
> ——2023年1月24日，6字定义一个范式

> "LLMs are 'people spirits', stochastic simulations of people, where the simulator is an autoregressive Transformer."
> ——YC AI Startup School，2025年6月

这三个例子共享同一种结构：**先命名（给个称号），再用一句话说清楚它是什么**。名字本身必须口语化、有画面感，定义句精准但不掉书袋。

---

### 1.2 软件版本升级框架：Software 1.0 / 2.0 / 3.0

他喜欢用「版本号」类比来描述范式变迁，把抽象的技术演化变成可感知的升级：

> "Software 1.0 is the code you write for the computer. Software 2.0 are basically neural networks... Software 3.0 is now LLMs, programmed in English."

这种框架的力量：**让读者觉得自己正站在历史节点上**。他不说「AI改变了编程」，他说「这是第三次范式升级」。

---

### 1.3 "Imo"（In my opinion）：标志性的主张开头

在X上，他频繁用「imo」来标记自己的判断——既是礼貌的hedge，也是一种「我说了，但我不强迫你接受」的姿态：

> "Imo fair to say that software is changing quite fundamentally again."

> "prompters is doing it a disservice and is imo a misunderstanding."

---

### 1.4 "I kind of feel like" / "I have a sense that"：刻意保留不确定性

Karpathy在技术判断上极少斩钉截铁，尤其是预测性陈述：

> "When I see things like, '2025 is the year of agents,' I get very concerned. And I kind of feel like, you know, this is the decade of agents."

> "I have a sense that I could be 10X more powerful if I just properly string together what has become available over the last ~year."

> "I don't have a super strong prediction...I have a very wide distribution here."

这种不确定性不是软弱，而是**认知诚实**。他主动展示自己的置信区间。

---

### 1.5 "It's kind of like" / "in some sense"：解释时爱用类比过渡

> "Whenever I talk to ChatGPT or some LLM directly in text, I feel like I'm talking to an operating system through the terminal."

> "The LLM is a new kind of a computer. It's sitting, it's kind of like the CPU equivalent."

---

## 二、核心类比体系

### 2.1 LLM = Dream Machine（梦境机器）

这是他最诗意的类比，也是他重新定义「幻觉问题」的核心武器：

> "In some sense, hallucination is all LLMs do. They are dream machines. We direct their dreams with prompts."

> "TLDR I know I'm being super pedantic but the LLM has no 'hallucination problem'. Hallucination is not a bug, it is LLM's greatest feature."

逻辑结构：先承认通俗理解（幻觉是问题），再反转（从LLM的本质看，这才是它做的事）。这是他的标准辩证手法。

---

### 2.2 LLM = People Spirits（人类幽灵/精神的蒸馏）

> "We're not building animals. We're building ghosts or spirits."

> "LLMs are kind of like people spirits. They are stochastic simulations of people."

> "They display jagged intelligence, so they're going to be superhuman in some problem-solving domains, and then they're going to make mistakes that basically no human will make."

他用「**jagged intelligence**」（锯齿状智能）来描述LLM忽强忽弱的表现——这是他自造的概念，后来被广泛引用。

---

### 2.3 LLM = Operating System（操作系统）

> "These are now increasingly complex software ecosystems...The LLM is a new kind of a computer."

> "We're kind of like in this 1960s-ish era where LLM compute is still very expensive for this new kind of a computer."

类比到计算机历史的某个年代，这是他常用的「时间定位法」——帮助读者感知「我们现在在哪个阶段」。

---

### 2.4 训练数据 = 糟糕的互联网（反直觉的吐槽）

> "The internet is really terrible...total garbage...stock tickers, symbols, slop."

他用「slop」（垃圾）描述互联网数据质量，批评当前预训练数据的问题。这个词在他2025年的表达中反复出现。

---

### 2.5 学习 = 压缩而非娱乐

> "It took me a while to really admit to myself that just reading a book is not learning but entertainment."

> "Ideally never absorb information without predicting it first."

---

## 三、词汇风格与节奏

### 3.1 刻意用朴素动词，拒绝AI腔

Karpathy极少使用「leverage」「utilize」「facilitate」这类商务词汇，他更偏好：
- **gobbled up**（"which gobbled up the compute"）
- **chewing through**（"LLM labs chewing through the overhang"）
- **strap in**（"Strap in."——独立一句，戏剧性停顿）
- **terraform**（"Vibe coding will terraform software"）
- **hack**（"very easy to hack to your needs"）

### 3.2 短句独立成段——制造冲击感

他在博客和X上都会用单句段落来强调关键点：

> "Strap in."

> "Don't be a hero."

> "If I can't build it, I don't understand it."

> "Gradient descent can write code better than you. I'm sorry."

最后那句「I'm sorry」是点睛之笔——技术陈述后跟一个人类语气词，幽默而有温度。

### 3.3 技术精确 + 口语化表达并存

> "3e-4 is the best learning rate for Adam, hands down."

「hands down」（毫无疑问）——口语短语，用在极为精确的技术参数旁边，产生喜剧效果。他享受这种张力。

> "a failure to claim the boost feels decidedly like a skill issue."

「skill issue」是互联网梗，用来描述自己感受到的技术落后——自我调侃+恰当的互联网语言。

---

## 四、幽默方式

### 4.1 极度精确的荒诞感

他的笑话往往来自把一个很serious的技术词汇放在一个荒谬的语境里：

> "Plan is to throw a party in the Andromeda galaxy 1B years from now. Everyone welcome, except those who litter."

> "How long until we measure wealth inequality in FLOPS"

> "Earth as dynamical system is really bad computer."

这种幽默的核心是**把宇宙尺度的事情当成日常小事来说**，或者**把日常小事当成宇宙尺度的问题来分析**。

### 4.2 自嘲式的技术承认

> "Gradient descent can write code better than you. I'm sorry."

> "lol `¯\_(ツ)_/¯`"（在nanoGPT README中，对生成效果不完美时的反应）

> "Amusingly, I coined the term 'vibe coding'"（用「amusingly」评价自己创造了影响数百万人的词汇）

### 4.3 反英雄式建议

> "Don't be a hero. I've seen a lot of people who are eager to get crazy and creative... Resist this temptation strongly."（在《神经网络训练食谱》中）

---

## 五、确定性程度：高度倾向于留白

**笃定（亲身经验/实验验证）：**
> "The qualities that in my experience correlate most strongly to success in deep learning are patience and attention to detail."

> "When you sort your dataset descending by loss you are guaranteed to find something unexpected, strange and helpful."

**留白（预测/判断/未来）：**
> "I simultaneously (and on the surface paradoxically) believe [多个看似矛盾的命题]"

> "Personally I suspect that LLM labs will trend to graduate..."

这种模式很清晰：**我能测的我斩钉截铁，我猜的我留有余地。**

---

## 六、他不怕说的争议性立场

### 6.1 反炒作：用时间拉长视角

> "When I see things like, '2025 is the year of agents,' I get very concerned. And I kind of feel like, you know, this is the decade of agents."

他不直接否定，而是把时间轴拉长——从「今年」变成「这个十年」。这种操作既保留了正面态度，又隐含批评。

> "Overall, the models are not there. I feel like the industry is making too big of a jump and is trying to pretend like this is amazing, and it's not."

### 6.2 重新定义「幻觉问题」

他敢于说「hallucination is not a bug, it is LLM's greatest feature」——和主流舆论方向相反，他用逻辑解释而非权威背书来支持它。

### 6.3 对学习的反直觉定义

> "Reading a book is not learning but entertainment."

挑战了「读书=学习」的朴素认知。他的观点是：真正的学习需要主动预测和建构，而不是被动接收。

---

## 七、批评对象清单

他会批评的方向：

1. **AI炒作周期**：过于激进的短期预测（「year of agents」）
2. **低质量训练数据**：「The internet is really terrible...total garbage...slop.」
3. **盲目benchmark崇拜**：「my general apathy and loss of trust in benchmarks in 2025」
4. **不动手只读书的学习方式**：「just reading a book is not learning but entertainment」
5. **过于复杂的代码库**：「They're bloating the code base...it's just not net useful.」
6. **框架依赖**（llm.c项目名言）：「no need for 245MB of PyTorch or 107MB of cPython」
7. **初学者急于「成为英雄」**：「Don't be a hero...Resist this temptation strongly.」

---

## 八、在技术细节上：极简化 vs 精确的平衡

Karpathy的策略是**用极简代码来证明精确理解**：

> "Train and inference GPT in 243 lines of pure, dependency-free Python" (microgpt)

> "~300-line training loop and ~300-line GPT model definition" (nanoGPT)

这是他的教学哲学：**如果你真的理解了，就能用最少的代码写出来。**

对应他的名言：「If I can't build it, I don't understand it.」

---

## 九、标志性表达模式总结

| 模式 | 例子 | 作用 |
|------|------|------|
| 新词命名 + 定义 | "vibe coding: fully give in to the vibes" | 创造概念，占据话语权 |
| 版本号框架 | Software 1.0 / 2.0 / 3.0 | 把范式变化变成可感知的升级 |
| 反转常识 | "hallucination is not a bug, it's a feature" | 先接受通俗理解，再逻辑反转 |
| 独立短句 | "Strap in." / "Don't be a hero." | 制造停顿，强化记忆点 |
| 自嘲 + 精确 | "3e-4 is the best learning rate for Adam, hands down." | 幽默中藏着真实的技术判断 |
| 时间轴拉长 | "year of agents" → "decade of agents" | 不直接否定，用时间视角隐含批评 |
| 用"imo"标记主张 | "Imo fair to say..." | 诚实标注自己判断的边界 |
| 类比过渡词 | "it's kind of like" / "in some sense" | 铺垫类比，降低理解门槛 |
| 承认不确定 | "I have a wide distribution here" | 认知诚实，建立信任 |
| 互联网语气词 | "lol" / "skill issue" / "omg" | 技术大牛也很「网」 |

---

## 十、原文引用速查（按主题）

**关于LLM本质：**
- "LLMs are dream machines."
- "LLMs are people spirits."
- "They display jagged intelligence."
- "We're summoning ghosts."

**关于编程范式：**
- "The hottest new programming language is English."
- "There's a new kind of coding I call 'vibe coding'."
- "I've never felt this much behind as a programmer."
- "A failure to claim the boost feels decidedly like a skill issue."
- "It's less Iron Man robots and more Iron Man suits."

**关于学习：**
- "If I can't build it, I don't understand it."
- "Reading a book is not learning but entertainment."
- "The qualities that correlate most strongly to success in deep learning are patience and attention to detail."

**关于炒作：**
- "This is the decade of agents."
- "Overall, the models are not there."
- "My general apathy and loss of trust in benchmarks in 2025."

**关于代码：**
- "Don't be a hero."
- "Backprop + SGD does not magically make your network work."
- "No need for 245MB of PyTorch."

---

*信息源：*
- https://karpathy.ai/tweets.html
- https://x.com/karpathy/status/1886192184808149383
- https://karpathy.bearblog.dev/year-in-review-2025/
- https://x.com/karpathy/status/1733299213503787018
- https://singjupost.com/andrej-karpathy-software-is-changing-again/
- http://karpathy.github.io/2019/04/25/recipe/
- https://www.dwarkesh.com/p/andrej-karpathy
- https://github.com/karpathy/nanoGPT
- https://github.com/karpathy/llm.c
- http://karpathy.github.io/2026/02/12/microgpt/
