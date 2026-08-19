---
topics:
  - programming
  - systems
  - dist-sys
created: 2026-08-19
tags:
  - 0🌲
---

> As a system *grows*, there should be reasonable ways of dealing with that growth.

From [[Designing Data-Intensive Applications]]:

**Load parameters:** Ways to describe load on a system. E.g. requests per second, ratio of reads to writes for a DB, etc.

> [No free lunch theorem](https://en.wikipedia.org/wiki/No_free_lunch_theorem)
> The idea that no algorithm is "better" than another; when reading/writing to services, we decide where to "spend" the effort - slower reads or slower writes?

**Response time:** The response delay, including network travel time, queues, and processing time.

We usually measure response time using percentiles: p95, p99, p999, etc.