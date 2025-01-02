### *Introduction:*

- Discusses the concept of CAP Theorem (Consistency, Availability, Partition Tolerance) and its relevance in distributed systems.
- Emphasizes the importance of considering CAP constraints early in system design to avoid costly changes later.

### *CAP Theorem:*

- *CAP:* Stands for Consistency, Availability, Partition Tolerance.
- *Desired Properties of Distributed Systems:* These three properties are desirable in a distributed system.
- *CAP Trade-off:* You cannot have all three properties simultaneously. You must choose two out of the three.
- *Example:*
    - Consider a distributed database with nodes in India and the US.
    - A user's data is replicated across both locations.
    - A distributed system should ideally be consistent (same data everywhere), available (responding to requests), and tolerant to partitions (network disruptions).

### *Understanding Each Property:*

- *Consistency:* Ensures that all nodes have the same, up-to-date data at any given time.
- *Availability:* Guarantees that every request is successfully processed by at least one node.
- *Partition Tolerance:* Allows the system to continue functioning even if communication between nodes is disrupted.

### *Why CAP Properties Cannot Co-Exist:*

- *Case 1: CA (Consistency and Availability) - Not possible with Partition Tolerance*
    - *Scenario:* A partition occurs, separating nodes A and B.
    - *Conflict:* Node A writes updated data, but node B cannot access it due to the partition.
    - *Result:* Inconsistency between nodes.
- *Case 2: CP (Consistency and Partition Tolerance) - Not possible with Availability*
    - *Scenario:* A partition occurs, separating nodes A and B.
    - *Strategy:* To maintain consistency, only one node (A) is allowed to process writes.
    - *Result:* Node B becomes unavailable for writes during the partition.
- *Case 3: AP (Availability and Partition Tolerance) - Not possible with Consistency*
    - *Scenario:* A partition occurs, separating nodes A and B.
    - *Strategy:* To maintain availability, both nodes can process writes.
    - *Result:* Potential for inconsistent data between nodes.

### *CAP Trade-off in Real-world Systems:*

- *Importance of Partition Tolerance:* In today's distributed systems, network disruptions are common.
- *Choosing between CP and AP:*
    - *CP:* Choose this option for systems where consistency is critical, even if it means some temporary downtime.
    - *AP:* Choose this option for systems where availability is paramount, even if it means some data inconsistency.

### *Key Takeaways:*

- *Understanding CAP is crucial for effective distributed system design.*
- *Early consideration of CAP constraints can prevent costly changes later.*
- *The choice between CP and AP depends on the specific needs of your system.*
- *Partition tolerance is a key factor in modern distributed systems.*
