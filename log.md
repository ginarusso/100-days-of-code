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

Day 1: April 7, 2022

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

Day 1: April 8, 2022

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

Day 1: April 9, 2022

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

Day 1: April 10, 2022

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








