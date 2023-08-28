# Conditionals

Introduction to the JavaScript if statement
The if statement executes block if a condition is true. The following shows the syntax of the if statement:

```JS 

if( condition )
   statement;

```

The condition can be a value or an expression. Typically, the condition evaluates to a Boolean value, which is true or false.

If the condition evaluates to true, the if statement executes the statement. Otherwise, the if statement passes the control to the next statement after it.

The following flowchart illustrates how the if statement works:

If the condition evaluates to a non-Boolean value, JavaScript implicitly converts its result to a Boolean value by calling the Boolean() function.

If you have more than one statement to execute, you need to use wrap them in a block using a pair of curly braces as follows:


```JS 

if (condition) {
  // statements to execute
}

```

However, it’s a good practice to always use curly braces with the if statement. By doing this, you make your code easier to maintain and avoid possible mistakes.

```JS 

let age = 18;
if (age >= 18) {
  console.log('You can sign up');
}

```

Output:

```JS 

You can sign up

```

How it works.

First, declare and initialize the variable age to 18:

```JS

let age = 18;

```

Second, check if the age is greater or equal to 18 using the if statement. Because the expression age >= 18 is true, the code inside the if statement executes that outputs a message to the console

```JS

if (age >= 18) {
  console.log('You can sign up');
}

```

The following example also uses the if statement. However, the age is 16 which causes the condition to evaluate to false. Therefore, you won’t see any message in the output:

```JS

let age = 16;
if (age >= 18) {
  console.log('You can sign up');
}

```

## Nested if statement

It’s possible to use an if statement inside another if statement. For example:

```JS

let age = 16;
let state = 'CA';

if (state == 'CA') {
  if (age >= 16) {
    console.log('You can drive.');
  }
}

```

Output:

```JS

You can drive.

```

How it works.

First, declare and initialize the age and state variables:

```JS

let age = 16;
let state = 'CA';

```

Second, check if the state is 'CA' using an if statement. If yes, check if the age is greater than 16 using a nested if statement and output a message to the console:

```JS

if (state == 'CA') {
  if (age == 16) {
    console.log('You can drive.');
  }
}

```
In practice, you should avoid using nested if statements as much as possible. For example, you can use the && operator to combine the conditions and use an if statements as follows:


```JS

let age = 16;
let state = 'CA';

if (state == 'CA' && age == 16) {
  console.log('You can drive.');
}

```

## Summary

* Use the JavaScript if statement to execute a statement if a condition is true.
* Avoid using nested if statement as much as possible.

## Introduction to the JavaScript if…else statement

The if statement executes a block if a condition is true. When the condition is false, it does nothing. But if you want to execute a statement if the condition is false, you can use an if...else statement.

The following shows the syntax of the if...else statement:

```JS

if (condition1) {
  // ...
} else if (condition2) {
  // ...
} else if (condition3) {
  //...
} else {
  //...
}

```

n this syntax, the if...else...if statement has three conditions. In theory, you can have as many conditions as you want to, where each else...if branch has a condition.

The if...else...if statement checks the conditions from top to bottom and executes the corresponding block if the condition is true.

The if...else...if statement stops evaluating the remaining conditions as soon as a condition is true. For example, if the condition2 is true, the if...else...if statement won’t evaluate the condition3.

If all the conditions are false, the if...else...if statement executes the block in the else branch.

et’s take some examples of using the if...else...if statement.

## A simple JavaScript if…else…if statement example

The following example uses the if...else...if statement to get the month name from a month number:

```JS

let month = 6;
let monthName;

if (month == 1) {
  monthName = 'Jan';
} else if (month == 2) {
  monthName = 'Feb';
} else if (month == 3) {
  monthName = 'Mar';
} else if (month == 4) {
  monthName = 'Apr';
} else if (month == 5) {
  monthName = 'May';
} else if (month == 6) {
  monthName = 'Jun';
} else if (month == 7) {
  monthName = 'Jul';
} else if (month == 8) {
  monthName = 'Aug';
} else if (month == 9) {
  monthName = 'Sep';
} else if (month == 10) {
  monthName = 'Oct';
} else if (month == 11) {
  monthName = 'Nov';
} else if (month == 12) {
  monthName = 'Dec';
} else {
  monthName = 'Invalid month';
}
console.log(monthName);

```

Output:

```JS

Jun

```

n this example, we compare the month with 12 numbers from 1 to 12 and assign the corresponding month name to the monthName variable.

Since the month is 6, the expression month==6 evaluates to true. Therefore, the if...else...if statement assigns the literal string 'Jun' to the monthName variable. Therefore, you see Jun in the console.

If you change the month to a number that is not between 1 and 12, you’ll see the Invalid Month in the console because the else clause will execute.

## Using JavaScript if…else…if statement to calculate the body mass index

The following example calculates a body mass index (BMI) of a person. It uses the if...else...if statement to determine the weight status based on the BMI:

```JS

let weight = 70; // kg
let height = 1.72; // meter

// calculate the body mass index (BMI)
let bmi = weight / (height * height);

let weightStatus;

if (bmi < 18.5) {
  weightStatus = 'Underweight';
} else if (bmi >= 18.5 && bmi <= 24.9) {
  weightStatus = 'Healthy Weight';
} else if (bmi >= 25 && bmi <= 29.9) {
  weightStatus = 'Overweight';
} else {
  weightStatus = 'Obesity';
}

console.log(weightStatus);

```

Output:

```JS

Healthy Weight

```

How it works.

First, declare two variables that hold the weight in kilogram and height in meter. In a realworld application, you’ll get these values from a web form.
Second, calculate the body mass index by dividing the weight by the square of the height.
Third, determine the weight status based on the BMI using the if...else..if statement.
Finally, output the weight status to the console.

## Summary

* Use the JavaScript if...else...if statement to check multiple conditions and execute the corresponding block if a condition is true.