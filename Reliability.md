---
topics:
  - programming
  - systems
created: 2026-08-19
tags:
  - 0🌲
---

> A system should continue to work *correctly*, even in the face of *adversity*.

From [[Designing Data-Intensive Applications]]:

Since we can't tolerate every kind of fault (e.g. a black hole), we define what kinds of fault we should tolerate.

Netflix's [chaos monkey](https://netflix.github.io/chaosmonkey) is useful for random fault injection.

Hard disks have a mean time to failure (MTTF) of 10-50 years, so with 10,000 disks, on disk will die per day on average.