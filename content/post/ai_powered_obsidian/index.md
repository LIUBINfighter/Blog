---
date: 2024-09-24
title: "AI|Obsidian|打造丝滑Ob+本地AI写作工作流"
categories: 
- articles
tags: 
- workflow
- AI
summary: Ollama+llama3.1+LocalGPT+Smart2Brain
draft: true
---

## 前言：一坑未平一坑又起

决策系列在更了在更了（），学校的课表变动非常大，这几天疯狂赶作业中。

这篇文章介绍ollama部署本地AI+obsidian插件接入的方法。可能一篇文章更不完，需要把一些技术问题单独拎出来写。在进行微调和知识库索引前，我们先分为本地AI部署和OB插件两端进行介绍。

AI端：在线部署需要调用openai格式的api；本地我们使用ollama。ollama的设计思想和docker很像，把llm运转所需的环境依赖打包运行，支持市面上非常多的大模型在cmd直接下载，很适合本地部署。模型我们使用未经过微调的llama3.1-7B。部署设备移动端4060，显存8G速度很快够用，对中文支持有需求的建议暂时使用llama2-chinese或者调用社区微调+手动编写modelfile。这不算啥大问题，更换llm在ollama一行代码的事。我们先跑通再说。

Ob插件：我个人体验过不少Ob-AI插件，本次向大家推荐我使用频率最高，目前效果也是最好的两个插件

1.Local GPT

![LocalGPT](localgpt.png)

2.smart second brain

![alt text](image.png)