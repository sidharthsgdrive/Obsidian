---
date: 2025-08-13
---
## Idea
To represent indented bullet points as hierarchies. Also include a checkbox mode.
###### Example
```
├ Random variables
├ Discrete & Continuous range of values
├ Distribution functions
├ Graphical representation
|    ├ line diagram
|    ├ bar graph / histogram
└ Standard distributions
     ├ Bernoulli distribution
     ├ binomial distribution
     ├ Poisson distribution
     └ Geometric distribution (?)
```

### Frontend
- For now: CLI for filepath (argv) to convert, stores original file in a particular folder (for debugging)
- Future: Website where users can input text field, output is shown in another text field (reverse engineer from sites like https://lingojam.com/ZalgoText)
- Features:
	- indented bulletpoints -> file hierarchy
	- indented bulletpoints -> file hierarchy with checkboxes

#### Language
- Python -- existing familiarity
- C -- also kind of familiar, could be better for handling trees using pointers 

##### Logic
- Indented bullet points are converted to a tree structure 
	- Could be nested list if Python (or other relevant tree structure), or as struct nodes in C. 
	- Use recursion to traverse
	- or an easier solution -- don't use trees, just parse the file line by line making use of the already existing indentation. One drawback is I can't see this working with more than one level of nesting.