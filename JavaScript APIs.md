# JavaScript APIs

## HTML DOM Document getElementById()

The getElementById() method returns an element with a specified value.

The getElementById() method returns null if the element does not exist.

The getElementById() method is one of the most common methods in the HTML DOM. It is used almost every time you want to read or edit an HTML element.

```JS

document.getElementById("demo");


```

### Get the element and change its color

```JS

const myElement = document.getElementById("demo");
myElement.style.color = "red";

```

## HTML DOM Document getElementsByTagName()

The getElementsByTagName() method returns a collection of all elements with a specified tag name.

The getElementsByTagName() method returns an HTMLCollection.

The getElementsByTagName() property is read-only.

```JS

const collection = document.getElementsByTagName("li");

const collection = document.getElementsByTagName("*");

document.getElementsByTagName("p")[0].innerHTML = "Hello World!";

```

## HTML DOM Document createElement()

The createElement() method creates an element node.

```JS

const para = document.createElement("p");
para.innerText = "This is a paragraph";
document.body.appendChild(para);

```'

## HTML DOM Element appendChild()

The appendChild() method appends a node (element) as the last child of an element.

```JS
const node = document.createElement("li");
const textnode = document.createTextNode("Water");
node.appendChild(textnode);
document.getElementById("myList").appendChild(node);

```

## HTML DOM Element innerHTML

The innerHTML property sets or returns the HTML content (inner HTML) of an element.


```JS

let html = document.getElementById("myP").innerHTML;

document.getElementById("myBtn").style.left = "100px";

```

## Style left Property

The left property sets or returns the left position of a positioned element.

This property specifies the left position of the element including padding, scrollbar, border and margin.

Tip: A positioned element is an element with the position property set to: relative, absolute, or fixed.

Tip: To set or return the right position of a positioned element, use the right property.

```JS

document.getElementById("myBtn").style.left = "100px";

let text = element.getAttribute("class");


```

## HTML DOM Element getAttribute()

The getAttribute() method returns the value of an element's attribute.

```JS

let text = element.getAttribute("class");

```

## HTML DOM Element addEventListener()

The addEventListener() method attaches an event handler to an element.

```JS

element.addEventListener("click", myFunction);

function myFunction() {
  document.getElementById("demo").innerHTML = "Hello World";
}

```

## JavaScript Window - The Browser Object Model

### The Browser Object Model (BOM)

There are no official standards for the Browser Object Model (BOM).

Since modern browsers have implemented (almost) the same methods and properties for JavaScript interactivity, it is often referred to, as methods and properties of the BOM.

### The Window Object

The window object is supported by all browsers. It represents the browser's window.

All global JavaScript objects, functions, and variables automatically become members of the window object.

Global variables are properties of the window object.

Global functions are methods of the window object.

Even the document object (of the HTML DOM) is a property of the window object:


```JS

element.addEventListener("click", myFunction);

function myFunction() {
  document.getElementById("demo").innerHTML = "Hello World";
}

```