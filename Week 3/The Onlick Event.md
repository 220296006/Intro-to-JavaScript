# JavaScript onclick event

The onclick event generally occurs when the user clicks on an element. It allows the programmer to execute a JavaScript's function when an element gets clicked. This event can be used for validating a form, warning messages and many more.

In HTML, we can use the onclick attribute and assign a JavaScript function to it. We can also use the JavaScript's addEventListener() method and pass a click event to it for greater flexibility.

Syntax
Now, we see the syntax of using the onclick event in HTML and in javascript (without addEventListener() method or by using the addEventListener() method).


In HTML

```HTML
<element onclick = "fun()">  
In JavaScript
object.onclick = function() { myScript };  
In JavaScript by using the addEventListener() method
object.addEventListener("click", myScript);  
Let's see how to use onclick event by using some illustrations. Now, we will see the examples of using the onclick event in HTML, and in JavaScript.

Example1 - Using onclick attribute in HTML
In this example, we are using the HTML onclick attribute and assigning a JavaScript's function to it. When the user clicks the given button, the corresponding function will get executed, and an alert dialog box will be displayed on the screen.

<!DOCTYPE html>  
<html>  
<head>  
<script>  
function fun() {  
alert("Welcome to the javaTpoint.com");  
}  
</script>  
</head>  
<body>  
<h3> This is an example of using onclick attribute in HTML. </h3>  
<p> Click the following button to see the effect. </p>  
<button onclick = "fun()">Click me</button>  
</body>  
</html>  

```