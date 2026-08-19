---
topics:
  - programming
  - data
  - systems
created: 2026-08-19
tags:
  - 0🌲
---

From [[Designing Data-Intensive Applications]]:

## Storage systems

The simplest **key-value store** can be implemented with an append-only file. Append for inserting/updating values, then scan the whole file for reads.
- Not a terrible idea; in fact, writes are super quick and easier to implement concurrently due to append-only restriction.
- However, reads are `O(N)` time, which is bad...

Ultimately we're trying to balance reading and writing efficiency.

**Hash index**: Maintain a hash table of keys to offsets in the log file to allow for faster indexing.

**Storage segment**: Stores a small chunk of append-only data. Background worker occasionally merges storage segments together, cleaning duplicates / deleted data (tombstones). New queries then routed to merged segment.

**SSTable (Sorted String Table)**: Segment files maintain keys in sorted order.
- Merging segments becomes easy, similar to the merge sort algorithm: Continually take lexicographically smallest key and append to new segment.
- If we know offsets for surrounding keys, we can simply loop through a small section of data to find target key. This means index table can be sparse and tiny.
- We can compress ranges of records before writing to disk!

**LSM-Tree (Log-Structured Merge-Tree)**: Since memory is faster than disk, handle queries by first modifying a Red-Black / AVL tree. Once the in-memory tree (a.k.a. **MemTable**) grows too large, it is flushed to disk as an SSTable (which can then be merged).

**B-Tree**: A binary tree with multiple children, fetching optimised by **pages** (less trips to disk). Links between leaf nodes make range queries easy.

Since crashes can be catastrophic, corruption handling is a common problem in data storage (especially in memory). Disk is considered more **durable** due to ability to survive power loss. Two examples of ways to handle:
- Maintain an append-only log on disk, then re-run operations in event of crash. Used for LSM-Trees.
- Maintain a **write-ahead log (WAL)** to note every operation before performing it. Used for B-Trees.

**Multi-column indexes**: Allow for queries based on multiple columns; e.g. "cities between these longitudes and latitudes" (requires long + lat columns).

**Fuzzy indexes**: Allow for searching for *similar* keys.

**In-memory key-value store**: Since we now have a lot of memory (supposedly), simply keep everything in memory.
- Counter-intuitively, performance gain isn't mainly due to not needing to access disk; it's due to not having to *format* data in a way that is writable to disk.

## Transaction processing or analytics?

**Online transaction processing (OLTP)**: High throughput, takes in less data to deliver immediate queries.

**Online analytic processing (OLAP)**: Slower, consumes and aggregates more data for a more holistic view (think financial reports).

**Data warehouse**: OLTP and OLAP are commonly split into separate systems since OLAP will bottleneck OLTP. A data warehouse is where OLAP is performed.

**Extract-Transform-Load (ETL)**: Moving data from OLTP database into data warehouse.

**Star schema**: Maintains a central **fact table**, logging all events. Some columns may refer to **dimension tables** for normalisation.

A way to remember:
> Twinkle twinkle little star, How I query what you are!
- Query for dimension tables
- Lots of stars in the night sky = lots of events logged

**Snowflake schema**: Dimension tables may refer to further dimension tables for more normalisation.

Star schemas / data warehouses usually maintain data in columnar format, since `SELECT` statements usually only deal with a few *columns* at a time, meaning we can cut down on the amount of data being processed by only looking at relevant columns.