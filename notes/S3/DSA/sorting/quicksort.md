## Idea
- works on the idea that **an element is sorted if the elements before it are lesser and the elements after it are greater**.
- is a **divide & conquer** type algorithm.

> [!note] 
>In the questions whenever we use Quick sort algorithm without explicitly saying
the pivot element, we always assume the pivot is selected as the first element. 

### Partitioning algorithm
```Python
partition(low, high):
	pivot = A[low]
	i = low - 1
	j = low 
	swap(A[low], A[high]) # put pivot at end, even though we chose first ele
	while j < high:
		if A[j] <= pivot:
			i += 1; 
			swap(A[i], A[j])
		j += 1; # increment j at the end of each iteration
	swap(A[i+1], A[high]) # set high (which is pivot) to its correct place
```

++Example++
![[Pasted image 20250908212855.png]]

#### Resources
- [Abdul Bari's Quicksort](https://www.youtube.com/watch?v=7h1s2SojIRw) -- to get an idea of how it works
- [KC Ang's partitioning algorithm](https://www.youtube.com/watch?v=MZaf_9IZCrc) -- in line with Soni sir's algorithm
