## Min-heap

```python
import heapq

heap = [1, 5, 4, 6, 7]
heapq.heapify(heap)
heapq.heappush(heap, 3)
heapq.heappop(heap)
```

## Segment tree

Idea: To maintain a dynamic prefix sum, construct smaller intervals and combine them to produce larger intervals.

Requires $O(N)$ space complexity.

Also see: Square Root Decomposition, Mo's Algorithm