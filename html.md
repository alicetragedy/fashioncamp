### [HTM-WHAT?](https://github.com/alicetragedy/fashioncamp-html.git)

Every webpage you look at is written in a language called HTML (HyperText Markup Language). You can think of HTML as the skeleton that gives every webpage structure. In this course, that's exactly what we'll do, using HTML to add paragraphs, headings, images and links to a webpage.

HTML is the main markup language for creating web pages and other information that can be displayed in a web browser. You can write your web application in any programming languages, but in the end it will always be transformed into HTML because that’s the language of the browser. It is a so-called hierarchical language, you'll find out why in bit.

### Inspect all the elements

We're hacking Facebook today. We'll not really. Only very locally actually. On your machine. Open up facebook.com and either right click your mouse or clickpad and select 'inspect element' or hit the command key (⌘) and 'u'. Et voila, you're looking at Facebook's HTML skeleton. It is a lot, but Facebook shares a lot of common features with other websites. For instance, try and find the ```title``` 'tag' (hint: it is inbetween ```head``` and ```/head```. Now there's Facebook in there. Try and change it into 'omg I am totally hacking Facebook!'. Hit the enter key and marvel at your accomplishments. We can also change the look of Facebook while we're at it. Find the ```<body>``` tag, select it and change the ```background-color``` to 'pink'. But that's all the CSS (CSS-WHAT?) we're discussing today!

### How to write a HTML document

This is actually pretty simple: HTML is written as a plain text document. A HTML file always uses the extension .html to indicate its filetype.

### Text editing

You will need a plain text editor in order to edit HTML files. We suggest downloading and using [Sublime](http://www.sublimetext.com/2).

**Why not use MS Word as a text editor?**

Microsoft Word or Pages are so-called rich text editors. MS Word has a lot of formatting information that can’t be understood by the web. The way Word knows where to put a paragraph (or bigger font sizes, or a picture, or anything) is totally different from how HTML and CSS work. For code of all kinds, including HTML and CSS, it’s important to use a text editor to keep your code clean.

In addition, text editors provide some hints about what pieces of code you have where. This is called syntax highlighting. <span style=”color:red”>It</span> <span style=”color:blue”>is</span> like <span style=”color:blue”>showing</span> <span style=”color:red”>nouns</span> in <span style=”color:red”>red</span> and <span style=”color:blue”>showing</span> the <span style=”color:red”>verbs</span> in <span style=”color:red”>blue</span> in a <span style=”color:red”>sentence</span>.

What’s next? Let's start a new HTML document.
1. Always put ```<!DOCTYPE html>``` on the first line. This tells the browser what language it's reading (in this case, HTML).
2. Always put ```<html>``` on the next line. This starts the HTML document.
3. Always put ```</html>``` on the last line. This ends the HTML document.

Then save it with the file extension .html. You’re now officially editing an html document!

### Understanding Common HTML Terms

While getting started with HTML, you will likely encounter new—and often strange—[terms](http://www.scriptingmaster.com/html/HTML-terms-glossary.asp). Over time you will become more and more familiar with all of them, but the three common HTML terms you should begin with are elements, tags, and attributes.

#### Elements

Elements are designators that define the structure and content of objects within a page. Some of the more frequently used elements include multiple levels of headings (identified as ```<h1>``` through ```<h6>``` elements) and paragraphs (identified as the ```<p>``` element); the list goes on to include the ```<a>```, ```<div>```, ```<span>```, ```<strong>```, and ```<em>``` elements, and many more.

Elements are identified by the use of less-than and greater-than angle brackets, < >, surrounding the element name. Thus, an element will look like the following:

```<strong>I am a bold element</strong>```

#### Tags

The use of less-than and greater-than angle brackets surrounding an element creates what is known as a tag. Tags most commonly occur in pairs of opening and closing tags.

An opening tag marks the beginning of an element. It consists of a less-than sign followed by an element’s name, and then ends with a greater-than sign; for example, ```<div>```.

A closing tag marks the end of an element. It consists of a less-than sign followed by a forward slash and the element’s name, and then ends with a greater-than sign; for example, ```</div>```.

The content that falls between the opening and closing tags is the content of that element. An anchor link, for example, will have an opening tag of ```<a>``` and a closing tag of ```</a>```. What falls between these two tags will be the content of the anchor link.

So, anchor tags will look a bit like this:

```<a>I am a link</a>```

#### Attributes

Attributes are properties used to provide additional information about an element. The most common attributes include the ```id``` attribute, which identifies an element; the ```class``` attribute, which classifies an element; the ```src``` attribute, which specifies a source for embeddable content; and the ```href``` attribute, which provides a hyperlink reference to a linked resource.

Attributes are defined within the opening tag, after an element’s name. Generally attributes include a name and a value. The format for these attributes consists of the attribute name followed by an equals sign and then a quoted attribute value. For example, an ```<a>``` element including an ```href``` attribute would look like the following:

```<a href="http://facebook.com/">Facebook</a>```

**Behind the scenes**

Inside the ```<html>``` element, the ```<head>``` element identifies the top of the document, including any metadata (accompanying information about the page). The content inside the ```<head>``` element is not displayed on the web page itself. Instead, it may include the document title (which is displayed on the title bar in the browser window), links to any external files, or any other beneficial metadata.

All of the visible content within the web page will fall within the <body> element. A breakdown of a typical HTML document structure looks like this:
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Hello World</title>
  </head>
  <body>
    <h1>Hello World</h1>
    <p>This is a web page.</p>
  </body>
</html>
```

When an element is placed inside of another element, also known as **nested**, it is a good idea to indent that element to keep the document structure well organized and legible. In the previous code, both the ```<head>``` and ```<body>``` elements were nested—and indented—inside the <html> element. The pattern of indenting for elements continues as new elements are added inside the ```<head>``` and ```<body>``` elements.

#### Open and close

In the previous example, the ```<meta>``` element had only one tag and didn’t include a closing tag. Fear not, this was intentional! Not all elements consist of opening and closing tags. Some elements simply receive their content or behavior from attributes within a single tag. We know, it's confusing... The ```<meta>``` element is one of these elements. The content of the previous <meta> element is assigned with the use of the charset attribute and value. Other common selfclosing elements include ```<br>```, ```<embed>```, ```<hr>```, ```<img>```, ```<input>```, ```<link>```, ```<meta>```, ```<param>``` and ```<source>```.

### Images

```<img>``` is one of those tags that doesn’t need a separate closing tag. You could put ```</img>``` after the tag if you like, it doesn’t change the way the browser views the page. Images have to be kept in separate image files, outside the HTML file. Find an image of your liking on the web and save it in the same directory as your HTML file. If you don’t have a picture in mind then here’s the best picture on the internet: <a href="http://addyosmani.com/blog/wp-content/uploads/2013/04/unicorn.jpg" target="_blank">http://addyosmani.com/blog/wp-content/uploads/2013/04/unicorn.jpg</a>

After you have your image, you can include it in your HTML page by using an ```<img>``` tag.

```<img src="kittens.jpg">```

Add the ```<img>``` tag anywhere inside the “body” of your HTML document where you’d like the image to appear. Replace “kittens.jpg” with the file name of the image that you saved in the same directory as the HTML file.

TIP: The image source name (```src```) of kittens.jpg is a path relative to the HTML document. So in this case kittens.jpg is located in the same directory, but you could use a name like "images/kittens.jpg" if you put the image file into a subdirectory called “images”.

#### Alt Text

A good habit to get into is using ```alt text``` to describe the contents of an image:

```<img src="kittens.jpg" alt="Some kittens">```

The alt text is a textual description of what’s in the image. This is important for anyone who can’t see the images (for instance vision impaired people using a screenreader.) Any image that isn’t purely decorative should have a description set with the “alt=” attribute.

### Indentation

Are you wondering why we wrote the ```h1``` and ```p``` tags 'indented' inside the body tags? It will not change at all how the browser reads or interpretates the document, but it is a good practice among developers to write code like that in order to have a more clear document and still be able to work with it when there is a lot of lines of code. It also shows the heircharcical nature of HTML pretty well.

### Comments

It is also possible to put “comments” in your HTML. Comments in HTML are there to remind you (or other people editing the HTML file) without changing the way the page displays in a browser. Like other HTML elements, comments are written by using a tag. Although comment tags look a little different:

```<!-- I am a comment -->```

The “start comment” tag is ```<!--``` and the “end comment” tag is ```-->```.

Comments can also enclose other HTML elements, to “comment them out”. This is a useful technique when you’re experimenting with a page to see how it looks when you change things around.

For example, how would we comment out the ```h1``` heading in your current page:

```
<body>
    <!-- <h1>I'm the title.</h1> -->
    <p>And I'm a paragraph!</p>
</body>
```

If you reload the page in your browser, you’ll notice the heading has vanished.

### Practice makes perfect

Now create a file called index.html, that has the right setup (```<html>```, ```<head>```, et al), contains one ```<h1>``` title (this can say anything you like), a ```<p>```aragraph, a link within that paragraph and an image. And yes you can ask for our help.

Done? Open your index.html in your browser (right-click) and marvel at your accomplishments. Your first web-page!

### Next steps: CSS
You may be thinking at this stage that your HTML page looks pretty... 90-ies. Can you spice it up a little? Yes you can, in our workshop tomorrow!

### Continue learning:
[Codecademy - Web Fundamentals](http://www.codecademy.com/tracks/web)

[Code School](https://www.codeschool.com/paths/html-css)

[HTML guides and tutorials](https://developer.mozilla.org/en-US/docs/Web/HTML)

[HTML Reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element) - with an explanation for every HTML element

[Learn to Code HTML & CSS](http://learn.shayhowe.com/html-css/)

[Learn to Code Advanced HTML & CSS](http://learn.shayhowe.com/advanced-html-css/)

[From zero to hero(ine) with SkillCrush](http://skillcrush.com/skillcrush-blueprints/)

[HTML & CSS for beginners](http://opentechschool.github.io/html-css-beginners/) - great German resource

The W3C has built both [HTML](http://validator.w3.org/) and [CSS](http://jigsaw.w3.org/css-validator/) validators that will scan code for mistakes.
Still unsure? We're pretty sure you'll find your solution on this little website called StackOverflow.
