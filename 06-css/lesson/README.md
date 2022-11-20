# CSS - The Cascade, Specificity, and Inheritance

A good blog on the topic can be found on the following [link](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance#understanding_the_cascade).

## Conflicting rules

CSS stands for Cascading Style Sheets, and that first word **cascading is incredibly important to understand** — the way that the cascade behaves is key to understanding CSS.

At some point, you will be working on a project and you will find that the CSS you thought should be applied to an element is not working. Often, the problem is that you create two rules that apply different values of the same property to the same element. Cascade and the closely-related concept of specificity are mechanisms that control which rule applies when there is such a conflict. The rule that's styling your element may not be the one you expect, so you need to understand how these mechanisms work.

Also significant here is the concept of inheritance, which means that some CSS properties by default inherit values set on the current element's parent element and some don't. This can also cause some behavior that you might not expect.

## Cascade

When two rules apply to the same element, the one that is defined last in the stylesheet is the one that will be used.

### Example 1 

In the following example we have two rules that select the `h1` tag. Which one will be applied?



## Specificity

Specificity is the algorithm that the browser uses to decide which property value is applied to an element. If multiple selectors apply to the same property, the more specific selector will win and its rule will determine the styling of the element

### Example 2

Below, we have two rules that could apply to the <h2> element. The <h2> content below ends up being colored red because the class selector `main-heading` gives its rule a higher specificity. So even though the rule with the <h2> element selector appears further down in the source order, the one with the higher specificity, defined using the class selector, will be applied.

As we can see, a class selector has more weight than an element selector, so the properties defined in the class style block will override those applied to the element style block.

Something to note here is that although we are thinking about selectors and the rules that are applied to the text or component they select, it isn't the entire rule that is overwritten, only the properties that are declared in multiple places.

This behavior helps avoid repetition in your CSS. A common practice is to define generic styles for the basic elements, and then create classes for those that are different.

### Example 3

In this example,  we have defined generic styles for level 2 headings, and then created some classes that change only some of the properties and values. The values defined initially are applied to all headings, then the more specific values are applied to the headings with the classes.

Let's now have a look at how the browser will calculate specificity. We already know that an element selector has low specificity and can be overwritten by a class. Essentially a value in points is awarded to different types of selectors, and adding these up gives you the weight of that particular selector, which can then be assessed against other potential matches.

The amount of specificity a selector has is measured using three different values (or components), which can be thought of as ID, CLASS, and ELEMENT columns in the hundreds, tens, and ones place:

- Identifiers: Score one in this column for each ID selector contained inside the overall selector.
- Classes: Score one in this column for each class selector, attribute selector, or pseudo-class contained inside the overall selector.
- Elements: Score one in this column for each element selector or pseudo-element contained inside the overall selector.

[Let's see some more examples on how to calculate specificity](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance#specificity_2)

A cool game to practice specificity: https://codepen.io/pehaa/pen/dEpvXN

### Inline styles

Inline styles, that is, the style declaration inside a style attribute, take precedence over all normal styles, no matter the specificity. Such declarations don't have selectors, but their specificity can be construed as 1-0-0-0; always more than any other specificity weight no matter how many IDs are in the selectors.

### !important

There is a special piece of CSS that you can use to overrule all of the above calculations, even inline styles - the !important flag. However, you should be very careful while using it. This flag is used to make an individual property and value pair the most specific rule, thereby overriding the normal rules of the cascade, including normal inline styles.

## Inheritance

Some CSS property values set on parent elements are inherited by their child elements, and some aren't.

### Example 3

For example, if you set a color and font-family on an element, every element inside it will also be styled with that color and font, unless you've applied different color and font values directly to them.

Some properties do not inherit — for example, if you set a width of 50% on an element, all of its descendants do not get a width of 50% of their parent's width. If this was the case, CSS would be very frustrating to use!