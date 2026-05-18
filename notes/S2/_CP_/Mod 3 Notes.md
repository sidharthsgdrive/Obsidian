
| CALL BY VALUE                                                                    | CALL BY REFERENCE                                                               |
| -------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| A copy of the actual arguments is passed to<br>formal arguments                  | The reference to the original arguments is<br>passed                            |
| The called function works with the formal<br>arguments                           | The called function works with the actual<br>arguments, but with the alias name |
| The changes made in the formal arguments<br>will not affect the actual arguments | The changes made in the formal arguments<br>do affect the actual arguments      |
| Memory is wasted for duplication of the<br>same data                             | Memory is not wasted as there is no<br>duplication                              |
*****
# Arrays as arguments
* When declaring a one-dimensional array as a formal argument, the array name is written with a pair of empty square brackets and the size of the array is not specified within the formal argument declaration.
	`float average(int num, float arr[]);`

* In C, we can also pass arrays with a variable second dimension. In this case, we still need to specify the second dimension (or more) while passing the array.
	`void display(int arr[][3], int rows);`
****
# Macros
 1. Constant Macros
	 `#define macro_name macro_value;`
	 called like a normal constant.
 2. Function-like Macros
	 `#define MACRO_NAME(arg1, arg2, ...) (expression)`
	 called like a normal function.
* Advantages:
	1. Code reusability
	2. Efficiency compared to functions (macros are expanded at compile time)
	3. Readability

***
***
# Command-line arguments
* Syntax: `int main(int argc, char *argv[]){}`
* `argc` (argument count): stores no. of arguments passed, including filename
* `*argv[]` (argument vector): pointer array of strings that stores arguments
***
# Structure vs Union

| Parameter                 | STRUCTURE                                                                                                                                                                                               | UNION                                                                                                                                                                                                    |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Keyword                   | The keyword struct is used to<br>define a structure.                                                                                                                                                    | The keyword union is used to<br>define a union.                                                                                                                                                          |
| Size                      | When a variable is associated<br>with a structure, the compiler<br>allocates the memory for<br>each member. The size of<br>structure is greater than or<br>equal to the sum of sizes of<br>its members. | When a variable is associated<br>with a union, the compiler<br>allocates the memory by<br>considering the size of the<br>largest memory. The size of<br>union is equal to the size of<br>largest member. |
| Memory location           | Each member within a<br>structure is assigned unique<br>storage area of location.                                                                                                                       | Memory allocated is shared<br>by individual members of<br>union.                                                                                                                                         |
| Value Altering            | Altering the value of a<br>member will not affect other<br>members of the structure.                                                                                                                    | Altering the value of any of<br>the member will alter other<br>member values.                                                                                                                            |
| Accessing members         | Individual member can be<br>accessed at a time.                                                                                                                                                         | Only one member can be<br>accessed at a time.                                                                                                                                                            |
| Initialization of members | Several members of a<br>structure can initialize at<br>once.                                                                                                                                            | Only the first member of a<br>union can be initialized.                                                                                                                                                  |
***

# Storage classes
1. Automatic (local) variables
2. External (global) variables
3. Static variables
4. Register variables


 



 

 


