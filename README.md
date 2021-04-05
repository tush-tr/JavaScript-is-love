# JavaScript all concepts
Amazing JavaScript learning and practice questions

### Content
<li><a href="#valuesandvariables">Values and Variables- Premitive data types- Numbers</a>
<li><a href="#premitive2">Premitive data types- Boolean, Null, Undefined, String</a>
<li><a href="#control-flow"> Control and logic flow- if/else, switch, ternary operator, logical operators etc.</a>
<li><a href="#arrays">Arrays, array methods</a>
<li><a href="#objects">Objects in JavaScript</a>
<li><a href="#loops">Loops in JavaScript</a>
<li><a href="#functions">Functions in JavaScript</a>



<h1 id="valuesandvariables"> Values and variables</h1>

## Primitive Data types
every language out there has a group of types.
Different categories for data.
<li>Number - its a numeric value
<li>String - text words, could be a number but inside quotation marks
<li>Boolean - true or false values
<li>Null
<li>Undefined
<li>technically there are two others- Symbol and BigInt

## Numbers in JS
JS has one number type
<li>positive numbers
<li>negative numbers
<li>whole number (integers)
<li>Decimal Numbers(floats)

> clear() - clears the console

with numbers we have different mathematical operations that we can use kind of like a calculator.

> Addition<br> 13+15

> Substraction<br> 15-2

> Multiply<br> 12*3

> Divide <br> 12/6

> Modulo <br> 12%4 - returns the remainder

> // <b>Comments</b> after these two forward slashes


#### exponent or exponential operator
which looks like this two star star.
> 4 ** 2 = 16

### NAN Not a Number
NaN is a numeric value that represents something that is not a number.
> 0/0 = NaN

> 122 + NaN = NaN

It doesn't necessarily mean something went wrong.


### Infinity
which we can generate by doing something like
1 divided by zero javascript just has a way of representing a value of infinity.
> 1/0 = infinity

<hr>


# Variables

Variables are like "labeled jars" for a value in JavaScript.

We can store a value and give it a name, so that we can--

<li>Recall it
<li>Use it
<li>Or change it later on

 the basic syntax that we'll see first is using a keyword called let.
```javascript
let age = 14;
```
Now there actually are two different ways that we can create variables in JavaScript at least two that
are commonly used today.

how to update a variable
```javascript
age = age +1;
```
we should always keep our variable names in camel case like this
```js
let ageOfTushar = 20;
```
## Unary operators
unary operators are operators where there's only one side.
```js
let counter = 1;
counter++;
```

## Const
const is just like let except we can't change the value.

## legacy of var
before let and const , var was only way to declare the variables. Now there's no reason to use it.

lets talk about other primitive data types-
<h1 id="premitive2"> Booleans</h1>
booleans are simply true or false values.

```js
let isFriend = true;
isFriend = false;
```

-- in javascript we can change type of variables.
if you have experience with any other programming language well maybe not any other but many other
languages.
When you declare a variable and you make it a number it needs to stay a number in JavaScript there is
no restriction on that.
We can change a number to a Boolean at any point.

That's not saying it's a good idea at all.
In fact it's one of the things a lot of people don't like about JavaScript and it's why things like
TypeScript exist.

# Strings
strings are pieces of text, or strings of characters.We wrap them in quotes.

```js
let rh = "This is going to be a good book";
"hi" + 1
> "hi1"
"hi" - 1
>NaN
```

> Strings are indexed
every character has a corresponding index.
we can check length of a string using:
```js
let s = "Tushar"
let lengthOfs = s.length
// accessing individual characters of a string using it's index
console.log(s[0])
// access last character of a string
console.log(s[s.length - 1])
// change characters 
s[1] = "u"
// we can't change strings individual characters this way
```
> strings are immutable in javascript

## String methods
strings come with a set of built in methods. which are actions that can be performed on or with that particular string.
```js
thing.method()
```

### toUpperCase()
```js
let s = "tushar";
s.toUpperCase(); // returns new string with UPPER case
```

### toLowerCase()
```js
s.toLowerCase();// returns new string with all lowercase characters
```

### trim()
It just removes trailing leading and trailing whitespace so spaces at the beginning and
end of a string when you call trim it returns a string where that space has been removed.
```js
s.trim()
```

## Methods with arguments
some methods accepts arguments that modify their behaviour.
```js
thing.method(args)
```

### indexOf()
tell you where in a string a given string occurs substring.

```js
let st = "Tushar Rajpoot";
st.indexOf("u") // returns the index
st.indexof("www") // return -1 not found
```

### slice()
takes index and gives sliced string
```js
let s = "Tushar";
s.slice(0,3);
>"Tus"
```

### replace()
returns a new string with replaced substring
```js
let as = "I'm Tushar and I'm a programmer";
as.replace("programmer","developer")
>"I'm Tushar and I'm a developer"
```

## String espace characters

<li> \n - newline
<li> \' - single quote
<li> \" - double quote
<li>\\ - backslash

## String template literals
template literals are strings that allow embedded expressions, which will be evaluated and then turned into a resulting string.

use backtick for string template literals

```js
let tu = 13;
let s = `Number of tushar- ${tu}`
```

# Null and Undefined
### Null
Intentional absence of any value.<br> Must be assigned.

### Undefined
Variables that don't have an assigned value are undefined.

```js
let logg = null;
```

# Math object
contains properties and methods for mathematical constantss and functions.

```js
Math.PI // 3.14...

//Rounding a number
Math.round(4.9) // 5

// Absolute value
Math.abs(-456) // 456

// Raises 2 to 5th power
Math.pow(2,5) // 32

// Removes decimal
Math.floor(3.23) // 3
```

## Random numbers
Math.random() gives us a random decimal between 0 and 1 (non- inclusive)

```js
Math.random() // it will return random decimal number between 0 and 1
// 0.33493

// genrate random number between 1 to 10
const step1 = Math.random();
const step2 = step1 * 10;
const step3 = Math.floor(step2);
const step4 = step3 +1;

// so basically we can do like this
Math.floor(Math.random() * 10)+1;

```

## TYPE OF
we use type of to determine type of a given value.

```js
let s = "tus";
typeof(s)// return string
// we can use without these parentheses also
typeof tu
```

# parseInt and parseFloat
use to parse strings into numbers, but watch out for NaN.
```js
let str = "123"
parseInt(str)
>123
let s = "1.2"
parseFloar(s);
>1.2
let st = "w1"
parseInt(st);
>NaN
```


<h1 id="control-flow">Controlling program logic and flow</h1>

## Comparison Operators
```js
> // greater than
< // less than
>= // greater than or equal to
<= // less than or equal to
== // equality
!= // not equal
=== // strict equality
!== // strict non-equality
// these give booleans true or false like this
5>2 // true
5<3 //false
```

### double equals(==)
<li>Checks for equality of value, but not equality of type.
<li>It coerces both values to the same type and then compares them.
<li>This can lead to some unexpected results.

### Triple equals(===)
<li>Checks for equality of value and type.

```js
7 == '7' // true
7 ==='7' //false
```

> Always go with triple equals.

## Making decisions in the code
A conditional statement can have three pieces-
<li>If
<li>Else if
<li>Else

### If 
Run code if a given condition is true.
```js
let rate = 3;
if(rate===3){
    console.log("Amazing");
}
```

### Else If
if not the first thing, maybe this another thing?
```js
let rate = 2;
if(rate===3){
    console.log("Amazing");
}
else if(rate === 2){
    console.log("Oh its ok");
}
```

### Else
if nothing else was true, do this..
```js
let rate = 349;
if(rate===3){
    console.log("Amazing");
}
else if(rate === 2){
    console.log("Oh its ok");
}
else{
    console.log("Ok we don't know about it")
}
```

### Nesting
we can nest conditionals inside conditionals
```js
let password = "hello kiry";
if(password.length >=6){
    if(password.indexOf(' ')!== -1){
        console.log("Password can't include spaces");
    }
    else{
        console.log("Valid password")
    }
}
else{
    console.log("password is too short");
}
```

## Truthy and Falsy values
<li> All values have an inherent truthy or falsy boolean value
<li> Falsy values:--<br>false<br>0<br>""(empty string)<br>null<br>undefined<br>NaN
<li>Everything else is truthy/

## Logical Operators
<li>AND(&&)
<li>OR(||)
<li>NOT(!)

### AND(&&)
Both sides must be true in order for the whole thing to be true

```js
1<=4 && 'a'==='a'; // true
9>10 && 9>=9 ; // false
```

### OR(||)
If one side is true, the whole thing is true

```js
// only one side needs to be true
1!==1 || 10===10 // true
```

### NOT(!)
returns true if the expression is false

```js
!null // true

!(0===0) // false
```

## Operator precedence
<li>NOT(!) has higher precedence than && and ||.
<li> && has higher precedence than ||. <br>
```js
! && ||
```
we can alter these using parentheses.


## Switch Statement

The switch statement evaluates an expression, matching the expression's value to a case clause, and executes statements associated with that case, as well as statements in cases that follow the matching case.

Syntax---

```js
switch (expression) {
  case value1:
    //Statements executed when the
    //result of expression matches value1
    [break;]
  case value2:
    //Statements executed when the
    //result of expression matches value2
    [break;]
  ...
  case valueN:
    //Statements executed when the
    //result of expression matches valueN
    [break;]
  [default:
    //Statements executed when none of
    //the values match the value of the expression
    [break;]]
}
```

## Ternary Operator

```js
condition ? expIfTrue: expIfFalse
```



## Some questions
<ol>
<li><a href="ifelse/prob1.js">Program to check if a number is even or odd.</a></li>
<li><a href="ifelse/prob2.js">Program to find maximum, minimum among two numbers</a></li>
<li><a href="ifelse/prob3.js">Program to find maximum, minimum among three numbers</a></li>
<li><a href="ifelse/prob4.js"> Program to check if an alphabet is a vowel or a consonant.</a></li>

</ol>

<h1 id="arrays">Arrays </h1>

Ordered collections of values
<li>List of comments on IG post
<li>Collection of levels in a game
<li>Songs in a playlist

### Creating arrays
```js
// make an empty array
let students = [];

// array of strings
let names = ["Rahul", "Tushar", "Sahul"];

// an array of numbers
let rollNo = [23,45,2,34,6,7]

// mixed array
let stuff = [true, 435, 'tushar', null];
```

#### Arrays are indexed
```js
let colors = ['red','orange','yellow','green']
colors.length//4

colors[0] // 'red'
colors[1] // 'orange'
colors[2] // 'yellow'
colors[3] // 'green'
colors[4] // 'undefined'
```
### modifying arrays
unlike strings, arrays are mutable, we can modify arrays

```js
let shop = ['milk','sugar'];
shop[1] = 'coffee';
// add something at the end
shop[shop.length] = 'tomatos'
```

## <a href="arrays"> Array Methods</a>
<li> Push - add to end
<li> Pop - remove from end
<li> Shift  remove from start
<li> Unshift - add to start
<li>________________________________________
<li> concat - merge arrays
<li> includes - look for a value, returns true or false
<li> indexOf - just like str.indexOf
<li> join - creates a string from arr
<li> reverse - reverses an array
<li> slice - copy portion of an arr
<li> splice - remove/replace elements
<li> sort - sorts an array.
The sort() method sorts the elements of an array in place and returns the sorted array. The default sort order is ascending, built upon converting the elements into strings, then comparing their sequences of UTF-16 code units values.

>arrays are reference types which means that the actual array data is not the content that is stored in the slot in memory for each variable.Instead it is a reference.

>we can modify array elements even it's initialized by const.

<h1 id="objects">Objects in JavaScript</h1>

An object allows us to store data where we can associate things in group pieces of data together but rather than simply ordering data based off of an index to zero with item the first the second like an array does.

<li>Objects are collections of properties.
<li>Properties are a key value pair.
<li>Rather than accessing data using an index, we use custom keys.
Property- key+ value
<br>

```js
const student = {
    name: "Tushar",
    rollno: 123,
    class: 12
}
```

in other languages like Python objects are actually
called dictionaries.

## Creating objects literals
Instead of the square braces that we use for an array we use curly braces to signify an object.

```js
// accessing properties
student.name // accessing name
```

>when we create an object when we make a property the keys are automatically converted to strings.

```js
let num ={
    34: "thirty four"
}
num.34 // throw error because it has converted to a string
```

### Accessing objects properties
```js
const colors ={
    red: "#eb4d4b",
    yellow: "#f9ca24",
    blue: "#30336b"
}
colors.red
colors['blue']
let cr = 'yellow';
colors[cr] 

const numbers = {
    100: 'one hundred',
    16: 'sixteen'
    '34 thing': "good"
};
numbers[100] // 'one hundred'
numbers['34 thing']
```

### Adding and updating properties

```js
const users={}
users['facebook'] = "Tushar";
users.insta = "tush_tr"; 
```

### Nested arrays and objects
We can fill objects with keys that are arrays or also keys that are other objects. And we do this all the time because most of the data we work with in the real world is generally a combination of list or ordered data as well as key value pairs of data.

```js
const shopCart = [
    {
        product: 'milk',
        price: 12,
        quantity: 1
    },
    {
        product: 'water bottle',
        price: 20,
        quantity: 5
    },
    {
        product: 'coffee',
        price: 2,
        quantity: 20
    }
]

const student = {
    firstName: 'Tushar',
    lastName: 'Rajpoot',
    hobbies: ['Music', 'reading'],
    marks:{
        mid: 56,
        final: 94
    }
}
```

We know that values in an array are not actually stored in a variable. The variable has limited space available to it. So it stores a reference sort of an address.<br>
objects also work the exact same way.

>we use const when we want the reference to stay the same like we always want to be pointing to this one object but the contents can come and go.

#### Equality in arrays and objects
the value of that variable has the little space in memory is not storing the array it's simply storing
a reference to this array.
```js
let n = [1,2,3];
let r = [1,2,3];
n==r // false
n===r // false
// so what we can do 
let newn = n;
// now
newn===n // true
```
 if you're trying to compare arrays if you're trying to see if an array is equal to another array it's not as straightforward as you might hope it would be because a lot of times you're not trying to check if an array is the exact same array.

<h1 id="loops">Loops in JavaScript</h1>
Doing things repeatedly.
<ul>
<li>
Loops allow us to repeat code
<li>---Print 'hello' 10 times</li>
<li>---Sum all numbers in an array</li>
</li>
<li>
There are multiple types:
<li>---For loop</li>
<li>---While Loop</li>
<li>---for....of loop</li>
<li>---for....in loop</li>
</li>
</ul>

## For Loops

```js
for(
    [initialExpression];
    [condition];
    [incrementExpression];
){}
// print hello 10 times--
for(let i=0;i<=10;i++){
    console.log('hello');
}
```

#### print a multiplication table
```js
const table = (num)=>{
    for(let i=0;i<=10;i++){
        console.log(`${num} X ${i} = ${num*i}`);
    }
}
table(4);
```

### For loops and arrays
we can use for loops to iterate over a string or an array.
<br>To loop over an array, start at 0 and continue to the last index(length-1).

```js
const students = ['Ram','Shyam','Mohan'];
for(let i=0;i<students.length;i++){
    console.log(i,students[i]);
}
// iterating a string
const studentName = "Tushar";
for(let i=studentName.length-1;i>=0;i--){
    console.log(studentName[i]);
}
```

### Nested for loops
we can nest loops
```js
for(let i=0;i<=10;i++){
    console.log("Outer loop",i);
    for(let j=10;j>=0;j--){
        console.log("Inner loop",j);
    }
}
// we can use nested loops for iterating 2d arrays
const gameBoard = [
    [4,32,8,4],
    [64,8,32,2],
    [8,32,16,4],
    [2,8,4,2]
];
for(let i=0;i < gameBoard.length;i++){
    // console.log(gameBoard[i]);
    for(let j=0;j<gameBoard[i].length;j++)
    {
        console.log(gameBoard[i][j]);
    }
}
// output---
/*
4
32
8
4
64
8
32
2
8
32
16
4
2
8
4
2
*/
```



## While Loops
A while loop continues to run as long as its test condition is true.
```js
let n = 0;
while(n<10){
    console.log(n);
    n++;
}
```

### Break Keyword
There is a special keyword in JavaScript called Break which we can use instead of loops to break out of that loop to stop its execution. Whenever javascript encounters break that loop that it's enclosed in is done so you can use this technically in a for loop.
```js
for(let i=0;i<10;i++){
    console.log(i);
    if(i===5){
        break;
    }
}
// in while loops
while(true){ // loop forever
    if(target === guess){
        break;
    }
}
```
### Continue keyword
for skipping something
```js
for(let i=0;i<10;i++){
    if(i===5){
        continue;
    }
    console.log(i)
}
```

## For of loop
A nice and easy way of iterating over arrays(or other iterable objects)[No internet explorer support]
```js
for(variable of iterable){
    statement
}
// example--
const arr = [1,2,3,4,5];
for(let i of arr){
    console.log(i);
}
// for of with objects
const movieRatings ={South: 9.5, BollyWood: 2.5,Hollywood: 9.8};
Object.keys(movieRatings)
// > ["South", "BollyWood", "Hollywood"]
Object.values(movieRatings)
// > [9.5, 2.5, 9.8]
for(let x of Object.keys(movieRatings)){
    console.log(x)
}
for(let ratings of Object.values(movieRatings)){
    console.log(ratings);
}
```

> We can loop over the keys of an object, using Object.key() and values using Object.values()

## For In Loop
Loop over the keys in an object
```js
for(variable in object){
    statement
}
// iterate over an object keys
const movieRatings ={South: 9.5, BollyWood: 2.5,Hollywood: 9.8};
for(let movie in movieRatings){
    console.log(movie)
}
// accessing values with for in loop
for(let movie in movieRatings){
    console.log(movie)
    console.log(movieRatings[movie])
}
```

<h1 id="functions">Functions</h1>

Reusable procedures
<li> Functions allow us to write reusable, modular code.
<li> We define a 'chunk' of code that we can then execute at a later point.

### Defining functions
```js
function funcName(){
    // do something
}
// let's write our first function
function hello(){
    console.log("Hello")
}
```

### function arguments

we can also write functions that accept inputs, called arguments.

```js
function greet(person){
    console.log(`hello ${person}`)
}
function add(a,b){
    console.log(a+b);
}
```

### Return statement
built-in methods return values when we call them. We can store those values:

```js
function add(x,y){
    return x+y;
}
console.log(add(2,3));
// we can capture a return value in a variable.
let a = add(2,3)
```

#### No return
our functions print values out, but don't return anything.
```js
function add(x,y){
    console.log(x+y)
}
add(3,3);
```






