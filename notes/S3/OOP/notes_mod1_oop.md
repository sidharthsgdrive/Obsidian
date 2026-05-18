### To revisit
- 
***
## 1. Java Basics  

- **Created:** 1991, by James Gosling, Sun Microsystems.  
- **Goals:** Platform-independent, secure, object-oriented.  
- **Execution:** `.java` → compile with `javac` → `.class (bytecode)` → JVM.  
- **Key Feature:** **“Write Once, Run Anywhere”** (WORA).  
***
## 2. OOP Concepts  

- **Class:** Blueprint (data + methods).  
- **Object:** Instance (identity, state, behavior).  
- **Abstraction:** Hide details via `abstract class` / `interface`.  
- **Encapsulation:** Bundle data + methods; restrict with `private`, `public`, `protected`.  
- **Inheritance:** Code reuse – subclass inherits superclass. Types: Single, Multilevel, Hierarchical, Hybrid (via interfaces).  
- **Polymorphism:**  
  - Overloading (compile-time).  
  - Overriding (runtime).  
***
## 3. Java Program Structure  

- Must be inside **class**.  
- **Entry point:** `public static void main(String[] args)`.  
- **Access modifiers:**  
  - `public` → anywhere  
  - `private` → same class only  
  - `protected` → same package + subclasses  
  - *default* → package-private  
***
## 4. Data Types  

- **Primitive Types (8):**  
  - Integer: `byte`(8), `short`(16), `int`(32), `long`(64).  
  - Floating: `float`(32), `double`(64).  
  - Char: `char`(16 Unicode).  
  - Logical: `boolean` (true/false).  
- **Wrappers:** `Integer`, `Double`, `Character`, `Boolean`, etc.  
- **Strings:** `String` class (immutable), use `+` for concatenation. Mutable → `StringBuffer`, `StringBuilder`.  
***
## 5. Variables & Scope  

- **Declaration:** `type var = value;`  
- **Dynamic Init:** `double c = Math.sqrt(a*a+b*b);`  
- **Scope:** Block `{}` defines visibility.  
- **Lifetime:** Limited to scope.  
- **`this`:** Refers to current object, resolves shadowing.  
***
## 6. Operators  

- **Arithmetic:** `+ - * / % ++ --`  
- **Assignment:** `=, +=, -=, *=, /=`  
- **Relational:** `== != > = > >>>`  
- **Ternary:** `condition ? true : false`  
- **Precedence:** Unary > Arithmetic > Relational > Logical > Assignment.  
***
## 7. Control Statements  

- **Selection:**  
  - `if`, `if-else`, `if-else-if`, `switch` (supports `byte, short, int, char, String, enums`).  
- **Iteration:**  
  - `while` (pre-test),  
  - `do-while` (post-test, executes once min.),  
  - `for(init; cond; inc)`  
  - `for-each` (`for(type x : array)`)  
- **Jump:** `break`, `continue`, `return`.  
***
## 8. Arrays  

- **1D:** `int[] arr = new int;`  
- **Init:** `int[] arr = {1,2,3};`  
- **Multi-D:** `int[][] arr = new int;`  
- **For-each:** Simplified array traversal.  
***
## 9. Strings  

- `length()` → length  
- `charAt(i)` → char at pos  
- `equals()` / `equalsIgnoreCase()` → compare  
- `compareTo()` → dictionary order  
- `substring(start,end)` → extract  
- `indexOf(), lastIndexOf()` → search  
- `toUpperCase(), toLowerCase(), trim(), replace()` → modify  
- **Note:** `==` checks reference, not content.  
***
## 10. Constructors & Methods  

- **Constructors:** Same name as class, no return type.  
  - Default (auto if none provided).  
  - Parameterized – initialize with values.  
- **Methods:** Define behavior.  
  - Args = inputs, Return = outputs.  
***
## 11. Type Casting & Wrappers  

- **Type Conversion:**  
  - Widening (auto, safe, e.g. int → long).  
  - Narrowing (needs cast, e.g. double → int).  
- **Promotion in Expressions:** byte/short/char → int.  
- **Boxing / Unboxing:** Primitive ↔ Wrapper.  
- **Autoboxing (JDK 5+):** Auto conversion.  
  - `Integer x = 10; // autobox`  
  - `int y = x; // auto-unbox`  
***
## 12. Command Line & Varargs  

- **Command-line args:** Passed into `main(String[] args)`.  
- **Varargs:** Method with variable arguments.  
  - Syntax: `void method(int... nums)`  
  - Stored internally as array.  
***
## 13. Memory Management  

- **Garbage Collection:** JVM reclaims unused objects automatically.  
- No explicit `delete` keyword (unlike C++).  
***
# 🔑 Quick Formulas / Must-Remember  
- **All code inside a class.**  
- **main()** = program entry.  
- **Primitive types are fixed-size, platform-independent.**  
- **Strings immutable; use StringBuilder/StringBuffer for mutable strings.**  
- **Inheritance → IS-A, Composition → HAS-A.**  
- **Polymorphism = Overloading (compile-time), Overriding (runtime).**  
- **Garbage Collector → automatic memory cleanup.**  
***