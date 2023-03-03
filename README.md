# 前言

一开始决定分为三个部分，第一部分为论文梳理，第二部分为具体细节，会放上一些论文的主体理解，第三部分放一些实验代码


# 目录

- [Papers](#目录)
  - [DP & Application Technology](#dp-scenario)
    - [Rappor](#rappor)
    - [IBM DP library](#IBM-DP-library)
    - [Heavy Hitter Estimation LDP](#Heavy-Hitter-Estimation-LDP)
   - [LDP & Collecting and analyzing method](#ldp-and-dp下数据分析)
   - [LDP & Answering method](#ldp-and-dp下数据发布)
   - [DB & Join queries](#数据库连接查询)
   - [DP & Meachine Learning](#dp-and-ldp与机器学习相结合)
   - [DP & Federated Learning](#dp-and-ldp与联邦学习相结合)

## DP scenario

这里会收集一些DP和LDP在现实生活中的用例
| Title | Team/Main Author | Venue and Year | Key Description 
| :------------| :------ | :---------- | :-----------------------
| [RAPPOR: Randomized Aggregatable Privacy-Preserving Ordinal Response](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)| Google | 2015 |https://github.com/google/rappor
|[IBM-differential-privacy-library](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note) | IBM | 2018 | https://github.com/IBM/differential-privacy-library/blob/main/
| [Heavy Hitter Estimation over Set-Valued Data with Local Differential Privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note) | Zhan Qin |2016/CCS | 

## LDP and DP下数据分析
多是一些LDP&DP下的数据融合分析
| Title | Team/Main Author | Venue and Year | Key Description 
| :------------| :------ | :---------- | :-----------------------
| [Collecting And Analyzing Data Jointly From Multiple Services under Local Differential Privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note) | Min Xu | 2020/VLDB Endowment | 针对多服务器场景下的本地化差分隐私数据收集与分析
| [Building a RAPPOR with the Unknown: Privacy-Preserving Learning of Associations and Data Dictionaries](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note) | G. Fanti, Vasyl Pihur, Ú. Erlingsson | 2015 | 在未知关系和词典的情况下构建RAPPOR
|[DPSAaS: Multi-Dimensional Data Sharing and Analytics as Services under Local Differential Privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note) | Min Xu| 2019/VLDB Endow | 由阿里提出的本地化差分隐私下的多维数据共享和分析云服务
|[Heavy Hitter Estimation over Set-valued Data with Local Differential Privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)|Qin Z,Yang Y|2016 ACM SIGSAC|本地差分隐私下对集值数据的频繁项估计|
|[Local DIfferentially Private Heavy Hitters Identification](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)|Tianhao Wang|2021 IEEE|本地化差分隐私下的频繁项识别：提出了前缀扩展方法(Prefix Extending Method,PEM)|
|[Budget Sharing for multi-analyst differential privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)|David Pujol, Yikai Wu|2021 PVLDB|本文首次研究了多分析师场景下的差分隐私预算共享，并针对此问题提出了三种机制：共享激励，不干涉和适应性
|[Multi-analyst differential privacy for online query answering](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)|David Pujol, Albert Sun|2022|本文基于作者们之前的研究，将多分析师差分隐私预算分配问题扩展到了在线查询回答的情况下

## LDP and DP下数据发布
多是一些LDP&DP下的数据发布和响应数据查询
| Title | Team/Main Author | Venue and Year | Key Description 
| :------------| :------ | :---------- | :-----------------------
| [AHEAD: Adaptive Hierarchical Decomposition for Range Query under Local Differential Privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note) | Linkang Du | 2021/CCS | 主要讲述的是针对LDP下响应范围查询的问题，作者提出了一种自适应构建多层次分析树的方案来提升在LDP下响应范围查询的精度
| [Answering Multi-Dimensional Analytical Queries under Local Differential Privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note) | Tianhao Wang | 2019 | pure-LDP概念。三种频率估计机制：单维和多维下的HIO机制、SC拆分再联接机制|
|[Continuous Release of Data Streams under both Centralized and Local Differential Privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)| Tianhao Wang |2019| 主要描述的是在数据流发布环境下如何使用DP和LDP对数据流施加差分隐私保护，同时作者提出了两个框架，一个是基于DP的ToPS框架，一个是基于LDP的ToPL框架
| [Empirical Risk Minimization in the Non-interactive Local Model of Differential Privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)| Di Wang | 2020 | 这篇文章提出使用内积多项式的形式释放函数，一般是用于分布式学习和联邦学习下，但在响应边缘查询（k-way Margin Query）时也提出了使用内积多项式的形式去简化查询函数（使用数学去定义查询函数），从而提升查询精度


## DB and Join queries 数据库连接查询
| Title | Team/Main Author | Venue and Year | Key Description 
| :------------| :------ | :---------- | :-----------------------
| [Residual Sensitivity for Differentially Private Multi-way joins](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)| Wei Dong, Ke Yi| 2021 |为了解决连接查询下差分隐私噪声敏感度过大以及计算效率的问题，本文提出残差查询和残差敏感度或最大边界，使敏感度计算满足高效率、高效用以及可一体化
| [Wander join and XDB: Online aggregation via random walks](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)|Feifei Li, Bin Wu, Ke Yi, Zhuoyue Zhao|2019|本文提出了一种新颖的采样算法对数据库连接进行采样，基于在线聚集利用随机游走的方式针对不同场景下的连接查询进行连接采样，得到独立非均匀地样本，具有高效性
| [Random Sampling over Joins Revisited](https://github.com/Triumphhh/LDP-Afterreading/tree/main/lx)|Zhuoyue Zhao, Feifei Li, Ke Yi|2018|本文对数据库连接采样的问题进行了回顾，总结了前人的方法与缺陷，并基于此提出改进。构建了连接随机采样框架统一化先前方法，并在更复杂场景下给出更加优化的方案来解决连接的随机采样

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



# 数据与代码

这一部分打算将收集到的一些数据和组内写的代码放在这里，数据出处也会进行标明，代码出处当然也会
> 机器学习相关论文查询：https://paperswithcode.com/
> 一些LDP协议的代码库：https://github.com/vvv214/LDP_Protocols


