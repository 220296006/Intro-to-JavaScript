# Functions

Generally speaking, a function is a "subprogram" that can be called by code external (or internal, in the case of recursion) to the function. Like the program itself, a function is composed of a sequence of statements called the function body. Values can be passed to a function as parameters, and the function will return a value.

To declare a function, you use the function keyword, followed by the function name, a list of parameters, and the function body as follows:

```JS

function functionName(parameters) {
    // function body
    // ...
}

```


The function name must be a valid JavaScript identifier. By convention, the function names are in camelCase and start with verbs like getData(), fetchContents(), and isValid().

A function can accept zero, one, or multiple parameters. In the case of multiple parameters, you need to use a comma to separate two parameters.

The following declares a function say() that accepts no parameter:

```JS

function say() {
}

```

The following declares a function named square() that accepts one parameter:

```JS

function square(a) {
}

```

And the following declares a function named add() that accepts two parameters:

```JS

function add(a, b) {
}

```

Inside the function body, you can write the code to implement an action. For example, the following say() function simply shows a message to the console:

```JS

function say(message) {
    console.log(message);
}

```

In the body of the say() function, we call the console.log() function to output a message to the console.

## Calling a function

To use a function, you need to call it. Calling a function is also known as invoking a function. To call a function, you use its name followed by arguments enclosing in parentheses like this:

```JS

functionName(arguments);

```

When calling a function, JavaScript executes the code inside the function body. For example, the following shows how to call the say() function:

```JS

say('Hello');

```

In this example, we call the say() function and pass a literal string 'Hello' into it.

## Parameters vs. Arguments

The terms parameters and arguments are often used interchangeably. However, they are essentially different.

When declaring a function, you specify the parameters. However, when calling a function, you pass the arguments that are corresponding to the parameters.

For example, in the say() function, the message is the parameter and the 'Hello' string is an argument that corresponds to the message parameter.

Returning a value
Every function in JavaScript implicitly returns undefined unless you explicitly specify a return value. For example:

```JS

function say(message) {
    console.log(message);
}

let result = say('Hello');
console.log('Result:', result);

```