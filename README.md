# Question 1
Cache Replacement Policies: (30 points)
FIFO: 
In case of a conflict, the cache evicts the block accessed first without any regard to how often or how many times it was accessed before.

Compare the performance of these policies with LRU (already implemented in the simulator).

# Question 2

Prefetcher: (70 points)
Stream Buffers with Sequential Prefetching:
On a cache miss, fetch the requested address A, and the k subsequent addresses in a buffer (k being the depth of the buffer). When the processor accesses address A+1, it will be moved up from stream buffer to processor’s cache. The first entry of the buffer would now be A+2. Following this, the prefetcher would fetch A+k+1 into the buffer.
Multiple such buffers exist - each of which would maintain a separate prefetch stream. For each new miss, replace the stream buffer which was least recently used. (Take depth = 4 entries and number of stream buffers = 8)
Compare the performance of this scheme with no prefetching and Next Line Prefetching (already implemented in the simulator).

