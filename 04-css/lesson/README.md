# CSS

## HTML Recap

We use HTML to give **content** to our site. Content of a site is everything we can see in the website: text, buttons, forms, tables, links, lists, multimedia, ...

Each of these things can be added to our website, we just need to know what **HTML tag** represents which thing.

By now, we have learned about many different tags:
- Text: h1, … h6, p, b, em
- anchor
- lists: ol, ul
- multimedia: img, iframe, …
- buttons, canvases, tables, …

To create a website, we also need the **basic HTML skeleton**. Every HTML website consists of 2 main parts:
- head - metadata about our site
- body - the content of our site

When we create a website by adding many different elements, they become nested inside other elements. We can think of the HTML document as a tree that shows the hierarchical relationship between the content inside the file. The HTML DOM is what we cal that tree and it is the logical representation of our website inside the computer's memory.

[Exercise #1: Let's create a small website](../exercise/exercise-01.md)

## What is CSS?

CSS (**C**ascading **S**tyle**s**heets) is the language we use to give our website **style**.

We can:
    - define colors
    - position elements inside the screen
    - set fonts, font sizes
    - animate transitions
    - ... and much more

We define styles by writing **CSS rules**

Multiple rules are gathered together in **stylesheets**

Stylesheets reside inside plaintext files and have a .css extension

## CSS rule

Let's create our first CSS rule that will make all text in our website red!

First, we need a CSS file so let's create it. Inside the same folder from exercise #1, create a new file named `style.css`

Then, write the following text inside the CSS file:

``` css
body {
	color: red;
}
```

What does the above text mean? What do we see?
- non-alphabetic characters: "{","}",":",";"
- `body`: for which kind of element do we write the rule for (For the `body` tag). **They are important for structure**
- `color`: the **property** we wish to change (add styling to)
- `red`: the **value** of the property

The above rule means: "I wish that the body tag has the color property set to red".

More simply that means: "I wish that all text inside the body tag has the color red"

If we reload our website after saving the CSS file, what do we get?

## Linking a CSS File

If the HTML file wants to use some stylesheet, it has to declare that
We add a `link` tag to **link** a CSS file to our HTML file:

``` HTML
<link rel="stylesheet" href="./base.css">
```

Inside what tag?
- head
- body
- some other

Now, we are able to see how our rule applies to our website.

## CSS Comments

We “can comment out” part of our CSS and make it not affect our page without deleting it.

This is also useful when using English to describe what a CSS rule does.

``` css
/*
Styling for the body element
This is also part of the comment
*/
body {
	/*background-color: red;*/
	color: #414141;    /* Dark gray */
}

```

## Multiple Properties Inside a Single Rule

Inside a single rule, we can add multiple CSS properties and specify their values

``` css
/*Styling for the body element*/
body {
	/*background-color: red;*/
	font-size: 20px;
	text-align: center;
}

```

## Selectors

What if we wanted to give a specific styling to all our headings (h1-h6)?

``` css
font-family: "Helvetica", "Arial", sans-serif;
```

What if we wanted to give specific styling to all HTML elements?

## Units of Measurement

There are a ton of units of measurement: https://developer.mozilla.org/en-US/docs/Web/CSS/length
The most common ones are:
- px: pixel
- em: relative to the current font size of the element in question
  - If the font size is 10px, then 2em is equal to 20px (2 times the font size)
- vh: Relative to 1% of the height of the viewport (the browser window size)

## Reusing the Same Stylesheet

We can link the same stylesheet to multiple HTML files

We can also include more than one stylesheet per HTML file


## Cascade?

We can define CSS in more places than the css file
- The browser has its default stylesheet
- User defined stylesheets
- External stylesheets 
  - CSS from CSS files
- Page-specific styles 
  - CSS inside the style tags inside HTML
- Inline styles 
  - CSS assigned to a specific element
  - Try to avoid that

[Exercise #2: Let's give our website more styling](../exercise/exercise-02.md)

## References

- https://www.internetingishard.com/html-and-css/hello-css
- https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics
- https://www.youtube.com/watch?v=1PnVor36_40

