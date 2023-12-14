# 前言

第一部分为论文梳理，第二部分为具体细节，第三部分为实验代码


# 目录

- [Papers](#目录)
  - [DP & Application Technology](#dp-scenario)
    - [Rappor](#rappor)
    - [IBM DP library](#IBM-DP-library)
    - [Heavy Hitter Estimation LDP](#Heavy-Hitter-Estimation-LDP)
   - [LDP & Collecting and analyzing method](#ldp-and-dp下数据分析)
   - [LDP & Answering method](#ldp-and-dp下数据发布)
   - [DP/LDP & Optimizing techniques](#dp-and-ldp下优化技术)
   - [DB & Join queries](#数据库连接查询)
   - [DP & Meachine Learning](#dp-and-ldp与机器学习相结合)
   - [DP & Federated Learning](#dp-and-ldp与联邦学习相结合)

## _Overview of Differential Privacy in Practice_
| Title | Team/Main Author | Venue and Year | Key Description 
| :------------| :------ | :---------- | :-----------------------
| [Differential Privacy in Practice: Expose your Epsilons!](https://journalprivacyconfidentiality.org/index.php/jpc/article/view/689) | Cynthia Dwork | 2019 | 文章针对差分隐私落地面临诸多阻碍的问题，使用访谈的方式，与部署了差分隐私的企业的相关人士进行了深入系统性的沟通交流，并对访谈结果进行了归纳整理。文中重点探讨了隐私预算在实际应用中的选择，提出**Epsilon Registry**.(知乎：https://zhuanlan.zhihu.com/p/641373746)
| [Privacy at Scale: Local Differential Privacy in Practice](https://dl.acm.org/doi/10.1145/3183713.3197390) | Graham Cormode, Ninghui Li, Tianhao Wang | 2018 | 文章概述了LDP的应用场景以及行业发展方向，对LDP的各个方面进行了详细介绍.
| [本地化差分隐私研究综述](https://www.jos.org.cn/jos/article/abstract/5364) | Qingqing Ye, Xiaofeng Meng | 2018 | 文章介绍了LDP的原理和特性，总结和归纳了当前研究工作以及阐述LDP的研究热点，指出了LDP的未来研究挑战.

## _Differential Privacy Open-source Project_
| Name | Team/Corporation | Year | Key Description 
| :------------| :------ | :---------- | :-----------------------
| [RAPPOR: Randomized Aggregatable Privacy-Preserving Ordinal Response](https://dl.acm.org/doi/10.1145/2660267.2660348)| Google | 2015 | 项目地址：https://github.com/google/rappor
| google-differential-privay | Google | 2019 | 项目地址：https://github.com/google/differential-privacy
| [IBM-differential-privacy-library](https://arxiv.org/abs/1907.02444) | IBM | 2018 | 项目地址https://github.com/IBM/differential-privacy-library/blob/main/ <br> 博客：https://research.ibm.com/blog/ibm-differential-privacy-library-the-single-line-of-code-that-can-protect-your-data
| [learning-privacy-at-scale](https://docs-assets.developer.apple.com/ml-research/papers/learning-with-privacy-at-scale.pdf) | Apple | 2017 | 项目地址https://github.com/Samuel-Maddock/Apple-Differential-Privacy <br> 博客：https://machinelearning.apple.com/research/learning-with-privacy-at-scale
| [Collecting Telemetry Data Privately](https://proceedings.neurips.cc/paper/2017/hash/253614bbac999b38b5b60cae531c4969-Abstract.html) | Microsoft | 2017 | 项目地址：None <br> 博客：https://www.microsoft.com/en-us/research/blog/collecting-telemetry-data-privately/
| Jeddak-DPSQL | Bytedance | 2023 | 项目地址：https://github.com/bytedance/Jeddak-DPSQL/ <br> 博客：https://zhuanlan.zhihu.com/p/571766114
| [OpenDP](https://projects.iq.harvard.edu/files/opendp/files/opendp_programming_framework_11may2020_1_01.pdf)| OpenDP | 2020 | 项目地址：https://github.com/opendp/opendp
| [Opacus](https://arxiv.org/abs/2109.12298) | Meta AI(Facebook) | 2021 | 项目地址：https://github.com/pytorch/opacus <br> 博客：https://zhuanlan.zhihu.com/p/212862132

### ~ _Some other useful DP tool libraries_ 
| Name | Author | Key Description 
| :------------| :------ | :-----------------------
| LDP_protocols | Tianhao Wang | 本地化差分隐私在Python中的简单应用，包括HIO、PEM、SVSM等。 <br> 项目地址：https://github.com/vvv214/LDP_Protocols
| pure_LDP | Samuel Maddock | 本地化差分隐私频率估计算法在Python中的简单应用，包括LH、DE、HM、AppleCMS/HCMS等。 <br> 项目地址：https://github.com/Samuel-Maddock/pure-LDP

## _Federated Learning Open-source Project_
| Name | Team/Corporation | Year | Key Description 
| :------------| :------ | :---------- | :-----------------------
| [FATE](https://jmlr.org/papers/v22/20-815.html) | FedAI | 2019 | 项目地址：https://github.com/FederatedAI/FATE <br> 博客：https://zhuanlan.zhihu.com/p/424465305
| [FederatedScope](https://www.vldb.org/pvldb/vol16/p1059-li.pdf) | Alibaba DAMO | 2023 | 项目地址：https://github.com/alibaba/FederatedScope <br> 博客：https://www.jiqizhixin.com/articles/2022-05-09-7 <br> 视频讲解：https://www.bilibili.com/video/BV1Sv4y197ju/?spm_id_from=333.788&vd_source=406c96d7ba3d57a6cbbe36c50b5a1b75

 
## LDP and DP下数据分析
多是一些LDP&DP下的数据融合分析
| Title | Team/Main Author | Year | Key Description 
| :------------| :------ | :---------- | :-----------------------
| [Collecting And Analyzing Data Jointly From Multiple Services under Local Differential Privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note) | Min Xu | 2020/VLDB Endowment | 针对多服务器场景下的本地化差分隐私数据收集与分析
| [Building a RAPPOR with the Unknown: Privacy-Preserving Learning of Associations and Data Dictionaries](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note) | G. Fanti, Vasyl Pihur, Ú. Erlingsson | 2015 | 在未知关系和词典的情况下构建RAPPOR
|[DPSAaS: Multi-Dimensional Data Sharing and Analytics as Services under Local Differential Privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note) | Min Xu| 2019/VLDB Endow | 由阿里提出的本地化差分隐私下的多维数据共享和分析云服务
|[Heavy Hitter Estimation over Set-valued Data with Local Differential Privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)|Qin Z,Yang Y|2016 ACM SIGSAC|本地差分隐私下对集值数据的频繁项估计|
|[Local DIfferentially Private Heavy Hitters Identification](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)|Tianhao Wang|2021 IEEE|本地化差分隐私下的频繁项识别：提出了前缀扩展方法(Prefix Extending Method,PEM)|
|[Budget Sharing for multi-analyst differential privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)|David Pujol, Yikai Wu|2021 PVLDB|本文首次研究了多分析师场景下的差分隐私预算共享，并针对此问题提出了三种机制：共享激励，不干涉和适应性
|[Multi-analyst differential privacy for online query answering](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)|David Pujol, Albert Sun|2022|本文基于作者们之前的研究，将多分析师差分隐私预算分配问题扩展到了在线查询回答的情况下|
|[DDRM: A Continual Frequency Estimation Mechanism With Local Differential Privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)|Qiao Xue, Qingqing Ye,Haibo Hu|2023TKDE|本文提出了一种时间序列数据收集方案，即动态差异报告机制DDRM，用于连续频率估计，解决了记忆技术存在的两个问题，同时保持高精度，提出了为连续频率估计分配隐私预算的最佳解决方案，实现了效用增强.|
|[Local Differentially Private Fuzzy Counting in Stream Data using Probabilistic Data Structures](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)|D. Vatsalan, R. Bhaskar and M. A. Kaafar|2023 TKDE|本文研究实时流数据中项目频率的隐私保护问题，目标是为计数查询功能的实时处理提供改进，其中计数查询需要实时和在线地进行响应，提出一种用于实时流应用的差分隐私计数方法.|

## LDP and DP下数据发布
多是一些LDP&DP下的数据发布和响应数据查询
| Title | Team/Main Author | Venue and Year | Key Description 
| :------------| :------ | :---------- | :-----------------------
| [AHEAD: Adaptive Hierarchical Decomposition for Range Query under Local Differential Privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note) | Linkang Du | 2021/CCS | 主要讲述的是针对LDP下响应范围查询的问题，作者提出了一种自适应构建多层次分析树的方案来提升在LDP下响应范围查询的精度
| [Answering Multi-Dimensional Analytical Queries under Local Differential Privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note) | Tianhao Wang | 2019 | pure-LDP概念。三种频率估计机制：单维和多维下的HIO机制、SC拆分再联接机制|
|[Continuous Release of Data Streams under both Centralized and Local Differential Privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)| Tianhao Wang |2019| 主要描述的是在数据流发布环境下如何使用DP和LDP对数据流施加差分隐私保护，同时作者提出了两个框架，一个是基于DP的ToPS框架，一个是基于LDP的ToPL框架
| [Empirical Risk Minimization in the Non-interactive Local Model of Differential Privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)| Di Wang | 2020 | 这篇文章提出使用内积多项式的形式释放函数，一般是用于分布式学习和联邦学习下，但在响应边缘查询（k-way Margin Query）时也提出了使用内积多项式的形式去简化查询函数（使用数学去定义查询函数），从而提升查询精度

## DP/LDP and Optimization techniques 优化技术
| Title | Team/Main Author | Venue and Year | Key Description
| :------------| :------ | :---------- | :-----------------------
| [The Matrix Mechanism: optimizing liner counting queries under differential privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)| Chao Li | 2015 | 本文提出的矩阵机制(MM)可以更准确回答计数查询集，并可以通过迭代求解半定规划计算最优策略.
| [Query optimization for differentially private datamanagement system](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)|Peng, Shangfu|2013|本文提出了 Pioneer，这是一种适用于 DP 兼容 DBMS 的有效且高效的查询优化器,其构建了一个重用历史查询的执行方案，以尽量减少隐私预算的使用。它还包括一种有效的算法，用于选择有助于回答新传入查询的历史查询，并且方案计算和历史查询选择的计算成本可忽略.

## DB and Join queries 数据库连接查询
| Title | Team/Main Author | Venue and Year | Key Description 
| :------------| :------ | :---------- | :-----------------------
| [Residual Sensitivity for Differentially Private Multi-way joins](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)| Wei Dong, Ke Yi| 2021 |为了解决连接查询下差分隐私噪声敏感度过大以及计算效率的问题，本文提出残差查询和残差敏感度或最大边界，使敏感度计算满足高效率、高效用以及可一体化.(https://github.com/hkustDB/ResidualSensitivity)
| [Wander join and XDB: Online aggregation via random walks](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)|Feifei Li, Bin Wu, Ke Yi, Zhuoyue Zhao|2019|本文提出了一种新颖的采样算法对数据库连接进行采样，基于在线聚集利用随机游走的方式针对不同场景下的连接查询进行连接采样，得到独立非均匀地样本，具有高效性.(https://github.com/InitialDLab/XDB)
| [Random Sampling over Joins Revisited](https://github.com/Triumphhh/LDP-Afterreading/tree/main/lx)|Zhuoyue Zhao, Feifei Li, Ke Yi|2018|本文对数据库连接采样的问题进行了回顾，总结了前人的方法与缺陷，并基于此提出改进。构建了连接随机采样框架统一化先前方法，并在更复杂场景下给出更加优化的方案来解决连接的随机采样.(https://github.com/InitialDLab/SampleJoin)
| [Better than Composition：How to Answer Multiple Relational Queries under Differential Privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)| Wei Dong, Dajun Sun, Ke Yi|2023|将单查询机制扩展到多个查询的标准解决方案是通过隐私组合。然而，这可能会产生一个误差范围，该误差范围可能比最优值差根号d因子，其中d是查询数量。在本文中，提出了一种不同的、更全面的方法来缩小这一差距.(https://github.com/hkustDB/PMSJA)

## DP and LDP与机器学习相结合
多是一类分布式与联邦学习下数据聚合方面，但是根据差分隐私与机器学习结合部位的不同（例如：目标函数扰动、输入扰动、梯度扰动、输出扰动）可以用于不同的场景下

| Title | Team/Main Author | Venue and Year | Key Description 
| :------------| :------ | :---------- | :-----------------------
| [Empirical Risk Minimization in the Non-interactive Local Model of Differential Privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)|  Di Wang | 2020 | 这篇文章基于前人工作（伯恩斯坦多项式机制、非交互式差分隐私方面等提出了使用内积多项式的方法释放函数，还提出了1-bit的通信方法，能够使泛化误差的上界更为紧致，且对样本量n的依赖度降为多项式级别，但是问题在于这只是理论上的，作者也表明了不知道在现实中的应用效果是怎么样的）
|[Optimal Algorithms for Mean Estimation under Local Differential Privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)|Hilal Asi, V. Feldman, Kunal Talwar|2022/ICML|用于处理聚合过程中的均值估计的问题，开发了一种基于高斯机制的PrivUnit方法，通过采样的方式降低噪声引入带来的误差

## DP and LDP与联邦学习相结合

问题描述
| Title | Team/Main Author | Venue and Year | Key Description 
| :------------| :------ | :---------- | :-----------------------
| [LDP-FL: Practical Private Aggregation in Federated Learning with Local Differential Privacy](https://github.com/Su-Whale/LDP-Afterreading/blob/main/FL-DP/Practical%20Private%20Aggregation%20in%20Federated%20Learning%20with%20Local%20Differential%20Privacy.pdf)|Lichao Sun | 2021 |本文针对在多层神经网络中存在隐私预算爆炸的问题提出了LDP-FL框架，不仅很好的保护了隐私，而且通过分割洗牌机制降低了隐私预算在多层迭代中的激增
| [LDP-Fed: Federated Learning with Local Differential Privacy](https://github.com/Su-Whale/LDP-Afterreading/blob/main/FL-DP/Federated%20Learning%20with%20Local%20Differential%20Privacy.pdf)|Stacey Truex|2020 |本文提出了LDP-Fed框架，LDP 模块为在多个个体参与者的私有数据集上的大规模神经网络联合训练中模型训练参数的重复收集提供了正式的差分隐私保证。其次，LDP-Fed实现了一套选择和过滤技术，用于扰动和与参数服务器共享选择的参数更新。

## AQP近似查询处理/Sketches 草图技术
流算法（Streaming algorithms）:使用次线性的时间、空间成本，以很高的计算速度快速响应大型流数据的处理。缺点是只能得到近似真实值的结果，但是很多算法会给出相应估计误差界限。
| Title | Team/Main Author | Venue and Year | Key Description
| :------------| :------ | :---------- | :-----------------------
|[Persistent Data Sketching ](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)|Zhewei Wei, Ke Yi|2015 SIGMOD|本文的是使草图持久化，从而使流式算法能够在历史上的任何先前时间回答查询，并且仍然有一个小的ε错误|
|[At-the-time and Back-in-time Persistent Sketches](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)|Benwei Shi, Zhuoyue Zhao, Feifei Li|本文提出了当时持久性（ATTP）和回溯性持久性（BITP）草图的概念，这些草图可以用小空间近似回答对先前版本的数据的查询|


# 数据与代码

这一部分打算将收集到的一些数据和组内写的代码放在这里，数据出处也会进行标明，代码出处当然也会
> 机器学习相关论文查询：https://paperswithcode.com/
> 一些LDP协议的代码库：
> -https://github.com/vvv214/LDP_Protocols
> - https://github.com/Samuel-Maddock/pure-LDP

