#Block vs inline elements

As we mentioned before block element occupy entire horizontal space of its parent container and vertical space equal to height of its content. It creates a block which pushes other elements to new line.

On the other hand, inline elements occupy only space which is enough for its content. They don't break the flow of the content. Therefore two inline elements will usually be next to each other (if there is enough horizontal space for both of them of course).

You can change default behaviour of particular element by changing its `display` property (e.g. `display: inline`).

Some of possible values of display property are listed in table (you will learn more about some of them later in the course):
<br>

Display      |
-------------|
block        |
inline       |
inline-block |
inline-flex  |
grid         |
inline-grid  |

[More info](https://developer.mozilla.org/en-US/docs/Web/CSS/display)

- - - -

# Box model

Every HTML element has box around its content. Using CSS you can change default behaivour of that box and create more complex layouts.

Element box is contained of:

* **content box** - area where your content is displayed
* **padding box** - padding (white space) around the content
* **border box** - border around content and padding
* **margin box** - outermost layer (white space), wrapping around content, padding and border

On picture below you can see example of box model:

![Box model](https://media.geeksforgeeks.org/wp-content/uploads/box-model-1.png)

Tip: *To apply border to your element it is enough to add `border-width` style to element. You also need to apply `border-style` and `border-color`.*

[More info](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model)
- - - -

#div and span
Div and span are generic HTML containers which can have any content inside. Because of that they don't have semantic meaning and although they are widely used, they should be used as last resort. For example, if you plan only to have text inside one container, it is better to use <p\> than <div\>.   
There is one difference between div and span. Div is *block* element and span is *inline* element.

[More info](https://www.geeksforgeeks.org/difference-between-div-and-span-tag-in-html/)
- - - -

#Width and Height

Width and height are CSS properties which control width and heigh of some element.
They can be expressed in different units, e.g. px, em, %.
One thing you should be aware of is, width and height work only on block elements. Because inline elements take exclusively only as much space as their content requires if you apply width or height properties on inline elements, nothing will change.

[More info](https://www.w3schools.com/css/css_dimension.asp)
- - - -

#Box sizing - content boxes and border boxes
box-sizing is css property which changes how box model is calculated in relation to width and height.

content-box is default value of box-sizing. That means, with content box, margin, padding and border will be **added** to width and height of element.

border-box on the other hand will **substract** margin, padding, and border values from width and height.

Here's one practical example below.

A div like

```html
<div class="example"></div>
```

with the CSS

```css
.example {
    border: 5px solid;
    height: 100px;
    padding: 8px;
    width: 100px;
}
```

would be 126x126px in total. 

100px width + 5px border (left and right) + 8px padding (left and right).
100px height + 5px border (top and bottom) + 8px padding (top and bottom). The content area (inside the padding) where your text would go, is 100x100px.

100 + 5 + 5 + 8 + 8 = 126

Using

```css
.example {
    border: 5px solid;
    box-sizing: border-box;
    height: 100px;
    padding: 8px;
    width: 100px;
}
```

would make it 100x100px, since the padding/border are now taken into account when calculating the width. So, the content area would only be 74x74px. 100 - (the padding of 8px * 2) - (the border of 5px * 2).

100 - 8 - 8 - 5 - 5 = 74

[More info](https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing)
- - - -

#Universal selector
Universal selector is special type of selector in css. It is used by typing * and then css style, e.g.
<pre>
* {
    <em>my styles</em>
  }
</pre>

When you used universal selector it matches every HTML element, meaning that style will be apply to every element on page. Universal selector is good when you have some common styles which you want to apply to whole web page, and then change individual elements's styles (e.g. font-family).

[More info](https://developer.mozilla.org/en-US/docs/Web/CSS/Universal_selectors)
- - - -

#class selector
Class selector matches elements based on their *class* attribute. You can use class selector by first adding some class on element, and then using that class in stylesheet. You can use class selector in stylesheet with dot(.) character. 
Tip: *One thing you should be aware of is, you are allowed to use same class on multiple elements, as opposed to* **id** *which you can use only on single element*. For example:

```html
<p class="my-class"></p>
```
```css
.my-class {
}
```
[More info](https://developer.mozilla.org/en-US/docs/Web/CSS/Class_selectors)
- - - -
#Id selectors
Id selector matches single element based on its *id* attribute. You can use id similar as you use class selector, but in css stylesheet instead of using dot character, you need to use # character.
Tip: *You can use one id on single element*. For example:
```html
<p id="my-id"></p>
```
```css
#my-id {
}
```

[More info](https://developer.mozilla.org/en-US/docs/Web/CSS/ID_selectors)
