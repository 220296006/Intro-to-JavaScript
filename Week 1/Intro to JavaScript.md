# Introduction to JavaScript
JavaScript is the world's most popular programming language.
JavaScript is a cross-platform, object-oriented scripting language used to make webpages interactive (e.g., having complex animations, clickable buttons, popup menus, etc.). There are also more advanced server side versions of JavaScript such as Node.js, which allow you to add more functionality to a website than downloading files (such as realtime collaboration between multiple computers). Inside a host environment (for example, a web browser), JavaScript can be connected to the objects of its environment to provide programmatic control over them.

JavaScript contains a standard library of objects, such as Array, Date, and Math, and a core set of language elements such as operators, control structures, and statements. Core JavaScript can be extended for a variety of purposes by supplementing it with additional objects; for example:

### Client-side

Client-side JavaScript extends the core language by supplying objects to control a browser and its Document Object Model (DOM). For example, client-side extensions allow an application to place elements on an HTML form and respond to user events such as mouse clicks, form input, and page navigation.

### Server-side 

Server-side JavaScript extends the core language by supplying objects relevant to running JavaScript on a server. For example, server-side extensions allow an application to communicate with a database, provide continuity of information from one invocation to another of the application, or perform file manipulations on a server.
This means that in the browser, JavaScript can change the way the webpage (DOM) looks. And, likewise, Node.js JavaScript on the server can respond to custom requests sent by code executed in the browser.

###  JavaScript and Java
JavaScript and Java are similar in some ways but fundamentally different in some others. The JavaScript language resembles Java but does not have Java's static typing and strong type checking. JavaScript follows most Java expression syntax, naming conventions and basic control-flow constructs which was the reason why it was renamed from LiveScript to JavaScript.

In contrast to Java's compile-time system of classes built by declarations, JavaScript supports a runtime system based on a small number of data types representing numeric, Boolean, and string values. JavaScript has a prototype-based object model instead of the more common class-based object model. The prototype-based model provides dynamic inheritance; that is, what is inherited can vary for individual objects. JavaScript also supports functions without any special declarative requirements. Functions can be properties of objects, executing as loosely typed methods.

## Javascript Basics

JavaScript borrows most of its syntax from Java, C, and C++, but it has also been influenced by Awk, Perl, and Python.

##  Variables

### How to create variables:

``` JavaScript

var x;
let y;

```
### How to use variables:

``` js
x = 5;
y = 6;

let z = x + y;

```

### Create and Initialise a const variable

JavaScript is case-sensitive and uses the Unicode character set. For example, the word Früh (which means "early" in German) could be used as a variable name.

``` js

const Früh = "foobar";

```
But, the variable früh is not the same as Früh because JavaScript is case sensitive.

In JavaScript, instructions are called statements and are separated by semicolons (;).

A semicolon is not necessary after a statement if it is written on its own line. But if more than one statement on a line is desired, then they must be separated by semicolons.


### Increment and Decrement in JavaScript

Increment (++)

The increment (++) operator increments (adds one to) its operand and returns the value before or after the increment, depending on where the operator is placed.

```js

let x = 3;
const y = x++;

console.log(`x:${x}, y:${y}`);
// Expected output: "x:4, y:3"

let a = 3;
const b = ++a;

console.log(`a:${a}, b:${b}`);
// Expected output: "a:4, b:4"

```

Decrement (--)

The decrement (--) operator decrements (subtracts one from) its operand and returns the value before or after the decrement, depending on where the operator is placed.

```js

let x = 3;
const y = x--;

console.log(`x:${x}, y:${y}`);
// Expected output: "x:2, y:3"

let a = 3;
const b = --a;

console.log(`a:${a}, b:${b}`);
// Expected output: "a:2, b:2"

```