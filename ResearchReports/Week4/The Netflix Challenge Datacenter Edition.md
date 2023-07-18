# The Netflix Challenge: Datacenter Edition

1. Category: What type of paper is this?

   A: A description of a research prototype.



2. Context: Which other papers is it related to? Which theoretical based were used to analyze the problem?

   A: 

   [1] L. A. Barroso. ”Warehouse-Scale Computing: Entering the Teenage Decade”. ISCA Keynote, SJ, June 2011.
   [2] L. A. Barroso, U. Holzle. ”The Datacenter as a Computer”. Synthesis Series on Computer Architecture, May 2009.
   [3] R. M. Bell. Y. Koren, C. Volinsky. ”The BellKor 2008 Solution to the Netflix Prize”. Technical report, AT&T Labs - Research, October 2007.

   [5] Amazon Elastic Compute Cloud-EC2. http://aws.amazon.com/ec2/ 

   [6] Google AppEngine. http://code.google.com/appengine/

   [9] J.Mars, L.Tang et al. ”Heterogeneity in ”Homogeneous” WarehouseScale Computers: A Performance Opportunity”. In IEEE CAL, 2011.
   [10] J. Mars, L. Tang, et al. ”Bubble-Up: Increasing Utilization in Modern Warehouse Scale Computers via Sensible Co-locations”. In Proc. of MICRO-44, Sao Paolo, 2011 [11] R. Narayanan, B. Ozisikyilmaz, et al. ”MineBench: A Benchmark Suite for DataMining Workloads ”. In Proc. of IISWC, CA, 2006.

   [15] Windows Azure. http://www.windowsazure.com/

   "ADSM overcomes the drawbacks of previous techniques, by leveraging robust and computationally efficient analytical methods to scale to tens of thousands of applications with minimal overheads."

   

3. Correctness: Do the assumptions appear to be valid?

   A: Yes

   

4. Contributions: What are the paper's main contributions?

   A: Over 390 real DC workloads, ADSM improves performance by 16% on average and up to 2.5x and efficiency by 22% in a DC with 10 different server configurations.

   



5. Clarity: Is the paper well written?

   Yes.





Understand the relationship between the Netflix challenge and the cluster resource allocation problem.





Introduction

Warehouse-scale systems now provide the compute and storage infrastructure for most popular online services, making their performance and power optimization critical design challenges. In this work, we examine one aspect of DC architectures which until recently has gone mostly unnoticed and has significant performance and energy potential. DCs have traditionally been embraced as homogeneous platforms. However, as machines get replaced over the 150-year provisioned deployment lifetime, they introduce some inherent heterogeneity in the system. This heterogeneity is at the platform level, differs from the one found in CMPs, and ignoring it can lead to significant inefficiencies.

Previous work has quantified the performance potential from sophisticated placement of workloads to heterogeneous machines. However, the proposed schemes rely mainly on empirical observations, require detailed profiling and do not scale beyond a small number of applications. This makes them unsuitable for virtualized environments that host thousands of new applications every day (e.g., EC2, Azure, Google AppEngine, or vMotion). Additionally, these schemes focus on performance, not energy savings. As a result, applications are mapped to serves with limited heterogeneity considerations. Going forward, heterogeneity-aware workload mapping is critical and doing so in a computationally efficient manner is a strict constraint for scalability.

We present Application to Datacenter Server Mapping (ADSM), a scalable and efficient scheme for application-to-server mapping that addresses the limitations of previous proposals. ADSM is derived from validated, computationally efficient analytical methods, not merely empirical observations, which allow it to scale to tens of thousands of servers and applications, improving system performance and efficiency, while enforcing strict per-application QoS guarantees, marginal overheads and tight error bounds It is designed as a lightweight controller that resides with the cluster scheduler and requires minimal changes to the system. ADSM identifies similarities between incoming an known applications and makes efficient recommendations of application placement to heterogeneous servers. Additionally, because the recommendation system is driven by analytical methods we can explicitly compute its complexity and guarantee marginal training and decision overheads. ADSM is based on a recommendation system similar to the one deployed as part of the Netflix Challenge, with user replaced by applications and movies by server configurations.

We evaluate ADSM for a wide range of applications: single-threaded, multi-threaded and multiprogrammed standard benchmark suites and 390 real DC workloads from Microsoft, including latency-critical(e.g., Search) and computationally-intensive applications. We use two 40-machine clusters; a "homogeneous" production cluster, with ten server configurations and a heterogeneous cluster with ten high-end and low-power machine types.

First, we quantify the mapping algorithm's benefits and overheads. ADSM improves performance by 22% and energy efficiency by 18% on average in the "homogeneous" cluster, over a heterogeneity-oblivious mapping scheme. The results are more striking in the heterogeneous cluster. ADSM not only does not degrade performance when mapping applications to the low-power systems, but improves it by 17% while reducing energy by 24% on average. ADSM, thus, motivates more radical heterogeneity in DCs, showing its efficiency potential, while enforcing strict QoS guarantees. Second, we validate the accuracy of the analytical methods that drive ADSM. Finally, we perform a sensitivity study on configuration parameters, such as training set size and time and strictness of QoS guarantees.