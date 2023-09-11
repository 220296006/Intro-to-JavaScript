# The OnSubmit Event

In JavaScript:

object.onsubmit = function(){
       myScript};
This example uses the HTML DOM to assign an "onsubmit" event to a form element.

When you submit the form, a function is triggered which alerts some text.

```html

<!DOCTYPE html>
<html>
<body>
<form id="myForm" action="/action_page.php">
  Enter name: <input type="text" name="fname">
  <input type="submit" value="Submit">
</form>//from  ww w. j  a  v  a 2s  .c  om

<p id="demo"></p>
<script>
document.getElementById("myForm").onsubmit = function() {myFunction()};

function myFunction() {
  document.getElementById("demo").innerHTML = "The form was submitted";
}
</script>

</body>
</html>

```