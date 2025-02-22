---
date: 2024-09-09
title: 加急特供|SUSTecher|如何做决策 1 决策分析基础
categories:
  - articles
tags:
  - SUSTecher
  - 杨小凯
  - 决策
summary: 搞清楚决策空间，并进行成本收益分析，是一切的开始。
draft: false
---

>搞清楚决策空间，并进行成本收益分析，是一切决策的开始。

## 决策空间：角点解与内点解

### 基础概念

在这里我们科普一下做决策的基本知识，**角点解与内点解**这个命名法多少有点致敬杨小凯了，算是二十年前的叫法（我们教决策的专业课还没上，先就这冷饭吃吧，以后还有热乎的）。

线性规划大家都知道吧？就是几根直线围一个可行域，然后让某一直线上下移动，使得参量形成极值。阅读下文时脑袋里装一个直角坐标系，就可以理解角点解与内点解这两个概念。

>所谓边际分析，就是假定最优决策不可能是角点解，而只能是内点解。所谓角点解，意味着最优决策中某个变量取尽可能最大或尽可能最小的值。所谓内点解，则意味着最优决策中所有变量都处于其可能的最小和最大值之间。而新兴古典经济学则证明，所有的内点解都不可能是最优解，最优解只会是角点解。——杨小凯《超边际分析》

什么意思呢？超边际分析和新兴古典什么经济学大家先不管，这里也借助小凯书中的例子，略加改编以更适合妮可的体质：

选课和选专业，就是只有角点解的决策问题。因为只有选和不选（1和0）。

不过它们也有区别。

对于特定的一门课，有选和不选两个选项；多门课程则自由度更大。只要学分充足，时间错开，先修课满足，你可以选了这一门再选另一门，也就是对于多门课是不互斥的。你的选课组合有很多种。

对于专业来说，则专业之间一定互斥，你能且仅能选择一门专业并修读。进专业的时机，从大多数人的选择来看，你可以选择1+3或2+2，少数是中外合作和医学院（情况更特殊，我们慢慢讨论）。有人甚至也会说0+4，我们可以之后从选课的角度解释这种“选择”。

角点解，算是离散的，非连续的，数学上很难处理，但是平时我们做决策稀松平常；而内点解，算是连续的，数学上好处理，我们却要想一想，算一算。比如，你准备胡罗卜炖多久，牛肉炖多久？炖不炖胡罗卜牛肉倒是很好想。

又或者，你要在某门课上做到多优秀？

选课之后，你要决定在某门课上的努力程度，这就从角点解变成了内点解。当然我们先做一个假设，就是以总评评价努力程度是合理的，而且目前只谈论这两个指标。相对于0和1，总评0-100可算得上是连续得多了。除此之外，你还要决定其他课怎么学，有时这是两难冲突，变成了经典的经济学边际分析问题（如时间精力分配）。

为什么要向大家普及这些概念？这是为了让大家在思考决策问题的时候，梳理清楚你究竟有怎样的选择，即**决策空间**。你手里有多个方案可供挑选总好过错漏重要的选项和机会。

### 坐稳，我要开始操作了

接下来我为大家示范一种考虑自己选课与进专业的案例。如果你想先学基础知识点，请继续往下读完这篇文章也行。如果你很着急具体的操作，请阅读[SUSTecher|用选课示范一种神奇的思路](https://liubinfighter.github.io/Blog/post/decision_making_insane_idea)。点不开别着急，最近几天就会更新。

## 成本收益分析

涂子沛博士在他的三本大数据丛书里面把老美对成本收益分析的玩法写尽了。我最早接触成本收益分析则是在温铁军先生的《八次危机》里。Anyway，掉书袋未免没意思，我的用意在于显示这是一个经济学的问题，并且运用广泛。

成本收益分析是我们做决策的基础，其中蕴含的一切皆可量化（至少值得去尝试）的思想，是值得我们去实践体会的。数学上（确切一点，代数上），就要求我们把多维空间的决策点映射到一维数轴上，损益相减进行排序，价高者得。——嗯，这一段看不懂完全没有问题（）。

比如：著名的上交生存手册[你的身价是多少 | SurviveSJTUManual (gitbook.io)](https://survivesjtu.gitbook.io/survivesjtumanual/li-zhi-pian/ni-de-shen-jia-shi-duo-shao)一文中，作者这样问道

>参加这样的工作，我们是不是正在以过于低廉的价格出卖自己的劳动力？

你如何判断参加一项工作是否贱卖了你的劳动力呢？

就我最近的实践而言，短期内我用最近一次工作平均时薪来判断。24年暑假我前往四川成都的一家教育培训机构担任助教工作共8天（一个短期冲刺营周期），包吃住的前提下共获得960元，平均每天120元。考虑到工作时长和强度，时薪不足10元，非常疲惫，是我评价最低的一次工作。虽然值得做的事情不能用这个下限判断，但是综合时薪低于10元的肯定是一律拒绝或者转移工作。

对于参与家教的同学们，对时薪肯定更为敏感。就我了解到附近同学们的价格，一小时200-800不等，算上通勤时间，平均下来差别非常大。如果有志于大学投入足够精力做分析总结以及积累，能成功消减参加家教的边际成本，提高边际收益和胜率的话，还是非常有价值的。

这里的所谓决策点，就是投入多少时间，做哪种项目，这一摞决策的集合，每一种组合分别对应着不同的时薪以及你的付出成本；而这里的排序的标尺，就是你的时薪-你的成本折算价格。如何把决策的成本折算成价格，以便和时薪相减，就非常见仁见智了。简单的情况下，你可以不做换算，就得出明显的满意的结论；去尝试换算也未尝不可。实践中讲求效率，而把知识点搞清楚则需多折腾。

我们再对上面的概念做一澄清：对于单一决策,无论是问**是否**的角点解还是问**多少**的内点解，就是简单的利弊权衡。利大于弊，或者弊大于利，或者利弊相当，是比较能得出结论的；而对含有多个维度的决策的时候，就会有一篮子组合给你挑花了眼。进行一定程度的量化就是为了解决“挑花了眼”的问题，用一个统一的标尺去衡量利弊，得出利最大弊最小的方案。

就我个人而言，尝试去写出成本收益对比表，本身就是一种思考，保障你的思维相对全面，客观。从鲁滨逊的落难优劣表到现代央行的资产负债表，这种简单的思维工具往往具有极大的能量。另外，去排序和量化也是拷问自己“什么是真正重要的”一个宝贵的机会。了解自己做决策时的所思所想，就是在了解自己。

下一期预告：[SUSTecher|如何做决策 2 沉没成本和机会成本]()

---

## English Corner (ChatGPT)

Here are some key terms and phrases from the article, along with their English definitions:

1. **Decision Space (决策空间)**: The set of all possible alternatives or options from which a choice can be made.

2. **Corner Solution (角点解)**: In optimization problems, a solution where at least one of the variables involved reaches its maximum or minimum possible value.

3. **Interior Solution (内点解)**: A solution to an optimization problem where none of the variables reach their maximum or minimum bounds, and all lie within the feasible region.

4. **Cost-Benefit Analysis (成本收益分析)**: A method of evaluating projects by comparing the total expected benefits of a project to its total expected costs.

5. **Marginal Analysis (边际分析)**: An economic technique used to analyze the change in cost or benefit that results from the production or consumption of one more (or one less) unit of a good or service.

6. **Optimal Decision (最优决策)**: The best possible decision in a given situation, often determined by maximizing benefits or minimizing costs.

7. **Quantify (量化)**: To express or represent (something) in terms of quantity; to measure or assign a numerical value to.

8. **Pros and Cons (利弊)**: The positive and negative aspects of an issue, decision, or course of action.

9. **Threshold (阈值)**: A level or point at which a change takes place or a new situation is reached.

10. **Tutoring (家教)**: The act of giving lessons to individuals or small groups outside of a traditional classroom setting, often to help them understand and master a particular subject.

11. **Marginal Cost (边际成本)**: The cost of producing one additional unit of a good or service, which typically increases as production increases.

12. **Marginal Benefit (边际收益)**: The additional benefit gained from consuming or producing one more unit of a good or service.

13. **Sunk Costs (沉没成本)**: Costs that have already been incurred and cannot be recovered, often a consideration in decisions about whether to continue with a project or investment.

14. **Opportunity Cost (机会成本)**: The potential benefit an individual, investor, or business misses out on when choosing one alternative over another.
