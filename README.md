# Differential Privacy Learning Repository of Privacy-preserving Big Data Analytics Group, CIAT, GZHU.
欢迎关注我们的b站账号：【隐私数据分析小组的个人空间-哔哩哔哩】 https://b23.tv/rq5CkmD

每周更新差分隐私经典算法，不定期更新最新文献解读

# 目录
1. [前言](#一-前言)
2. [差分隐私相关文献](#差分隐私相关文献)
3. [其他相关文献](#其他相关文献)
4. [我们的工作](#我们的工作)
5. [通用数据与代码](#通用数据与代码查询)


# 一、前言
该学习库中包括差分隐私相关研究的汇总，以及小组工作汇报内容（考虑隐私原因，不再提供组内相关汇报文件）

## _Overview/Survey of Differential Privacy_
| Title | Team/Main Author | Year | Key Description 
| :--------------| :------ | :---------- | :-----------------------
| [差分隐私研究进展综述](https://core.ac.uk/download/561074268.pdf) | Zhao Yuqi, Yang Min | 2023 | 文中给出了差分隐私技术的全面概述，总结并分析了差分隐私的最新进展。特别地，文章给出了包括中心化差分隐私、本地化模型和洗牌模型地理论总结，并对他们做了详细比较，分析了不同模型地优势和缺点.
| [Differential Privacy in Practice: Expose your Epsilons!](https://journalprivacyconfidentiality.org/index.php/jpc/article/view/689) | Cynthia Dwork | 2019 | 文章针对差分隐私落地面临诸多阻碍的问题，使用访谈的方式，与部署了差分隐私的企业的相关人士进行了深入系统性的沟通交流，并对访谈结果进行了归纳整理。文中重点探讨了隐私预算在实际应用中的选择，提出**Epsilon Registry**.(知乎：https://zhuanlan.zhihu.com/p/641373746)
| [Privacy at Scale: Local Differential Privacy in Practice](https://dl.acm.org/doi/10.1145/3183713.3197390) | Graham Cormode, Ninghui Li, Tianhao Wang | 2018 | 文章概述了LDP的应用场景以及行业发展方向，对LDP的各个方面进行了详细介绍.
| [差分隐私综述](https://jcs.iie.ac.cn/xxaqxb/ch/reader/view_abstract.aspx?file_no=20180508&flag=1) | Li Xiaoguang, Li Hui, Li Fenghua, Zhu Hui | 2018 | 本文介绍了差分隐私的基础理论和目前的研究进展，以及一些已有的差分隐私保护理论和技术，最后对未来的工作和研究热点进行了展望.
| [本地化差分隐私研究综述](https://www.jos.org.cn/jos/article/abstract/5364) | Qingqing Ye, Xiaofeng Meng | 2018 | 文章介绍了LDP的原理和特性，总结和归纳了当前研究工作以及阐述LDP的研究热点，指出了LDP的未来研究挑战.
| [The Algorithm Fundamentions of Differential Privacy](https://privacytools.seas.harvard.edu/files/privacytools/files/the_algorithmic_foundations_of_differential_privacy_0.pdf) | Cynthia Dwork, Aaron Roth | 2014 | 本文详细介绍了差分隐私的算法基础，是差分隐私初学者必看的文献之一.

## _Differential Privacy Open-source Project_
| Name | Team/Corporation | Year | Key Description 
| :------------| :------ | :---------- | :-----------------------
| [Jeddak-DPSQL](https://www.volcengine.com/product/Jeddak) | 火山引擎/Bytedance | 2023 | 项目地址：https://github.com/bytedance/Jeddak-DPSQL/ <br> 博客：https://zhuanlan.zhihu.com/p/571766114
| [Opacus](https://arxiv.org/abs/2109.12298) | Meta AI(Facebook) | 2021 | 项目地址：https://github.com/pytorch/opacus <br> 博客：https://zhuanlan.zhihu.com/p/212862132
| [OpenDP](https://projects.iq.harvard.edu/files/opendp/files/opendp_programming_framework_11may2020_1_01.pdf)| OpenDP | 2020 | 项目地址：https://github.com/opendp/opendp
| [google-differential-privay](https://desfontain.es/privacy/friendly-intro-to-differential-privacy.html) | Google | 2019 | 项目地址：https://github.com/google/differential-privacy
| [IBM-differential-privacy-library](https://arxiv.org/abs/1907.02444) | IBM | 2018 | 项目地址https://github.com/IBM/differential-privacy-library/blob/main/ <br> 博客：https://research.ibm.com/blog/ibm-differential-privacy-library-the-single-line-of-code-that-can-protect-your-data
| [learning-privacy-at-scale](https://docs-assets.developer.apple.com/ml-research/papers/learning-with-privacy-at-scale.pdf) | Apple | 2017 | 项目地址https://github.com/Samuel-Maddock/Apple-Differential-Privacy <br> 博客：https://machinelearning.apple.com/research/learning-with-privacy-at-scale
| [Collecting Telemetry Data Privately](https://proceedings.neurips.cc/paper/2017/hash/253614bbac999b38b5b60cae531c4969-Abstract.html) | Microsoft | 2017 | 项目地址：None <br> 博客：https://www.microsoft.com/en-us/research/blog/collecting-telemetry-data-privately/
| [RAPPOR: Randomized Aggregatable Privacy-Preserving Ordinal Response](https://dl.acm.org/doi/10.1145/2660267.2660348)| Google | 2015 | 项目地址：https://github.com/google/rappor <br> 博客：https://www.cnblogs.com/sftsgly/articles/17501447.html


### ~ _Some other useful DP tool libraries_ 
| Name | Author | Key Description 
| :------------| :------ | :-----------------------
| LDP_protocols | Tianhao Wang | 本地化差分隐私在Python中的简单应用，包括HIO、PEM、SVSM等。 <br> 项目地址：https://github.com/vvv214/LDP_Protocols
| pure_LDP | Samuel Maddock | 本地化差分隐私频率估计算法在Python中的简单应用，包括LH、DE、HM、AppleCMS/HCMS等。 <br> 项目地址：https://github.com/Samuel-Maddock/pure-LDP
| Awesome-Differential-Privacy-and-Meachine-Learning | Jie Fu | 机器学习和差分隐私的论文笔记和代码仓。 <br> 项目地址：https://github.com/JeffffffFu/Awesome-Differential-Privacy-and-Meachine-Learning
| awesome-differential-privacy | menisadi | 差分隐私相关资源的列表。 <br> 项目地址：https://github.com/menisadi/awesome-differential-privacy
| prv_accountant | Microsoft | 一个快速算法，用于以任意精度最优地组合差分隐私机制的隐私保证。 <br> 项目地址：https://github.com/microsoft/prv_accountant

### ~_其他国内部署DP技术的厂商_
| Name | Key Description | Source
| :------------| :------ | :-----------------------
| SecretFlow | 蚂蚁集团隐语SecretFlow是一个统一的框架，用于保护隐私的数据智能和机器学习. | 官网：https://secret-flow.antgroup.com/ <br> 项目地址：https://github.com/secretflow/secretflow
| DataTrust | 阿里巴巴DataTrust平台是基于安全多方计算、联邦学习、**差分隐私**等隐私增强计算技术打造的隐私增强计算平台。 | 阿里云DataTrust：https://help.aliyun.com/document_detail/208025.html
| 百度网盘 | 为进一步保障数据拥有者的权益安全和隐私，百度网盘采用隐私计算、**差分隐私**、AI自动脱敏、芯片级可信安全计算服务框架MesaTEE等多项前沿技术手段来保障数据可用不可见 | 百度网盘隐私保护白皮书：https://pan.baidu.com/disk/agreement#/
| vivo | 基于**差分隐私**技术，OriginOS能够在保护个人隐私的同时，在可靠性、性能、功耗等方面进行持续改进和优化，为用户提供更极致的使用体验。 | VIVO安全白皮书：https://privacy.vivo.com.cn/static/pdf/security-book-pdf.pdf
| OPPO | OPPO已在手机端侧系统和部分应用中使用**本地化差分隐私**技术，在数据中添加随机噪声，仅保留数据整体统计特征，确保用户数据不出终端设备即可实现相关功能，从而更好地保护用户隐私安全。 | OPPO移动终端隐私保护白皮书：https://privacy.oppo.com/privacy-center/pdf/OPPO移动终端隐私保护白皮书V1.0.pdf
| Webank | 微众银行的多方大数据隐私计算平台，解决大模型推理过程中隐私泄露风险较高的问题：...对第二梯度进行**差分隐私**处理，得到第三梯度；基于第一梯度对答案预测模型进行迭代更新，并基于第三梯度对编码器进行迭代更新。 | 来源：https://www.mpaypass.com.cn/news/202406/19120626.html
| 小米 | **差分隐私**技术使小米能够在不侵犯您隐私的情况下深入了解我们手机的质量性能和用户体验。 | 小米信任中心：https://trust.mi.com/zh-CN/privacy
| 华为 | 使用了**差分隐私技术**，既提升用户体验，又可保护你共享给华为的数据。运用该技术可在数据中添加随机噪声，我们无法获知真实数据。只有与其他大量用户数据结合，并平均掉随机添加的噪声，相关统计信息才会显现。 | Huawei隐私用户体验改进计划：https://consumer.huawei.com/cn/privacy/privacy-control/
| 洞见科技 | 数智联邦平台InsightOne采用面向计算场景的融合引擎架构，将多方安全计算、联邦学习等算法拆分为细化的算子，并结合了差分隐私、同态加密、零知识证明等技术。 | 洞见科技InsightOne：https://www.insightone.cn/product/insightone
| 美团 | 为了满足大数据量级的训练和推理，美团采取经过特定场景设计的**差分隐私**方案，用以保护纵向NN，性能高且对模型精度影响小。 | 来源：https://www.shaqiu.cn/case/55


## _Federated Learning Open-source Project_
| Name | Team/Corporation | Year | Key Description 
| :------------| :------ | :---------- | :-----------------------
| [FederatedScope](https://www.vldb.org/pvldb/vol16/p1059-li.pdf) | Alibaba DAMO | 2023 | 项目地址：https://github.com/alibaba/FederatedScope <br> 博客：https://www.jiqizhixin.com/articles/2022-05-09-7 <br> 视频讲解：https://www.bilibili.com/video/BV1Sv4y197ju/?spm_id_from=333.788&vd_source=406c96d7ba3d57a6cbbe36c50b5a1b75
| [FATE](https://jmlr.org/papers/v22/20-815.html) | FedAI/WeBank | 2019 | 项目地址：https://github.com/FederatedAI/FATE <br> 博客：https://zhuanlan.zhihu.com/p/424465305

# 二、差分隐私相关文献

## LDP/DP下的数据挖掘
| Title | Team/Main Author | Journal/Conference | Key Description 
| :------------| :------ | :------- | :-----------------------
|[Heavy Hitter Identification Over Large-Domain Set-Valued Data With Local Differential Privacy](https://ieeexplore.ieee.org/document/10286079/)| Youwen Zhu,Qihui Wu | 2024/Inf. Forensics Secur| 本文基于前缀扩展方法PEM提出了解决大域场景下集值数据收集频繁项估计的问题，结合先前方法研究了多重集的保护方案，保证可靠的精度的同时提升了效率. <br> - 实验代码：https://github.com/Joy-Xue/PemSet. <br> - ☑️ 组内汇报：
|[Local Differentially Private Fuzzy Counting in Stream Data using Probabilistic Data Structures](https://ieeexplore.ieee.org/document/9855874)|D. Vatsalan, R. Bhaskar and M. A. Kaafar|2023/TKDE|本文研究实时流数据中项目频率的隐私保护问题，目标是为计数查询功能的实时处理提供改进，其中计数查询需要实时和在线地进行响应，提出一种用于实时流应用的差分隐私计数方法. <br> - 实验代码：无 <br> - ☑️ 组内汇报：
|[DDRM: A Continual Frequency Estimation Mechanism With Local Differential Privacy](https://ieeexplore.ieee.org/document/9782510)|Qiao Xue, Qingqing Ye,Haibo Hu|2023/TKDE|本文提出了一种时间序列数据收集方案，即动态差异报告机制DDRM，用于连续频率估计，解决了记忆技术存在的两个问题，同时保持高精度，提出了为连续频率估计分配隐私预算的最佳解决方案，实现了效用增强. <br> - 实验代码：https://github.com/Joy-Xue/DDRM <br> - ☑️ 组内汇报：
|[Multi-analyst differential privacy for online query answering](https://arxiv.org/pdf/2212.09884.pdf)|David Pujol, Albert Sun|2022/PVLDB|本文基于作者们之前的研究，将多分析师差分隐私预算分配问题扩展到了在线查询回答的情况下。 <br> - 实验代码：无 <br> - ☑️ 组内汇报：
|[Locally DIfferentially Private Heavy Hitters Identification](https://ieeexplore.ieee.org/document/8758350)|Tianhao Wang, Ninghui Li| 2021/TDSC | 本地化差分隐私下的频繁项识别：提出了前缀扩展方法(Prefix Extending Method,PEM)。 <br> - 实验代码：https://github.com/vvv214/LDP_Protocols <br> - ☑️ 组内汇报：
|[Budget Sharing for multi-analyst differential privacy](https://arxiv.org/pdf/2011.01192.pdf)|David Pujol, Yikai Wu|2021/PVLDB|本文首次研究了多分析师场景下的差分隐私预算共享，并针对此问题提出了三种机制：共享激励，不干涉和适应性。 <br>- 实验代码：https://github.com/yikai-wu/Multi-Analyst-DP <br> - ☑️ 组内汇报：
| [Collecting And Analyzing Data Jointly From Multiple Services under Local Differential Privacy](https://www.vldb.org/pvldb/vol13/p2760-xu.pdf) | Alibaba, Min Xu, Bolin Ding, Tianhao Wang | 2020/VLDB Endowment | 针对多服务器场景下的本地化差分隐私数据收集与分析。 <br> - 实验代码：无 <br> - ☑️ 组内汇报：
|[DPSAaS: Multi-Dimensional Data Sharing and Analytics as Services under Local Differential Privacy](https://www.vldb.org/pvldb/vol12/p1862-xu.pdf) | Alibaba, Min Xu, Tianhao Wang, Bolin Ding| 2019/VLDB Endow | 由阿里提出的本地化差分隐私下的多维数据共享和分析云服务。 <br> - 实验代码：无 <br> - ☑️ 组内汇报：
|[Heavy Hitter Estimation over Set-valued Data with Local Differential Privacy](https://dl.acm.org/doi/10.1145/2976749.2978409)|Qin Z,Yang Y|2016/CCS|本地差分隐私下对集值数据的频繁项估计。 <br> - 实验代码：https://github.com/Jun-Zhang-32108/GFIM_LDP <br> - ☑️ 组内汇报：
| [Building a RAPPOR with the Unknown: Privacy-Preserving Learning of Associations and Data Dictionaries](https://petsymposium.org/popets/2016/popets-2016-0015.php) | G. Fanti, Vasyl Pihur, Ú. Erlingsson | 2015/Priv.Enhancing Technol | 文章提出新颖的解码算法在未知关系和词典的情况下构建RAPPOR，并且开发了估计RAPPOR收集的两个或多个变量的联合分布的方法。 <br> - 实验代码：https://github.com/google/rappor <br> - ☑️ 组内汇报：
| [RAPPOR: Randomized Aggregatable Privacy-Preserving Ordinal Response.](https://dl.acm.org/doi/10.1145/2660267.2660348) | Google, Úlfar Erlingsson | 2014/CCS | 文章提出了基于两阶段随机响应机制的本地化差分隐私算法，用于保护客户端数据上的人口统计信息和隐私。其中随机响应机制是利用布隆过滤器实现的。 <br> - 实验代码：https://github.com/google/rappor <br> - ☑️ 组内汇报：


## LDP/DP下的数据发布
| Title | Team/Main Author | Venue and Year | Key Description 
| :------------| :------ | :---------- | :-----------------------
| [AHEAD: Adaptive Hierarchical Decomposition for Range Query under Local Differential Privacy](https://dl.acm.org/doi/10.1145/3460120.3485668) | Linkang Du | 2021/CCS | 主要讲述的是针对LDP下响应范围查询的问题，作者提出了一种自适应构建多层次分析树的方案来提升在LDP下响应范围查询的精度。 <br> - 实验代码：无 <br> - ☑️ 组内汇报：
| [Empirical Risk Minimization in the Non-interactive Local Model of Differential Privacy](https://jmlr.org/papers/v21/19-253.html)| Di Wang | 2020 | 这篇文章提出使用内积多项式的形式释放函数，一般是用于分布式学习和联邦学习下，但在响应边缘查询（k-way Margin Query）时也提出了使用内积多项式的形式去简化查询函数（使用数学去定义查询函数），从而提升查询精度。 <br> - 实验代码：无 <br> - ☑️ 组内汇报：
| [Answering Multi-Dimensional Analytical Queries under Local Differential Privacy](https://dl.acm.org/doi/10.1145/3299869.3319891) | Tianhao Wang | 2019 | pure-LDP概念。三种频率估计机制：单维和多维下的HIO机制、SC拆分再联接机制。 <br> - 实验代码：https://github.com/vvv214/LDP_Protocols  <br> - ☑️ 组内汇报：
|[Continuous Release of Data Streams under both Centralized and Local Differential Privacy](https://dl.acm.org/doi/10.1145/3460120.3484750)| Tianhao Wang |2019| 主要描述的是在数据流发布环境下如何使用DP和LDP对数据流施加差分隐私保护，同时作者提出了两个框架，一个是基于DP的ToPS框架，一个是基于LDP的ToPL框架。 <br> - 实验代码：https://github.com/dp-cont/dp-cont <br> - ☑️ 组内汇报：

## LDP/DP下的优化技术
| Title | Team/Main Author | Venue and Year | Key Description
| :------------| :------ | :---------- | :-----------------------
| [The Matrix Mechanism: optimizing liner counting queries under differential privacy](https://link.springer.com/article/10.1007/s00778-015-0398-x)| Chao Li | 2015 | 本文提出的矩阵机制(MM)可以更准确回答计数查询集，并可以通过迭代求解半定规划计算最优策略。 <br> - 实验代码：无 <br> - ☑️ 组内汇报：
| [Query optimization for differentially private datamanagement system](https://ieeexplore.ieee.org/document/6544900)|Peng, Shangfu|2013|本文提出了 Pioneer，这是一种适用于 DP 兼容 DBMS 的有效且高效的查询优化器,其构建了一个重用历史查询的执行方案，以尽量减少隐私预算的使用。它还包括一种有效的算法，用于选择有助于回答新传入查询的历史查询，并且方案计算和历史查询选择的计算成本可忽略。 <br> - 实验代码：无 <br> - ☑️ 组内汇报：

## LDP/DP与机器学习相结合
| Title | Team/Main Author | Venue and Year | Key Description 
| :------------| :------ | :---------- | :-----------------------
|[Optimal Algorithms for Mean Estimation under Local Differential Privacy](https://proceedings.mlr.press/v162/asi22b.html)|Hilal Asi, V. Feldman, Kunal Talwar|2022/ICML|用于处理聚合过程中的均值估计的问题，开发了一种基于高斯机制的PrivUnit方法，通过采样的方式降低噪声引入带来的误差。 <br> - 实验代码：无 <br> - ☑️ 组内汇报：
| [Empirical Risk Minimization in the Non-interactive Local Model of Differential Privacy](https://jmlr.org/papers/v21/19-253.html)|  Di Wang | 2020 | 这篇文章基于前人工作（伯恩斯坦多项式机制、非交互式差分隐私方面等提出了使用内积多项式的方法释放函数，还提出了1-bit的通信方法，能够使泛化误差的上界更为紧致，且对样本量n的依赖度降为多项式级别，但是问题在于这只是理论上的，作者也表明了不知道在现实中的应用效果是怎么样的）。 <br> - 实验代码：无 <br> - ☑️ 组内汇报：

## LDP/DP与联邦学习相结合
| Title | Team/Main Author | Venue and Year | Key Description 
| :------------| :------ | :---------- | :-----------------------
| [LDP-FL: Practical Private Aggregation in Federated Learning with Local Differential Privacy](https://www.ijcai.org/proceedings/2021/217)|Lichao Sun | 2021/IJCAI |本文针对在多层神经网络中存在隐私预算爆炸的问题提出了LDP-FL框架，不仅很好的保护了隐私，而且通过分割洗牌机制降低了隐私预算在多层迭代中的激增. <br> - 实验代码：无 <br> - ☑️ 组内汇报：
| [LDP-Fed: Federated Learning with Local Differential Privacy](https://dl.acm.org/doi/10.1145/3378679.3394533)|Stacey Truex|2020/EdgeSys |本文提出了LDP-Fed框架，LDP 模块为在多个个体参与者的私有数据集上的大规模神经网络联合训练中模型训练参数的重复收集提供了正式的差分隐私保证。其次，LDP-Fed实现了一套选择和过滤技术，用于扰动和与参数服务器共享选择的参数更新. <br> - 实验代码：无 <br> - ☑️ 组内汇报：

## LDP/DP下的隐私保护数据库查询
| Title | Team/Main Author | Venue and Year | Key Description 
| :------------| :------ | :---------- | :-----------------------
| [Better than Composition：How to Answer Multiple Relational Queries under Differential Privacy](https://dl.acm.org/doi/10.1145/3589268)| Wei Dong, Dajun Sun, Ke Yi|2023/ACM Maanage.Data|将单查询机制扩展到多个查询的标准解决方案是通过隐私组合。然而，这可能会产生一个误差范围，该误差范围可能比最优值差根号d因子，其中d是查询数量。在本文中，提出了一种不同的、更全面的方法来缩小这一差距. <br> - 实验代码：https://github.com/hkustDB/PMSJA <br> - ☑️ 组内汇报：
| [Residual Sensitivity for Differentially Private Multi-way joins](https://dl.acm.org/doi/10.1145/3448016.3452813)| Wei Dong, Ke Yi| 2021/SIGMOD |为了解决连接查询下差分隐私噪声敏感度过大以及计算效率的问题，本文提出残差查询和残差敏感度或最大边界，使敏感度计算满足高效率、高效用以及可一体化. <br> - 实验代码：https://github.com/hkustDB/ResidualSensitivity <br> - ☑️ 组内汇报：

## LDP/DP下的大语言模型(LLM)隐私保护
| Title | Team/Main Author | Venue and Year | Key Description 
| :------------| :------ | :---------- | :-----------------------
| [DP-Forward: Fine-tuning and Inference on Language Models with Differential Privacy in Forward Pass](https://doi.org/10.1145/3576915.3616592)|Minxin Du, Tianhao Wang, et al|2023/CCS|本文介绍了一种在前向传递中扰乱嵌入矩阵的方法，以实现差分隐私的语言模型微调和推理. <br> - 实验代码：https://github.com/xiangyue9607/dp-forward <br> - ☑️ 组内汇报：

## 基于混洗模型的DP(Shuffle DP)
| Title | Team/Main Author | Venue and Year | Key Description 
| :------------| :------ | :---------- | :-----------------------
| [Improving Utility and Security of the Shuffler-based Differential Privacy](http://www.vldb.org/pvldb/vol13/p3545-wang.pdf)|Tianhao Wang, Bolin Ding, Min Xu, et al|2020/VLDB Endow|本文从两个角度研究了差分隐私的洗牌模型。首先，从算法角度进行研究，并对现有技术进行改进。其次，从模型的安全性角度出发，强调了两种攻击类型：串通攻击和数据中毒攻击；随后，提出了在这些攻击下更加安全的 PEOS 协议。 <br> - 实验代码：https://github.com/vvv214/LDP_Protocols/tree/master/murs <br> - ☑️ 组内汇报：

# 三、其他相关文献

## AQP近似查询处理/Sketch草图技术
流算法（Streaming algorithms）:使用次线性的时间、空间成本，以很高的计算速度快速响应大型流数据的处理。缺点是只能得到近似真实值的结果，但是很多算法会给出相应估计误差界限。
| Title | Team/Main Author | Venue and Year | Key Description
| :------------| :------ | :---------- | :-----------------------
|[Persistent Data Sketching](https://dl.acm.org/doi/10.1145/2723372.2749443)|Zhewei Wei, Ke Yi|2015/SIGMOD|本文的是使草图持久化，从而使流式算法能够在历史上的任何先前时间回答查询，并且仍然有一个小的ε错误. <br> - 实验代码：无 <br> - ☑️ 组内汇报：
|[At-the-time and Back-in-time Persistent Sketches](https://dl.acm.org/doi/10.1145/3448016.3452802)|Benwei Shi, Zhuoyue Zhao, Feifei Li|2021/SIGMOD|本文提出了当时持久性（ATTP）和回溯性持久性（BITP）草图的概念，这些草图可以用小空间近似回答对先前版本的数据的查询. <br> - 实验代码：无 <br> - ☑️ 组内汇报：

## 关系数据库连接查询优化技术
| Title | Team/Main Author | Venue and Year | Key Description
| :------------| :------ | :---------- | :-----------------------
| [Random Sampling over Joins Revisited](https://github.com/Triumphhh/LDP-Afterreading/tree/main/lx)|Zhuoyue Zhao, Feifei Li, Ke Yi|2018/SIGMOD|本文对数据库连接采样的问题进行了回顾，总结了前人的方法与缺陷，并基于此提出改进。构建了连接随机采样框架统一化先前方法，并在更复杂场景下给出更加优化的方案来解决连接的随机采样. <br> - 实验代码：https://github.com/InitialDLab/SampleJoin <br> - ☑️ 组内汇报：
| [Wander join and XDB: Online aggregation via random walks](https://dl.acm.org/doi/10.1145/3284551)|Feifei Li, Bin Wu, Ke Yi, Zhuoyue Zhao|2017/SIGMOD|本文提出了一种新颖的采样算法对数据库连接进行采样，基于在线聚集利用随机游走的方式针对不同场景下的连接查询进行连接采样，得到独立非均匀地样本，具有高效性. <br> - 实验代码：https://github.com/InitialDLab/XDB <br> - ☑️ 组内汇报：

# 四、我们的工作
| Title | Team/Main Author | Venue and Year | Key Description
| :------------| :------ | :---------- | :-----------------------
|[Local differentially private frequency estimation based on learned sketches](https://doi.org/10.1016/j.ins.2023.119667)| Sixin Lin, Meifan Zhang|2023/Inf. Sci <br> - CCF-B| 在本文中，我们提出了一种基于 LDP 学习草图的大域数据的两阶段频率估计框架，该框架将高频项和低频项分开，以避免哈希冲突引起的误差. <br> - 实验源码：待发布
|[Sketches-based join size estimation under local differential privacy](https://ieeexplore.ieee.org/document/10598055)| Meifan Zhang, Xin Liu, Lihua Yin|2024/ICDE <br> - CCF-A|本文首次研究了本地化差分隐私下基于草图技术的数据库连接查询连接大小的隐私保护，提出了LDPJoinSketch实现了高效准确的连接大小估计，并通过两阶段的频率感知扰动技术进一步优化了估计准确性. <br> - 实验源码：https://github.com/Triumphhh/LDPJoinSketch/


# 五、通用数据与代码查询

> **机器学习相关论文查询**：https://paperswithcode.com/ <br>
> **数据集查找**：https://snap.stanford.edu/data/， https://www.kaggle.com/datasets

