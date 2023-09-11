# JavaScript Events

## Handling Events

JavaScript's interaction with HTML is handled through events that occur when the user or the browser manipulates a page. When the page loads, it is called an event. When the user clicks a button, that clicks to is called an event. 

Other examples include events like pressing any key, closing a window, resizing a window, etc. Developers can use these events to execute JavaScript coded responses, which cause buttons to close windows, messages to be displayed to users, data to be validated, and virtually any other type of response imaginable. Events are a part of the Document Object Model (DOM) Level 3 and every HTML element contains a set of events which can trigger JavaScript Code.

## Strings Operations

### Section 1

Searching

search() – locate a substring in a string using a regular expression.


```JS

let re = /[A-Z]/;
let str = 'hi There! How are you?';
let index = str.search(re);

console.log(index);

```

Output:

```JS

3

```

indexOf() – get the index of the first occurrence of a substring in a string.

```JS

let str = 'finding substring in string';
let index = str.indexOf('str');

console.log(index); // 11

```

lastIndexOf() – find the index of the last occurrence of a substring in a string.


```JS
let str = 'JavaScript';
let index = str.lastIndexOf('a');

console.log(index);

```

includes() – check if a string contains a substring.

```JS
let email = 'admin@example.com';
console.log(email.includes('@'));

```

startsWith() – check if a string starts with another string.

```JS

String.startsWith(searchString [,position])

```

endsWith() – determine if a string ends with another string.

```JS
const title = 'Jack and Jill Went Up the Hill';

console.log(title.endsWith('Hill'));

```

### Section 2

 Trimming

- trim() – remove whitespace characters from a string.

```JS
let str = '  JS trim  ';
let result = str.trim();

console.log(result);

Output: "JS trim"
```

- trimStart() – remove the leading whitespace characters of a string.

```JS
const str = '   JavaScript   ';
const result = str.trimStart();

console.log({ str });
console.log({ result });

Output: 

{ str: '   JavaScript   ' }
{ result: 'JavaScript   ' }

```

- trimEnd() – remove the ending whitespace characters of a string.

```JS
const str = '   JavaScript   ';
const result = str.trimEnd();

console.log({ str });
console.log({ result });

Output:

{ str: '   JavaScript   ' }
{ result: '   JavaScript' }

```

### Section 3

Padding

padStart() & padEnd() – pad a string with another string until the result string reaches the given length.

```JS
String.prototype.padStart(padLength [,padString]);

String.prototype.padEnd(padLength [,padString]);

```

### Section 4

Extracting

- split() – split a string into an array of substrings.

```JS
let str = 'JavaScript String split()';
let substrings = str.split(' ');

console.log(substrings);

Output:
["JavaScript", "String", "split()"]

```

- substring() – extract a substring from a string.

```JS
let str = 'JavaScript Substring';
let substring = str.substring(0,10);

console.log(substring);

Output:

JavaScript
```


- slice() – extract a part of a string.

```JS
const str = 'Hello';
const substr = str.slice(3);

console.log({ substr });

Output:

{ substr: 'lo' }
```

### Section 5

Concatenating & interpolating

- concat() – concatenate multiple strings into a new string.

```JS

```

-Template literals – learn how to substitute variables in a string.

```JS
let greeting = 'Hi';
let message = greeting.concat(' ', 'John');

console.log(message);

Output:

Hi John
```

### Section 6

Replacing

- replace() – replace a substring in a string with a new one.

```JS
let str = 'JS will, JS will rock you!';
let newStr = str.replace('JS','JavaScript');

console.log(newStr);

Output:

JavaScript will, JS will rock you!
```

- replaceAll() – replace all occurrences of a substring that matches a pattern with a new one.

```JS
let str = 'JS will, JS will, JS will rock you.';
let newStr = str.replaceAll('JS','JavaScript');

console.log(newStr);

Output:

JavaScript will, JavaScript will, JavaScript will rock you. 
```

### Section 7

Changing cases

- toUpperCase – return a string with all characters converted to uppercase.

```JS
const message = 'Hello';
const newMessage = message.toUpperCase();

console.log(newMessage);

Output:

HELLO
```

- toLowerCase – return a string with all characters converted to lowercase.

```JS
const message = 'Hi';
const newMessage = message.toLowerCase();

console.log(newMessage);

Output:

hi
```



