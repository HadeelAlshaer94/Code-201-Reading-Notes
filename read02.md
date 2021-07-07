# Hyber Text Markup Language (HTML)
## Headings and paragraphs
### Headings 
##### HTML has six "levels" of headings: \<h1> is used for main headings \<h2> is used for subheadings If there are further sections under the subheadings then the \<h3> element is used, and so on... Browsers display the contents of headings at different sizes. The contents of an \<h1> element is the largest, and the contents of an \<h6> element is the smallest. The exact size at which each browser shows the headings can vary slightly. Users can also adjust the size of text in their browser. You will see how to control the size of text, its color, and the fonts used when we come to look at CSS.

```html
<h1>This is a Main Heading</h1>
<h2>This is a Level 2 Heading</h2>
<h3>This is a Level 3 Heading</h3>
<h4>This is a Level 4 Heading</h4>
<h5>This is a Level 5 Heading</h5>
<h6>This is a Level 6 Heading</h6>

```
### The Headings Results
<h1>This is a Main Heading</h1>
<h2>This is a Level 2 Heading</h2>
<h3>This is a Level 3 Heading</h3>
<h4>This is a Level 4 Heading</h4>
<h5>This is a Level 5 Heading</h5>
<h6>This is a Level 6 Heading</h6>

### Paragraphs
##### To create a paragraph, surround the words that make up the paragraph with an opening \<p> tag and closing \</p> tag. By default, a browser will show each paragraph on a new line with some space between it and any subsequent paragraphs.

```html 
<p> A paragraph consists of one or more sentences
    that form a self-contained unit of discourse. The
    start of a paragraph is indicated by a new
    line. </p>
<p> Text is easier to understand when it is split up
    into units of text. For example, a book may have
   chapters. Chapters can have subheadings. Under
   each heading there will be one or more
   paragraphs. </p>

```

### The Paragraphs Results
<p> A paragraph consists of one or more sentences
    that form a self-contained unit of discourse. The
    start of a paragraph is indicated by a new
    line. </p>
<p> Text is easier to understand when it is split up
    into units of text. For example, a book may have
   chapters. Chapters can have subheadings. Under
   each heading there will be one or more
   paragraphs. </p>


## Bold, italic
### Bold
##### By enclosing words in the tags \<b> and \</b> we can make characters appear bold. The ]\<b> element also represents a section of text that would be presented in a visually different way (for example key words in a paragraph) although the use of the \<b> element does not imply any additional meaning.

```html
<p>This is how we make a word appear <b>bold.</b>
</p>
<p>Inside a product description you might see some
<b>key features</b> in bold.</p>
```
### The Bold Results
<p>This is how we make a word appear <b>bold.</b>
</p>
<p>Inside a product description you might see some
<b>key features</b> in bold.</p>

### Italic 
##### By enclosing words in the tags \<i> and \</i> we can make characters appear italic. The \<i> element also representsn a section of text that would be said in a different way from surrounding content — such as technical terms, names of ships, foreign words, thoughts, or other terms that would usually be italicized.

```html
<p>This is how we make a word appear <i>italic</i>.
</p>
<p>It's a potato <i>Solanum teberosum</i>.</p>
<p>Captain Cook sailed to Australia on the
<i>Endeavour</i>.</p>
```

### Italic Results
<p>This is how we make a word appear <i>italic</i>.
</p>
<p>It's a potato <i>Solanum teberosum</i>.</p>
<p>Captain Cook sailed to Australia on the
<i>Endeavour</i>.</p>


## Line Breaks & Horizontal Rules
### Line Breaks 
##### As you have already seen, the browser will automatically show each new paragraph or heading on a new line. But if you wanted to add a line break inside the middle of a paragraph you can use the line break tag \<br />.

```html
<p>The Earth<br />gets one hundred tons heavier
every day<br />due to falling space dust.</p>
```
### Line Break Results
<p>The Earth<br />gets one hundred tons heavier
every day<br />due to falling space dust.</p>



### Horizontal Rules
##### To create a break between themes — such as a change of topic in a book or a new scene in a play — you can add a horizontal rule between sections using the \<hr /> tag. There are a few elements thatdo not have any words between an opening and closing tag. They are known as empty elements and they are written differently. An empty element usually has only one tag. Before the closing angled bracket of an empty element there will often be a space and a forward slash character. Some web page authors miss this out but it is a good habit to get into.
 ```html
<p>Venus is the only planet that rotates
clockwise.</p>
<hr />
<p>Jupiter is bigger than all the other planets
combined.</p>
```


### Horizontal Rules Results
<p>Venus is the only planet that rotates
clockwise.</p>
<hr />
<p>Jupiter is bigger than all the other planets
combined.</p>


# Cascading Style Sheet (CSS)


# Javascript (JS)
