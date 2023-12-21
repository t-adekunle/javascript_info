# javascript_info

**Maths symbols**

Math.sqrt( number ); - finds square root of a number
Math.pow(base, exponent) - calucaltes something to the power of. Only takes numbers
** - used to create indicies. To the power of
toFixed(x) - rounds number to x number of decimal places. returns a string
Math.round(a*100)/100; - rounds number. /10 is one decimal place, /100 is 2 decimal places, /1000 is 3 decimal places, etc


javascript methods and functions:


<h4>STRINGS</h4>

**Joining strings**
let text1 = "Hello";
let text2 = "world!";
let result = text1.concat(" ", text2);

string.charAt(0).toUpperCase() + string.slice(1) - Capitalise the first letter of a string

let text = "How are you doing today?";
const myArray = text.split(" ") ---> changes a string to an array. " " uses the blank space to act as the separation factor

str.replace(value1, value2) - replaces first value with second value
string.replace(/GeeksForGeeks/g, 'Gfg') - /g will replace globally so all occurance (case sensitive)
string.replace(/GeeksForGeeks/gi, 'Gfg') - /i will replace regardless of case. If you put the slashes, then you don't need quotation marks

string.includes(substring, index); - check if a string contrains a certain substrng. Index is optional

Regex Matching:

const str = 'Bread and Milk';
console.log(/d/.test(str)); // true
console.log(/p/.test(str)); // false

const str = 'Bread and Milk';
// Contains a digit?
console.log(/\d/.test(str)); // false
// Contains 'r', 'l' or 'c'?
console.log(/[rlc]/.test(str)); // true
// Contains whitespace?
console.log(/\s/.test(str)); // true

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
- .flat(depth) - creates a new array with all sub-array elements concatenated into it recursively up to the specified depth. Depth is optional and defaults to 1. Depth refers to the number of levels flattened not the final number of levels in the returned array

- **Combine arrays**
arr1.concat(arr2)

Sorting an Array 

points.sort(function(a, b){return a - b}); - sorts ascending
points.sort(function(a, b){return b - a}); - sorted desceneding



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
<h2>Loops</h2>
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

**For ...in**

```
for (variable in object)
  statment
```
EG - the function takes as its arguments object and the object's names. The it iterates over all the objects properties and returns a string that lists the property names and their values. 
```
function dumpProps(obj, objName) {
  let result = "";
  for (const i in obj) {
    result += `${objName}.${i} = ${obj[i]}<br>`;
  }
  result += "<hr>";
  return result;
}
```
- To be used with objects.
- The for...in statement iterates a specified avariable over all the enumarable properties of an object.
- For each distinct property, JavaScript executes the specifieed statements.
- Don't use with arrays as it will return the name of your user-defined properties in adition to the numeric indexes. 


**For...of**

- Created a loop interating over iterable objects (which include Array, Map, Set, arguments object) invoking a custom iteration hook with statemtns wto be executed for the calue of each distince property.

- ```
  for (variable of object)
    statement
  ```
  - For ... in iterates over property names.
  - For...of iterates over proprety values.
```
    const arr = [3, 5, 7];
    arr.foo = "hello";

  for (const i in arr) {
    console.log(i);
  }
  // "0" "1" "2" "foo"

  for (const i of arr) {
    console.log(i);
  }
  // Logs: 3 5 7
```
- The for... of and for...in statments can also be used with destructuring (for info on destructuing see here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment - it makes it possible to unpack vcalues from arrays or properties from objetd, into distinct varibles.)
- For instance, you can simultaneiously loop over the keys and values of an object using the Object.entries()
```
const obj = { foo: 1, bar: 2 };

for (const [key, val] of Object.entries(obj)) {
  console.log(key, val);
}
// "foo" 1
// "bar" 2
```

**Do While**

- The do...whle statement repeats until a specified condition evaluates to false.
 ```
  do
  statement
while (condition);
```
- statment is alwys executes once before the confistion is checked.
-   To execute multiple statemnts use a black stament ({ }) to group those statemnts
- If the condition ois trye, the tatemtns executes again.
- At the end of every execution, the condition is checkes. When the con


**While**


**Labelled Statement**

**Break Statement**

**Continue Statement**

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

**Turn Object keys into an array**

```
const object1 = {
  a: 'somestring',
  b: 42,
  c: false,
};

console.log(Object.keys(object1));
// Expected output: Array ["a", "b", "c"]
```
**Turn Object values into an array**

```
const object1 = {
  a: 'somestring',
  b: 42,
  c: false,
};

console.log(Object.values(object1));
// Expected output: Array ["somestring", 42, false]
```
<h4>For...in Loops</h4>

This section will outline the 
object's alternative to for loops, the for...in loop.

Components of a For In Loop
A for...in loop loop can access each 
property of an object by referencing its keys
```
const tree = {
    name: "Oak",
    hasAcorns: true,
    ageInYears: 530,
};

for (const key in tree) { 
    // code to be executed
};
```
The syntax is similar to a for loop, but instead of having a counter 
variable
 (i) to work with inside the 
code block
, each key of the object is exposed. There are no stop or step 
expressions
 - the code block will be run as many times as there are properties in the object.

Within the code block, we can use the key to 
dynamically
 access the values in the object. As key is a variable, we need to use square bracket notation.
```
for (const key in tree) { 
    const value = tree[key]
    console.log(`The tree has a key of ${key} holding the value ${value}`)
    // The tree has a key of name holding the value Oak
    // The tree has a key of hasAcorns holding the value true
    // The tree has a key of ageInYears holding the value 530
};
```

<h2> Javascript Functions</h2>

array.join(separator) - can take an array and turn it into a string
**map () method - instead of for loop** ---->
```
const array1 = [1, 4, 9, 16];

// Pass a function to map
const map1 = array1.map((x) => x * 2);

console.log(map1);
// Expected output: Array [2, 8, 18, 32]
```

**every() method - instead of for loop** ----> 

```
const isBelowThreshold = (currentValue) => currentValue < 40;

const array1 = [1, 30, 39, 29, 10, 13];

console.log(array1.every(isBelowThreshold));
// Expected output: true
```
```
function isSweetEnough(foods) {
  return foods.every(food => food.flavour === 'sweet');
}
```
<h2>Regular Expression or RegEx</h2>

check this website for RegEX reference: https://regexr.com/



