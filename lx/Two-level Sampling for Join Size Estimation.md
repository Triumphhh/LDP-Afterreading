# Introduction
在本文中，引入了一种新的连接规模估计的采样算法，称为两级采样，该算法结合了以往采样算法的优点，在多种连接上都优于之前的算法。未来工作的一个重要方向是将其集成到大规模分布式查询处理引擎中。最近关于复杂连接处理的研究表明，中间结果大小在决定使用的最佳连接算法中起着至关重要的作用，特别是在分布式环境中。因此，研究提出的算法如何为大规模分布式查询处理引擎做出贡献是非常有意义的。
# Clear Steps:
## First, it samples a small number of tuples from each relation involved in the join using uniform random sampling.
## Second, it performs a join on the sampled tuples using a hash-based algorithm and computes a join selectivity estimate based on the number of joined tuples and the sample sizes.
## Third, it uses a stratified sampling technique to divide each relation into strata based on their join attribute values and samples more tuples from each stratum using a weighted sampling scheme that considers both the join selectivity estimate and the stratum size.
## Fourth, it performs another join on the enlarged samples using a hash-based algorithm and computes a refined join size estimate based on the number of joined tuples and the sample sizes.
## Advantages:  it can handle arbitrary selection predicates, reduce sampling errors by exploiting correlation information, avoid unnecessary sampling by pruning irrelevant strata,and adjust sample sizes dynamically according to data characteristics.
