---
topics:
  - programming
  - systems
  - low-level
created: 2026-08-24
tags:
  - 0🌲
---

From [[What's a Memory Allocator Anyway - Benjamin Feng]]:

Various allocation strategies:
- Page allocator: Handled by OS
- Bump allocator: Stores a simple offset pointer
- Arena allocator: Bump allocator with expandable memory (requires a backing allocator, e.g. a page allocator)
- Free list: Slower, requires $O(N)$ scanning
- Free lists with size buckets: Reduces memory fragmentation, faster lookups
- Slab allocator: Stores memory in an array; good memory locality

## Related

- [[4. Memory]]
- [[8. Dynamic Memory]]