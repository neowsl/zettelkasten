---
topics:
  - programming
  - data
  - dist-sys
created: 2026-08-19
tags:
  - 0🌲
---

From [[Designing Data-Intensive Applications]]:

A network request is different from a local function call in that it introduces a third case (other than returning or erroring): Network requests can **timeout**. This requires considerations of retry and idempotence.

According to DDIA, we shouldn't try to make a remote service look too much like a local object *because they are fundamentally different*.

We can introduce middleware to facilitate message-passing, through middleware like RabbitMQ or Apache Kafka. Can also use an **actor model**, where services send messages to each other, knowing some may get lost.