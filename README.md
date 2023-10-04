# javascript_info

javascript methods and functions:

**Add Elements to an Array**

.push() - adds to end of array and mutates it
.unshift() - adds to beginning of an array and mutates it
**Remove elements from an Array**
.pop() - removes last element from an array and mutates the array. Doesn't take an argument
.shift() - removed first element from an array and mutates it. DOesn't take an argument

**Slicing an array**

.slice(0,3) - creates a new variable with the first 4 elements of an existing list. If not second argument is provided, the slice will go to the end of the array. 
.slice(-3) - creates a new variable with the last 3 items of an existing list. 

.includes(value,index(optional) - Returns true or false if an array contains given value. Can have a second value as index
.indexOf(value, index(optional) - returns the first index at which a given element can be found in an array. Will return -1 if it is not present.
.reverse() - reverses the order of values in an array. is destructive
.toReversed() - reverses the order of values in an array and returns a new array. Non-destructive
.splice(start, deleteCount, item1, item2) - changes the contans of an array by removing or replacing existing element and/or adding new elements in place. Mutates orginal array
.toSpliced(start, deleteCount, item1, item2) - non-descrutive version of splice

**NESTED ARRAYS**

```
const starter = ['tomato', 'cream', 'basil']
const main = ['lemon', 'thyme', 'chicken']
const dessert = ['apple', 'pastry', 'cream']

const dinner = [starter, main, dessert]

console.log(dinner)
/*
[
  ['tomato', 'cream', 'basil'],
  ['lemon', 'thyme', 'chicken'],
  ['apple', 'pastry', 'cream']
]
*/

Access using

const cream = dinner[0][1]
```



