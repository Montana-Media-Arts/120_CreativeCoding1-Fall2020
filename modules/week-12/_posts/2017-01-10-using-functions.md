---
title: Using Functions
module: 12
jotted: true
---

# Using Functions

<div class="tab">
    <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
    <button class="tablinks" onclick="openTab(event, 'Circle')">circle</button>
    <button class="tablinks" onclick="openTab(event, 'MyCircle')">myCircle Example</button>
</div>
<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<div class="tabhtml" markdown="1">

With **setup** and **draw**, we use them, but we never had to call them. However, luckily, we have used some functions already. Do you remember which ones?

I am going to list some, and hopefully, they will sound familiar.

* Math.floor()
* Math.random()
* isKeyDown()
* circle()
* square()
* point()
* line()
* rect()
* ellipse()

Can you believe all the functions you have used already? (see the previous section as to why)  

There are a couple of things to notice. When we **define** functions, it starts with keyword **function**, and the body is in between the curly braces.

However, when you use functions, you call the **function name**, and then the name is followed by **parentheses**.

Except for Math.random(), all the other functions required numbers between the parenthesis.  For example, the circle function requires an x, y, and a diameter.  These are called **parameters**.  When you call the function, then you pass **arguments** into the functions.

</div>
</div>
<div id="Circle" class="tabcontent">

<div class="tabhtml" markdown="1">

So, to recap, the function calculateSum might look something like this.

```js
      // define the calculateSum function
    function calculateSum(number1, number2)
    {
        number1 = number1 + number2;
        number2 = number1 + number2;
        sum = number1 + number2;
    }
```

So, let's start like this. What if we wanted to create a concentric circle?

```js
    function setup()
    {
        createCanvas(500,500);
    }
    function draw()
    {
        fill(50,120,120);
        circle(110,120,100);
        fill(120,50,120);
        circle(110,120,50);
    }
```

To make this work, it requires, two calls to the fill function and two to the circle function.  How would one create a function to create a concentric circle?

</div>
</div>
<div id="MyCircle" class="tabcontent">

<div class="tabhtml" markdown="1">

We can **define** a concentric circle function like this.

```js

function ConcentricCircle(x,y, outer_radius, inner_radius outer_red, outer_green,outer_blue, inner_red, inner_green, inner_blue)
{
        fill(outer_red,outer_green, outer_blue);
        circle(x,y,outer_radius);
        fill(inner_red, inner_green, inner_blue);
        circle(x,y,inner_radius);
}

```
I can then **call** the `ConcentricCircle` function in the draw function like this.

```js
    function setup()
    {
        createCanvas(500,500);
    }
    function draw()
    {
        ConcentricCircle(110, 120, 100, 50, 50, 120, 120, 120, 50, 120);
    }
```

I called the **ConcentricCircle** function in the draw function.  Did it work?  Good!  Now I can create a multiple concentric circles in the draw function by calling ConcentricCircle many times.  However, if I call it again, it will generate another concentric circle in the same place.

```js
    function setup()
    {
        createCanvas(500,500);
    }
    function draw()
    {
        // creates two Concentric Cirles in the same place
        ConcentricCircle(110, 120, 100, 50, 50, 120, 120, 120, 50, 120);
        ConcentricCircle(110, 120, 100, 50, 50, 120, 120, 120, 50, 120);
    }
```

So, what we need to do is create a concentric circle using a different x and y.

```js
    function setup()
    {
        createCanvas(500,500);
    }
    function draw()
    {
        // concentric circle where x = 110 and y = 120
        ConcentricCircle(110, 120, 100, 50, 50, 120, 120, 120, 50, 120);
        // concentric circle where x = 210 and y = 220
        ConcentricCircle(210, 220, 100, 50, 50, 120, 120, 120, 50, 120);
    }
```

What if I wanted to create random circles in random locations? Can you do that?

**Hint** use Math.random() to get move the location of the circles.

</div>
</div>