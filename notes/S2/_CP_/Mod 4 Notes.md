# Static Memory Allocation vs Dynamic Memory Allocation

| SI. No. | Static Memory Allocation                                                                     | Dynamic Memory Allocation                                                 |
| ------- | -------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| 1       | variables get allocated permanently, till the<br>program executes or function call finishes. | variables get allocated only if the program<br>unit gets active.          |
| 2       | Static memory allocation is done before<br>program execution, i.e., during compile time.     | Dynamic memory allocation is done during<br>program execution.            |
| 3       | It uses stack for managing the allocation of<br>memory.                                      | It uses heap for managing the allocation of<br>memory.                    |
| 4       | It is less efficient                                                                         | It is more efficient                                                      |
| 5       | There is no memory re-usability                                                              | There is memory re-usability and memory<br>can be freed when not required |
| 6       | Once the memory is allocated, the memory<br>size cannot change.                              | The memory size can be changed.                                           |
| 7       | Execution is faster than dynamic memory<br>allocation.                                       | Execution is slower than static memory<br>allocation.                     |
| 8       | Allocated memory remains same from start<br>to end of the program.                           | Allocated memory can be released at any<br>time during the program.       |

#  Dynamic memory allocation functions
1. malloc():
	* stands for memory allocation
	* allocates a single large block of memory with the specified size
	* `ptr = (cast-type *) malloc(n * sizeof(type));`
2. calloc():
	* stands for contiguous allocation
	* allocates specified no. of blocks of memory of specified type
	* `ptr = (cast-type *) calloc(n, sizeof(type));`
3. realloc():
	* changes memory location of previously allocated memory
	* `ptr = (cast-type *) realloc(ptr, new_size);`
4. free():
	* de-allocates memory
	* `free(ptr);`

# Reading and writing in files
1. fscanf(): `fscanf(fp, "controlstring", &var);`
2. fgetc(): `fgetc(fp);`
3. fgets(): `fgets(string, length, fp);`
4. fprintf(): `fprintf(fp, "controlstring", var);`
5. fputc(): `fputc(var, fp);`
6. fputs(): `fputs(string, fp);`
# Other file pointer operations
1. `feof(fp)`: if all data has been read, returns nonzero integer; else returns zero
2. `ferror(fp)`: if errors, returns nonzero integer; else returns zero
3. `n = ftell(fp);`: returns offset corresponding to current position (n bytes have been read/written)
4. `fseek(fp, offset, position);`: offset may be + or -, position may be 0,1,2
5. `rewind(fp);`: resets fp position to start of file