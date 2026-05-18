## Memory deallocation -- compaction
- Compaction is a memory management technique used to collect scatterred free memory fragments into one **large contiguous block**, thereby **removing external fragmentation**.
- **Advantages:**
	- Removes external fragmentation
	- Efficient memory usage
	- Supports loading of large processes
- **Disadvantages:**
	- Time-consuming
	- CPU remains idle using compaction
	- Not always possilbe in real systems
***
## Garbage collection
- GC is the process of (either automatically or manually) reclaiming memory that is **no longer in use** by the program, for reuse.
- **Need:**
	- Prevent memory learks
	- Avoid dangling pointers
	- Improve memory utilization
- **Techniques:**
	- Mark & Sweep: Marks reachable objects and frees unmarked memory
	- Reference counting: Keeps a count of references, and frees memory when count is zero.
	- Copying: Copies live objects to another space, leaving garbage behind.
- **Difference from Compaction:**
	- While GC frees memory that is no longer used, compaction rearranges memory to eliminate fragmentation.
	- GC identifies garbage, while compaction reorganizes memory.
***