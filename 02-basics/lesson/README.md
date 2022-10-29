# HTML #1 - basics<br>
## HTML boilerplate

Every html page have (at minimum) these 3 elements.
<br>

* **html**
* **head**
* **body**
<br>

Html tag is tag which contains all other web page content.

Head tag is tag which contains page title and other metadata. They are not rendered on web page (outside title being visible on browser tab), but instead they are visible when viewing page source and they are interpreted by browser in order to set some configuration or fetch some other assets.

Body tag is tag which contains content that will be rendered in viewing window of browser.
<br>

Read more:
<br>
[<html\>](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/html)
<br>
[<head\>](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/head)
<br>
[<body\>](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/body)
- - - -
## Title
Title is tag which contains title of that particular web page. Title is visible on browsers tab. [More info](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/title)
- - - -

## Paragraph
Paragraphs (<p\>) are elements which generally contains blocks of text. They can contain other content or media. They can also contain elements for applying particular style to text (like bold or italic). [More info](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/p)
- - - -

## Headings
Headings represent different level of section headings starting from <h1\> up to <h6\>. H1 is first and therefore biggest font size, and H6 is smallest. Headings can contain other elements. [More info](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading_Elements)
- - - -

## Lists
Lists are element which contain items that should be displayed in order. There are ordered lists (<ol\>) and unordered lists (<ul\>). Difference between them is that ordered list have incremental numbers next to items (starting from 1), and unordered lists have bullets next to the item. They only differ visually. Both unordered and ordered lists can contain list items (<li\>), but list items can contain other elements.<br>

Read more:

[Unordered list](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul)<br>
[Ordered list](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ol)<br>
[List item](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/li)
- - - -
## <em\> vs <i\> & <strong\> vs <b\>
For applying bold and italic styles to text we have at our disposal two sets of tags.   
em and i make text italic while strong and b make text bold. Visually em and i are the same. So are strong and b. Difference is only that they have different semantics. Each one has purpose for specific case. They shouldn't contain other tags or content beside text.

Read more:

[em](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/em)<br>
[i](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/i)<br>
[strong](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/strong)<br>
[b](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/bold)
- - - -
## Empty elements (br, hr)
br (<br\> or <br/\>) is tag which makes visual line break in content. This tag is empty tag, meaning it shouldn't contain any other tags or content.

hr (<hr\> or <hr/\>) is tag which creates horizontal line in your content. It can be used as a section separator. This tag is also empty and shouldn't contain any other content.

Empty tags can be written like this also (<br\><br/\> and <hr\><hr/\>). They can be written with opening and closing, but considering they shouldn't have any content standard practice is just to write one pair of tag, either opening or closing.
<br>

Read more:

[br](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/br)<br>
[hr](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/hr)
- - - -

## Comments
Comments are special elements which can contain anything between opening (<!--) and closing (--\>) tags. They can contain anything because any content inside comment is not rendered or impacts page behaviour in any way. Actually, only way you will see comment in web page is if you open page source (or if you open page in editor like Visual studio code). [More info](https://www.w3schools.com/tags/tag_comment.asp)
- - - -
## Span
Span is generic type of container which can have any type of content inside its tags. Considering span doesn't have any semantic meaning and doesn't inherently represent anything, you should use it as last resort. [More info](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/span)
- - - -
## Anchor
Anchor (<a\>) creates a hyperlink to other web pages, emails, phone numbers, files, and even to different location on the same page. Between anchor tags you can put any type of content. To create a hyperlink, you need to open a tag and put attribute (*href*) with link to other resource. They between opening in closing tags you put content which will be displayed on web page and act as a hyperlink. Example:<br>
<a href="www.google.com"\>I am opening google</a\>
[More info](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a)
- - - -
## Inline vs block
Inline elements are those which take only as much space as needed to display content. Opposed to that block elements are elements which take whole width of the page and break the flow of the content despite the space its content actually take.
Some of the block and inline elements we talked about on this lessons are in table below:<br>

Block      | Inline
---------- | -------------
paragraph  | em
headings   | i
lists      | b
           | strong
           | span
           | anchor


<br>Read more:
<br>[Inline elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements)
<br>[Block elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements)
- - - -
<br>
[Homework](/02-basics/homework/README.md)
