---
title: What are Functions
module: 12
jotted: false
---

# What are Functions

Functions are pieces of code that perform actions.  What does that mean?  Well, let's think about the two main functions we already use.

```js
    function setup()
    {

    }

    function draw()
    {

    }
```
Both setup and draw are functions that perform actions.  

The **setup** function is called only one time, and it calls  **createCanvas**, which is also a function!  

The **draw** is also a function that is called continuously and allowing us to make things appear in the browser.

How do we know they are functions?

```js
    function setup()
    {

    }
```

Let's breakdown the **setup** function.  

1. It's easy to know what section is a function because it starts with the keyword **function**.  
2. Then it is followed by the name of the function, in this case, **setup**.
3. Then the function name is always followed by **()** parentheses.  These contain parameters if there are any.
4. Finally, the body of the function is surrounded by **{}** curly braces.

Let's break this down in a different way.
