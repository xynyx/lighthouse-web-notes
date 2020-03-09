# Week 2 - Day 1

### TDD with Mocha and Chai

* Test-Driven Design, Error-Driven Design
* Better to write tests first, THEN write the code
* If you export as an object, you can module.exports an object of a list of all the functions instead of separate module.exports
>`module.exports = { eqArrays, assertEqual };`

* Better way of comparing two arrays would be a for...in loop (looks at index instead of each value; easier to then access each value in arrTwo)
``` javascript
for (let index in arrOne) {
  if (arrOne[index] !== arrTwo[index]) {
    return false;
  }
}
return true;
```