# JavaScript Methods and “this” Keyword 


What is this?
In JavaScript, the this keyword refers to an object.

Which object depends on how this is being invoked (used or called).

The this keyword refers to different objects depending on how it is used:

```JS

const person = {
  firstName: "John",
  lastName : "Doe",
  id       : 5566,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};

```

- In an object method, this refers to the object.
- Alone, this refers to the global object.
- In a function, this refers to the global object.
- In a function, in strict mode, this is undefined.
- In an event, this refers to the element that received the event.
- Methods like call(), apply(), and bind() can refer this to any object.

$ NOTE

- this is not a variable. It is a keyword. You cannot change the value of this.

this in a Method
When used in an object method, this refers to the object.

In the example on top of this page, this refers to the person object.

Because the fullName method is a method of the person object.

## this in a Function (Default)

In a function, the global object is the default binding for this.

In a browser window the global object is [object Window]:

```JS

function myFunction() {
  return this;
}

```

this in a Function (Strict)
JavaScript strict mode does not allow default binding.

So, when used in a function, in strict mode, this is undefined.

```JS

"use strict";
function myFunction() {
  return this;
}

```

## this in Event Handlers

In HTML event handlers, this refers to the HTML element that received the event:

````JS

<button onclick="this.style.display='none'">
  Click to Remove Me!
</button>

```

