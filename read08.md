# Cascading Style Sheet (CSS)
## Layout
### Normal Flow position:static
##### In normal flow, each block-level element sits on top of the next one. Since this is the default way in which browsers treat HTML elements, you do not need a CSS property to indicate that elements should appear in normal flow, but the syntax would be: position: static; I have not specified a width property for the heading element, so you can see how it stretches the width of the entire browser window by default. The paragraphs are restricted to 450 pixels wide. This shows how the elements in normal flow start on a new line even if they do not take up the full width of the browser window. 

## HTML
```html
<body>
<h1>The Evolution of the Bicycle</h1>
<p>In 1817 Baron von Drais invented a walking
machine that would help him get around the
royal gardens faster...</p>
</body>

```



## CSS

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



### Relative Positioning position:relative
##### Relative positioning moves an element in relation to where it would have been in normal flow. For example, you can move it 10 pixels lower than it would havebeen in normal flow or 20% to the right. You can indicate that an element should be relatively positioned using the position property with a value of relative. You then use the offset properties (top or bottom and left or right) to indicate how far to move the element from where it would have been in normal flow. To move the box up or down, you can use either the top or bottom properties. To move the box horizontally, you can use either the left or right properties. The values of the box offset properties are usually given in pixels, percentages or ems.

## HTML
```html
<body>
<h1>The Evolution of the Bicycle</h1>
<p>In 1817 Baron von Drais invented a walking
machine that would help him get around the
royal gardens faster...</p>
</body>
```

## CSS
```html
p.example {
position: relative;
top: 10px;
left: 100px;}
```



## Absolute Positioning position:absolute
##### When the position property is given a value of absolute, the box is taken out of normal flow and no longer affects the position of other elements on the page. (They act like it is not there.) The box offset properties (top or bottom and left or right) specify where the element should appear in relation to its containing element. In this example, the heading has been positioned at the top of the page and 500 pixels from its left edge. The width of the heading is set to be 250 pixels wide. The width property has also been applied to the \<p> elements in this example to prevent the text from overlapping and becoming unreadable.


## HTML
```html
<body>
<h1>The Evolution of the Bicycle</h1>
<p>In 1817 Baron von Drais invented a walking
machine that would help him get around the
royal gardens faster...</p>
</body>
```



## CSS

```html
h1 {
position: absolute;
top: 0px;
left: 500px;
width: 250px;}
p {
width: 450px;}
```


## Fixed Positioning position:fixed
##### Fixed positioning is a type of absolute positioning that requires the position property to have a value of fixed. It positions the element in relation to the browser window.Therefore, when a user scrolls down the page, it stays in the exact same place. It is a good idea to try this example in your browser to see the effect. To control where the fixed position box appears in relation to the browser window, the box offset properties are used. In this example, the heading has been positioned to the top left hand corner of the browser window. When the user scrolls down the page, the paragraphs disappear behind the heading. The \<p> elements are in normal flow and ignore the space that the \<h1> element would have taken up. Therefore, the margin-top property has been used to push the first \<p> element below where the fixed position \<h1> element is sitting.


## HTML
```html
<body>
<h1>The Evolution of the Bicycle</h1>
<p class="example">In 1817 Baron von Drais
invented a walking machine that would help him
get around the royal gardens faster...</p>
</body>
```


## CSS
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


### Overlapping Elements z-index
##### When you use relative, fixed, orabsolute positioning, boxes canoverlap. If boxes do overlap, the elements that appear later in the HTML code sit on top of those that are earlier in the page. If you want to control which element sits on top, you can use the z-index property. Its value is a number, and the higher the number the closer that element is to the front. For example, an element with a z-index of 10 will appear over the top of one with a z-index of 5. This example looks similar to the one on page 368, but it uses relative positioning for the \<p> elements. Because the paragraphs are relatively positioned, by default they would appear over the top of the heading as the user scrolls down the page. To ensure that the \<h1> element stays on top, we use the z-index property on the rule for the \<h1> element. The z-index is sometimes referred to as the stacking context (as if the blocks have been stacked on top of each other on a z axis). If you are familiar with desktop publishing packages, it is the equivalent of using the 'bring to front' and 'send to back' features.


## CSS

```html
h1 {
position: fixed;
top: 0px;
left: 0px;
margin: 0px;
padding: 10px;
width: 100%;
background-color: #efefef;
z-index: 10;}
p {
position: relative;
top: 70px;
left: 70px;}
```


### Floating Elements float
##### The float property allows you to take an element in normal flow and place it as far to the left or right of the containing element as possible. Anything else that sits inside the containing element will flow around the element that is floated. When you use the float property, you should also use the width property to indicate how wide the floated element should be. If you do not, results can be inconsistent but the box is likely to take up the full width of the containing element (just like it would in normal flow). In this example, a \<blockquote> element is used to hold a quotation. It's containing element is the \<body> element. The \<blockquote> element is floated to the right, and the paragraphs that follow the quote flow around the floated element.


## HTML
```html
<h1>The Evolution of the Bicycle</h1>
<blockquote>"Life is like riding a bicycle.
To keep your balance you must keep moving." -
Albert Einstein</blockquote>
<p>In 1817 Baron von Drais invented a walking
machine that would help him get around the royal
gardens faster: two same-size in-line wheels, the
front one steerable, mounted in a frame ... </p>
```

## CSS
```html
blockquote {
float: right;
width: 275px;
font-size: 130%;
font-style: italic;
font-family: Georgia, Times, serif;
margin: 0px 0px 10px 10px;
padding: 10px;
border-top: 1px solid #665544;
border-bottom: 1px solid #665544;}
```






