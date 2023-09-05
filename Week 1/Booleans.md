# JavaScript Booleans

## JavaScript boolean primitive type

JavaScript provides a boolean primitive type that has two values of true and false. The following example declares two variables that hold boolean values of false and true:

```JS

let isPending = false;
let isDone = true;

```

When you apply the  typeof operator to a variable that holds a primitive boolean value, you get the boolean as the following example:

```JS
console.log(typeof(isPending)); //  boolean
console.log(typeof(isDone)); // boolean

```

## JavaScript Boolean object

In addition to the boolean primitive type, JavaScript also provides you with the global Boolean() function, with the letter B in uppercase, to cast a value of another type to boolean.

The following example shows how to use the Boolean() function to convert a string into a boolean value. Because the string is not empty, it returns true.

```JS

let a = Boolean('Hi');
console.log(a); // true
console.log(typeof(a)); // boolean

```

The Boolean is also a wrapper object of the boolean primitive type. It means that when you pass either true or false to the Boolean constructor, it’ll create a Boolean object. For example:

```JS

let b = new Boolean(false);

```

To get the primitive value back, you call the valueOf() method of the Boolean object as follows:

```JS
console.log(b.valueOf()); // false

```

However, if you call the toString() method of a Boolean object, you get a string value "true" or "false". For example

```JS
console.log(b.toString()); // "false"

```

## JavaScript boolean vs. Boolean

Consider this example:

```JS

let completed = true;
let active = new Boolean(false);

```

first, active is an object so you can add a property to it:

```JS

active.primitiveValue = active.valueOf();
console.log(active.primitiveValue); // false

```

However, you cannot do it with the primitive boolean variable like the completed variable:

```JS

completed.name = 'primitive';
console.log(completed.name); // undefined

```

Second, the typeof of Boolean object returns object, whereas the typeof of a primitive boolean value returns boolean.

```JS

console.log(typeof completed); // boolean
console.log(typeof active); // object

```

Third, when applying the  instanceof operator to a Boolean object, it returns true. However, it returns false if you apply the  instanceof operator to a boolean value.

```JS

console.log(completed instanceof Boolean); // false
console.log(active instanceof Boolean); // true

```

It is a good practice never to use the Boolean object because it will create many confusions, especially when using in an expression. For example:

```JS

let falseObj = new Boolean(false);
if (falseObj) {
    console.log('weird part of the Boolean object');
}

```

How the script works.

* First, create falseObj as a Boolean object wrapper for the false value.
* Second, use falseObj in the  if statement. Because falseObj is an object, and JavaScript engine coerces it to a boolean value of true. As a result, the statement inside the if block is executed.

It is recommended that you use the Boolean() function to convert a value of a different type to a Boolean type, but you should never use the Boolean as a wrapper object of a primitive boolean value.

In this tutorial, you have learned about the JavaScript Boolean object and the differences between the Boolean object and boolean primitive type.