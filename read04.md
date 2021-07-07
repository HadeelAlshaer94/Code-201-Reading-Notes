# Links
## Linking to Other Sites
##### Links are created using the \<a> element which has an attribute called href. The value of the href attribute is the page that you want people to go to when they click on the link. Users can click on anything that appears between the opening \<a> tag and the closing \</a> tag and will be taken to the page specified in the href attribute. When you link to a different website, the value of the href attribute will be the full web address for the site, which is known as an absolute URL.

```html
<p>Movie Reviews:
<ul>
<li><a href="http://www.empireonline.com">
Empire</a></li>
<li><a href="http://www.metacritic.com">
Metacritic</a></li>
<li><a href="http://www.rottentomatoes.com">
Rotten Tomatoes</a></li>
<li><a href="http://www.variety.com">
Variety</a></li>
</ul>
</p>

```
## Linking to Other Pages on the Same Site
##### When you are linking to other pages within the same site, you do not need to specify the domain name in the URL. You can use a shorthand known as a relative URL. If all the pages of the site are in the same folder, then the value of the href attribute is just the name of the file. If you have different pages of a site in different folders, then you can use a slightly more complex syntax to indicate where the page is in relation to the current page. You will learn more about these on the pages 81-84. If you look at the download code for each chapter, you will see that the index.html file contains links that use relative URLs.

```html
<p>
<ul>
<li><a href="index.html">Home</a></li>
<li><a href="about-us.html">About</a></li>
<li><a href="movies.html">Movies</a></li>
<li><a href="contact.html">Contact</a></li>
</ul>
</p>
```

## Email Links
##### To create a link that starts up the user's email program and addresses an email to a specified email address, you use the \<a> element. However, this time the value of the href attribute starts with mailto: and is followed by the email address you want the email to be sent to. On the right you can see that an email link looks just like any other link but, when it is clicked on, the user's email program will open a new email message and address it to the person specified in the link.

```html
 <a href="mailto:jon@example.org">Email Jon</a>
``` 

## Opening Links in a New Window

##### If you want a link to open in a new window, you can use the target attribute on the opening \<a> tag. The value of this attribute should be _blank. One of the most common reasons a web page author might want a link to be opened in a new window is if it points to another website. In such cases, they hope the user will return to the window containing their site after finishing looking at the other one. Generally you should avoid opening links in a new window, but if you do, it is considered good practice to inform users that the link will open a new window before they click on it.

```html
<a href="http://www.imdb.com" target="_blank">
Internet Movie Database</a>
```

## Linking to a Specific Part of the Sa me Page
##### At the top of a long page you might want to add a list of contents that links to the corresponding sections lower down. Or you might want to add a link from part way down the page back to the top of it to save users from having to scroll back to the top. Before you can link to a specific part of a page, you need to identify the points in the page that the link will go to. You do this using the id attribute (which can be used on every HTML element). You can see that the \<h1> and \<h2> elements in this example have been given id attributes that identify those sections of the page. The value of the id attribute should start with a letter or an underscore (not a number or any other character) and, on a single page, no two id attributes should have the same value. To link to an element that uses an id attribute you use the \<a> element again, but the value of the href attribute starts with the \# symbol, followed by the value of the id attribute of the element you want to link to. 

```html
<h1 id="top">Film-Making Terms</h1>
<a href="#arc_shot">Arc Shot</a><br />
<a href="#interlude">Interlude</a><br />
<a href="#prologue">Prologue</a><br /><br />
<h2 id="arc_shot">Arc Shot</h2>
<p>A shot in which the subject is photographed by an
encircling or moving camera</p>
<h2 id="interlude">Interlude</h2>
<p>A brief, intervening film scene or sequence, not
specifically tied to the plot, that appears
within a film</p>
<h2 id="prologue">Prologue</h2>
<p>A speech, preface, introduction, or brief scene
preceding the the main action or plot of a film;
contrast to epilogue</p>
<p><a href="#top">Top</a></p>
```



# Layout
## Normal Flow: position:static
##### In normal flow, each block-level element sits on top of the next one. Since this is the default way in which browsers treat HTML elements, you do notneed a CSS property to indicate that elements should appear in normal flow, but the syntax would be: position: static; I have not specified a width property for the heading element, so you can see how it stretches the width of the entire browser window by default. The paragraphs are restricted to 450 pixels wide. This shows how the elements in normal flow start on a new line even if they do not take up the full width of the browser window.

```html
<body>
<h1>The Evolution of the Bicycle</h1>
<p>In 1817 Baron von Drais invented a walking
machine that would help him get around the
royal gardens faster...</p>
</body>
```

```html
body {
width: 750px;
font-family: Arial, Verdana, sans-serif;
color: #665544;}
h1 {
background-color: #efefef;
padding: 10px;}
p {
width: 450px;}
```




## Fixed Positioning, position:fixed
##### Fixed positioning is a type of absolute positioning that requires the position property to have a value of fixed. It positions the element in relation to the browser window. Therefore, when a user scrolls down the page, it stays in the exact same place. It is a good idea to try this example in yourbrowser to see the effect. To control where the fixed position box appears in relation to the browser window, the box offset properties are used. In this example, the heading has been positioned to the top left hand corner of the browser window. When the user scrolls down the page, the paragraphs disappear behind the heading. The \<p> elements are in normal flow and ignore the space that the \<h1> element would have taken up. Therefore, the margin-top property has been used to push the first \<p> element below where the fixed position \<h1> element is sitting.

```html
<body>
<h1>The Evolution of the Bicycle</h1>
<p class="example">In 1817 Baron von Drais
invented a walking machine that would help him
get around the royal gardens faster...</p>
</body>
```

```html
h1 {
position: fixed;
top: 0px;
left: 50px;
padding: 10px;
margin: 0px;
width: 100%;
background-color: #efefef;}
p.example {
margin-top: 100px;}
```


# Functions, Methods, and Objects
## Functions
##### Functions let you group a series of statements together to perform a specific task. If different parts of a script repeat the same task, you can reuse the function (rather than repeating the same set of st atements).


### A BASIC FUNCTION
##### In this example, the user is shown a message at the top of the page. The message is heldin an HTML element whose id attribute has a value of message. The message is going to be changed using JavaScript. Before the closing \</body> tag, you can see the link to the JavaScript file. The JavaScript file starts with a variable used to hold a new message, and is followed by a function ca lled updateMessage(). You do not need to worry about how this function works yet - you will learn about that over the next few pages. For the moment, it is just worth noting that inside the curly braces of the function are two statements.

```html
<!DOCTYPE html>
<html>
<head>
<ti t l e>Basic Function</title>
<l i nk rel ="stylesheet" href="cs s/ c03.css" />
</head>
<body>
<hl>TravelWorthy</ hl>
<div id="message">We lcome to our site! </ div>
<script src="js/ basic-function .js"></ script>
</ body>
</ html>
```



## Methods


## Objects






















