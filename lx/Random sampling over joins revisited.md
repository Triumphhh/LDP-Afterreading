# Random sampling over joins revisited (1)

> Ke Yi , Feifei Li, Zhuoyue Zhao （SIGMOD’18)
> 
- Problem: Random sampling over joins
- Prior method: Simple random sampling\ Ripple Join\ Wander Join
- What we need : Uniform and Independent samples
    - Taking a random sample over the join and training the model with the sample can bring great savings for both join computation and training, while incurring a small and bounded loss in accuracy.
    - neither ripple join nor wander join can be used
- To obatain the samples above:
    - reject samples with approprite posibilities;
    - takes samples non-uniformly, guided by the statistical information.
    - however, above method only for 2 relation joins.
- Contribution:
    - design a general join sampling framework
    - existing algorithms are special cases
    - extend the framework to more complicated situations
    - extensive experimental evaluations
    - present extensions and limitations
- Problem defination: Join as a Hyper-Graph
    
    ![Untitled](Random%20sampling%20over%20joins%20revisited%20(1)%20250d48e16e7a46ea9b1ca7e466cbed83/Untitled.png)
    
- Sampling 2-relation joins:
    - Olken’s algorithm: based on the (max) frequency of attribute v in R2, maybe causing high rejection rate.
    - Chaudhuri’s algorithm: with frequency infomation available, return the join result without rejection, including using hybrid strategy to handle high-frequency values.
    - Both of above can be implemented if indexes are available on the join attribute, or a full scan is needed.
- Sampling multi-way foreign-key joins:
    - Archaya’s algorithm: only works for acyclic foreign-key joins with a single source relation.
        - there must be a commen attribute among all relations.
        - sampling from join results reduce to sampling from the source relation.
- A join sampling framework:
    - Basic idea: a tuple t should be sampled using weight w(t). But w(t) is not available , so using W(t), the upper bound of w(t), as a proxy with an approprite probability to reject.
    - some invariants:
    
    ![Untitled](Random%20sampling%20over%20joins%20revisited%20(1)%20250d48e16e7a46ea9b1ca7e466cbed83/Untitled%201.png)
    
    - Algorithm 1: each join result will be returned with equal probability under invariants above.
    
    ![Untitled](Random%20sampling%20over%20joins%20revisited%20(1)%20250d48e16e7a46ea9b1ca7e466cbed83/Untitled%202.png)
    
    - Remarks:
        - The probability that (r0,t1,…,ti) is sampled is:
        
        ![Untitled](Random%20sampling%20over%20joins%20revisited%20(1)%20250d48e16e7a46ea9b1ca7e466cbed83/Untitled%203.png)
        
        - don’t need to have all W(t) as an input.
        - regardless of the choice of W(t), this algorithm always returns independent samples as well.
        - Olken’s and Chaudhuri’s methods are special cases of the algorithm above when it generates into the case n=2.
        
- Framework Instantiations
    - differ in algorithm 1 corresponds to differ in W(t).
    - tradeoff between latency and throughput: tighter upper bounds with high cost ↔ sample efficient; looser upper bounds with low cost ↔ low sample efficiency.
- Generalizing Olken’s algorithm
- Generalizing Chaudhuri et al’s algorithm
- Other join size upper bounds:
    - the AGM bound is the optimal bound on the join size when only the relation sizes are given. Instead, Olken’s bound can be much largger in some conditions.
    - if partial frequency information is available, handling the frequent and infrequent values separately.
    - upper bound the size of each subjoin with a threshold h, which indicates the tuple in R is heavy or light.
    
    ![Untitled](Random%20sampling%20over%20joins%20revisited%20(1)%20250d48e16e7a46ea9b1ca7e466cbed83/Untitled%204.png)
    
- Wander join as initialization
    - Observation: Wander join can not only be used to estimate |J|=w(r0), but also each intermediate join size w(t).
    - estimation on w(t) is based on the central limit theorem, which requires a minimun sample size to hold.
    - a threshold θ is set and after θ random walks have passed through, set W(t) to be the upper bound of the confidence interval.
    - raise W(t) in a bottom-up fashion to restore Invariant(3) for all W(t)’s.
    - executing algorithm1: run the dynamic program top-down, computing and memorizing only those W(u)’s that are needed for computing w(t’).
    - algorithm 1 also perfroms random walks while leading to tighter upper bounds as more samples being returned.
- Other types of joins
    - Acyclic join queries
        - basic idea: whenever reaching a relation that has more than one  child below, branching the sampling process into two subtrees.
        - Invariants changes in this situation:
            
            ![Untitled](Random%20sampling%20over%20joins%20revisited%20(1)%20250d48e16e7a46ea9b1ca7e466cbed83/Untitled%205.png)
            
        - Algorithm 2 : Acyclic sample
            
            ![Untitled](Random%20sampling%20over%20joins%20revisited%20(1)%20250d48e16e7a46ea9b1ca7e466cbed83/Untitled%206.png)
            
        - it turns into a recursive algorithm. line 2 and 6 iteratively tighten the join size upper bounds, hence improving the sampling efficiency over time.
    - Cyclic queries
        - break up all the cycles in the query hyper-graph.
        - residual query & skeleton query. Usually residual query tends to be smaller.
        - Algorithm 3: Cyclic sample
            
            ![Untitled](Random%20sampling%20over%20joins%20revisited%20(1)%20250d48e16e7a46ea9b1ca7e466cbed83/Untitled%207.png)
            
        - Remarks:
            - this algorithm coincides with the wedge sampling on a triangle query.
            - it generates into the path sampling on sampling subgraph patterns with 4 vertices.
            - the algorithm generalizes graph sampling algorithms to arbitrary hyper-graphs.
            - how to decompose the query
    - Selection predicates
        - simply push them down to relations
        - enforce them during the sampling process