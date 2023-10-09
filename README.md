# javascript_info

javascript methods and functions:

**Add Elements to an Array**

- .push() - adds to end of array and mutates it
- .unshift() - adds to beginning of an array and mutates it

**Remove elements from an Array**

- .pop() - removes last element from an array and mutates the array. Doesn't take an argument
- .shift() - removed first element from an array and mutates it. DOesn't take an argument

**Slicing an array**
- .slice(0,3) - creates a new variable with the first 4 elements of an existing list. If not second argument is provided, the slice will go to the end of the array.
- .slice(-3) - creates a new variable with the last 3 items of an existing list. 

- .includes(value,index(optional) - Returns true or false if an array contains given value. Can have a second value as index
- .indexOf(value, index(optional) - returns the first index at which a given element can be found in an array. Will return -1 if it is not present.
- .reverse() - reverses the order of values in an array. is destructive
- .toReversed() - reverses the order of values in an array and returns a new array. Non-destructive
- .splice(start, deleteCount, item1, item2) - changes the contentsbn  of an array by removing or replacing existing element and/or adding new elements in place. Mutates orginal array
- .toSpliced(start, deleteCount, item1, item2) - non-descrutive version of splice
- .flat(depth) - creates a new array with all sub-array elements concatenated into it recursively up to the specified depth. Depth is optional and defaults to 1


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
**IF STATMENTS**
syntax: 
```
if (condition1) {
  //  block of code to be executed if condition1 is true
} else if (condition2) {
  //  block of code to be executed if the condition1 is false and condition2 is true
} else {
  //  block of code to be executed if the condition1 is false and condition2 is false
}
```
**FOR LOOPS**

- Allows you to reapeat a code black until a condition evaluates true.
- Syntax:
```
for (start; stop; step) {
    // code to execute
}
```
 Example:
 ```
for (let i = 0; i < 3; i++){
console.log(i)
}
```
 - let i = 0 ---> is the start expression. used to declare a variable before the loop begins. This is often counter. can be any letter but i is often used.
 - i < 3 ---> is the stop expression. Before each repetition of the loop, this expression is evaluated to a boolean. If true, the loop will continue to iterate, if false then the loop will end.
 - i++ ---. is the step expression. This code is evalusated at the end of each repetition. i++ means i = i +1. we reassign the calue of i to be itself plus one.
 - **incraments**
  - i-- decrrement by one
  - i +=3 // eqiuvalent to i = i+3
  - i -= 5 // equivalent to i = i - 5

- Infinite loops - ion a for loops, if the stop expression can never evaluate to false, the loop will be infinite

  


