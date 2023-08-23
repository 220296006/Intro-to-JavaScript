# Strings and Arrays

##  Strings 

The String object is used to represent and manipulate a sequence of characters.

## Description

Strings are useful for holding data that can be represented in text form. Some of the most-used operations on strings are to check their length, to build and concatenate them using the + and += string operators, checking for the existence or location of substrings with the indexOf() method, or extracting substrings with the substring() method.

```JS

const string1 = "A string primitive";
const string2 = 'Also a string primitive';
const string3 = `Yet another string primitive`;

const string4 = new String("A String object");


```

## Character access
There are two ways to access an individual character in a string. The first is the charAt() method:

```JS

"cat".charAt(1); // gives value "a"

"cat"[1]; // gives value "a"

```

## Comparing strings

Use the less-than and greater-than operators to compare strings

```JS

const a = "a";
const b = "b";
if (a < b) {
  // true
  console.log(`${a} is less than ${b}`);
} else if (a > b) {
  console.log(`${a} is greater than ${b}`);
} else {
  console.log(`${a} and ${b} are equal.`);
}

```

### String primitives and String objects

Note that JavaScript distinguishes between String objects and primitive string values. (The same is true of Boolean and Numbers.)

String literals (denoted by double or single quotes) and strings returned from String calls in a non-constructor context (that is, called without using the new keyword) are primitive strings. In contexts where a method is to be invoked on a primitive string or a property lookup occurs, JavaScript will automatically wrap the string primitive and call the method or perform the property lookup on the wrapper object instead.

```JS
const strPrim = "foo"; // A literal is a string primitive
const strPrim2 = String(1); // Coerced into the string primitive "1"
const strPrim3 = String(true); // Coerced into the string primitive "true"
const strObj = new String(strPrim); // String with new returns a string wrapper object.

console.log(typeof strPrim); // "string"
console.log(typeof strPrim2); // "string"
console.log(typeof strPrim3); // "string"
console.log(typeof strObj); // "object"

```

## Arrays

The Array object, as with arrays in other programming languages, enables storing a collection of multiple items under a single variable name, and has members for performing common array operations.

### Description

In JavaScript, arrays aren't primitives but are instead Array objects with the following core characteristics:

JavaScript arrays are resizable and can contain a mix of different data types. (When those characteristics are undesirable, use typed arrays instead.)

JavaScript arrays are not associative arrays and so, array elements cannot be accessed using arbitrary strings as indexes, but must be accessed using nonnegative integers (or their respective string form) as indexes.

JavaScript arrays are zero-indexed: the first element of an array is at index 0, the second is at index 1, and so on — and the last element is at the value of the array's length property minus 1.
JavaScript array-copy operations create shallow copies. (All standard built-in copy operations with any JavaScript objects create shallow copies, rather than deep copies).

```JS

 const myGames = [ "CALL OF DUTY", "PAC-MAN", "SUPER MARIO BROS"];

 myGames.push("SPIDER-MAN: 2");

 console.log(myGames); // 4 Games in myGames array

```

## Relationship between length and numerical properties

A JavaScript array's length property and numerical properties are connected.

Several of the built-in array methods (e.g., join(), slice(), indexOf(), etc.) take into account the value of an array's length property when they're called.

Other methods (e.g., push(), splice(), etc.) also result in updates to an array's length property.


```JS

 const myGames = [ ];

 myGames.push("CALL OF DUTY", "PAC-MAN", "SUPER MARIO BROS");

 console.log(myGames.length); // 3

```
## Accessing the First Array Element

```JS

 const myGames = [ "CALL OF DUTY", "PAC-MAN", "SUPER MARIO BROS"];

 let myGames = myGames[0];

```

## Accessing the Last Array Element


```JS

 const myGames = [ "CALL OF DUTY", "PAC-MAN", "SUPER MARIO BROS"];

 let myGames = myGames[myGames.length -1];

```

## Array Elements Can Be Objects
JavaScript variables can be objects. Arrays are special kinds of objects.

Because of this, you can have variables of different types in the same Array.

You can have objects in an Array. You can have functions in an Array. You can have arrays in an Array:

```JS

myArray[0] = Date.now;
myArray[1] = myFunction;
myArray[2] = myCars;

```

## Array methods and empty slots

Empty slots in sparse arrays behave inconsistently between array methods. Generally, the older methods will skip empty slots, while newer ones treat them as undefined.

Among methods that iterate through multiple elements, the following do an in check before accessing the index and do not conflate empty slots with undefined:

```JS

concat()
copyWithin()
every()
filter()
flat()
flatMap()
forEach()
indexOf()
lastIndexOf()
map()
reduce()
reduceRight()
reverse()
slice()
some()
sort()
splice()


entries()
fill()
find()
findIndex()
findLast()
findLastIndex()
includes()
join()
keys()
toLocaleString()
values()

```


