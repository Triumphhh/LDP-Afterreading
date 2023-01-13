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
| [Collecting And Analyzing Data Jointly From Multiple Services under Local Differential Privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note) | Min Xu | 2020/VLDB Endowment | 
| [Building a RAPPOR with the Unknown: Privacy-Preserving Learning of Associations and Data Dictionaries](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note) | G. Fanti, Vasyl Pihur, Ú. Erlingsson | 2015 | 
|[DPSAaS: Multi-Dimensional Data Sharing and Analytics as Services under Local Differential Privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note) | Min Xu| 2019/VLDB Endow | 
|[Heavy Hitter Estimation over Set-valued Data with Local Differential Privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)|Qin Z,Yang Y|2016 ACM SIGSAC|本地差分隐私下对集值数据的频繁项估计|

## LDP and DP下数据发布
多是一些LDP&DP下的数据发布和响应数据查询
| Title | Team/Main Author | Venue and Year | Key Description 
| :------------| :------ | :---------- | :-----------------------
| [AHEAD: Adaptive Hierarchical Decomposition for Range Query under Local Differential Privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note) | Linkang Du | 2021/CCS | 主要讲述的是针对LDP下响应范围查询的问题，作者提出了一种自适应构建多层次分析树的方案来提升在LDP下响应范围查询的精度
| [Answering Multi-Dimensional Analytical Queries under Local Differential Privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note) | Tianhao Wang | 2019 | 
|[Continuous Release of Data Streams under both Centralized and Local Differential Privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)| Tianhao Wang |2019| 主要描述的是在数据流发布环境下如何使用DP和LDP对数据流施加差分隐私保护，同时作者提出了两个框架，一个是基于DP的ToPS框架，一个是基于LDP的ToPL框架
| [Empirical Risk Minimization in the Non-interactive Local Model of Differential Privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)| Di Wang | 2020 | 这篇文章提出使用内积多项式的形式释放函数，一般是用于分布式学习和联邦学习下，但在响应边缘查询（k-way Margin Query）时也提出了使用内积多项式的形式去简化查询函数（使用数学去定义查询函数），从而提升查询精度
| 

## DP and LDP与机器学习相结合
多是一类分布式与联邦学习下数据聚合方面，但是根据差分隐私与机器学习结合部位的不同（例如：目标函数扰动、输入扰动、梯度扰动、输出扰动）可以用于不同的场景下

| Title | Team/Main Author | Venue and Year | Key Description 
| :------------| :------ | :---------- | :-----------------------
| [Empirical Risk Minimization in the Non-interactive Local Model of Differential Privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)|  Di Wang | 2020 | 这篇文章基于前人工作（伯恩斯坦多项式机制、非交互式差分隐私方面等提出了使用内积多项式的方法释放函数，还提出了1-bit的通信方法，能够使泛化误差的上界更为紧致，且对样本量n的依赖度降为多项式级别，但是问题在于这只是理论上的，作者也表明了不知道在现实中的应用效果是怎么样的）
|[Optimal Algorithms for Mean Estimation under Local Differential Privacy](https://github.com/Triumphhh/LDP-Afterreading/tree/main/Note)|Hilal Asi, V. Feldman, Kunal Talwar|2022/ICML|用于处理聚合过程中的均值估计的问题，开发了一种基于高斯机制的PrivUnit方法，通过采样的方式降低噪声引入带来的误差
|


## DP and LDP与联邦学习相结合

问题描述
| Title | Team/Main Author | Venue and Year | Key Description 
| :------------| :------ | :---------- | :-----------------------
| 1|2|3|4
|




# 数据与代码

这一部分打算将收集到的一些数据和组内写的代码放在这里，数据出处也会进行标明，代码出处当然也会
> 机器学习相关论文查询：https://paperswithcode.com/
> 一些LDP协议的代码库：https://github.com/vvv214/LDP_Protocols


