* Manhattan distance (taxicab distance) `d = |x1-x2| + |y1-y2|`
***
## iterators

```python
fruits = ["mango","kiwi","pineapple"]
basket = iter(fruits) # creates a list iterator out of the list
print(next(object)) # prints the next object that hasn't been printed yet
```
### generators

```Python
def square(limit): # generator function
	x = 0
	while x < limit:
		yield x * x # used instead of return statement
		yield x * x * x
		x += 1

a = square(5)
print(next(a),next(a)) # output: 0 0
print(next(a),next(a)) # output: 1 1
print(next(a),next(a)) # output: 4 8
```
We have control over how many times the iterator is actually used, even though it is yielded earlier.
#### lambda

```Python
add = lambda x,y: x + y # anonymous lambda function with two parameters, returning sum of parameters
print(add(5,4)) # output: 20
print(type(add)) # output: <class "function">
```

##### enumerate

To find the index of some element in a list, it is better to use enumerate rather than run a for loop.

```Python
fruits = ["mango","kiwi","pineapple"]
for fruit in enumerate(fruits): # using a loop
	print(fruit)
# output:
# (0, 'mango')
# (1, 'kiwi')
# (2, 'pineapple')
```

## zip function

to couple values from 2 different lists

```Python
fruits = ["mango","kiwi","pineapple"]
sizes = [5,4,9] # lengths of words
print(list(zip(fruits,size)))
# output: 
# [('mango', 5), ('kiwi', 4), ('pineapple', 9)]
```

### map function

Say we want to repeat an operation for all members of a list, for example,

```Python
# subtract each element of list b from each element of list a
a = [10,20,30,40]
b = [1,2,3,4]
def sub(x,y):
	return x - y
c = map(sub,a,b) # [9,18,27,36]
```

`map(funcname,iter1,iter2,...)` returns an iterator object consisting of the returned values of `funcname` when each element of `iter1`, `iter2`, etc are passed into it.

```Python
# increment every element of a
a = [1,2,3,4]
b = map(lambda a:a+1, a)
```

#### filter

Say we are trying to find square root of every member of a list, but there are some negative elements. How do we apply the sqrt method only to non-negative elements?

* `filter(funcname, iterable)` creates an iterator consisting of the values of `iterable` that return `True` when passed into `funcname`.

```Python
import math
a = [25,-16,4]

def square_root(n):
	return math.sqrt(n)

def is_positive(n):
	if n >= 0:
		return n 

b = map(square_root, filter(is_positive, a))
print(list(b))
```
***

> [!info]
> * methods like `sort()` and `reverse()` return an object of NoneType.
> * `reversed()` returns a reversed object (iterator).
> * `sorted()` returns a list.
> * `dict.popitem()` pops a tuple



