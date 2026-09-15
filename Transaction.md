---
topics:
  - dist-sys
  - programming
created: 2026-09-14
tags:
  - 0🌲
---

From [[Designing Data-Intensive Applications]]:

**ACID** acronym: Atomic, Consistent, Isolated, Durable

---

Isolation can be very difficult due to **write skew**, where consistency rules are dependent on many columns and states.

**Serialisable isolation** is a guarantee that even though transactions may be processed in parallel, they can effectively be **serialised**, i.e. placed in a known order, as if they were running on a single process.

---

Since network requests introduce latency, clients can invoke **stored procedures** which are kept on server disks. This eliminates the back-and-forth overhead. Stored procs can be implemented in custom DSLs, or in general purpose languages like Lua for Redis. [[Functional programming]] is also an interesting topic to explore here: if stored procs are deterministic, they can be [[Replication|replicated]].

---

**Pessimistic** concurrency control avoids all conflict, but may lead to slow throughput or poor concurrency. This is the method used by serial execution, 2PL, and index-range locking. On the flipside, **optimistic** concurrency control assumes everything goes well, then resolves conflicts if they occur (potentially by aborting).