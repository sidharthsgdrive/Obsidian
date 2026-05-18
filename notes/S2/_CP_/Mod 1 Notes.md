# Character Set
A-Z: 65-90
a-z: 97-122
space: 32
# Identifier rules
* begin with letter or underscore
* consist **only** of letters, digits, underscore (no spl chars, whitespace)
* should not be a keyword

| Primary data types             | Derived  | User Defined |
| ------------------------------ | -------- | ------------ |
| Integer (short, int, long)     | Array    | Structure    |
| Floating point (float, double) | Function | Union        |
| Character (char)               | Pointer  | Typedef      |
# Precedence of Operators (left-right association unless specified)
1. (), \[], ., ->, postfix increment 
2. prefix increment, NOT, unary +-, \*, & (RIGHT-LEFT)
3. \*, / , %
4. +, -
5. <, >, \<=, >=
6. \==, !=
7. AND, OR
8. Augmented operations (RIGHT-LEFT)
# Structure of a C Program
1. Comments
2. Preprocessor directives
3. Global variables declaration
4. Main function
5. User defined functions
# Switch statement syntax
`switch(expression)`
`{`
`case constant1: seq1;`
				`break;`
`case constant2: seq2;`
				`break;`
`....`
`....`
`default: seqn;`
`}`
# goto statement syntax
`labelname:`
`sequence;`
`....`
`goto label;`
# Types of loops
1. Entry controlled (for, while)
2. Exit controlled (do while)