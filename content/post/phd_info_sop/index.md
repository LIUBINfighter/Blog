---
date: 2025-02-05
title: "KAUST 如何使用工具高效率选导师陶瓷"
categories: 
- worksheet
tags: 
- academic
summary: 八爪鱼+Kimi
draft: false
---

有一段时间在观察KAUST，顺便思考了下之后升学时怎么选教授，我决定使用SPA以及AI来帮我初选。

## 处理思路

### 信息获取

使用八爪鱼进行信息爬取。

[点击此处进行注册](https://affiliate.bazhuayu.com/qDvnJT)

邀请码： `qDvnJT`

功能强大，操作简单，无需编写代码就能采集网站数据！我晚一些会出教程，但是相信简单的操作你一上手就会。即使对于具有代码能力的人来说，也节省了很多自行编写和调试代码的时间和精力。

### 信息处理

使用Deepseek-r1编写脚本，比如我想要知道可能和network即网络方向的教授。

```prompt
帮我简单写一个处理表格的excel脚本，输出所有满足以下条件的行：任何一格中含有network字段
```

检查并修改输出的代码并运行。

```python
import pandas as pd

# 读取Excel文件（修改为你的文件路径）
input_file = "Faculty _ King Abdullah University.xlsx"
df = pd.read_excel(input_file)

# 创建筛选条件：任一单元格包含"network"（不区分大小写）
condition = df.apply(lambda row: row.astype(str).str.contains('network', case=False).any(), axis=1)

# 应用筛选条件
filtered_df = df[condition]

# 保存结果到新文件
output_file = "filtered_rows.xlsx"
filtered_df.to_excel(output_file, index=False)

print(f"找到 {len(filtered_df)} 行匹配结果，已保存到 {output_file}")
```

将所有结果直接喂给Kimi k1.5，让他筛选。

## 样例结果

### 1. **SHEHAB AHMED**

- **职位**：电气与计算机工程教授
- **个人主页**：[Shehab Ahmed](https://www.kaust.edu.sa/en/study/faculty/shehab-ahmed)
- **照片**：[Shehab Ahmed](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/shehab-ahmed-400x400.jpeg)
- **研究方向**：Ahmed教授的研究领域涵盖电力转换和机电系统。他的研究旨在将电子学、机械学、计算机科学和控制学科智能融合，开发用于未来智能电网和智能油田的新型设备和软件。他在智能电网领域的具体研究兴趣包括：分布式/可再生能源发电、电力转换、微电网能源管理/存储、混合动力和电动汽车传动系统以及高压直流输电系统（HVDC）。他在油田地下机电系统方面的工作旨在提高钻井操作效率、改善井筒完整性评估并支持成功的电缆输送。

- **联系方式**：[shehab.ahmed@kaust.edu.sa](mailto:shehab.ahmed@kaust.edu.sa)


### 2. **TALAL AL ATTAR**

- **职位**：计算机、电气与数学科学与工程教学教授

- **个人主页**：[Talal Al Attar](https://www.kaust.edu.sa/en/study/faculty/talal-al-attar)

- **照片**：[Talal Al Attar](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/talal-alattar.png)

- **所属部门**：计算机、电气与数学科学与工程部

- **联系方式**：[talal.attar@kaust.edu.sa](mailto:talal.attar@kaust.edu.sa)


### 3. **TAREQ AL-NAFFOURI**

- **职位**：电气与计算机工程教授

- **个人主页**：[Tareq Al-Naffouri](https://www.kaust.edu.sa/en/study/faculty/tareq-alnaffouri)

- **照片**：[Tareq Al-Naffouri](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/alnaffouri.jpg)

- **研究方向**：Al-Naffouri教授的研究兴趣集中在自适应、稀疏和统计信号处理及其应用，包括通信、超宽带和超声定位与跟踪。他的研究还扩展到无线网络的设计与分析。

- **联系方式**：[tareq.alnaffouri@kaust.edu.sa](mailto:tareq.alnaffouri@kaust.edu.sa)


### 4. **MOHAMED-SLIM ALOUINI**

- **职位**：电气与计算机工程教授，阿尔·花拉子米杰出教授

- **个人主页**：[Mohamed-Slim Alouini](https://www.kaust.edu.sa/en/study/faculty/mohamed-slim-alouini)

- **照片**：[Mohamed-Slim Alouini](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/bio-alouini.jpg)

- **研究方向**：Mohamed-Slim Alouini教授于2009年加入阿卜杜拉国王科技大学（KAUST），是创始教员之一。他现任联合国教科文组织“连接未连接者”教育主席，并领导通信理论实验室的活动。他的研究兴趣包括多样性合并技术、MIMO技术、多跳/合作通信系统、光学无线通信系统、认知无线电系统、绿色通信系统和网络、极端环境下的无线通信系统和网络以及天地空一体化网络。他目前特别关注农村、低收入、灾难和/或难以到达地区的信息和通信技术分布、接入和使用的不均衡问题。

- **联系方式**：[slim.alouini@kaust.edu.sa](mailto:slim.alouini@kaust.edu.sa)


### 5. **HAKAN BAGCI**

- **职位**：电气与计算机工程教授

- **个人主页**：[Hakan Bagci](https://www.kaust.edu.sa/en/study/faculty/hakan-bagci)

- **照片**：[Hakan Bagci](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/bio-bagci.jpg)

- **研究方向**：Bagci教授的研究兴趣包括应用和理论计算电磁学的各个方面，重点是时域积分方程及其快速行进时间求解；基于时域积分方程求解器的复杂集成和大型光电系统中波相互作用的表征；开发用于分析加载电缆和电路的复杂平台上电磁波相互作用的快速混合方法；复杂平台上波相互作用的统计表征；良条件积分方程公式；以及利用信号处理技术解决电磁逆散射问题。

- **联系方式**：[hakan.bagci@kaust.edu.sa](mailto:hakan.bagci@kaust.edu.sa)


### 6. **DANIELE BOFFI**

- **职位**：应用数学与计算科学教授

- **个人主页**：[Daniele Boffi](https://www.kaust.edu.sa/en/study/faculty/daniele-boffi)

- **照片**：[Daniele Boffi](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/daniele-boffi-400x400.jpeg)

- **研究方向**：Boffi教授的研究兴趣与偏微分方程的数值逼近有关。他的专长包括有限元方法、混合有限元以及特征值问题的数值逼近；他的研究主要应用于流体动力学、流体与结构的相互作用以及电磁学。

- **联系方式**：[daniele.boffi@kaust.edu.sa](mailto:daniele.boffi@kaust.edu.sa)


### 7. **DAVID BOLIN**

- **职位**：统计学副教授

- **个人主页**：[David Bolin](https://www.kaust.edu.sa/en/study/faculty/david-bolin)

- **照片**：[David Bolin](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/david.bowin.jpeg)

- **研究方向**：Bolin教授的主要研究兴趣在于随机偏微分方程及其在统计学中的应用，重点是开发实用且计算高效的工具，用于建模非平稳和非高斯过程。他还从事空间统计学和医学成像领域的不确定性量化和可视化研究。

- **联系方式**：[david.bolin@kaust.edu.sa](mailto:david.bolin@kaust.edu.sa)


### 8. **MARCO CANINI**

- **职位**：计算机科学副教授

- **个人主页**：[Marco Canini](https://www.kaust.edu.sa/en/study/faculty/marcocanini)

- **照片**：[Marco Canini](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/marco-Canini.png)

- **研究方向**：Canini教授的研究兴趣在于大规模网络计算机系统的原理构建和运行，特别是在分布式系统、大规模计算和计算机网络方面，重点是云计算和可编程网络。他目前的工作重点是改进网络系统的设计、实现和运行，关注可靠性、性能、安全性和能源效率等关键属性。

- **联系方式**：[marco@kaust.edu.sa](mailto:marco@kaust.edu.sa)


### 9. **MARC DACIER**

- **职位**：计算机科学教授

- **个人主页**：[Marc Dacier](https://www.kaust.edu.sa/en/study/faculty/marc-dacier)

- **照片**：[Marc Dacier](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/Marc_Dacier.png)

- **研究方向**：Marc Dacier是计算机科学（CS）的全职教授，也是King Abdullah University of Science and Technology（KAUST）弹性计算与网络安全研究中心（RC3）的成员。Dacier博士1994年在法国图卢兹的INPT获得博士学位，之后在学术界和工业界都有丰富的职业经历。他曾在法国电信和法国内政部担任安全顾问，之后加入IBM Research在瑞士苏黎世创建全球安全分析实验室（GSAL）。2002年，他成为Eurecom的教授。2008年，他加入Symantec，建立了其欧洲研究实验室。后来，他在美国管理全球所有的合作研究项目。他还曾担任Symantec Research Labs的大学关系经理。2014年，他成为卡塔尔计算研究中心（QCRI）网络安全研究小组的主任。2017年10月，他回到EURECOM，担任数字安全部门的负责人和全职教授。Dacier博士是网络安全领域的国际知名专家，曾担任120多个主要安全和可靠性会议的程序委员会成员，并担任多个顶级技术同行评审期刊的编委。

- **联系方式**：[marc.dacier@kaust.edu.sa](mailto:marc.dacier@kaust.edu.sa)


### 10. **ROBERTO DI PIETRO**

- **职位**：计算机科学教授

- **个人主页**：[Roberto Di Pietro](https://www.kaust.edu.sa/en/study/faculty/roberto-di-pietro)

- **照片**：[Roberto Di Pietro](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/roberto-dipietro.jpg)

- **研究方向**：Roberto教授的目标是在网络安全研究中追求卓越，解决该领域的基础和应用挑战，并产生影响和创新。他的研究兴趣特别在于分布式系统的安全和隐私，特别是支持关键基础设施的系统。他还对数据科学、在线社交网络以及应用人工智能技术解决当前和未来系统中的安全和隐私问题感兴趣。

- **联系方式**：[roberto.dipietro@kaust.edu.sa](mailto:roberto.dipietro@kaust.edu.sa)


### 11. **NAZEK EL-ATAB**

- **职位**：电气与计算机工程副教授

- **个人主页**：[Nazek El-Atab](https://www.kaust.edu.sa/en/study/faculty/nazek-el-atab)

- **照片**：[Nazek El-Atab](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/nazek.png)

- **研究方向**：El-Atab博士的研究兴趣集中在智能存储器和电子设备的设计与制造及其应用，包括存内计算和存内传感。

- **联系方式**：[nazek.elatab@kaust.edu.sa](mailto:nazek.elatab@kaust.edu.sa)


### 12. **MOHAMED ELHOSEINY**

- **职位**：计算机科学副教授

- **个人主页**：[Mohamed Elhoseiny](https://www.kaust.edu.sa/en/study/faculty/mohamed-elhoseiny)

- **照片**：[Mohamed Elhoseiny](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/Mohamed-Elhoseiny.png)

- **研究方向**：Mohamed Elhoseiny博士是KAUST（阿卜杜拉国王科技大学）视觉计算中心的计算机科学副教授。Elhoseiny博士与Facebook AI Research的多位研究人员合作，包括Marcus Rohrbach、Yann LeCun、Devi Parikh、Dhruv Batra、Manohar Paluri、Marc'Aurelio Ranzato和Camille Couprie。他还与KULeuven（与Rahaf Aljundi和Tinne Tuytelaars）、UC Berkeley（与Sayna Ebrahimi和Trevor Darrell）、University of Oxford（与Arslan Chaudry和Philip Torr）以及Technical University of Munich（与Shadi AlBarqouni和Nassir Navab）等学术机构进行了富有成效的合作。他的主要研究兴趣在于计算机视觉、自然语言与视觉的交叉以及计算创造力。Elhoseiny博士于2016年10月在Rutgers University获得博士学位，导师为Ahmed Elgammal。他的工作得到了广泛认可。2018年，他因在ECCV研讨会上关于创意时尚生成的工作获得了最佳论文奖，该奖项由UNC Chapel Hill的Tamara Berg颁发，并由IBM Research和JD AI Research赞助。这项工作还被《New Scientist》杂志报道，他与Camille Couprie共同在Facebook F8年度大会上展示了这项工作。他早期关于创意艺术生成的工作在2017年被《New Scientist》杂志和MIT技术评论报道，并在2018年HBO的《硅谷》第五季第三集中出现。他的创意AI艺术作品在2017年迪士尼的最佳AI会议上（观众超过6000人）、Facebook在NeurIPS 2017上的展位以及2018年6月的官方FAIR视频中展出。他在2018年MIT技术评论上关于终身学习的工作也得到了报道。2018年11月，基于他在零样本学习领域的五年工作，Elhoseiny博士在联合国生物多样性大会上（观众超过10,000人，来自192个国家和数十个重要组织）发表了关于AI如何造福生物多样性的演讲，这反映了疾病管理和气候变化的影响。Elhoseiny博士在CVPR 2016上获得了博士生论坛奖，并在2014年因其“Write-a-Classifier”项目获得了NSF奖学金。

- **联系方式**：[mohamed.elhoseiny@kaust.edu.sa](mailto:mohamed.elhoseiny@kaust.edu.sa)


### 13. **AHMED ELTAWIL**

- **职位**：电气与计算机工程教授

- **个人主页**：[Ahmed Eltawil](https://www.kaust.edu.sa/en/study/faculty/ahmed-eltawil0209-4878)

- **照片**：[Ahmed Eltawil](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/ahmad.png)

- **研究方向**：Ahmed博士的研究兴趣集中在低功耗数字电路和信号处理架构领域，特别关注移动系统。他是加州大学尔湾分校普适通信与计算中心（CPCC）和嵌入式与网络物理系统中心（CECS）的成员。

- **联系方式**：[ahmed.eltawil@kaust.edu.sa](mailto:ahmed.eltawil@kaust.edu.sa)


### 14. **PAULO ESTEVES-VERÍSSIMO**

- **职位**：计算机科学教授

- **个人主页**：[Paulo Esteves-Verissimo](https://www.kaust.edu.sa/en/study/faculty/paulo-verissimo)

- **照片**：[Paulo Esteves-Verissimo](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/KAUST-CEMSE-CS-RC3-Paulo-Esteves-Verissimo-N-Z-7-7346-edited-1080px-square.jpg)

- **研究方向**：Esteves-Veríssimo教授目前对弹性模块化和分布式计算的架构、中间件和算法感兴趣。人们越来越相信，弹性计算将成为未来实现计算机系统和网络安全可靠运行的主要范式，超越经典的网络安全技术。这归因于这一领域的几个内在特性，例如：对偶然和恶意故障/攻击的通用方法；针对多态威胁表面的渐进和自适应保护；弹性、可塑性和可持续性。

- **联系方式**：[paulo.verissimo@kaust.edu.sa](mailto:paulo.verissimo@kaust.edu.sa)


### 15. **SUHAIB FAHMY**

- **职位**：计算机科学副教授

- **个人主页**：[Suhaib Fahmy](https://www.kaust.edu.sa/en/study/faculty/suhaib-fahmy)

- **照片**：[Suhaib Fahmy](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/suhaibfahmy-448px-square.jpg)

- **研究方向**：Fahmy教授的研究兴趣集中在可重构计算和定制硬件加速器的设计，以提高计算密集型应用的性能和效率。他的研究已应用于多个领域，包括汽车系统、网络安全、无线通信和机器学习。

- **联系方式**：[suhaib.fahmy@kaust.edu.sa](mailto:suhaib.fahmy@kaust.edu.sa)


### 16. **ERIC FERON**

- **职位**：电气与计算机工程教授

- **个人主页**：[Eric Feron](https://www.kaust.edu.sa/en/study/faculty/eric-feron)

- **照片**：[Eric Feron](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/Eric-Feron2.png)

- **研究方向**：Feron教授的研究兴趣集中在利用控制系统、优化和计算机科学的基本概念来解决现代航空航天工程的关键问题。更具体地说，无人驾驶飞行器的特技控制、多智能体操作（包括空中交通管制系统）以及航空航天软件系统的认证。

- **联系方式**：[eric.feron@kaust.edu.sa](mailto:eric.feron@kaust.edu.sa)


### 17. **MAURIZIO FILIPPONE**

- **职位**：统计学副教授

- **个人主页**：[Maurizio Filippone](https://www.kaust.edu.sa/en/study/faculty/maurizio-filippone)

- **照片**：[Maurizio Filippone](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty/maurizio-filippone-v2.jpg)

- **研究方向**：Filippone教授的当前研究兴趣包括开发高斯过程和深度学习模型的可处理且可扩展的贝叶斯推断技术，应用于生命和环境科学。

- **联系方式**：[maurizio.filippone@kaust.edu.sa](mailto:maurizio.filippone@kaust.edu.sa)


### 18. **ANDREA FRATALOCCHI**

- **职位**：电气与计算机工程教授

- **个人主页**：[Andrea Fratalocchi](https://www.kaust.edu.sa/en/study/faculty/andrea-fratalocchi)

- **照片**：[Andrea Fratalocchi](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/bio-fratalocci.jpg)

- **研究方向**：Fratalocchi教授的研究兴趣集中在利用无序作为新技术的基石，从自然系统的千年进化中受益。他的愿景是揭开随机性的隐藏秘密，以揭示新的基本过程和一类新的电磁材料，这些材料可以以最低的成本大规模组装。他的研究应用包括但不限于：革命性的能量收集过程、一类可以大规模组装并实现超薄层功能操作的纳米结构、利用纳米尺度的破坏性自然现象实现光子的非常规功能、新型复杂成像装置的研究、新型“智能”激光器的开发。

- **联系方式**：[andrea.fratalocchi@kaust.edu.sa](mailto:andrea.fratalocchi@kaust.edu.sa)


### 19. **XIN GAO**

- **职位**：计算机科学教授，智能健康卓越中心联合主席

- **个人主页**：[Xin Gao](https://www.kaust.edu.sa/en/study/faculty/xin-gao)

- **照片**：[Xin Gao](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/xin-gao-400x400.jpeg)

- **研究方向**：Gao的研究位于计算机科学与生物学的交叉点。他的工作有两个主要焦点：1）在机器学习和算法领域开发理论和方法；2）通过构建计算模型、开发机器学习技术以及设计有效和高效的算法来解决生物学和医学领域的关键开放问题。特别是，他致力于解决从蛋白质氨基酸序列到其三维结构和功能的问题，这些功能最终导致其在复杂生物网络中的不良表达。

- **联系方式**：[xin.gao@kaust.edu.sa](mailto:xin.gao@kaust.edu.sa)


### 20. **MARC G. GENTON**

- **职位**：统计学阿尔·花拉子米杰出教授

- **个人主页**：[Marc G. Genton](https://www.kaust.edu.sa/en/study/faculty/marc-genton)

- **照片**：[Marc G. Genton](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/bio-genton.jpg)

- **研究方向**：Genton教授的主要研究兴趣涉及时空数据的统计分析、可视化、建模、预测和不确定性量化，应用于环境和气候科学、可再生能源（如风能和太阳能）、地球物理学和海洋科学。他的研究活动还包括偏斜多变量非高斯分布和稳健统计。

- **联系方式**：[marc.genton@kaust.edu.sa](mailto:marc.genton@kaust.edu.sa)


### 21. **BERNARD GHANEM**

- **职位**：电气与计算机工程教授，生成式AI卓越中心主席

- **个人主页**：[Bernard Ghanem](https://www.kaust.edu.sa/en/study/faculty/bernard-ghanem)

- **照片**：[Bernard Ghanem](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty/bernard-v4.png)

- **研究方向**：Ghanem教授的研究兴趣集中在计算机视觉、机器学习和图像处理领域。包括：建模视频序列中的动态对象以改善运动分割、视频压缩、视频配准、运动估计和活动识别；为大规模计算机视觉和机器学习问题开发高效的优化和随机化技术；探索新的方法，通过人类判断来开发更有效和更具感知相关的识别和压缩技术；通过利用数据的稀疏性和低秩性，开发联合表示和分类的框架。

- **联系方式**：[bernard.ghanem@kaust.edu.sa](mailto:bernard.ghanem@kaust.edu.sa)


### 22. **ALEXANDRA A. GOMES**

- **职位**：教学教授

- **个人主页**：[Alexandra A. Gomes](https://www.kaust.edu.sa/en/study/faculty/alexandra-a-gomes)

- **照片**：[Alexandra A. Gomes](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/Alexandraa.png)

- **研究方向**：Alexandra A. Gomes和Afzal Suleman，2011年，《变形机翼的气动结构设计优化》，《智能材料系统与结构》杂志，第22卷（10），1113-1124。[链接](https://doi.org/10.1177/1045389X11417652)。Alexandra A. Gomes和Afzal Suleman，2008年，《增强滚转机动的加强翼盒的拓扑优化》，《AIAA杂志》，第46卷（3），548-556。[链接](https://doi.org/10.2514/1.23028)。Alexandra A. Gomes和Afzal Suleman，2006年，《光谱水平集方法在拓扑优化中的应用》，《结构与多学科优化》，第31卷（6），430–443。[链接](https://doi.org/10.1007/s00158-006-0005-2)。Victor M. Franco Correia、Maria A. Aguiar Gomes、Afzal Suleman、Cristóvão M. Mota Soares和Carlos A. Mota Soares，2000年，《自适应复合结构的建模与设计》，《计算机方法在应用力学与工程中的应用》，第185卷，325-346。[链接](https://doi.org/10.1016/S0045-7825\(99\)00265-0)。

- **联系方式**：[alexandra.gomes@kaust.edu.sa](mailto:alexandra.gomes@kaust.edu.sa)


### 23. **DIOGO GOMES**

- **职位**：应用数学与计算科学教授

- **个人主页**：[Diogo Gomes](https://www.kaust.edu.sa/en/study/faculty/diogo-gomes)

- **照片**：[Diogo Gomes](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/bio-gomes.jpg)

- **研究方向**：Gomes教授的研究兴趣在于偏微分方程（PDE），特别是椭圆、抛物和哈密顿-雅可比方程的粘性解，以及相关的平均场模型。这一领域包括从经典线性方程到高度非线性PDE的大量方程和示例，包括Monge-Ampere方程、图像处理的几何方程、非线性弹性方程和多孔介质方程。他的研究直接或间接地受到具体应用的启发。这些应用包括人口和人群建模、价格形成和扩展的平均场模型、无限维PDE的数值分析以及计算机视觉。

- **联系方式**：[diogo.gomes@kaust.edu.sa](mailto:diogo.gomes@kaust.edu.sa)


### 24. **MARKUS HADWIGER**

- **职位**：计算机科学教授

- **个人主页**：[Markus Hadwiger](https://www.kaust.edu.sa/en/study/faculty/markus-hadwiger)

- **照片**：[Markus Hadwiger](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/markus-hadwiger.png)

- **研究方向**：Hadwiger教授的研究重点包括：科学可视化、千万亿级可视化和科学计算、体可视化、医学可视化、交互式分割和图像处理、基于GPU的算法、GPU上的通用计算。

- **联系方式**：[markus.hadwiger@kaust.edu.sa](mailto:markus.hadwiger@kaust.edu.sa)


### 25. **ALI HASSAN**

- **职位**：教学教授

- **个人主页**：[Ali Hassan](https://www.kaust.edu.sa/en/study/faculty/ali-hassan)

- **照片**：[Ali Hassan](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/Ali-Hassan.png)

- **研究方向**：Ali教授的研究兴趣在于恶意软件分析和漏洞研究，特别关注利用大语言模型（LLMs）进行恶意样本的逆向工程和二进制利用。

- **联系方式**：[ali.hassan.1@kaust.edu.sa](mailto:ali.hassan.1@kaust.edu.sa)


### 26. **WOLFGANG HEIDRICH**

- **职位**：计算机科学教授

- **个人主页**：[Wolfgang Heidrich](https://www.kaust.edu.sa/en/study/faculty/wolfgang-heidrich)

- **照片**：[Wolfgang Heidrich](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/bio-heidrich.jpg)

- **研究方向**：Heidrich教授的核心研究兴趣在于计算摄影和显示，这是视觉计算领域的一个新兴研究方向，结合了计算机图形学、机器视觉、成像、逆方法、光学和感知的方法，以开发新的传感和显示技术。计算摄影旨在开发新的相机和成像模式，以光学方式编码关于真实世界的信息，使其能够被图像传感器捕获。生成的图像代表了详细的信息，例如场景几何、固体和液体的运动、多光谱信息或高对比度（高动态范围），然后可以使用逆方法、机器学习和数值优化进行计算解码。计算显示采用类似的方法，但方向相反。这里的目标是计算编码目标图像，然后由显示硬件光学解码以呈现给人类观察者。计算显示能够生成无眼镜3D显示、高动态范围图像或具有空间和/或时间超分辨率的图像和视频。

- **联系方式**：[wolfgang.heidrich@kaust.edu.sa](mailto:wolfgang.heidrich@kaust.edu.sa)


### 27. **ROBERT HOEHNDOFF**

- **职位**：计算机科学副教授

- **个人主页**：[Robert Hoehndorf](https://www.kaust.edu.sa/en/study/faculty/robert-hoehndorf)

- **照片**：[Robert Hoehndorf](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/robert-hoehndorf--400x400.jpeg)

- **研究方向**：Hoehndorf教授对人工智能、知识表示、生物医学信息学和本体论感兴趣。

- **联系方式**：[robert.hoehndorf@kaust.edu.sa](mailto:robert.hoehndorf@kaust.edu.sa)


### 28. **RAPHÄL HUSER**

- **职位**：统计学副教授

- **个人主页**：[Raphaël Huser](https://www.kaust.edu.sa/en/study/faculty/raphael-huser)

- **照片**：[Raphaël Huser](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/bio-huser.png)

- **研究方向**：Huser教授的主要研究兴趣在于极端事件统计、风险评估、时空统计和大数据统计方法的交叉领域，特别关注环境应用，如极端洪水、干旱和阵风的预测。他开发了用于罕见事件的统计模型以及适合这些数据的高效推断方法。

- **联系方式**：[raphael.huser@kaust.edu.sa](mailto:raphael.huser@kaust.edu.sa)


### 29. **DAVID I. KETCHESON**

- **职位**：应用数学与计算科学教授

- **个人主页**：[David Ketcheson](https://www.kaust.edu.sa/en/study/faculty/david-ketcheson)

- **照片**：[David Ketcheson](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty/2025-David-Ketcheson.png)

- **研究方向**：Ketcheson教授的研究兴趣在于数值分析和双曲PDE。他的工作包括开发高效的时间积分方法、波传播算法以及在非均质介质中波现象的建模。

- **联系方式**：[david.ketcheson@kaust.edu.sa](mailto:david.ketcheson@kaust.edu.sa)


### 30. **DAVID E. KEYES**

- **职位**：应用数学与计算科学教授

- **个人主页**：[David Keyes](https://www.kaust.edu.sa/en/study/faculty/david-keyes)

- **照片**：[David Keyes](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/david-keyes-2021.png)

- **研究方向**：David Keyes是应用数学与计算科学教授，也是极端计算研究中心的主任。他在KAUST的数学与计算机科学与工程部担任了前3.5年的院长。他还是哥伦比亚大学的应用物理和应用数学的兼职教授，以及美国能源部几个实验室的成员。Keyes于1978年在普林斯顿大学获得航空航天和机械科学学士学位，并于1984年在哈佛大学获得应用数学博士学位。在加入KAUST的创始教员团队之前，他领导了美国能源部ASCI和SciDAC计划中的可扩展求解器软件项目。


Keyes致力于并行计算和偏微分方程数值分析之间的算法接口，重点是新兴架构上的隐式可扩展求解器及其在能源和环境中受守恒定律支配的大规模应用，这些应用由于高分辨率、高维度、高保真物理模型或优化、控制、敏感性分析、逆问题、数据同化或不确定性量化的要求而需要高性能。

他命名并贡献了用于PDEs的大规模稀疏线性和非线性系统的牛顿-克里洛夫-施瓦茨（NKS）、加性施瓦茨预条件不精确牛顿（ASPIN）和代数快速多极子（AFM）方法。通过ECRC，他现在致力于满足通信和同步大幅减少、共享内存的核心并发增加、本地负载重新分配以及这些和其他算法的基于算法的容错需求。

- **联系方式**：[david.keyes@kaust.edu.sa](mailto:david.keyes@kaust.edu.sa)


### 31. **NAEEMULLAH KHAN**

- **职位**：教学助理教授

- **个人主页**：[Naeemullah Khan](https://www.kaust.edu.sa/en/study/faculty/naeemullah-khan)

- **照片**：[Naeemullah Khan](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/Naeemullah-Khan.png)

- **研究方向**：Khan教授的研究兴趣包括深度神经网络的持续学习和鲁棒性，其中模型从持续的数据流中训练，目标是在学习新数据的同时不忘之前的知识，同时对有界输入扰动具有鲁棒性。

- **联系方式**：[naeemullah.khan@kaust.edu.sa](mailto:naeemullah.khan@kaust.edu.sa)


### 32. **OMAR KNIO**

- **职位**：应用数学与计算科学教授

- **个人主页**：[Omar Knio](https://www.kaust.edu.sa/en/study/faculty/omar-knio)

- **照片**：[Omar Knio](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/omar-knio-400x400.jpeg)

- **研究方向**：Knio教授的研究兴趣包括不确定性量化、贝叶斯推断、计算流体力学、燃烧、海洋和大气流动、湍流、物理声学、高能材料、微流体设备、动力系统、渐近技术、多分辨率方法、高性能计算、优化和数据驱动的预测科学。

- **联系方式**：[omar.knio@kaust.edu.sa](mailto:omar.knio@kaust.edu.sa)


### 33. **CHARALAMBOS KONSTANTINOU**

- **职位**：电气与计算机工程副教授

- **个人主页**：[Charalambos Konstantinou](https://www.kaust.edu.sa/en/study/faculty/charalambos-konstantinou)

- **照片**：[Charalambos Konstantinou](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/Harrys.png)

- **研究方向**：Konstantinou教授的研究兴趣在于安全、可信赖和弹性的网络物理系统和嵌入式物联网系统。他还对关键基础设施的安全和弹性特别感兴趣，重点关注智能电网技术、可再生能源集成和实时仿真。

- **联系方式**：[charalambos.konstantinou@kaust.edu.sa](mailto:charalambos.konstantinou@kaust.edu.sa)


### 34. **ROLF KRAUSE**

- **职位**：应用数学与计算科学教授

- **个人主页**：[Rolf Krause](https://www.kaust.edu.sa/en/study/faculty/rolf-krause)

- **照片**：[Rolf Krause](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/rolf-krause.png)

- **研究方向**：应用数学、计算力学、力学中的接触问题、科学软件、多级和区域分解方法、优化、大规模系统的迭代求解、并行计算、高性能计算（HPC）、耦合问题、有限元、非线性求解方法、神经网络、物理信息神经网络、心脏模拟、生物力学和计算地球科学。

- **联系方式**：[rolf.krause@kaust.edu.sa](mailto:rolf.krause@kaust.edu.sa)


### 35. **TAOUS-MERIEM LALEG-KIRATI**

- **职位**：电气与计算机工程兼职副教授

- **个人主页**：[Taous-Meriem Laleg-Kirati](https://www.kaust.edu.sa/en/study/faculty/taous-kirati)

- **照片**：[Taous-Meriem Laleg-Kirati](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/bio-kirati.jpg)

- **研究方向**：Laleg-Kirati教授的研究兴趣涵盖应用数学、控制系统和信号分析领域的研究。她致力于基于半经典方法的新信号分析方法，应用于动脉血压分析。Laleg-Kirati还对建模、识别、控制、故障检测、逆问题特别是地震反演以及孤子波和散射理论方面有研究。

- **联系方式**：[taousmeriem.laleg@kaust.edu.sa](mailto:taousmeriem.laleg@kaust.edu.sa)


### 36. **XIAOHANG LI**

- **职位**：电气与计算机工程副教授

- **个人主页**：[Xiaohang Li](https://www.kaust.edu.sa/en/study/faculty/xiaohang-li)

- **照片**：[Xiaohang Li](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/xiaohang-li-2021.png)

- **研究方向**：李教授对超宽带和宽带半导体（包括GaN、AlN、Ga2O3、In2O3）感兴趣。他专注于下一代器件和集成电路的生长、仿真、制造和表征，包括LED、激光器、高功率和高频率晶体管和二极管以及堆叠晶体管集成电路。李教授的研究成果在IEEE、SPIE、美国晶体生长协会和爱迪生创新基金会等领先组织和会议中得到了广泛认可和奖励。


这些器件有望成为革命性技术，推动能源、通信、健康、传感等领域的可持续发展。李教授的研究活动高度跨学科，涉及电气工程、应用物理、材料科学等相关学科的学生和研究人员。他们得到了最先进的设施支持，包括但不限于：MOCVD、PLD、ALD、光刻、电子束光刻、PL、TEM、XRD、拉曼、XPS、SIMS、RBS、实验室和KAUST的超级计算机。

- **联系方式**：[xiaohang.li@kaust.edu.sa](mailto:xiaohang.li@kaust.edu.sa)


### 37. **PETER MARKOWICH**

- **职位**：应用数学与计算科学阿尔·花拉子米杰出教授

- **个人主页**：[Peter Markowich](https://www.kaust.edu.sa/en/study/faculty/peter-markowich)

- **照片**：[Peter Markowich](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/bio-markowich.jpg)

- **研究方向**：Markowich教授的主要研究兴趣在于偏微分方程（PDE）的数学和数值分析及其在物理学、生物学和工程学中的应用。特别是，他对以下领域感兴趣：经典和量子力学动力学理论、高度振荡PDE（如半经典渐近）中的分析和数值问题、Wigner变换、描述色散和/或扩散现象的非线性PDE、奇异摄动和长时间渐近、广义Sobolev不等式、固态物理中的逆问题、使用PDE的图像处理。

- **联系方式**：[peter.markowich@kaust.edu.sa](mailto:peter.markowich@kaust.edu.sa)


### 38. **DOMINIK L. MICHELS**

- **职位**：计算机科学副教授

- **个人主页**：[Dominik Michels](https://www.kaust.edu.sa/en/study/faculty/dominik-michels)

- **照片**：[Dominik Michels](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/dominik.jpg)

- **研究方向**：Michels教授的研究目标是实现科学和视觉计算的准确高效模拟。为此，他基于坚实的理论基础开发新的计算方法，并贡献了涵盖算法、人工智能和机器学习、计算机图形学和基于物理的建模、微分方程、数学建模和数值分析的广泛主题。

- **联系方式**：[dominik.michels@kaust.edu.sa](mailto:dominik.michels@kaust.edu.sa)


### 39. **PAULA MORAGA**

- **职位**：统计学副教授

- **个人主页**：[Paula Moraga](https://www.kaust.edu.sa/en/study/faculty/paula-moraga)

- **照片**：[Paula Moraga](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/Paula_Moraga.png)

- **研究方向**：Moraga教授的研究重点是开发用于地理空间数据分析和健康监测的创新统计方法和计算工具，包括理解疾病地理和时间模式的方法、评估其与潜在风险因素的关系、检测聚集以及评估干预措施的影响。她还对开发统计软件感兴趣，包括R包和用于可重复研究和沟通的交互式可视化应用程序。Moraga教授的工作直接为减少疟疾和癌症等疾病负担的战略政策提供了信息。

- **联系方式**：[paula.moraga@kaust.edu.sa](mailto:paula.moraga@kaust.edu.sa)


### 40. **MIKHAIL MOSHKOV**

- **职位**：应用数学与计算科学教授

- **个人主页**：[Mikhail Moshkov](https://www.kaust.edu.sa/en/study/faculty/mikhail-moshkov)

- **照片**：[Mikhail Moshkov](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/bio-moshkov.jpg)

- **研究方向**：Moshkov教授发表了140多篇论文，他的研究兴趣包括：研究决策树、决策规则系统和无环程序等计算模型中算法的时间复杂度，应用于组合优化、故障诊断、模式识别、机器学习、数据挖掘和贝叶斯网络分析。基于决策树、约简、决策规则系统、抑制规则系统和懒学习算法的分类器分析与设计。动态规划在不同成本函数的顺序优化中的扩展，以及研究两个成本函数之间的关系，应用于组合优化和数据挖掘。

- **联系方式**：[mikhail.moshkov@kaust.edu.sa](mailto:mikhail.moshkov@kaust.edu.sa)


### 41. **KAZUHIRO OHKAWA**

- **职位**：电气与计算机工程教授

- **个人主页**：[Kazuhiro Ohkawa](https://www.kaust.edu.sa/en/study/faculty/kazuhiro-ohkawa)

- **照片**：[Kazuhiro Ohkawa](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/kazuhiro-ohkawa-400x400.jpeg)

- **研究方向**：Ohkawa教授的研究兴趣包括面向更可持续未来的能源转换现象的科学和器件应用。有前途的应用包括固态照明和人工光合作用。Ohkawa将MOVPE技术改进到可以专门设计InGaN的程度，这是制造高效黄色、琥珀色和红色LED的关键组件。InGaN对环境无害，将取代砷化物和磷化物在器件领域的地位。他还尝试利用他发明的氮化物光催化剂从光能中产生清洁化学能。这被称为人工光合作用，不仅可以从H2O还原中产生H2，还可以从CO2还原中产生HCOOH、CH4和C2H5OH。氮化物光合作用的效率已经高于生物光合作用的平均水平。

- **联系方式**：[Kazuhiro.ohkawa@kaust.edu.sa](mailto:Kazuhiro.ohkawa@kaust.edu.sa)


### 42. **HERNANDO OMBAO**

- **职位**：统计学教授

- **个人主页**：[Hernando Ombao](https://www.kaust.edu.sa/en/study/faculty/hernando-ombao)

- **照片**：[Hernando Ombao](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/ombao.jpg)

- **研究方向**：Ombao教授的研究兴趣在于时间序列数据的统计建模和高维信号与图像的可视化。他开发了一套用于复杂脑信号依赖性建模和推断的方法；测试患者群体之间网络的差异；基于网络的生物标志物识别和疾病分类；以及建模不同领域（例如遗传学、脑功能和行为）高维数据之间的关联。

- **联系方式**：[hernando.ombao@kaust.edu.sa](mailto:hernando.ombao@kaust.edu.sa)


### 43. **BOON S. OOI**

- **职位**：电气与计算机工程教授

- **个人主页**：[Boon S. Ooi](https://www.kaust.edu.sa/en/study/faculty/boon-ooi)

- **照片**：[Boon S. Ooi](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/bio-ooi.jpg)

- **研究方向**：Ooi教授的研究主要涉及半导体激光器和光子集成电路的研究。具体来说，他对半导体光子集成电路的实用技术开发以及新型宽带半导体激光器、多波长激光器和超辐射二极管的开发做出了重要贡献。最近，他将研究重点放在GaN基纳米结构和激光器上，用于固态照明和可见光通信等领域。

- **联系方式**：[boon.ooi@kaust.edu.sa](mailto:boon.ooi@kaust.edu.sa)


### 44. **FRANCESCO ORABONA**

- **职位**：计算机科学副教授

- **个人主页**：[Francesco Orabona](https://www.kaust.edu.sa/en/study/faculty/francesco-orabona)

- **照片**：[Francesco Orabona](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/francesco-orabona.jpg)

- **研究方向**：Orabona教授的研究位于实际和理论机器学习的交叉点。他的研究兴趣包括在线学习、优化和统计学习理论。他目前的研究重点是设计“无参数”机器学习算法，这些算法无需昂贵的参数调整即可有效运行。

- **联系方式**：[francesco.orabona@kaust.edu.sa](mailto:francesco.orabona@kaust.edu.sa)


### 45. **JOAQUIN ORTEGA**

- **职位**：教学教授

- **个人主页**：[Joaquin Ortega](https://www.kaust.edu.sa/en/study/faculty/joaquin-ortega)

- **照片**：[Joaquin Ortega](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/Official_Photo.png)

- **研究方向**：Euán, C., Ombao, H. & Ortega, J. 脑信号的频谱同步性。《统计学在医学中的应用》，37, 2855-2873, 2018, doi: [https://doi.org/10.1002/sim.7695](https://doi.org/10.1002/sim.7695)。Rivera-García, D., García-Escudero, L.A., Mayo-Iscar, A. & Ortega, J. 时间序列、频谱密度和稳健函数聚类。《神经处理快报》，2018 [https://doi.org/10.1007/s11063-018-9926-1](https://doi.org/10.1007/s11063-018-9926-1)。

- **联系方式**：[joaquin.ortegasanchez@kaust.edu.sa](mailto:joaquin.ortegasanchez@kaust.edu.sa)


### 46. **SHINKYU PARK**

- **职位**：电气与计算机工程副教授

- **个人主页**：[Shinkyu Park](https://www.kaust.edu.sa/en/study/faculty/shinkyu-park)

- **照片**：[Shinkyu Park](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/71626851_park_headshot_small_02.jpg)

- **研究方向**：Park教授的研究兴趣在于机器人学、多智能体决策和反馈控制的一般领域。他最近的研究集中在多机器人系统的设计和控制以及博弈论和反馈控制系统相关主题，应用于多机器人学习和协调。

- **联系方式**：[shinkyu.park@kaust.edu.sa](mailto:shinkyu.park@kaust.edu.sa)


### 47. **MATTEO PARSANI**

- **职位**：应用数学与计算科学副教授

- **个人主页**：[Matteo Parsani](https://www.kaust.edu.sa/en/study/faculty/matteo-parsani)

- **照片**：[Matteo Parsani](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/bio-parsani.jpg)

- **研究方向**：Matteo Parsani教授的研究兴趣与在非结构化网格上设计和实现新型、稳健且可扩展的数值方法有关，这些方法用于双曲和混合双曲/抛物偏微分方程，以及其在自然科学和工程各个领域的实际流动问题求解中的应用。为此，他结合数值分析、物理学和高性能计算，开发具有更好数学和数值属性的稳健空间和时间离散化方法，以考虑被建模的物理现象和现代计算架构。目前推动他研究的应用领域包括计算空气动力学和气体动力学、密集气体流动模拟和计算气动声学。Parsani教授在KAUST的研究兴趣将集中在设计和实现非线性稳定、高阶自适应数值方法，用于解决工业上迄今为止难以处理的多尺度流动问题（例如，使用LES和DNS的高分离湍流流动；以及不同流动 regime 下的超临界流体），在数十万核心和新兴的异构数据密集型计算硬件（CPU + GPU）上。

- **联系方式**：[matteo.parsani@kaust.edu.sa](mailto:matteo.parsani@kaust.edu.sa)


### 48. **HELMUT POTTMANN**

- **职位**：应用数学与计算科学兼职教授

- **个人主页**：[Helmut Pottmann](https://www.kaust.edu.sa/en/study/faculty/helmut-pottmann)

- **照片**：[Helmut Pottmann](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/helmut-pottmann-400x400.jpeg)

- **研究方向**：Pottmann教授的研究兴趣在于应用几何、经典几何、离散微分几何、计算设计和几何处理，重点关注建筑和制造领域的应用。

- **联系方式**：[helmut.pottmann@kaust.edu.sa](mailto:helmut.pottmann@kaust.edu.sa)


### 49. **PETER RICHTARIK**

- **职位**：计算机科学教授

- **个人主页**：[Peter Richtarik](https://www.kaust.edu.sa/en/study/faculty/peter-richtarik)

- **照片**：[Peter Richtarik](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/PETER-RICHTARIK.jpg)

- **研究方向**：Richtarik教授的研究兴趣位于数学、计算机科学、机器学习、优化、数值线性代数、高性能计算和应用概率的交叉点。他对开发用于描述大数据的凸和非凸优化问题的零阶、一阶和二阶算法特别感兴趣，特别关注随机、并行和分布式方法。他是联邦学习的共同发明者，这是谷歌用于移动设备机器学习的平台，保护用户数据的隐私。

- **联系方式**：[peter.richtarik@kaust.edu.sa](mailto:peter.richtarik@kaust.edu.sa)


### 50. **HÅVARD RUE**

- **职位**：统计学教授

- **个人主页**：[Håvard Rue](https://www.kaust.edu.sa/en/study/faculty/haavard-rue)

- **照片**：[Håvard Rue](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/haavard-rue-400x400.jpeg)

- **研究方向**：Rue教授的研究兴趣在于计算贝叶斯统计和贝叶斯方法，如先验、敏感性和稳健性。他的主要研究围绕R-INLA项目（[www.r-inla.org）展开，该项目旨在提供一个实用的工具，用于潜在高斯模型的近似贝叶斯分析，通常在极端数据规模下。该项目还包括使用随机偏微分方程表示高斯场，用于空间统计学。](http://www.r-inla.xn--org\),,,-9t3kid8n21bx0df9aqzpn9bz8mdtogae98qxz4b4sdbvlg3bnwi6o0bejcj1r8wbda56osyzboam43ema2039bx26bda286kka044b3u9c7j8jgtta1rmpj4ai2ces0mkkya.xn--,-4v6az3a1xz6dw0br7ng2iy3jcnil7hod30un82dia563e4zkqxdpsc482bny9b22odnbk45cx38azjd2urbgq./)

- **联系方式**：[haavard.rue@kaust.edu.sa](mailto:haavard.rue@kaust.edu.sa)


### 51. **KHALED NABIL SALAMA**

- **职位**：电气与计算机工程教授

- **个人主页**：[Khaled Nabil Salama](https://www.kaust.edu.sa/en/study/faculty/khaled-nabil-salama)

- **照片**：[Khaled Nabil Salama](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/Salama1.png)

- **研究方向**：Salama教授的研究兴趣涵盖电子电路设计和半导体制造的多个跨学科领域。他致力于开发器件、电路、系统和算法，以实现各种工业、环境和生物医学应用的低成本分析平台。最近，他一直在研究用于大脑仿真的神经形态电路。

- **联系方式**：[khaled.salama@kaust.edu.sa](mailto:khaled.salama@kaust.edu.sa)


### 52. **JÜRGEN SCHMIDHUBER**

- **职位**：计算机科学教授，生成式AI卓越中心联合主席

- **个人主页**：[Jürgen Schmidhuber](https://www.kaust.edu.sa/en/study/faculty/juergen-schmidhuber)

- **照片**：[Jürgen Schmidhuber](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/jurgen-schmidhuber-400x400.jpeg)

- **研究方向**：Jürgen Schmidhuber是阿卜杜拉国王科技大学（KAUST）计算机、电气和数学科学与工程部（CEMSE）计算机科学项目的AI倡议主任和教授。Schmidhuber教授是一位著名的计算机科学家，以其在人工智能（AI）、深度学习和人工神经网络领域的开创性工作而闻名。


在加入KAUST之前，Schmidhuber教授于2009年至2021年在卢加诺大学（USI）担任人工智能教授（Ordinarius）。

Schmidhuber教授将领导并与几位对AI研究感兴趣的现任教员合作，规划AI倡议的研究重点，招聘新教员，开发教育项目和创业活动，并与沙特阿拉伯和全球的关键公共和私营部门组织合作。

在KAUST的出色硬件和多学科专业知识的支持下（参见KAUST Discovery Magazines），AI倡议将专注于所有领域的AI应用，包括医疗保健、药物设计、化学、材料科学、语音识别和自然语言处理、自动化、机器人、软机器人等。KAUST的AI倡议已经拥有一支杰出的可视化计算团队，该团队在计算机视觉（例如计算机视觉与模式识别会议）、计算机图形学（例如SIGGRAPH）等领域的顶级会议中始终名列前茅。

- **联系方式**：[juergen.schmidhuber@kaust.edu.sa](mailto:juergen.schmidhuber@kaust.edu.sa)


### 53. **GIANLUCA SETTI**

- **职位**：电气与计算机工程教授

- **个人主页**：[Gianluca Setti](https://www.kaust.edu.sa/en/study/faculty/gianluca-setti)

- **照片**：[Gianluca Setti](https://www.kaust.edu.sa/PublishingImages/about/Adminstration/Gianluca-Setti.png?renditionId=19)

- **研究方向**：Gianluca教授的研究兴趣包括非线性电路、统计信号处理、电磁兼容性、压缩感知、生物医学电路和系统、电力电子、物联网（IoT）节点的设计与实现以及用于异常检测和预测性维护的机器学习技术。

- **联系方式**：[gianluca.setti@kaust.edu.sa](mailto:gianluca.setti@kaust.edu.sa)


### 54. **ATIF SHAMIM**

- **职位**：电气与计算机工程教授，电气与计算机工程项目主席

- **个人主页**：[Atif Shamim](https://www.kaust.edu.sa/en/study/faculty/atif-shamim)

- **照片**：[Atif Shamim](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/bio-shamim.jpg)

- **研究方向**：Shamim教授的研究重点是个人区域网络、汽车雷达、可穿戴和植入式无线传感器、无线供电和可再生能源。以下具体研究项目正在进行中：CMOS RF SoC设计（带片上天线的RFIC）、天线设计、集成和小型化技术、3D IC封装以及LTCC、LCP和IPD环境中的嵌入式无源器件，用于SoP应用、基于铁氧体LTCC的可调谐和可重构电路、基于碳的纳米无线电设计（碳纳米管和石墨烯介质）、柔性RF电子设备（在纸、塑料等上的喷墨打印）、通过环境资源（红外、电磁）进行能量收集、可穿戴和一次性无线传感器。

- **联系方式**：[atif.shamim@kaust.edu.sa](mailto:atif.shamim@kaust.edu.sa)


### 55. **BASEM SHIHADA**

- **职位**：计算机科学教授

- **个人主页**：[Basem Shihada](https://www.kaust.edu.sa/en/study/faculty/basem-shihada)

- **照片**：[Basem Shihada](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/bio-shihada.jpg)

- **研究方向**：Shihada教授的研究涵盖了有线和无线通信网络的广泛主题，包括无线网状网络、无线传感器网络、多媒体网络和光网络。他还对网络安全和云计算感兴趣。

- **联系方式**：[basem.shihada@kaust.edu.sa](mailto:basem.shihada@kaust.edu.sa)


### 56. **MALEK SMAOUI**

- **职位**：教学副教授

- **个人主页**：[Malek Smaoui](https://www.kaust.edu.sa/en/study/faculty/malek-smaoui)

- **照片**：[Malek Smaoui](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/Malek1.png)

- **联系方式**：[malek.smaoui@kaust.edu.sa](mailto:malek.smaoui@kaust.edu.sa)


### 57. **AHMED K. SULTAN SALEM**

- **职位**：教学教授

- **个人主页**：[Ahmed K. Sultan Salem](https://www.kaust.edu.sa/en/study/faculty/ahmed-k-sultan-salem)

- **照片**：[Ahmed K. Sultan Salem](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/ahmed_salem.jpg)

- **研究方向**：能源收集、认知无线电技术、动态频谱接入、合作通信、分布式和顺序检测、基于物理层的保密性、用于光通信的OFDM、遥感和合成孔径雷达（SAR）。

- **联系方式**：[ahmed.salem@kaust.edu.sa](mailto:ahmed.salem@kaust.edu.sa)


### 58. **YING SUN**

- **职位**：统计学副教授

- **个人主页**：[Ying Sun](https://www.kaust.edu.sa/en/study/faculty/ying-sun)

- **照片**：[Ying Sun](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/bio-yingsun.jpg)

- **研究方向**：Ying Sun是计算机、电气和数学科学与工程部（CEMSE）的统计学副教授。她在俄亥俄州立大学统计系担任助理教授一年后加入了KAUST。


在加入俄亥俄州立大学之前，她曾是芝加哥大学统计方法在大气和海洋科学中的应用研究网络（STATMOS）的博士后研究员，以及统计和应用数学科学研究所（SAMSI）不确定性量化项目的博士后研究员。

她的研究兴趣包括具有环境应用的时空统计、大数据的计算方法、不确定性量化和可视化、函数数据分析、稳健统计和极端值统计。

- **联系方式**：[ying.sun@kaust.edu.sa](mailto:ying.sun@kaust.edu.sa)


### 59. **RAUL F. TEMPONE**

- **职位**：应用数学与计算科学教授

- **个人主页**：[Raul Tempone](https://www.kaust.edu.sa/en/study/faculty/raul-tempone)

- **照片**：[Raul Tempone](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/Photo-_R._Tempone.jpg)

- **研究方向**：Tempone教授的研究兴趣在于计算科学与工程的数学基础。更具体地说，他专注于各种微分方程（包括常微分方程、偏微分方程和随机微分方程）数值解的后验误差估计和相关自适应算法。


他还对最优控制、不确定性量化和贝叶斯模型校准、验证和最优实验设计的高效数值方法的开发和分析感兴趣。他考虑的应用领域包括工程、化学、生物学、物理学以及社会科学和计算金融。

- **联系方式**：[raul.tempone@kaust.edu.sa](mailto:raul.tempone@kaust.edu.sa)


### 60. **ATHANASIOS TZAVARAS**

- **职位**：应用数学与计算科学教授

- **个人主页**：[Athanassios Tzavaras](https://www.kaust.edu.sa/en/study/faculty/athanasios-tzavaras)

- **照片**：[Athanassios Tzavaras](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/bio-tzavaras.jpg)

- **研究方向**：Tzavaras教授的研究兴趣包括流体和材料的数学建模、分析和计算。他还对双曲守恒律和流体力学和弹性方程的结构感兴趣。


其他兴趣包括固体力学中的奇异性形成（如空穴化和剪切带）、多尺度分析、流体动力学极限以及流体的有效性质，以及稀聚合物系统的动力学模型和离散晶格系统的动力学。

- **联系方式**：[athanasios.tzavaras@kaust.edu.sa](mailto:athanasios.tzavaras@kaust.edu.sa)


### 61. **MIGUEL URBANO**

- **职位**：应用数学与计算科学教授

- **个人主页**：[Miguel Urbano](https://www.kaust.edu.sa/en/study/faculty/miguel-urbano)

- **照片**：[Miguel Urbano](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/miguel-urbano-400x400.jpeg)

- **研究方向**：Urbano教授的研究兴趣在于非线性偏微分方程的正则性理论，特别是奇异或退化类型，源于不同的应用，如相变、多孔介质中的流动或半监督学习。他还对自由边界问题感兴趣，重点是理解弱解的局部行为和界面的几何性质。

- **联系方式**：[miguel.urbano@kaust.edu.sa](mailto:miguel.urbano@kaust.edu.sa)


### 62. **IVAN VIOLA**

- **职位**：计算机科学教授

- **个人主页**：[Ivan Viola](https://www.kaust.edu.sa/en/study/faculty/ivan-viola)

- **照片**：[Ivan Viola](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/ivan.png)

- **研究方向**：Viola教授的研究兴趣在于可扩展技术，用于交互式分子可视化，最终目标是构建、可视化和建模整个复杂生物细胞的原子细节。这项技术将使人们能够交互、探索、研究和理解纳米尺度的生命。

- **联系方式**：[ivan.viola@kaust.edu.sa](mailto:ivan.viola@kaust.edu.sa)


### 63. **YATING WAN**

- **职位**：电气与计算机工程副教授

- **个人主页**：[Yating Wan](https://www.kaust.edu.sa/en/study/faculty/yating-wan)

- **照片**：[Yating Wan](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/yw1.png)

- **研究方向**：Yating Wan博士是KAUST的副教授，专长于硅光子学，重点是芯片上光源的集成。她于2017年在香港科技大学（HKUST）获得博士学位（导师为Kei May Lau）。2016年至2022年，她在加州大学圣巴巴拉分校（UCSB）工作（导师为John Bowers），领导英特尔关于异质集成量子点激光器的项目，为与硅CMOS兼容的光源做出了重要贡献。Wan博士发表了100多篇经过同行评审的出版物，包括29篇第一作者期刊论文（10篇为封面论文）、7篇通讯作者期刊论文和20多次国际会议邀请报告。她的研究被引用超过3500次，h指数为33。她的研究获得了多项荣誉，包括香港科技大学博士研究卓越奖（2017）、PIERS青年科学家奖（2018）、CLEO Tingye Li创新奖（2021）、Light: Science & Applications的Rising Stars of Light（2022）、MIT Technology Review的“中国35岁以下35位创新者”（2023）、Optica Ambassador（2024）和索尼与自然的女性科技奖（2025）。她是《应用光学》、《IEEE光电子学杂志》的副主编，《IEEE光电子学快报》的客座副主编，IPC和CLEO的TPC成员，以及IEEE光子学会（IPS）会议委员会的成员。

- **联系方式**：[yating.wan@kaust.edu.sa](mailto:yating.wan@kaust.edu.sa)


### 64. **DI WANG**

- **职位**：计算机科学副教授

- **个人主页**：[Di Wang](https://www.kaust.edu.sa/en/study/faculty/di-wang)

- **照片**：[Di Wang](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/di-wang-380x380.png?sfvrsn=72a718c0_1)

- **研究方向**：Di Wang教授的研究兴趣包括差分隐私、隐私保护机器学习、隐私保护数据挖掘、机器学习中的隐私攻击、可信赖机器学习和统计学习理论。他还对数字医疗、生物医学成像和生物信息学中的可信赖问题感兴趣。

- **联系方式**：[di.wang@kaust.edu.sa](mailto:di.wang@kaust.edu.sa)


### 65. **JIAN WENG**

- **职位**：计算机科学副教授

- **个人主页**：[Jian Weng](https://www.kaust.edu.sa/en/study/faculty/jian-weng)

- **照片**：[Jian Weng](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/jian-weng.png)

- **研究方向**：Jian Weng的研究兴趣涉及硬件/软件协同设计加速的所有内容，包括但不限于加速器的设计与分析、加速器相关的软件栈从抽象到编译器转换，以及它们的设计自动化技术。

- **联系方式**：[jian.weng@kaust.edu.sa](mailto:jian.weng@kaust.edu.sa)


### 66. **GABRIEL WITTUM**

- **职位**：应用数学与计算科学教授

- **个人主页**：[Gabriel Wittum](https://www.kaust.edu.sa/en/study/faculty/gabriel-wittum)

- **照片**：[Gabriel Wittum](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/wittum.jpg)

- **研究方向**：Wittum教授的研究重点是使用高性能计算（HPC）对经验科学中的问题进行建模和仿真。特别关注的领域包括：开发用于建模和仿真的先进数值方法，如并行自适应多网格方法等快速求解器，允许应用于复杂的现实模型；开发相应的仿真框架和工具；以及高效使用顶级超级计算机来实现这一目的。这些方法和工具应用于计算流体动力学、环境研究、能源研究、金融、神经科学、制药技术等领域的问题解决。

- **联系方式**：[gabriel.wittum@kaust.edu.sa](mailto:gabriel.wittum@kaust.edu.sa)


### 67. **PETER WONKA**

- **职位**：计算机科学教授

- **个人主页**：[Peter Wonka](https://www.kaust.edu.sa/en/study/faculty/peter-wonka)

- **照片**：[Peter Wonka](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/peter-wonka.png)

- **研究方向**：Wonka教授的主要研究兴趣在于深度学习、计算机视觉和计算机图形学。他还对相关领域如可视化、图像处理、遥感、数据挖掘和机器学习感兴趣。

- **联系方式**：[peter.wonka@kaust.edu.sa](mailto:peter.wonka@kaust.edu.sa)


### 68. **YING WU**

- **职位**：应用数学与计算科学教授

- **个人主页**：[Ying Wu](https://www.kaust.edu.sa/en/study/faculty/ying-wu)

- **照片**：[Ying Wu](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/ying-wu-400x400.jpeg)

- **研究方向**：Wu教授的研究兴趣在于计算物理领域，重点是非均质介质中的波传播，如电磁、声学和弹性超材料、有效介质理论、输运理论、时间反演成像和超分辨率。她的研究还扩展到在解决大规模经典波传播问题中实现快速算法。

- **联系方式**：[ying.wu@kaust.edu.sa](mailto:ying.wu@kaust.edu.sa)


### 69. **JINCHAO XU**

- **职位**：应用数学与计算科学教授，KAUST深圳创新中心主任

- **个人主页**：[Jinchao Xu](https://www.kaust.edu.sa/en/study/faculty/jinchao-xu)

- **照片**：[Jinchao Xu](https://www.kaust.edu.sa/images/kaustlibraries/publishingimages/study/faculty-images/jinchao-xu-dsc_9234.png)

- **研究方向**：Jinchao Xu是KAUST深圳创新中心的主任，阿卜杜拉国王科技大学（KAUST）应用数学与计算科学的教授，KAUST-SRIBD联合实验室（科学计算与机器学习）的主任，宾夕法尼亚州立大学数学教授及计算数学与应用中心的主任。

Xu倡导实用应用、理论完整性和美感可以相辅相成的理念。他研究偏微分方程的数值方法和大数据，特别是有限元方法、多重网格方法和深度神经网络，进行理论分析、算法开发和实际应用。最近，他领导了阿拉伯语大型语言模型（LLM）AceGPT的开发合作，该模型在所有开源阿拉伯语LLM中表现出最具竞争力的性能。

- **联系方式**：[jinchao.xu@kaust.edu.sa](mailto:jinchao.xu@kaust.edu.sa)
