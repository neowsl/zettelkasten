---
topics:
  - programming
  - dist-sys
created: 2026-08-19
tags:
  - 0🌲
---

From [[Designing Data-Intensive Applications]]:

One of the most common ways to distribute storage/compute is to use a **leader-follower** architecture. Leaders are responsible for actually performing computation, followers are for scaling out reads and network communication.

**Failover**: When a leader dies (noticeable with dropped heartbeats), a new leader is elected among the followers.

It's difficult to replicate statements, as the **ordering** is extremely difficult, if not impossible, to get correct. Therefore, most storage systems replicate via another form of data representation.

**Read-your-writes**: Allowing a client to immediately read what they have written. Can be handled via topology and routing. Can also be implemented using a [[Lamport clock]].
**Monotonic reads:** Once a client has read something, it can't read any changes earlier than that timestamp.
**Consistent read prefixes:** Ensuring [[causality]] holds.

If we have more than one leader at a time, that's **multi-leader replication**. This allows leaders to be physically closer to their clients, but requires much more difficult **conflict resolution**. A leader doesn't even have to be in a data centre: an offline device can be a leader, or collaborators on a Google Doc can be leaders.

**Convergence:** All replicas must arrive at the same final value when all changes have been replicated.

Can also replicate via **leaderless replication**. In this case, data validity is handled via **quorums** and Last-Write-Wins (LWW). [[Concurrency|Concurrent]] writes require careful consideration.

> If there are $n$ replicas, every write must be confirmed by $w$ nodes to be considered successful, and we must query at least $r$ nodes for each read. As long as $w + r > n$, we expect to get an up-to-date value when reading.

## Related

- [[8. Special Relativity]]