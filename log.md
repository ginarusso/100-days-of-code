# 100 Days Of Code - Log

Day 0: April 5, 2022

**Today's Progress**: Scrimba - listened to latest Scrimba podcast and learned about 100 days of code. Almost finished "Learn Javascript for free" course.

**Thoughts:** Agree with Ineza Bonté about staying focused on one language and learning it well before trying to learn another one: https://ineza.codes/

**Link to work:** n/a

******************************

Day 1: April 6, 2022

**Today's Progress**: Scrimba - finished Javascript for free" course and started Javascript Bootcamp - intermediate tutorials.

**Thoughts:** Starting off as a review - feeling pretty confident.

**Link to work:** n/a
******************************

Day 2: April 7, 2022

**Today's Progress**: Scrimba - continued Javascript Bootcamp course. 
- Don't use \n or \r - instead use backticks with template literal strings.
- Use switch statements when if-else statements are too long
- two data types:
  - primitive - there are 6 primitive types - they are immutable (can't change their properties:
                  - string
                  - number
                  - boolean
                  - undefined
                  - null
                  - symbol
  - object (can be changed dynamically and are passed by reference) []:

**Thoughts:** Easy to understand. 

**Link to work:** n/a
******************************

Day 3: April 8, 2022

**Today's Progress**: Scrimba - continued Javascript Bootcamp course.
conversion types:
  - explicit
  - implicit (coercion)

Anything passed in a condition will automatically try to convert to a boolean
  - truthy
  - falsy
    - false
    - 0
    - ""
    - null
    - undefined (empty variable)
    - NaN
Avoid direct comparisons within conditionals
Strict operator === doesn't allow type conversions

**Thoughts:** Easy to understand. 

**Link to work:** n/a
******************************

Day 4: April 9, 2022

**Today's Progress**: Scrimba - continued Javascript Bootcamp course.
Ternary operations (instead of if-else)
example:
const greeting = age < 10 ? "Hey there!": age > 18 ? "Greetings!";

Short circuting ternaries (operator precedence - && gets 1st precedence; || gets 2nd precedence):
const username = response || "guest";
const username = isVerified && response || "guest";

Closures (only Javascript function have closures)
- to observe closure, you must call a function in a different scope than where the function was originally defined
- closures allow us to keep track or remember values
- allows you to call a function from outside the scope it was defined in 
- toFixed() string method is used to return a number that is wrapped in a Number function

You can use default parameters instead of conditional statements to handle undefined argument values:
function convertTemperature(celsius, decimalPlaces = 1) {
  const fahrenheit = celsius * 1.8 + 32;
  return Number(fahrenheit.toFixed(decimalPlaces));
}
console.log(convertTemperature(21, 0);
----> 70
console.log(convertTemperature(21);
----> 69.8

Arrow functions are anonymous
- can't use function keyword
- return keyword & braces are unnecessary (implicityly returned)
example:
const username = "john";
const capitalize = name => `${name.charAt(0).toUpperCase()} ${name.slice(1)}`;
console.log(capitalize(username));
----> John

callback is a function that is called after another function (higher-order function)

functions: Partial application - need to review this concept - it will be reviewed in Async Javascript section of Scrimba Javascript Bootcamp tutorial.

Objects:
- methods are just functions on objects - methods are a direct property on an object
- objectName.methodName();
- keys are strings
- are good for using static information, unchanging key-value data

**Thoughts:** Need more review on partial applications of functions. 

**Link to work:** n/a
******************************

Day 5: April 10, 2022

**Today's Progress**: Scrimba - continued Javascript Bootcamp course.

Property access with destructuring:
- eliminates repetition
example:
const user = {key: "value", key: "value"}
for this:
(`username: ${user.username}, email: ${user.email}`);
Use this instead:
const {username, email} = user;
(`username: ${username}, email: ${email}`);

example:
const user = {
  details: {
      title: "Programmer"
      }
};

const { details: {title} } = user
But instead of above, place right in the function parameters like this:
function displayUserBio({details:{title}}) {
};

**Thoughts:** So much information! Just need more practice to remember it all. 

**Link to work:** n/a

******************************

Day 6: April 11, 2022

**Today's Progress**: Scrimba - continued Javascript Bootcamp course.
Object.assign() = lets you update an object with properties fro another object
- to avoid updating or mutating original object, pass an empty object as the first parameter

Object spread operator
- better than Object.assign()
- used to individually spread in an object's properties into another one
- used to establish common default properties of any object through merging 2 or more objects
- non-destructively update or add properties (doesn't mutate original objects)
Limits with objects:
- keys have to be strings or symbols
- if key is not string, it is transformed into a string 
- can't be easily iterated over
- can't easily get length of objects
- order isn't preserved, instead use arrays
Instead....use new Map()
- new Map ([['key', 'value']]);
- .set mutates original Map object
- .forEach iterates through data in a Map
- normal javascript object - there is no length property
-   use object.keys to convert to an array of key values
this keyword
- a feature of function which allows us to get access to an object's data
- only functions declared with a function keyword have a dynamic this
- the value of this is determined how the function is called
- arrows don't have a this value when this is used within an arrow function; it grabs the this from the scope above where the arrow function was declared

use arrays because they preserve order and array methods allow easy manipulation of a collection of data
- arrow functions should only be used for this when they are inside another function, otherwise you will get undefined when console.log(this)

use includes() - to check for element existence with simple arrays of primitive values (strings, numbers, booleans)
use some() and every() for complex arrays that contain an object

**Thoughts:** This is so overwhelming! 

**Link to work:** n/a
******************************

Day 7: April 12, 2022

**Today's Progress**: Scrimba - continued Javascript Bootcamp course.
Map()
- transforms the entire array and creates a brand new array
forEach()
- allows you to perform operations to every element of an array
- does NOT create a new array; just allows you to iterate over the array and perform an operation in a callback
- usually used when you already have an array in the format that you want using methods - such as a Map 
filter() 
- creates a new array and doesn't change original array
- if nothing is found, it returns an empty array
- is the best way to get a selection of any array and search arrays based on multiple conditions
find()
- works like filter but it finds the element you are looking for or returns undefined
- if you know in advance that you need just one array element, use the find method
reduce()
- iterates all elements in an array
- pass a callback function, but needs 2 arguments
concat() - updates the array
.push is a mutating method

arrays are reference types


**Thoughts:** So much information! Just need more practice to remember it all. 

**Link to work:** n/a
******************************

Day 8: April 13, 2022

Today's Progress: Scrimba - continued Javascript Bootcamp course.
spread operator - create and order new arrays
- sorks with any iterable
slice() is immutable
replacing an item: .findIndex()
array destructuring

turning objects into arrays
- 1) Object.keys() - takes keys and objects and turns into an array
- 2) Object.values() - takes values
- 3) Object.entries() - takes keys and values; for static data structure
- can use= keys names to check if a property exists

Set Object type
- new Set()
-   each value can only occur once (useful when filtering items that occur multiple times in an array)
-   arrays are object or reference types and are unique
-   Set is like an array because it doesn't include keys
-   you can't reference its values by referencing a key or index
-   to get the value of a set you an use a for of loop to reference key or index values
spread operator
- works with any iterable


Thoughts: How will you be able to figure out which method to use when there are so many????

Link to work: n/a
******************************

Day 9: April 14, 2022

Today's Progress: Scrimba - needed a break from the bootcamp and worked on the Valentine's Challenges: https://scrimba.com/learn/codeweeks
Gift Selector
Valentine's Greeting
Grammar Corrector
Filter Duplicate Emojis
Heart Customizer API

Thoughts: These exercises were really helpful. They helped me practice what I've been learning and included some new coding concepts. Next week they are having a week-long Earth Day Challenge. 

Link to work: n/a






