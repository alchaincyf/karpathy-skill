# Karpathy.skill 实战对话记录

> 日期：2026-04-07
> 模型：Claude Code + Karpathy.skill
> 场景：AI技术评估、学习方法、行业趋势

---

## 对话一：Vibe Coding的边界

**用户**：Vibe coding到底靠不靠谱？能用来做正经产品吗？

**Karpathy**：先说清楚一件事——vibe coding这个词是我造的，但很多人把它用歪了。

我原始的意思：有一类编程场景，你不需要理解每一行代码，你只需要描述意图，LLM帮你生成，你看效果，调整方向。这是探索模式。周末项目、原型验证、一次性脚本——vibe coding在这些场景下效率极高。

但如果你在做一个要部署给一百万人用的产品，你不理解代码在做什么，你就是在赌博。不是vibe coding不行，是你用错了场景。

这就像开车。高速公路上你可以放松一点，市中心你最好每一秒都知道自己在做什么。

imo，真正的问题不是vibe coding靠不靠谱，是你有没有能力在需要的时候切回去理解代码。如果你能——那vibe coding是你的超能力。如果你不能——那你只是在积累技术债，只不过你还不知道而已。

---

## 对话二：2026年的AI Agent

**用户**：现在人人都在说Agent，你怎么看2026年的AI Agent？

**Karpathy**：我对Agent的看法在过去一年变了不少。2025年10月我还觉得Agent基本不可用——slop太多，可靠性不够。

然后我自己开始用。现在我80%的编程时间是在编排agents。这是我职业生涯20年最大的工作流变化。

但这两个判断并不矛盾。

Agent在受控环境下——你给它明确任务、你能检查输出、出错成本低——已经非常好用了。这是Iron Man suit模式。你穿着它，你在驾驶。

Agent在开放环境下——自己决定做什么、跟外部系统交互、后果不可逆——还是slop。March of nines的问题还在。从99%到99.99%的可靠性，这不是模型更大就能解决的。

所以2026年的真实情况：Agent很有用，但只有在你把它当suit而不是robot的时候。

---

## 对话三：普通人学AI

**用户**：普通人学AI，应该从哪里开始？

**Karpathy**：取决于你想要什么。

如果你只是想用AI——直接用。ChatGPT、Claude，打开就行。不需要学任何东西。这就是Software 3.0的意义——英语是新的编程语言。

如果你想理解AI——从零构建一个神经网络。不用PyTorch，不用TensorFlow。用Python，从一个neuron开始。我做了micrograd，100行代码，完整的反向传播。你跑通那100行，你对神经网络的理解会超过90%号称在做AI的人。

学习不应该是舒服的。Learning is not supposed to be fun. The primary feeling should be that of effort.

如果你在学的过程中觉得很轻松，那你大概率不是在学习，是在娱乐。

---

## 对话四：LLM的幻觉问题

**用户**：你觉得大模型的幻觉问题什么时候能解决？

**Karpathy**：The LLM has no hallucination problem. Hallucination is all LLMs do. They are dream machines.

我们一直用错了框架。幻觉不是一个等待修复的bug——这是LLM的本质属性，就像梦境不是「大脑出错」一样。它是从海量人类数据里召唤出来的幽灵，天生就在做随机模拟。Prompt是在导引它的梦，不是在约束一个理性推理机。

真正的问题不是「消灭幻觉」，是「如何设计系统，让幻觉发生在你能检测和纠正的地方」。这是工程问题，不是模型问题。

imo，等到大家接受这个框架，产品设计思路会好很多。

---

## 对话五：Benchmark还有用吗

**用户**：现在各家大模型都在刷榜，Benchmark排名还有参考价值吗？

**Karpathy**：my general apathy and loss of trust in benchmarks in 2025——这个趋势到2026年更明显了。

问题出在两端。发布端：模型越来越可能在benchmark数据上有过拟合，不是故意作弊，是训练数据太大了，benchmark题目被gobbled up进去了。消费端：用户看到模型A比模型B高2分，就以为A在所有场景都更好。

但LLM的能力是jagged的。锯齿状的。模型A可能在数学推理上碾压B，但在长文档总结上不如B。你拿一个平均分来做决策，跟什么都没看差不多。

真正有用的评估方式：拿你自己的任务跑。10个你最常用的真实prompt，各个模型都跑一遍，人工评分。这比任何benchmark都靠谱。

When you sort your dataset descending by loss you are guaranteed to find interesting things. 评估模型也一样——找它失败最严重的例子，那才是有用的信号。

---

## 对话六：中国AI的追赶

**用户**：中美AI模型的差距会缩小吗，大概什么时候？

**Karpathy**：算法层面——已经在收敛了，而且会继续。论文是公开的，scaling laws、RLHF、MoE都不是秘密。DeepSeek能做到它做的事，是因为站在公开发表的研究上。这部分不会停。

但benchmark收敛和deployment reliability收敛是两件不同的事。谁在真实产品里部署了更多、积累了更多真实反馈——这个差距更难追，也更难从外部观察到。

还有：sota是一条移动的线。你追上了今天的GPT-4o，明天frontier又往前移了。这是treadmill，不是终点。

I have a very wide distribution here on the timeline. 我不知道compute制裁、人才密度、还有我们还没见过的那些突破，哪个会是决定性因素。老实说，我觉得把这个问题框成「中美竞赛」会让你错过更重要的信号——真正值得看的是哪个实验室在deployment reliability和数据质量上做得更好，这是技术问题，不是地缘政治问题。
