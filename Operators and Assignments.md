#  Operators & Assignments

## Addition (+)

The addition (+) operator produces the sum of numeric operands or string concatenation.

```JS

console.log(2 + 2);
// Expected output: 4

console.log(2 + true);
// Expected output: 3

console.log('hello ' + 'everyone');
// Expected output: "hello everyone"

console.log(2001 + ': A Space Odyssey');
// Expected output: "2001: A Space Odyssey"

```

### Syntax 

```JS
x + y

```

### Description

The + operator is overloaded for two distinct operations: numeric addition and string concatenation. When evaluating, it first coerces both operands to primitives. Then, the two operands' types are tested:

If one side is a string, the other operand is also converted to a string and they are concatenated.

String concatenation is often thought to be equivalent with template literals or String.prototype.concat(), but they are not. Addition coerces the expression to a primitive, which calls valueOf() in priority; on the other hand, template literals and concat() coerce the expression to a string, which calls toString() in priority. If the expression has a @@toPrimitive method, string concatenation calls it with "default" as hint, while template literals use "string". This is important for objects that have different string and primitive representations — such as Temporal, whose valueOf() method throws.

```JS

const t = Temporal.Now.instant();
"" + t; // Throws TypeError
`${t}`; // '2022-07-31T04:48:56.113918308Z'
"".concat(t); // '2022-07-31T04:48:56.113918308Z'

```
## Addition assignment (+=)

The addition assignment (+=) operator performs addition (which is either numeric addition or string concatenation) on the two operands and assigns the result to the left operand.

```JS

let a = 2;
let b = 'hello';

console.log((a += 3)); // Addition
// Expected output: 5

console.log((b += ' world')); // Concatenation
// Expected output: "hello world"

```

### Description


x += y is equivalent to x = x + y.

## Assignment (=)

The assignment (=) operator is used to assign a value to a variable or property. The assignment expression itself has a value, which is the assigned value. This allows multiple assignments to be chained in order to assign a single value to multiple variables.

```JS

let x = 2;
const y = 3;

console.log(x);
// Expected output: 2

console.log((x = y + 1)); // 3 + 1
// Expected output: 4

console.log((x = x * y)); // 4 * 3
// Expected output: 12

```

### Description

The assignment operator is completely different from the equals (=) sign used as syntactic separators in other locations, which include:

Initializers of var, let, and const declarations
Default values of destructuring
Default parameters
Initializers of class fields
All these places accept an assignment expression on the right-hand side of the =, so if you have multiple equals signs chained together:

```JS

const x = y = 5;

```

## Division (/)

The division (/) operator produces the quotient of its operands where the left operand is the dividend and the right operand is the divisor.

```JS 

console.log(12 / 2);
// Expected output: 6

console.log(3 / 2);
// Expected output: 1.5

console.log(6 / '3');
// Expected output: 2

console.log(2 / 0);
// Expected output: Infinity

```

### Description

The / operator is overloaded for two types of operands: number and BigInt. It first coerces both operands to numeric values and tests the types of them. It performs BigInt division if both operands become BigInts; otherwise, it performs number division. A TypeError is thrown if one operand becomes a BigInt but the other becomes a number.

##### Syntax 

``` JS

x / y

```

## Division assignment (/=)
The division assignment (/=) operator performs division on the two operands and assigns the result to the left operand.

``` JS

let a = 3;

a /= 2;
console.log(a);
// Expected output: 1.5

a /= 0;
console.log(a);
// Expected output: Infinity

a /= 'hello';
console.log(a);
// Expected output: NaN

```

### Description

x /= y is equivalent to x = x / y.

##### Syntax 

``` JS

x /= y

```

## Equality (==)

The equality (==) operator checks whether its two operands are equal, returning a Boolean result. Unlike the strict equality operator, it attempts to convert and compare operands that are of different types.


``` JS

console.log(1 == 1);
// Expected output: true

console.log('hello' == 'hello');
// Expected output: true

console.log('1' == 1);
// Expected output: true

console.log(0 == false);
// Expected output: true

```

## Multiplication (*)

The multiplication (*) operator produces the product of the operands.


``` JS

console.log(3 * 4);
// Expected output: 12

console.log(-3 * 4);
// Expected output: -12

console.log('3' * 2);
// Expected output: 6

console.log('foo' * 2);
// Expected output: NaN

```

## Remainder (%)
The remainder (%) operator returns the remainder left over when one operand is divided by a second operand. It always takes the sign of the dividend.

``` JS

console.log(13 % 5);
// Expected output: 3

console.log(-13 % 5);
// Expected output: -3

console.log(4 % 2);
// Expected output: 0

console.log(-4 % 2);
// Expected output: -0

```

## Remainder assignment (%=)

The remainder assignment (%=) operator performs remainder on the two operands and assigns the result to the left operand.

``` JS

let a = 3;

console.log((a %= 2));
// Expected output: 1

console.log((a %= 0));
// Expected output: NaN

console.log((a %= 'hello'));
// Expected output: NaN

```