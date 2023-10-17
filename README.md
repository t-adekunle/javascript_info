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
- 

<h3>Objects</h3>
- Like dictionaries in python.

Accessing Values
We can use dot notation to access individual values inside an object, using the 
key
 we are interested in learning more about. Let's check what Mezz's hobbies are.

const person = {
    firstName: 'Mezz',
    lastName: 'Guster',
    likesCoding: true,
    hobbies: ['reading', 'pottery', 'cooking']
}

console.log(person.hobbies);
// ['reading', 'pottery', 'cooking']
If this looks familiar, we used exactly the same approach to query the .length property when we covered 
arrays
.

Sometimes, the keys of an object prevent us from using this notation. In this example, the keys are the people's names, and the values are some imaginary test scores.
```
const testScores = {
    "Leslie Knope": 85,
    "Ron Swanson": 59,
    "April Ludgate": 67
}
```
All object keys are 
strings
 - in previous examples, we haven't included quotations marks, but here we must, because the names contains space 
characters
. Without quotation marks, JavaScript wouldn't run the code, but instead give us a 
syntax
 error.

Accessing the value under a key like this with dot notation would also cause a syntax error. We can use bracket notation instead.
```
const aprilsScore = testScores["April Ludgate"]

console.log(aprilsScore) // 67
```
Sometimes the key that we use to access the value might be stored in a 
variable
 - this is known as a dynamic key. Again, we must use bracket notation if we are to use the variable to access the value. JavaScript will 
evaluate
 the variable, and use it to access the correct value.
```
const employee = 'Ron Swanson'

const ronsScore = testScores[employee]

console.log(ronsScore) // 59
```
If we were to use dot notation we would be attempting to find a value in the object under that key. If that key does not exist on the object, then JavaScript will find no value, and the result will evaluate to 
undefined
```
console.log(testScores.employee) // undefined
 ```
Changing our objects
JavaScript provides the delete keyword to remove properties from an object. Our geology shop was for sale, but the purchase fell through, so we could delete this property.
```
const geologyShop = {
    owner: 'Flint Eastwood'
    purchaser: 'Stony Hawk'
}

delete geologyShop.purchaser

console.log(geologyShop) // { owner: 'Flint Eastwood' }

console.log(geologyShop.purchaser) // undefined
```
An alternative to deleting a property may be setting its value to null. We mentioned 
null
 right at the beginning of the course as a way of representing the lack of a value. Assigning null as a value is sometimes a more appropriate way of coding the data we want to represent. The remaining key can still give meaning to the object.
```
const geologyShop = {
    owner: 'Flint Eastwood'
    purchaser: 'Stony Hawk'
}

geologyShop.purchaser = null

console.log(geologyShop) // { owner: 'Flint Eastwood', purchaser: null }
```

