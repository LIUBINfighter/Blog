---
date: 2024-10-03
title: "AI|记录以往的AI作品"
categories: 
- portfolio
tags: 
- workflow
- AI
summary: 年久失修的Stable Diffusion, gpt-sovits等工具的作品集。 求求你给我个活干吧我自带干粮什么都会做的（bushi）。
draft: false
---

## 前言

今天把我暂时结项的AI相关的项目做一个小整理。由于时间跨度长达一年，之前的文件治理还不是很完善，所以补充了很多工程文件和说明。感觉自己这些天还是没白干，至少懂得如何折腾一个项目了。这篇文章会涵盖Stable Diffusion, gpt-sovits等项目，并尽快补充参考的链接和资料。

btw，想要一个自己的neuro/做自己oc的动画还是很困难啊，也没有那么多折腾的时间。

版权相关：I am not profiting commercially from any work presented here. 我通过这里的任何作品以及本文提到的链接推广和盈利。这只是为了展示以前自己捣鼓AI作品的经历以供参考。如果有侵权情况，请及时联系我。（suggest change或者github issue）

## Stable Diffusion

项目时间：2023-09-23

自然是秋葉大佬

- [【AI绘画】SD-WebUI 整合包 / 绘世启动器 / 训练器下载导航 （长期有效） - 哔哩哔哩 (bilibili.com)](https://www.bilibili.com/read/cv31254871/?spm_id_from=333.999.rich-text.link.click)

哎，Lora涉及版权，自己玩玩还行，就不能发出来了。不过还是可以发纯提示词的图。

![backTheme_58MB](backTheme_58MB.png)

超分辨率的效果真的超级惊人，很难想象之前的技术已经达到的这种效果。

## GPT-Sovits

项目时间：2024-03-02

- [耗时两个月自主研发的低成本AI音色克隆软件，免费送给大家！【GPT-SoVITS】_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV12g4y1m7Uw/?spm_id_from=333.999.0.0&vd_source=8bff7cdac17c4bc79b5b5163a742ba14)

这个值得多写一点。这个项目仅需要1分多种的音频内容就能直接训练和迁移不同语言，移动端4060足够本地微调和推理，很适合快速出Demo。


微调语音均为AN94，语音来自[少前百科GFwiki](https://www.gfwiki.org/w/%E9%A6%96%E9%A1%B5/%E5%85%B3%E4%BA%8EGFwiki#:~:text=Gfwiki%E5%B0%91%E5%89%8D%E7%99%BE%E7%A7%91)

### 文本直出

当年很焦虑的时候听这个。

<audio controls src="实事求是，不自卑-2 1.wav" title="Title"></audio>

文本参考[看完麻省理工博士胡渊鸣用代码实现「冰雪奇缘」后，自己陷入了深深的自卑，如何排解这种情绪？ - 知乎用户Wz5GSb的回答 - 知乎](https://www.zhihu.com/question/365148040/answer/968807103)

### 讲课工作流

我自己的想法是AI讲课，让你喜欢的角色给你讲书。

ChatGPT等LLMs负责把课本和slides转换为讲稿，然后安排给sovits读，就这么简单。由于当时没什么脚本经验（现在也没有），也不知道ollama这种强大的本地模型部署器，没有把整个流程自动化，有点小遗憾。

全书pdf切分，也没有找到合适的本地自动化工具，手动用adobe切的。

Demo参照文案参考[OpenIntro… by OpenIntro et al. [Leanpub PDF/iPad/Kindle]](https://leanpub.com/os), AI使用Kimi，在此基础上的流程为：

- 选领域

- 挑选教材

- pdf切分章节

- 喂给ai，提示词

#### Prompt upgrading

1. 撰写提纲，对大致情况有了解，先写提纲！一定要写提纲，如果数量太多可以分开写。

```Prompt
你现在是一名大学教授，提供给你的是之后lecture要讲的教材，请你根据教材编写你的讲稿提纲，使用中文、英文
```

2. 身份+情景+相关性+要求

```Prompt
你现在是一名经验丰富的大学教授，任教于数学和统计数据科学专业，能用流利的英文结合原教材授课。结合给我提供的文件，写出根据以下内容的讲稿，使用原书中的概念和语句，使用英语，务必使用英语
```

3. 修改提示词

```Prompt
你好！我希望你作为一名人工智能，能为我撰写一些使表达更加有效和丰富的提示词。请串联并改写以下词句，使其更加连贯和重点突出。
```

4. 修改细节、人称、决定语言，并输入对应的提纲+文件（拆分pdf）

```Prompt
Greetings! I wish you, as an experienced university professor with a robust background in mathematics and statistical data science, you are well-versed in delivering lectures with fluency in English, integrating key concepts and phrases from the original textbook. To craft an effective and engaging lecture, you will draw upon the provided document to create a comprehensive script that emphasizes the essential themes and ideas, ensuring that the content is articulated in a clear and coherent manner, with a focus on the English language as the primary medium of instruction.
```

#### 成果

- Lec_intro_V2.wav

<audio controls src="OpenIntro Statistics-Lec1_intro_V2.wav" title="Title"></audio>

- Ch1Lec1-Core Concepts.wav

<audio controls src="OpenIntro Statistics-Ch1Lec1-Core Concepts.wav" title=""></audio>

- Ch1Lec2-data.wav

<audio controls src="OpenIntro Statistics-Ch1Lec2-data.wav" title="Title"></audio>

-Ch1Lec3-Sampling.wav

<audio controls src="OpenIntro Statistics-Ch1Lec3-Sampling.wav" title="Title"></audio>

- Ch1Lec4-design.wav

<audio controls src="OpenIntro Statistics-Ch1Lec4-design.wav" title="Title"></audio>

## So-VITS-SVC

项目时间：2023-11-09

文件太大，现在已经找不到了www。社区镜像应该还有，但是AutoDL已经一万年没有登录了。

这个至少要90min以上的数据集训练checkpoints，建议上云跑，自己电脑不一定受的住。当时23年末尾还没有太多功能集成，本地至少要有以下工具：（现在可能不需要了）

- Adobe Audition 2022 SP

- Audio Slicer

- UVR5

## 算力云租借

- [AutoDL算力云 | 弹性、好用、省钱。租GPU就上AutoDL](https://www.autodl.com/home)

当时直接上V100完事了。社区镜像也很多，jupyter notebook拉下来就能跑，然后就静静等待别人的显卡发挥作用吧。

## 小结

感觉自己开始做一点交易以来就没太多时间放在AI上了。写这篇文章也算是心血来潮，把github当成网盘用。

什么时候有自己的neuro啊。
