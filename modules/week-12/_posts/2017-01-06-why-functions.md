---
title: Why Functions
module: 12
jotted: false
---

# Why Use Functions

To answer this question, one must look at the entire life cycle of software.  Once software written, it goes into what is called **maintenance** mode.  This means bugs are fixed, changes made, and upgrades are applied.

This accounts for over 75% of the entire life of the product!  That's a really long time.

As such, we want to minimize the amount of work that must be performed to maintain something that is "complete".  Functions help with that.

Functions:

1. Can be used over and over
2. Reduces duplicate code
3. Reduces bugs that can arise

The main goal is to reduce your overall work. Functions can help with that.

Example without a function:

```js

    // create sum and two numbers
    var sum;
    var number1;
    var number2;

    // create another sum and two more numbers
    var sum2;
    var number3;
    var number4;

    // calculate the first sum
    number1 = 4;
    number2 = 5;    
    sum = number1 + number2;

    // calculate the second sum
    number3 = 3;
    number4 = 2;
    sum2 = number3 + number4;

```

Example with a function:

```js

    // create sum and two numbers
    var sum;
    var number1;
    var number2;

    // calculate the first sum
    number1 = 4;
    number2 = 5;    
    calculateSum(number1, number2);

    // calculate the second sum
    number3 = 3;
    number4 = 2;
    calculateSum(number3, number4);
    
    function calculateSum(number1, number2)
    {
        sum = number1 + number2;
    }

```

Doesn't seem super impressive right?  What if we did it like this though?

```js

    // create sum and two numbers
    var sum;
    var number1;
    var number2;

    // calculate the first sum
    number1 = 4;
    number2 = 5;    
    calculateSum(number1, number2); // call calculateSum

    // calculate the second sum
    number1 = 3; // overwrite the number1 variable with a new value
    number2 = 2; // overwrite the number2 variable with a new value
    calculateSum(number1, number1); // call calculateSum
    
    // define the calculateSum function
    function calculateSum(number1, number2)
    {
        number1 = number1 + number2;
        number2 = number1 + number2;
        sum = number1 + number2;
    }

```

Now, the call the calculateSum function performs more actions which we no longer have to duplicate which makes things simpler. Additionally, the call to calculateSum doesn't change.

**Note** Keep in mind this is for example purposes, functions should perform only one action.  This is just a simple, yet verbose example.


