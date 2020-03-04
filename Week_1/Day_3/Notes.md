# Day 3

## Objects

* Using undefined as an object value is not typically done as accessing a key that doesn't exist will also return undefined and may cause confusion

* If var name points to a string, you can then access the key
* Object.keys(...) inspects an objects keys

```javascript
const person = { firstName: "Khurram" };
const propertyName = "firstName";
const firstName = person[propertyName]; // interpreted as person["firstName"], and therefore works fine :)
```

* Keys do not need quotations and are always strings
* However if your key has underscores, dashes, or spaces, it will require quotations

```javascript
const spam = "spam";
person["dislikes"] = { food: spam, "e-mail": "spam" };
```
  * Spam without quotes is a variable
  * E-mail requires quotes because it contains a hyphen


## Lecture

#### Arrays

* Try to avoid using decimal place numbers in JS; better to use whole numbers
* Don't use arrays that contain multiple different data types
* for...of vs for...in
  * for...in returns the index, not the item itself (for OBJECTS)
  * for...of returns the values
* for loops can accept break statements, however forEach cannot

#### Objects

* Objects typically declared as const 
* Good for mixed types of data that are related
* "this" will allow you to jump outside of a function declared inside an object and reference the object itself

``` javascript
const person = {
  firstName = "Matt",
  lastName = "Taylor",
  heightInCm: 188,
  heightInInches: function() {
    console.log(this.heightInCm / 2.54); 
    console.log(`${this.firstName} ${this.lastName}`);

  }
}
```

* Iterable data types = arrays, strings
* Objects can be iterated over with for...in (gives keys in the object)
* In a loop, when you don't know the key name, use bracket notation instead of dot notation 

``` javascript
for (let key in person) {
  console.log(person[key]);
}
```
* for... in can have issues by inheriting properties from their prototype chain as well as method names
  * Additional filtering necessary

    ```javascript
    for (var planet in planetMoons) {
    // additional filter for object properties:
      if (planetMoons.hasOwnProperty(planet)) {
        //  ...
      }
    }
    ```

``` javascript
// Prints out array
Object.keys(person);
Object.values(person);
```

* console.table() prints out a table of the object/array