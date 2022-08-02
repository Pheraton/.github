# Pheraton Base Contribution Guidelines
In this paper, you will face the base contribution guidelines for Pheraton's software.
Reading this paper doesn't justify ignoring any of the software's contribution guidelines that you would like to contribute to.

# 1. Optimization
Optimization isn't only in the form of performance optimization, it can be applied to many things we care about, such as reading and writing the code. 
Avoid specifc optimization that will take negative effect on another feature, as these will only cause bad than good

## 1.1 Performance
When you are writing code, you should be sure that the code you are shipping is performant at all time, 
some optimizations or algorithms that we tend to reject are:

* **Speed is Dependable on Input:** You should not be writing code that it's speed will change depending on the number of inputs unless there is no other way *(e.g, updating all dependencies)*. 
  * Avoid linear algorithms, for example, a tbl[Key] in a dictionary is more performant than a linear search or binary search.
  * Avoid unstable algorithms or paradigms. 
* **Optimization when needed:** We highly encourge our contributers to only "optimize" methods and software codebases only when needed. 
  * Optimize when there is a problem, other than that, do nothing
  * Optimization that may limit productivity isn't recommended
* **Domain-specific Optimization:** Optimization in Pheraton's software should be general optimization and not to be so specific that will be nearly useful to the average user. Pheraton Software is built to be extended upon.
  * Adding on this, you should optimize for the general audience of the software, rather than explict groups *(such as "power users")*. These optimization should be applied on the said groups' own versions.

## 1.2 Reading
Optimizing readability should be chosen over writing.

* **Avoid applying premature optimization:** Any code should not perform premature performance optimization that will lower the code's readability quality.
  * If possible, use a switch class *(we recommend our own version, as the difference between the implemention and an if-statement isn't notable)* instead of ugly if-statements
* **Moduler code wins:** Your code should always be moduler if possible and deemed necessary.
  * A whole chain of if-statements is worse than a module of commands for an admin system.
