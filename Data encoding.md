---
topics:
  - programming
  - data
  - pl
created: 2026-08-19
tags:
  - 0🌲
---

From [[Designing Data-Intensive Applications]]:

Distributed systems must be capable of **evolving** to scale. This includes two main concerns:
**Backwards compatibility:** Newer code can read data that was written by older code.
**Forwards compatibility:** Older code can read data that was written by newer code.

Encoding/decoding (serde) data allows for translation between a source language and a data shape.

It may be useful to retain a database of schema versions to check for compatibility.

Key idea: *Data outlives code.*