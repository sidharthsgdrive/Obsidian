The **Collatz function** is defined for a positive integer nn as follows.



We consider the repeated application of the Collatz function starting with a given integer nn, which results in the following sequence:

f(n),f(f(n)),f(f(f(n))),…f(n),f(f(n)),f(f(f(n))),…  

It is conjectured that no matter which positive integer nn you start from, the sequence will always reach 11. For example, if n=10n=10, the sequence is:

|Seq No.|n|f(n)|
|---|---|---|
|1|10|5|
|2|5|16|
|3|16|8|
|4|8|4|
|5|4|2|
|6|2|1|

Thus, if you start from n=10n=10, you need to apply the function ff six times in order to **first** reach 1.

---

Write a recursive function named collatz that accepts a positive integer nn as argument, where 1<n≤32,0001<n≤32,000, and returns the number of times ff has to be applied repeatedly in order to first reach 1.

---

You do not have to accept input from the user or print output to the console. You just have to write the function definitio