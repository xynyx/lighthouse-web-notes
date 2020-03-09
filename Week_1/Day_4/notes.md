# Day 4

* Function Declaration
```javascript
function sayHi() {
  alert( "Hello" );
};
```

* Function Expression
```javascript
let sayHi = function() {
  alert( "Hello" );
};
```

* Functions should always only have ONE job - if it does multiple things, split into separate functions

* You can define a new function as a parameter when calling the function
```javascript
const forEachReverse = (array, callback) => {
  for (let i = array.length - 1; i >= 0; i--) {
    callback(array[i], i, Int32Array);
  }
}

forEachReverse(['a', 'b', 'c', 'c'], value => {
  console.log(value.charCodeAt(0));
});

forEachReverse([1, 2, 3, 4, 5], (value, i) => {
  console.log(value * i);
})
```
* If you need to return an object from a function, you can't just have ```r => {}```, it must be ```r => ({})```

* Arrow functions 
  * Don't get assigned a value for ```this``` in a way that traditional function expressions do *super important when using `this`*
  * Do not have arguments
  * Can't be called with ```new```
  * Do not have ```super``` (?)

* Functions are instances of Object type, and can have properties and methods 

* Higher Order Functions - Functions that take a callback (major aspect of Functional Programming)
