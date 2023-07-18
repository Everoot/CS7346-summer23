# Quasar: Resource-Efficient and QoS-Aware Cluster Management

Abstract

Cloud computing promises flexibility and high performance for users and high cost-efficiency for operators. Nevertheless, most cloud facilities operate at very low utilization, hurting both cost effectiveness and future  scalability. 

We present Quasar, a cluster management system that increases resource utilization while providing consistently high application performance. Quasar employs three techniques. First, it does not rely on resource reservations, which lead to underutilization as users do not necessarily understand workload dynamic and physical resource requirements of complex codebases. Instead, users express performance constraints for each workload, letting Quasar determine the right amount of resources to meet these constraints at any point. Second, Quasar uses classification techniques to quickly and accurately determine the impact of the amount of resources (scale-out and scale-up) 