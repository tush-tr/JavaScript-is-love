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
<li><a href="#scope">Scope,Function expressions, Higher Order functions, callbacks, hoisting</a>
<li><a href="#arraymethods">Array callback methods- filter, forEach, reduce, map, some, every etc.
</a>
<li><a href="#more-js">Default Parameters, Spreads,Rest Parameters, Destructuring</a>
<li><a href="#objectmethods">Object Methods and the "This" Keyword</a>
<li><a href="#dom">Document Object Model</a>
<li><a href="#events">Communicating with Events</a>
<li><a href="#async">Asynchronous JavaScript, Callbacks and Promises</a>
<li><a href="#making-requests">Making http requests: Fetch, Axios</a>


<br><br>

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

```javascript
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
<li>Songs in a playlist<br><br>

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
The sort() method sorts the elements of an array in place and returns the sorted array. The default sort order is ascending, built upon converting the elements into strings, then comparing their sequences of UTF-16 code units values.<br><br>

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





<h1 id="scope">Other Important concepts about functions</h1>

### What is scope?

> Variable "visibility"

<li>The location where a variable is defined dictates where we have access to that variable.

### Function Scope

```js
function show(){
    let msg = "Hey I'm here";
    // msg is scoped to the show function
}
// we can't access or manipulate msg variable outside of this function.
```

### Block Scope

```js
let rad = 8;
if(rad>0){
    var a = 12;
    const PI  = 3.14;
    let area = 2*PI*rad;
}
console.log(rad) // 8
console.log(area) // undefined
console.log(a) // 12
// this tells us that let and const have
// different scoping rules than var
// there was one more problem with var
let arr = [1,2,3,4];
for(var i=0;i<arr.length;i++){
    console.log(i,arr[i]);
}
console.log(i) // 3
```

### Lexical Scope
```js
function outer(){
    let hero = "Black Panther";
    function inner(){
        let cryForHelp = `${hero}, please save me! `;
        console.log(cryForHelp);
    }
    inner();
}
```

## Function Expressions
there's another syntax we can use to define functions:
```js
const square = function(num){
    return num*num;
}
square(7); // 49
```

The main distinction here is that the function does not actually have a name. It's stored in a variable but we haven't provided a name.

## Higher Order Functions
> Functions are objects
We can put functions in an array.<br>
We can also put a function in an object.

### Functions as arguments
passing functions as an argument to another function or returning a function which is actually a very key part of javascript.
<br>

#### What are higher order functions?
Functions that operate on/with other functions. They can:
<li>Accept other functions as arguments
<li>Return a function

```js
function callTwice(func){
    func();
    func();
}

function laugh(){
    console.log("hahahahahhah");
}

callTwice(laugh);
```

### Returning functions
```js
function makeBetweenFunc(min,max){
    return function (val){
        return val>=min && val<=max;
    }
}
const inAgeRange = makeBetweenFunc(18,100);
console.log(inAgeRange(45)) // true
```

## Callback Functions
A callback function is a function passed into another function as an argument, which is then  invoked inside the outer function.

```js
function callTwice(func){
    func();
    func();
}
function laugh(){
    console.log("hahahahha");
}
callTwice(laugh) // pass a function as argument
// so here laugh is a callback function
// we can also do the same like this
callTwice(function (){
    console.log("Calling again");
})
```

We can write our own function that accepts callbacks but also tons of the built in methods, that are really useful ones in JavaScript expect you to pass in a callback.
if you want to make a request to load data from Facebook API. That request takes time. We pass in a callback function that will be called when the request is finished. When the data is back if we want to run code when a user clicks on a button on a page or when they hover over a photo the code that we write to set that up requires us to pass in a callback function which will be executed when the user hovers or when the user clicks.

#### Anonymous functions
we use anonymous functions when we call callback functions(higher order functions). We pass in an anonymous function rather than an existing function like laugh.

There's nothing wrong with this
```js
callTwice(laugh)
```
but sometimes we just need a one time use function. We don't need it to be a standalone function in which case we use an anonymous function.

### setTimeout function
There is a method called set timeout set timeout will run a certain block of code or a function of code after a certain number of milliseconds or seconds we pass in a number of milliseconds like five thousand which is five seconds but the first argument we need to pass it is a function so a function to run and then how long to wait before it runs.

```js
function notice(){
    alert("go away");
}
setTimeout(notice,5000);
// this will wait till 5 second then execute notice function
// so we don't to define a function always we can use anonymous function like this
setTimeout(function(){
    alert("Go away");
},5000);
```

## Hoisting

>Hoisting is JavaScript's default behavior of moving declarations to the top.

Remember that variables when we declare them but don't initialize them. For example var x and I don't give it a value, X is set to undefined.
```js
let x;
>undefined
```

so when you execute a js program, it hoists up all variable declaration. for ex, if you try to run this code
```js
console.log(student); // undefined
var student = "Tushar"
```
When javascript is interpreting the code what happens is that it hoists up I'm doing air quotes but
you can't see it. It hoist up the variable declaration.(var student)

#### With let and const-
Variables defined with let and const are hoisted to the top of the block, but not initialized.
Meaning: The block of code is aware of the variable, but it cannot be used until it has been declared.

Using a let variable before it is declared will result in a ReferenceError.

>when you declare variable with let it's not hoisted.


Using a const variable before it is declared, is a syntax errror, so the code will simply not run.

> Let and const are not hoisted

#### Functions are hoisted
```js
show();
function show(){
    console.log("helooooo");
}
```

But But if we use function expression, it not gonna work
```js
console.log(show) // undefined because its a variable that has been declared
show(); // error
var show = function(){
    console.log("Hloooo")
}
// but if we declare this function using let or const it will not work.
```

<h1 id="arraymethods">Array callback methods</h1>

<li>Arrays come with many built-in methods that accept callback functions.

## For Each 
accepts a callback function.
Calls the function once per element in the array.

```js
const num = [1,2,3,4,5,6];
num.forEach(function(n){ // n parameter represents one element at a time
    console.log(n)
})
```
We can also add a second parameter to our callback to the function here if we want to use the index.
```js
num.forEach(function(e,i){
    console.log(i,e);
})
```

## Map Method
creates a new array with the results of calling a callback on every element in the array

```js
const texts = ['fer','rrer','rer','erre'];
const caps = texts.map(function(t){
    return t.toUpperCase();
})
```

## Arrow Functions
Syntactically compact alternative to a regular function expression.
```js
const square = (x)=>{
    return x*x;
}
```

### Implicit return
all these functions do the same thing:
```js
const isEven = function(num){
    return num%2===0;
}
const isEven = (num)=>{
    return num%2===0;
}
const isEven = num =>{
    return num%2===0;
}
const isEven = num =>{ // implicit return
    num%2===0
} 
const isEven = num=> num%2===0;// one-liner implicit return
```

## Find method
returns the value of the first element in the array that satisfies the provided testing function.

```js
let shoppingList = [
    "Veggies",
    "Milk",
    "Notebooks"
]
let item = shoppingList.find(item=>{
    return item.includes("Milk");
})
```

## Filter method
creates a new array with all elements that pass the test implemented by the provided function.
```js
const numbers = [12,334,542,3,34,54,5,45,3,4,523,6,3]
const evens = numbers.filter(n=>{
    return n%2===0;
})
```

## Every and Some method
#### Every-
tests whether all elements in the array pass the provided function It returns a boolean value.
```js
const words = ['dog','dog','dig','dag','bag'];
words.every(word=>{
    return word.length === 3;
}) // true
```

#### Some -
Similar to every, but returns true if any of the array elements pass the test function.
```js
words.some(word=>{
    return word.length >4;
})
```

## Sort
<pre>
arr.sort(compareFunc(a,b)))
</pre>
<li>If compareFunc(a,b) returns less than 0 
-> Sort a before b
<li>If compareFunc(a,b) returns 0
-> leave a and b unchanged with respect to each other
<li>If compareFunc(a,b) returns greater than 0
-> Sort b before a



```js
const prices = [122,4542,453,5248,78709,3435];
prices.sort(); // it's weird converts into strings then sort

prices.sort((a,b)=> a-b);

prices.sort((a,b)=>b-a);

```

## Reduce Method
executes a reducer function on each element of the array, resulting in a single value.

#### Summing an array
```js
const arr = [3,5,7,9,11];
arr.reduce((accumulator, currentValue)=>{
    return accumulator+currentValue;
})
```

<table>
<tr>
<td>Callback</td>
<td>Accumulator</td>
<td>Currentvalue</td>
<td>return value</td>
</tr>
<tr>
<td>first call</td>
<td>3</td>
<td>5</td>
<td>8</td>
</tr>
<tr>
<td>second call</td>
<td>8</td>
<td>7</td>
<td>15</td>
</tr>
<tr>
<td>third call</td>
<td>15</td>
<td>9</td>
<td>24</td>
</tr>
<tr>
<td>fourth call</td>
<td>24</td>
<td>11</td>
<td>35</td>
</tr>
</table>


it's not always about summing or multiplying or accumulating data in one number. It could be finding the maximum value in an entire array.

#### Initial value
when you use reduce you can actually pass in an initial starting value. So after your callback the format would be something dot reduce.
```js
[12,23,5,6].reduce((acc,curr)=>{
    return acc+curr;
},100)
```

#### Tallying
we can tally up results from an array we can group different values in an array using an object.
```js
const vote = ['y','y','n','y','y','y','n']
const tally = vote.reduce((tally, vote)=>{
    tally[vote] = (tally[vote] || 0)+1
    return tally;
},{})
// {}- initial object
```
<h1 id="more-js">Default Parameters, Spreads,Rest Parameters, Destructuring</h1>

list of some important JS new features
<table>
<tr>
<td>Arrow functions</td>
<td>String template literals</td>
<td>Let and const</td>
</tr>
<tr>
<td>For...of</td>
<td>for...in</td>
<td>Exponent operator</td>
</tr>
<tr>
<td>String.includes()</td>
<td>Array.includes()</td>
<td>Object.values()</td>
</tr>
<tr>
<td>Rest & Spread</td>
<td>Destructuring</td>
<td>Default function params</td>
</tr>
<tr>
<td>Object Enhancements</td>
<td>Classes</td>
<td>Async Functions</td>
</tr></table>

## Default parameter
```js
function multiply(a,b=1){
    //means if no b is passed in if it's undefined.  Use this value.
    return a*b;
}
multiply(4); // 4
multiply(4,3); // 12
```

## Spread
It does many things.
<br>
Spread syntax allows an iterable such as an array to be expanded in places where zero or more arguments(for function calls) or elements(for array literals) are expected, or an object expression to be expanded in places where zero or more key-value pairs(for object literals) are expected.

```js
function sum(x, y, z) {
  return x + y + z;
}

const numbers = [1, 2, 3];

console.log(sum(...numbers));
// expected output: 6
console.log(sum.apply(null, numbers));
// expected output: 6
```

### Spread in array literals
In array literals -
<br>
Create a new array using an existing array. Spreads the elements from one array into a new array.

```js
const n1 = [1,2,3];
const n2 = [4,5,6];
[...n1,...n2];
// [1,2,3,4,5,6]

['a','b',...n2];
// ["a","b",4,5,6]

const a = [1,2,3]
const b = [23]
b.push(...a)
console.log(b)
// [23, 1, 2, 3]
```

#### In object literals
copies properties from one object into another object literal.

```js
const dog = {name: "Joolie",age:6};
const animal = {...dog, isPet: true};
// {name: "Joolie",age:6,isPet: true}
```

## The arguments object
<li>Available inside every function
<li>It's like an array-like object
<br>Has a length  property
<br>Does not have array methods like push/pop
<li>Contains all the arguments passed to the function
<li>Not available inside of arrow functions

```js
function sumAll(){
    let total = 0;
    for(let i=0; i< arguments.length; i++){
        total += arguments[i];
    }
    return total;
}
sumAll(8,3,4,5);
```

## Rest (...) Params
collects all remaining arguments into an actual array.

```js
function sum(...numbers){
    return nums.reduce((t,c)=>{
        return t+c;
    })
}
// we can use this in arrow function
const fullName = (firstName, secondName, ...titles)=>{
    console.log('first',firstName)
    console.log('second',secondName)
    console.log('titles',titles)
}
```


## Destructuring
A short, clean syntax to 'unpack':
<li> values from arrays
<li> Properties from objects
Into distinct variables.

### Destructuring arrays
```js
const arr = [223,535,536];
const [one,two,three] = arr;
one// 223
two // 535
three // 536

const [one, ...everyElse] = arr;
one // 223
everyElse // [535,536]
```

### Destructuring objects
```js
const runner = {
    first :  "Eliud",
    last: "Kipchoge",
    country: "Kenya",
    title: "Elder of the order of the golden heart of kenya"
}

const {first, last, country} = runner;
first // "Eliud"
last // "Kipchoge"
country // "Kenya"

const {country: nation} = runner;
nation // "Kenya"
```

### Parameters destructuring
```js
const fullName = ({first,last})=>{
    return `${first} ${last}`
}
const runner = {
    first :  "Eliud",
    last: "Kipchoge",
    country: "Kenya",
    title: "Elder of the order of the golden heart of kenya"
}
fullName(runner); // Eliud Kipchoge
```

<h1 id="objectmethods">Object Methods and the "This" Keyword</h1>

### Short hand properties
```js
const a = 12;
const t = "Tushar";
const n = {a,t};
console.log(n)
// {a: 12, t: "Tushar"}
```

### Computed Properties
we can use a variable as a key name in an object literal property.
```js
const role = 'SDE';
const person = "Tushar";
const role2 = 'Sys Admin';
const person2 = 'Navneet';

const team = {};
team[role] = person;
team[role2] =  person2;
// or
const team = {
    [role]: person,
    [role2]: person2,
    [23+34]: 'Another'
}

const addProp = (obj,k,v)=>{
    return{
        ...obj,
        [k]:v
    }
}
```

## Methods
We can add functions as properties on objects.

we call them methods.

```js
const math ={
    multiply: function(x,y){
        return x*y;
    },
    divide: function(x,y){
        return x/y;
    }
}
```

### Method short hand syntax
we do this so often that there's a new shorthand way ofadding methods.

```js
const math = {
    msg: "Hii this is math",
    add(x,y){
        return x+y;
    }
    multiply(x,y){
        return x*y
    }
}

math.add(40,50) // 90
```

## This keyword
The JavaScript this keyword refers to the object it belongs to. It has different values depending on where it is used: ... In a function, this refers to the global object. 


It has different values depending on where it is used:
<li>In a method, this refers to the owner object.
<li>Alone, this refers to the global object.
<li>In a function, this refers to the global object.
<li>In a function, in strict mode, this is undefined.
<li>In an event, this refers to the element that received the event.
<li>Methods like call(), and apply() can refer this to any object.

>The value of this depends on the invocation context the unction it is used in.

```js
const person = {
    first: "Tushar",
    last : "Rajpoot",
    nickName: false,
    fullName(){
        // console.log(this)
        return `${this.first} ${this.last}`
    },
    printBio(){
        const fullName = this.fullName();
        console.log(`${fullName} is a person`)
    }
}
```
> We should not use arrow functions in methods


<h1 id="dom" align=center> Document Object Model</h1>
<li>The DOM is a JavaScript representation of a webpage.
<li>It's your JS "window" into the contents of a webpage
<li>It's just a bunch of objects that you can interact with via JS.

### The Document Object
The document object is our entry point into the world of the DOM. It contains representations of all the content on a page, plus tons of useful methods and properties.

### Selecting
<li>getElementById
<li>getElementsByTagName
<li>getElementsByClassName

#### querySelector
<li>A newer, all-in-one method to select a single element.
<li>Pass in a CSS selector

```js
const btn = document.querySelector(".red")
```


#### querySelectorAll
Same idea but it selects a collection of elements.

```js
const buttons = document.querySelector(".red")
```

### properties and methods

<li>classList
<li>getAttribute()
<li>setAttribute()
<li>appendChild()
<li>append()
<li>prepend()
<li>removeChild()
<li>remove()
<li>createElement
<li>innerText
<li>textContent
<li>innerHTML
<li>value
<li>parentElement
<li>children
<li>nextSibling
<li>previousSibling
<li>style

### Events in DOM
Responding to user inputs and actions !

<li>clicks
<li>drags
<li>drops
<li>hovers
<li>scrolls
<li>form submission
<li>key presses
<li>focus/blur
<li>mouse wheel
<li>double click
<li>copying
<li>pasting
<li>audio start
<li>screen resize
<li>printing


### addEventListener
Specify the event type and a callback to run.

```js
const button = document.querySelector("h1");
button.addEventListener("click",()=>{
    alert("You clicked me")
})
```


### getAttribute() and setAttribute()

```js
const btn = document.querySelector('input[type="submit"]')

btn.getAttribute('type')
>"submit"
btn.setAttribute('type','new')
```

### finding parent/children/sibling

```js
element.parentElement
element.children
element.nextSibling
element.previousSibling
```

### changing multiple elements

```js
const buttons = document.querySelectorAll('.btn')
buttons.forEach((e)=>{
    e.innerText = 'new Button'
})
```

### Altering styles
every element has a style property.

we can use the style property to change colors or styles we can change any of those properties and they will be affected on the page but if we're trying to use the style property to read existing properties to read existing styles it won't work unless those styles are defined inline.

#### getComputedStyle
```js
let styles = getComputedStyle(h1)
```

### Manipulating classes

```js
todo.setAttribute("class","done")
// remove a class
todo.classList.remove('done')
// add a class
todo.classlist.add('done')
// check element has class or not
todoAdd.getAttribute('class').includes('done')
// toggle will remove if class exist and add class if it doesn't'
todoAdd.classList.toggle('done')
```


### Creating elements

```js
let h1 = document.createElement('h1')
h1.innerText = "This is heading 1"
// add class to the element
h1.classList.add('heading')
// add an id to the element
h1.setAttribute('id','heading1')

// add an element to the existing element
const section = document.querySelector('section')
const newImg = document.createElement('img')
newImg.setAttribute('src',url)
section.appendChild(newImg)
```

### append, prepend and insertBefore

```js
const parentUl = document.querySelector('ul')
const newLi = document.createElement('li')
newLi.innerText = "Tushar"
parentUl.appendChild(newLi)
const firstLi = document.querySelector('li')​
parentUl.insertBefore(newLi,firstLi)
```

#### insertAdjacentElement


```js
element.insertAdjacentHTML(position, text);
```

>'beforebegin': Before the element itself.
>'afterbegin': Just inside the element, before its first child.
>'beforeend': Just inside the element, after its last child.
>'afterend': After the element itself.

```HTML
<!-- beforebegin -->
<p>
  <!-- afterbegin -->
  foo
  <!-- beforeend -->
</p>
<!-- afterend -->
```
```js
const le = document.createElement('li')
h1.insertAdjacentElement('beforebegin',le)
```

#### append()
```js
firstP.append(i,newLi);
firstP.prepend(i,newLi)
```

#### removeChild()
```js
const ul = document.querySelector('ul')​
const removeMe = ul.querySelector('.special')​
ul.removeChild(removeMe)
```

#### remove()
> doesn't need parent element

```js
removeMe.remove()
```

<h1 id="events"> DOM Events</h1>

#### Responding to user inputs and actions.

<li>clicks
<li>drags
<li>drops
<li>hovers
<li>scrolls
<li>form submission
<li>key presses
<li>focus/blur
<li>mouse wheel
<li>double click
<li>copying
<li>pasting
<li>audio start
<li>screen resize
<li>printing

## Using Events
### using on
```HTML
<button onclick="fun()">Click</button>
```
>More content will be added soon for events
<hr>



<h1 id="async" align=center>Asynchronous JavaScript, Callbacks and Promises</h1>

## Call Stack
The mechanism the JS interpreter uses to keep track of its place in a script that calls multiple functions.

How JS "knows" what function is currently being run and what functions are called from within that function etc.

### How it works

<li> When a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function.

<li>Any functions that are called by that function are added the call stack further up, and run where their callls are reached

<li>When the current function is finished, the interpreter takes it off the stack and resumes execution where it left off the last code listing.

>Stack is a linear data structure which follows a particular order in which the operations are performed. The order may be LIFO(Last In First Out) or FILO(First In Last Out). There are many real-life examples of a stack

```js
const multiply = (x,y) => x*y;
const square = (x) => multiply(x,x);

const isRightTriangle = (a,b,c)=>{
    return square(a) + square(b)=== square(c);
}

isRightTriangle(3,4,5);
// square(3) + square(4)===square(4)

```

## JavaScript is a single threaded language
At any given point in time, that single JS thread is running at most one line of JS code.


## How asynchronous callbacks actually work?

<li>Browsers come with web APIs that are able to handle certain tasks in the background (like making requests or setTimeout)                   
<li>The JS call stack regocnizes these web API functions and passes them off to the browser to take care of
<li>Once the browser finishes those tasks, they return and are pushed onto the stack as a callback.

try your code here :- <a href="http://latentflip.com/loupe/?code=JC5vbignYnV0dG9uJywgJ2NsaWNrJywgZnVuY3Rpb24gb25DbGljaygpIHsKICAgIHNldFRpbWVvdXQoZnVuY3Rpb24gdGltZXIoKSB7CiAgICAgICAgY29uc29sZS5sb2coJ1lvdSBjbGlja2VkIHRoZSBidXR0b24hJyk7ICAgIAogICAgfSwgMjAwMCk7Cn0pOwoKY29uc29sZS5sb2coIkhpISIpOwoKc2V0VGltZW91dChmdW5jdGlvbiB0aW1lb3V0KCkgewogICAgY29uc29sZS5sb2coIkNsaWNrIHRoZSBidXR0b24hIik7Cn0sIDUwMDApOwoKY29uc29sZS5sb2coIldlbGNvbWUgdG8gbG91cGUuIik7!!!PGJ1dHRvbj5DbGljayBtZSE8L2J1dHRvbj4%3D">click here</a>


## Callback Hell

### What is Synchronous Javascript?
In Synchronous Javascript, when we run the code, the result is returned as soon as the browser can do. Only one operation can happen at a time because it is single-threaded. So, all other processes are put on hold while an operation is executing.

### What is Asynchronous Javascript?

<li>Some functions in Javascript requires AJAX because the response from some functions are not immediate. It takes some time and the next operation cannot start immediately. It has to wait for the function to finish in the background. In such cases, the callbacks need to be asynchronous.
<li>There are some external Javascript Web APIs that allows AJAX – Asynchronous Javascript and XML.
In AJAX, many operations can be performed simultaneously.

### What is a callback?

<li>Callbacks are nothing but functions that take some time to produce a result.
<li>Usually these async callbacks (async short for asynchronous) are used for accessing values from databases, downloading images, reading files etc.
<li>As these take time to finish, we can neither proceed to next line because it might throw an error saying unavailable nor we can pause our program.
<li>So we need to store the result and call back when it is complete.

### What is callback hell?
This is a big issue caused by coding with complex nested callbacks. Here, each and every callback takes an argument that is a result of the previous callbacks. In this manner, The code structure looks like a pyramid, making it difficult to read and maintain. Also, if there is an error in one function, then all other functions get affected.

# Promises
A promise is an object representing the eventual completion or failure of an asynchronous operation. 

> A Pattren for writing async code. 

A promise is a returned object to which we can attach callbacks, instead of passing callbacks into a function.

when we create a promise, we pass in a function. And this function has two parameters. Always these two parameters we usually call resolve and reject. And these are actually functions. 

Inside of inside promise function if we call resolve, the promise will be resolved. If we call reject, the promise will be rejected.

<li>If we don't resolve or reject it, it's status will be pending.
<li>If we reject it, our promise status will be rejected.
<li>If we resolve it, promise status will be resolved. 



```js
// create a promise which resolved using a random number
const getMePhone = new Promise((resolve,reject) => {
    let rand = Math.random()
    if(rand<0.5){
        resolve()
    }
    else{
        reject()
    }

})
```

#### How do I run code if this promise was rejected versus run code, if this promise was resolved?
<b>.then:</b> every promise has a then method. this then method will run if our promise is resolved.

<b>.catch</b> Every promise has a catch method also. We can chain it with .then or we can write along with promise.

```js
getMePhone.then(()=>{
    console.log("Yeah I got a Phone")
}).catch(()=>{
    console.log("No Phone")
})
```



## Returning promises from Functions

```js
// returning a promise from a function
const makeDogPromise = () => {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            const rand = Math.random();
            if (rand < 0.5) {
                resolve()
            }
            else
                reject()
        }, 5000)
    })
}
makeDogPromise().then(()=>{
    console.log("hello")
})
```

## Resolving/rejecting promises with values
we can pass information in to the resolve or reject calls.
```js
const fakeRequest = (url)=>{
    return new Promise((resolve,reject)=>{
        setTimeout(()=>{
            const pages = {
                '/users' : "Users pages",
                '/about' : "About page"
            }
            const data = pages[url]
            if(data){                

                resolve(pages[url])
            }
            else{
                reject({status:400})
            }
        },2000)
    })
}

fakeRequest('/users').then((data)=>{
    console.log(data)
}).catch((res)=>{console.log(res.status)})
```

## Promise Chaining
```js
const fakeRequest = (url) => {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            const pages = {
                '/users': [
                    { id: 1, username: 'Tushar' },
                    { id: 5, username: 'Rahul' }
                ],
                '/users/1': {
                    id: 1,
                    username: 'Tushar',
                    country: 'India',
                    work: 'Noida',
                    role: 'Software Engineer',
                    postid: 54
                },
                '/users/5': {
                    id: 5,
                    username: 'Rahul',
                    country: 'India',
                    work: 'Noida',
                    role: 'DevOps Engineer'
                },
                '/posts/54': {
                    id: 54,
                    title: 'My new Post',

                },
                '/about': "About page"
            }

            const data = pages[url]
            if (data) {
                resolve(pages[url])
            }
            else {
                reject({ status: 400 })
            }
        }, 2000)
    })
}

fakeRequest('/users').then((data) => {
    let id = data[0].id;
    return fakeRequest(`/users/${id}`)
})
    .then((data) => {
        // console.log(data)
        let postid = data.postid;
        return fakeRequest(`/posts/${postid}`)
    })
    .then((data) => {
        console.log(data)
    })
    .catch((err) => { console.log(err) })
```

<hr>

<h1 id="making-requests" align=center>Making http requests</h1>

<li>XMLHTTP (old standard method)
<li>Fetch (a better way)
<li>Axios (a third party library)

## What is AJAX?
Asynchronous Javascript and XML.<br>
AJAX is a technique for accessing web servers from a web page.
<li>Read data from a web server - after a web page has loaded
<li>Update a web page without reloading the page
<li>Send data to a web server - in the background

### AJAX just uses a combination of:<br>
A browser built-in XMLHttpRequest object (to request data from a web server)
JavaScript and HTML DOM (to display or use the data)


AJAX allows web pages to be updated asynchronously by exchanging data with a web server behind the scenes. This means that it is possible to update parts of a web page, without reloading the whole page.

<img src="https://www.w3schools.com/whatis/img_ajax.gif">

1. An event occurs in a web page (the page is loaded, a button is clicked)
2. An XMLHttpRequest object is created by JavaScript
3. The XMLHttpRequest object sends a request to a web server
4. The server processes the request
5. The server sends a response back to the web page
6. The response is read by JavaScript
7. Proper action (like page update) is performed by JavaScript

## XML and JSON 
AJAJ- Asyncrhonous Javascript and JSON .

XML and JSON are two ways of basically formatting data so that you can send it from a server to another server or a server to a browser.

### XML Format

```XML
<note>
<to>Tove</to>
<from>Jani</from>
<heading>Reminder</heading>
<body>Don't forget me this weekend!</body>
</note>
```

### JSON Format
(JavaScript Object Notation)

```JSON
{  
    "employee": {  
        "name":       "sonoo",   
        "salary":      56000,   
        "married":    true  
    }  
}  
```

<li>JSON is not JS object
<li>Every key in JSON must be a string 
<li>We can also use arrays in JSON 
<li>We can easily translate between JSON to JavaScript

## XMLHttpRequest 
<li>The "original" way of sending requests via JS.
<li>Does not support promises, so... lots of callbacks
<li>WTF is going on with the weird capitalization
<li>Clunky syntax that I find difficult to remember.

```js
const myReq = new XMLHttpRequest();
myReq.onload = function(){
    const data = JSON.parse(this.responceText)
    console.log(data);
}
myReq.onerror = (err)=>{
    console.log("Error",err)
}
myReq.open('get','sample.com',true);
myReq.setRequestHeader('Accept','application/json');
myReq.send();
console.log(myReq.response)
```

## Making requests using fetch
<li>The newer way of making requests via JS.
<li>Supports promises. 
<li>Not supported in Internet Explorer.

```js
fetch('url',{header: { Accept: 'application/json'}})
.then((res)=> {
    if(res.status!=200){
        console.log("Problem",res.status)
        return;
    }
    res.json().then((data)=> {
        console.log(data)
    })

})
.catch((err)=> {console.log(err)})
```
### Chaining fetch requests

```js
const url = "https://swapi.dev/api/planets";
fetch(url).then((res)=>{
    return res.json()
    
})
.then((data)=>{
    return data.results
})
.then((results)=>{
    const filmUrl = results[0].films[0];
    return fetch(filmUrl)
})
.then((results)=>{
    return results.json()
}).then((data)=>{
    console.log(data)
})
.catch((err)=>{console.log(err)})
```

### Refactoring fetch requests
```js
const checkStatusAndParse = (response)=>{
    if(!response.ok) throw new Error('Status code error')
    return response.json();
}
const printPlanets = (data)=>{
    console.log("FETCHED ALL PLANETS")
    data.results.forEach((planet)=>{
        console.log(planet.name)
    })
    return Promise.resolve(data.next)
}

const fetchMorePlanets = (url)=>{
    return fetch(url);
}

fetch(url)
.then(checkStatusAndParse)
.then(printPlanets)
.then(fetchMorePlanets)
.then(checkStatusAndParse)
.then(printPlanets)
.catch((err)=>{console.log(err)})
```

## Axios
<li>A library for making http requests. 

```js
axios.get(url).then((res)=>{
    console.log(res.data)
})
.catch((err)=>{
    console.log(err)
})
```

## Sequential requests using axios
```js
const showData = ({data})=>{
    data.results.forEach((planet) => {
        console.log(planet.name)
    })
    return axios.get(data.next)
}

axios.get(url)
.then(showData)
.then(showData)
```

<hr>










