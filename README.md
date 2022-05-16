[TOC]



### CCF A

#### NSDI

##### 2022

###### 标题：MLaaS in the Wild: Workload Analysis and Scheduling in Large-Scale Heterogeneous GPU Clusters

摘要：随着机器学习 (ML) 的持续技术进步和最近大规模数据集的可用性，科技公司正在部署大型ML即服务 (MLaaS) 云，通常使用异构gpu，以提供大量ML应用程序。但是，在异构GPU集群中运行各种ML工作负载会带来许多挑战。在本文中，我们对从具有超过6,000个gpu的生产MLaaS集群中收集的两个月工作负载跟踪进行了表征研究。我们解释了集群调度带来的挑战，包括低GPU利用率、长时间排队延迟、存在难以调度的任务，这些任务要求高端GPU具有挑剔的调度要求、异构机器之间的不平衡负载以及cpu上的潜在瓶颈。我们描述了我们目前的解决方案，并呼吁对仍有待解决的挑战进行进一步调查。我们已经发布了用于公共访问的跟踪，就工作负载和集群规模而言，这是最全面的。

简介：针对**混合GPU集群**，提供ML服务问题。利用阿里GPU数据集，描述了GPU低利用率，排队高延迟，苛刻的调度，异质调度平衡及CPU瓶颈。本文提出了简单对策。

##### 2021

###### 标题：Ownership: A Distributed Futures System for Fine-Grained Tasks

摘要：

简介：针对执行细粒度计算的应用，基于ownership机制（给每个object一个leader），提出了一种支持**容错**而不降低效率的分布式futures系统，实现了scale,latency,failure方面的改进。

PS：分布式futures指其值最终可能存储在远程节点的引用。

#### OSDI

##### 2018

###### 标题：Ray: A Distributed Framework for Emerging AI Applications

简介：基于动态执行引擎，提出一种支持 **task-parallel** 和 **actor-based copute** 的计算。Ray还使用了**调度**和**容错存储**。在扩展性和性能方面达到最优。

#### SIGCOMM

##### 2021

###### 标题：Hoplite: Efficient and Fault-Tolerant Collective Communication for Task-Based Distributed Systems

简介：针对task-based systems(e.g., Ray, Dask, Hydro) ，优化了集体**通信**库(e.g., MPI, Horovod, NCCL),并提供了**容错**机制。（主要包括异步梯度下降、强化学习和模型服务。）

1.动态计算数据传输计划，通过细粒度的流水线执行。

2.当一项任务失败时，数据传输计划会调整，允许其他任务继续进行。

#### SIGKDD

##### 2021

###### 标题：Simple and Automatic Distributed Machine Learning on Ray

简介：

- 描述ML训练的痛点	
- 介绍了主流的训练策略。实现ML自动并行化，并编译系统架构。
- 参数选取和资源分配策略。
- 基于Ray接口编程。

#### SOSP

##### 2019

###### 标题：Lineage Stash: Fault Tolerance Off the Critical Path

简介：**容错**的两种方法：checkpoint& lineage。前者在执行时开销小，恢复时开销大。后者相反。本文提出方法降低了运行时开销而不影响恢复时开销。

本文不是在任务执行之前记录任务的信息，而是异步记录它。

### CCF B 

#### HotOs

##### 2017

###### 标题：Real-Time Machine Learning: The Missing Pieces

简介：针对**实时机器学习**，如毫秒延时，任务图自构建，异构内核。本文提出一种具有概念验证架构的候选方法。

### CCF C

#### BIGDATA

##### 2017

###### 标题：Imbalance in the Cloud: an Analysis on Alibaba Cluster Trace

简介：

### arvix

##### 2022

###### 标题：Exoshuffle Large-Scale Shuffle at the Application Level

简介：针对**shuffle**的1从头构建，2系统单一性导致的灵活性不足问题，本文提出shuffle的抽象实现,即**distributed futures**。这是第一次构建支持大范围的shuffle组件。实现了1优于之前shuffle系统，2与数据处理应用完美衔接。



### SCI

##### 2017

###### 标题：Ensemble learning for data stream analysis: A survey(2017)

简介：针对处理大数据的空间和时间成本问题，其同时具有的非稳定性特征，**集成学习**很重要。本文调查了用于数据流分类和回归任务的集成学习。介绍了先进的学习概念如不平衡数据流，新奇检测，半监督，复杂信息表示和结构输出。

### 其他

###### 标题：SPARKNET TRAINING DEEP NETWORKS IN SPARK(2016，192引用)    

简介：针对批处理训练框架的不支持异步和通信密集型负载，提出Sparknet，提供获取信息的接口和扩展规模的接口。提供在IMageNet上量化了加速比，通信频率，开销数据。

###### 标题：Towards Creating a Generalized Complex Event Processing Operator Using FlinkCEP: Architecture & Benchmark(2021)

PS：Complex Event Processing (CEP)

简介：**FlinkCEP**将模式检测扩展到集群和云。FlinkCEP语言具有高表达能力和要监控的模式参数化繁琐。本文提出了能扩展正则表达的输入规范和自动重写的operator。





### 团队：

#### UC Berkely

- I. Stoica

  

- Philipp Moritz

  

- Robert Nishihara

  

- Stephanie Wang

![image-20220506151127255](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20220506151127255.png)