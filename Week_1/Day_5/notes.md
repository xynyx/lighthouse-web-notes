# Day 5

## Recursion

* Every recursive function must have a base case and a recursive case
* The recursive case must eventually reach the base case, where the function terminates
* <strong> An unknown number of nested loops are a common characteristic of all problems that are recursive in nature 
  * USE A RECURSIVE FUNCTION!

```javascript
if (Array.isArray(a[i])) {
    result += sum(a[i])
```
  * Do not think about what will happen when sum is executed...
  * Instead, TRUST that it returns the correct sum for all elements of an array a[i]
  * Do NOT think about the recursion as a series of execution steps -> will lead to confusion

