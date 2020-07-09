---
title: Accessing HTML Tags
module: 8
jotted: true
---

# Accessing HTML Tags

<div class="embed-responsive embed-responsive-16by9"><iframe class="embed-responsive-item" src="https://www.youtube.com/embed/1aQplfKL2eI" frameborder="0" allowfullscreen></iframe></div>

One of the most useful things that JavaScript can do is access HTML tags and change their content. Look at the example below.

### getElementById

```js
 document.getElementById("myTag").innerHTML = "New Text";
```
If you were to have an HTML page like the following, the JavaScript above would change the tag with the id "myTag".

```html
 <html>
    <body>
        <span id="myTag">This is my favorite text</span>
    </body>
 </html>
```
### document.write

Another way to access HTML is by using the document.write function.  It looks something like this.

```js
 document.write("I am being written to the HTML page");
```

But what if there is an error? For example, what if we misspell something or put the script tag in the wrong place?

Initially, we put the script tag in the head tag.

### debugging

However, when the browser renders the HTML, it is read from top to bottom. So, if the JavaScript is at the top and you try to access an HTML element in the body, it won't be found.  Or, if you misspell a function name, an error will occur as well.  However, web pages won't show you the error. Browsers do their best to show what they can.  

For example, if you were doing the following.

```html
 <html>
    <head>
        <script>
            document.getElementById("myTag").innerHTML = "New Text";
        </script>
    </head>
    <body>
        <span id="myTag">This is my favorite text</span>
    </body>


 </html>
```

The previous code will cause an error. We can fix this error by doing the following.


```html
 <html>
    <body>
        <span id="myTag">This is my favorite text</span>
    </body>

    <script>
        document.getElementById("myTag").innerHTML = "New Text";
    </script>
 </html>
```

However, if we mistype something like this:

```html
 <html>
    <body>
        <span id="myTag">This is my favorite text</span>
    </body>

    <script>
        dcument.getElementById("myTag").innerHTML = "New Text";
    </script>
 </html>
```
We will also get an error.

How do we fix it?

It's in the browser settings. To access those in Chrome, follow these steps.

1. Click on the three vertical dots in the upper right-hand corner of the web browser.
2. Navigate to **More Tools**->**Developer Tools**
3. Click on the console tab. The area shows you the error and where it is in your code. Nice!

### console.log

We can also use another command to write to the console. It's called console.log.

Try this now.

```html
 <html>
    <body>
        <span id="myTag">This is my favorite text</span>
    </body>

    <script>
        console.log("I am in the console!");
    </script>
 </html>
```

Open your web page. It won't show anything on the page. However, if you go to the console in the Developer Tools again, you will see the console.log message. Console.log is an excellent way to find out what is happening in your JavaScript code.

Next, let's talk about variables in JavaScript.

<!-- video -->
<a href="https://umontana.zoom.us/recording/share/nLX4YN7iloCtutSQ-s9sNWpHoEogIDNuBiMzFjWX5r6wIumekTziMw" target="_new" style="font-family:Ariel; font-size:32px;">Click here for this section's Video</a>