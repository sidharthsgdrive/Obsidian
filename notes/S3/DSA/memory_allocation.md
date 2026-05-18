## Introduction
- Memory allocation is the process of assigning portions of main memory to process when they are executed.
- Linked lists are used to represent free and allocated blocks of memory.
- **Avail list:**
	- Memory is divided into blocks/partitions.
	- An *Avail List* or *Free List* is a linked list that maintains information about free memory blocks.
	- Each node in the list contains
		- **Starting address** of the block
		- **Size** of the block
		- **Link** to the next block
***
## Comparison between allocation schemes

| Allocation Scheme | Description                                                                   | Advantages                                                                                                                                  | Disadvantages                                                               |
| ----------------- | ----------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| First fit         | Process is allocated to the **first free block** that is large enough         | Simple to implement.<br>Less allocation time.                                                                                               | Leads to external fragmentation (many small unusable holes near beginning). |
| Best fit          | Process is allocated to the **smallest available block** that can hold enough | Leaves larger free blocks available for bigger processes.<br>Reduces wastage of memory.                                                     | Allocation is slow.<br>Creates many small unusable fragments.               |
| Worst fit         | Process is allocated to the **largest free block** available                  | Leaves medium and small blocks free for other processes.<br>Reduces small fragmentation.<br>May be useful if mostly small processes arrive. | Wastes large memory blocks.<br>                                             |
***
## Answering questions
When choosing between fits:
- **Best fit** is preferred in theory (better memory utilization, reduces waste).
- **First fit** is preferred in real systems (faster allocation, less overhead).
- If worst fit ties with another scheme, it is rarely preferred due to poor utilization.
***
## Algorithms

**First fit:**
1. Mark all memory blocks as free
2. For each process:
	1. Start from first free block
	2. If process size \<= block size, 
		1. Allocate block to process
		2. Move to next process

**Best fit:**
1. Mark all memory blocks as free
2. For each process:
	1. Search entire list of free blocks for the *smallest block large enough to hold the process*
	2. Allocate the process to that block

**Worst fit:**
1. Mark all memory blocks as free
2. For each process:
	1. Search the entire list of free blocks for the *largest block available that can hold the process*
	2. Allocate the process to that block
***