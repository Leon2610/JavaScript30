# 04 - Array Cardio Day 1

This is a JavaScript practice for the [#JavaScript30](https://javascript30.com/) created by [Wes Bos](https://github.com/wesbos), the challenge is to create 30 things in 30 days just with Vanilla JS

## Overview

### About this project

Work with some of the JS array methods and various examples given.

### What I learned

The **filter method** allows to create a new array with all the elements that meet a condition given by a function.

The **map method allows** to create a new array with the results of the call to a given function applied to each of its elements.

* It is in charge of executing the function indicated for each of the elements of the array. 
* It does not change the original array.

The **sort method** sorts the elements of an array locally and returns the sorted array.The order is not stable and depends on different factors, for which it will show different results:

* If no comparison function is provided (i.e., if it is sent without arguments) then it takes the elements as strings (even if they are numbers) and sorts them according to their Unicode value. 
* If a comparison function is provided, the array elements are sorted according to the value returned by the comparison function.
For this case we take as arguments ( a, b ):

```javascript
function compare(a, b) {
  if (a is less than b by some ordering criterion) {
    return -1;
  }
  if (a is greater than b by the ordering criterion) {
    return 1;
  }
  // a must be equal to b
  return 0;
}
```

 To compare numbers simply perform a subtraction between the two arguments:

 ```javascript
 function compareNumbers(a, b) {
  return a - b;
}
 ```

 You can also sort objects by the value of one of their properties:

 ```javascript
 const inventors = [
      { first: 'Albert', last: 'Einstein', year: 1879, passed: 1955 },
      { first: 'Isaac', last: 'Newton', year: 1643, passed: 1727 },
      { first: 'Galileo', last: 'Galilei', year: 1564, passed: 1642 },
      { first: 'Marie', last: 'Curie', year: 1867, passed: 1934 },
      { first: 'Johannes', last: 'Kepler', year: 1571, passed: 1630 },
      { first: 'Nicolaus', last: 'Copernicus', year: 1473, passed: 1543 },
      { first: 'Max', last: 'Planck', year: 1858, passed: 1947 },
      { first: 'Katherine', last: 'Blodgett', year: 1898, passed: 1979 },
      { first: 'Ada', last: 'Lovelace', year: 1815, passed: 1852 },
      { first: 'Sarah E.', last: 'Goode', year: 1855, passed: 1905 },
      { first: 'Lise', last: 'Meitner', year: 1878, passed: 1968 },
      { first: 'Hanna', last: 'Hammarström', year: 1829, passed: 1909 }
    ];

// Sort the inventors by birthdate, oldest to youngest
const ordered = inventors.sort((a,b) => {
      if (a.year > b.year) {
        return 1;
      } else {
        return -1;
      }
    });

    console.table(ordered);
 ```

The **reduce method** executes a reduce function on each element of an array, returning a single result.
* This method executes a callback that has as parameters the accumulator and the initial value. Also the method includes an Initial value which is optional.
* It receives four arguments:
    * previousValue
    * currentValue
    * currentIndex (optional)
    * array (optional)
```javascript
arr.reduce(callback(previousValue, currentValue[, currentIndex[, array]])[, initialValue])
```

* Some of the examples of use are:
    * Sum all the values of an array.
    * Subtract all the numbers of an array.
    * Integrate an array from several arrays.

### Useful resources

- [Filter method](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)
- [Map method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)
- [Sort method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort)
- [Reduce method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce)