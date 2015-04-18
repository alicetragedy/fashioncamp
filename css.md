###CSSmerizing

CSS (short for Cascading Style Sheets) is a language used for describing the look and formatting of a document written in a markup language like HTML. In fact it is closely connected with HTML, since it gives style to HTML elements. In contrast to HTML, CSS has no hierarchy and can be written in the order that we choose.

CSS3 is the last released version of CSS, and it also improves CSS a lot. For example, it gives the possibility to animate an element.

The two languages — HTML, as discussed in yesterday's workshop, and CSS — are independent of one another. HTML will always represent content, and CSS will always represent the appearance of that content.

### Let's get started

In order to get our CSS talking to our HTML, we need to reference our CSS file within our HTML. The best practice for referencing our CSS is to include all of our styles in a single external style sheet, which is referenced from within the ```<head>``` element of our HTML document.

For our external CSS style sheet, create a new plain text file with a .css file extension. Our CSS file should be saved within the same folder, or a subfolder, where our HTML file is located.

Within the ```<head>``` element of the HTML document, the ```<link>``` element is used to define the relationship between the HTML file and the CSS file. Because we are linking to CSS, we use the ```rel``` attribute with a value of stylesheet to specify their relationship. Furthermore, the ```href``` (or hyperlink reference) attribute is used to identify the location, or path, of the CSS file.

Consider the following example of an HTML document ```<head>``` element that references a single external style sheet.

```
<head>
  <link rel="stylesheet" href="style.css">
</head>
```

With our style.css file starting to take shape, let’s connect it to our index.html file. Opening the index.html file in our text editor, let’s add the ```<link>``` element within our ```<head>``` element, just after the ```<title>``` element. Because we’ll be referencing a style sheet within the ```<link>``` element, let’s add the relation attribute, ```rel```, with a value of stylesheet.

We also want to include a hyperlink reference, using the ```href attribute```, to our main.css file. Remember, our style.css file is saved within the “stylesheets” folder, which is inside the “assets” folder. Therefore, the href attribute value, which is the path to our style.css file, needs to be assets/stylesheets/style.css.

### Understanding Common CSS Terms

In addition to HTML terms, there are a few common CSS terms you will want to familiarize yourself with. These terms include selectors, properties, and values. As with the HTML terminology, the more you work with CSS, the more these terms will become second nature.

#### Selectors

As elements are added to a web page, they may be styled using CSS. A selector designates exactly which element or elements within our HTML to target and apply styles (such as color, size, and position) to. Selectors may include a combination of different qualifiers to select unique elements, all depending on how specific we wish to be. For example, we may want to select every paragraph on a page, or we may want to select only one specific paragraph on a page.

Selectors generally target an attribute value, such as an ```id``` or ```class``` value, or target the type of element, such as ```<h1>``` or ```<p>```.

Within CSS, selectors are followed with curly brackets, {}, which encompass the styles to be applied to the selected element. The selector here is targeting all ```<p>``` elements.

```
p {
color: blue;
}
```

#### Properties

Once an element is selected, a property determines the styles that will be applied to that element. Property names fall after a selector, within the curly brackets, ```{}```, and immediately preceding a colon, ```:```. There are numerous properties we can use, such as background, color, font-size, height, and width, and new properties are often added. In the following code, we are defining the color and font-size properties to be applied to all ```<p>``` elements.

```
p {
  color: ...;
  font-size: ...;
}
```

#### Values

So far we’ve selected an element with a selector and determined what style we’d like to apply with a property. Now we can determine the behavior of that property with a value. Values can be identified as the text between the colon, ```:```, and semicolon, ```;```. Here we are selecting all <p> elements and setting the value of the color property to be orange and the value of the font-size property to be 16 pixels.

```
p {
  color: orange;
  font-size: 16px;
}
```

To review, in CSS our rule set begins with the selector, which is followed by curly brackets. Within these curly brackets are declarations consisting of property and value pairs. Each declaration begins with a property, which is followed by a colon, the property value, and finally a semicolon.

It is a common practice to indent property and value pairs within the curly brackets. As with HTML, these indentations help keep our code organized and legible.

### Working with Selectors

Selectors, as previously mentioned, indicate which HTML elements are being styled. It is important to fully understand how to use selectors and how they can be leveraged. The first step is to become familiar with the different types of selectors. We’ll start with the most common selectors: type, class, and ID selectors.

#### Type Selectors

Type selectors target elements by their element type. For example, should we wish to target all division elements, ```<div>```, we would use a type selector of div. The following code shows a type selector for division elements as well as the corresponding HTML it selects.

**CSS:**
```div { ... }```

**HTML:**
```
<div>...</div>
<div>...</div>
```

#### Class Selectors

Class selectors allow us to select an element based on the element’s class attribute value. Class selectors are a little more specific than type selectors, as they select a particular group of elements rather than all elements of one type.

Class selectors allow us to apply the same styles to different elements at once by using the same class attribute value across multiple elements.

Within CSS, classes are denoted by a leading period, ```.```, followed by the class attribute value. Here the class selector will select any element containing the class attribute value of awesome, including both division and paragraph elements.

**CSS:**
```.awesome { ... }```

**HTML:**
```
<div class="awesome">...</div>
<p class="awesome">...</p>
```

#### ID Selectors

ID selectors are even more precise than class selectors, as they target only one unique element at a time. Just as class selectors use an element’s class attribute value as the selector, ID selectors use an element’s ```id``` attribute value as a selector.

Regardless of which type of element they appear on, ```id``` attribute values can only be used once per page. If used they should be reserved for significant elements.

Within CSS, ID selectors are denoted by a leading hash sign, ```#```, followed by the id attribute value. Here the ID selector will only select the element containing the ```id``` attribute value of 'awesome'.

**CSS:**
```
#awesome { ... }
```

**HTML:**
```
<div id="awesome">...</div>
```

#### Additional Selectors

Selectors are extremely powerful, and the selectors outlined here are the most common selectors you’ll come across. These selectors are also only the beginning. Many more advanced selectors exist, don’t be afraid to look into some of them once you feel you're ready!

### Color!

Web colours are colours used in designing web pages. Colours may be specified as an RGB triplet or in hexadecimal format (a hex triplet). Hexadecimal color codes begin with a number sign (#). This number can be picked from a graphics software or from some nice web tool, such as, Color picker, for example. When you have chosen your color, copy the number that starts with # and paste that in your CSS file.

Good to know: ```#000``` is black and ````#fff``` is white.

### Stylish

Let’s try to give a nice border to our image.

```
img {
    border: 1px solid #000;
}
```

Here we are giving the following style to all the img tags we have: a 1-pixel thick, solid black border to all four edges of our images. If we want to give the style to just one of the four edges, for example, the top edge, we would write

```
img {
    border-top: 1px solid #000;
}
```

### Hierarchy

As you learned in the structure section in HTML you can nest your tags inside of one another like so:

```
<div id="main-content">
    <h1>The h1 tag indicates the primary header of the document.</h1>
    <p>Some text.</p>
</div>
```

In CSS you can apply hierarchical styling like this:

```
p {
    color: black;
}
div p {
    color: red;
}
```

So we have two rules here. The first says the text colour in paragraphs should be black. The second rule is more specific - it says the text in paragraphs should be red, but only if those paragraphs are inside of a ```div``` tag. **A more specific rule always beats a less specific rule.**

### Comments

It is also possible to put “comments” in your CSS, there to remind you (or other people editing the HTML file) of stuff without changing the way the page displays in a browser. A CSS comment looks like this:

```/* remember always to write a ; after your value */```

Comments can also enclose other CSS elements, to “comment them out”. This is a useful technique when you’re experimenting with a page to see how it looks when you change things around.

### Troubleshooting

Nothing changed when you refreshed your index.html?

Double check the name of the CSS file in the ```<link>``` tag, and also double check that the CSS file is in the same directory as the HTML file.

Also make sure that all rules end with a ; and are placed inside of the curly brackets of the selector you want to style.

#### Practice makes perfect

We've created a ready-to-use project for you using HTML and CSS in the 'blog' folder. Try playing around with it and get the following done:

1. Make the first (```h1```) title a darker shade of pink.
2. In the second (```#second```) div, add an image in between the two paragraphs. It can be of whatever you want – but don't forget the alt text!
3. Style the div with class ```info-box```: add a 1px wide black border (dashed, dotted or solid).
4. At the bottom of the style.css file, we have commented out some code. Uncomment it, and watch what happens! 

Time to check out our work and see if our HTML and CSS are getting along. Now opening our ```index.html``` file (or refreshing the page if it’s already opened) within a web browser should show slightly different results than before. Your first styled web-page!

### Continue learning:
[Codecademy - Web Fundamentals](http://www.codecademy.com/tracks/web)

[Code School](https://www.codeschool.com/paths/html-css)

[CSS Guides and tutorials](https://developer.mozilla.org/en-US/docs/Web/CSS)

[CSS Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference) - listing all standard CSS properties, pseudo-classes and pseudo-elements, ```@```-rules, units, and selectors in alphabetic order.

[Learn to Code HTML & CSS](http://learn.shayhowe.com/html-css/)

[Learn to Code Advanced HTML & CSS](http://learn.shayhowe.com/advanced-html-css/)

[From zero to hero(ine) with SkillCrush](http://skillcrush.com/skillcrush-blueprints/)

[HTML & CSS for beginners](http://opentechschool.github.io/html-css-beginners/) - great German resource

The W3C has built both [HTML](http://validator.w3.org/) and [CSS](http://jigsaw.w3.org/css-validator/) validators that will scan code for mistakes.

Still unsure? We're pretty sure you'll find your solution on this little website called StackOverflow.
