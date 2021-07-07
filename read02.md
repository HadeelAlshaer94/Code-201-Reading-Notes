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
### Specifying Typefaces font-family
##### The font-family property allows you to specify the typeface that should be used for any text inside the element(s) to which a CSS rule applies. The value of this property is the name of the typeface you want to use. The people who are visiting your site need the typeface you have specified installed on their computer in order for it to be displayed. You can specify a list of fonts separated by commas so that, if the user does not have your first choice of typeface installed, the browser can try to use an alternative font from the list. It is also common to end with a generic font name for that type of font (which you saw on pages 269-270). If a font name is made up of more than one word, it should be put in double quotes. Designers suggest pages usually look better if they use no more than three typefaces on a page.

```html
<!DOCTYPE html>
<html>
<head>
<title>Font Family</title>
<style type="text/css">
body {
font-family: Georgia, Times, serif;}
h1, h2 {
font-family: Arial, Verdana, sans-serif;}
.credits {
font-family: "Courier New", Courier,
monospace;}
</style>
</head>
<body>
<h1>Briards</h1>
<p class="credits">by Ivy Duckett</p>
<p class="intro">The <a class="breed"
href="http://en.wikipedia.org/wiki/
Briard">briard</a>, or berger de brie, is
a large breed of dog traditionally used as
a herder and guardian of sheep...</p>
</body>
</html>
```

### Size of Type font-size
##### The font-size property enables you to specify a size for thefont. There are several ways to specify the size of a font. The most common are: pixels Pixels: are commonly used because they allow web designers very precise control over how much space their text takes up. The number of pixels is followed by the letters px. percentages The default size of text in browsers is 16px. So a size of 75% would be the equivalent of 12px, and 200% would be 32px. If you create a rule to make all text inside the \<body> element to be 75% of the default size (to make it 12px), and then specify another rule that indicates the content of an element inside the \<body> element should be 75% size, it will be 9px (75% of the 12px font size). ems: An em is equivalent to the width of a letter m.

```html
body {
font-family: Arial, Verdana, sans-serif;
font-size: 12px;}
h1 {
font-size: 200%;}
h2 {
font-size: 1.3em;}
```

### Underst anding Font Formats
##### Different browsers support different formats for fonts (in the same way that they support different audio and video formats), so you will need to supply the font in several variations to reach all browsers. If you do not have all of these formats for your font, you can upload the font to a website called FontSquirrel where they will convert it for you: [Font Formats](https://www.fontsquirrel.com/)

##### Font Squirrel also provides you with the CSS code for the @font-face rule. This is very helpful because, when you are dealing with multiple font formats, the src and format properties of the @font-face rule can get rather complicated. You can see an example of a more complicated @font-face rule on the left.nThe various font formats should appear in your code in this order:

# Javascript (JS)
### Decisions
##### In any programming language, the code needs to make decisions and carry out actions accordingly depending on different inputs. For example, in a game, if the player's number of lives is 0, then it's game over. In a weather app, if it is being looked at in the morning, show a sunrise graphic; show stars and a moon if it is nighttime. In this article, we'll explore how so-called conditional statements work in JavaScript. Human beings (and other animals) make decisions all the time that affect their lives, from small ("should I eat one cookie or two?") to large ("should I stay in my home country and work on my father's farm, or should I move to America and study astrophysics?") Conditional statements allow us to represent such decision making in JavaScript, from the choice that must be made (for example, "one cookie or two"), to the resulting outcome of those choices (perhaps the outcome of "ate one cookie" might be "still felt hungry", and the outcome of "ate two cookies" might be "felt full, but mom scolded me for eating all the cookies".)

![DECISION](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/conditionals/cookie-choice-small.png)
#### if...else statements
##### Here we've got: The keyword if followed by some parentheses.
- A condition to test, placed inside the parentheses (typically "is this value bigger than this other value?", or "does this value exist?"). The condition makes use of the comparison operators we discussed in the last module and returns true or false.
- A set of curly braces, inside which we have some code — this can be any code we like, and it only runs if the condition returns true.
The keyword else.
- Another set of curly braces, inside which we have some more code — this can be any code we like, and it only runs if the condition is not true — or in other words, the condition is false.

```html
if (condition) {
  code to run if condition is true
} else {
  run some other code instead
}
```

```html
const select = document.querySelector('select');
const para = document.querySelector('p');

select.addEventListener('change', setWeather);

function setWeather() {
  const choice = select.value;

  if (choice === 'sunny') {
    para.textContent = 'It is nice and sunny outside today. Wear shorts! Go to the beach, or the park, and get an ice cream.';
  } else if (choice === 'rainy') {
    para.textContent = 'Rain is falling outside; take a rain coat and an umbrella, and don\'t stay out for too long.';
  } else if (choice === 'snowing') {
    para.textContent = 'The snow is coming down — it is freezing! Best to stay in with a cup of hot chocolate, or go build a snowman.';
  } else if (choice === 'overcast') {
    para.textContent = 'It isn\'t raining, but the sky is grey and gloomy; it could turn any minute, so take a rain coat just in case.';
  } else {
    para.textContent = '';
  }
}

```

### Loop
### For Loop
##### a for-loop (or simply for loop) is a control flow statement for specifying iteration, which allows code to be executed repeatedly. Various keywords are used to specify this statement: descendants of ALGOL use "for", while descendants of Fortran use "do". There are other possibilities, for example COBOL which uses "PERFORM VARYING". A for-loop has two parts: a header specifying the iteration, and a body which is executed once per iteration. The header often declares an explicit loop counter or loop variable, which allows the body to know which iteration is being executed. For-loops are typically used when the number of iterations is known before entering the loop. For-loops can be thought of as shorthands for while-loops which increment and test a loop variable. The name for-loop comes from the word for, which is used as the keyword in many programming languages to introduce a for-loop. The term in English dates to ALGOL 58 and was popularized in the influential later ALGOL 60; it is the direct translation of the earlier German für, used in Superplan (1949–1951) by Heinz Rutishauser, who also was involved in defining ALGOL 58 and ALGOL 60. The loop body is executed "for" the given values of the loop variable, though this is more explicit in the ALGOL version of the statement, in which a list of possible values and/or increments can be specified.

```html 
for (let i = 0; i < 5; i++) {
  text += "The number is " + i + "<br>";
}
```

### While Loop
##### The while construct consists of a block of code and a condition/expression.The condition/expression is evaluated, and if the condition/expression is true,[1] the code within all of their following in the block is executed. This repeats until the condition/expression becomes false. Because the while loop checks the condition/expression before the block is executed, the control structure is often also known as a pre-test loop. Compare this with the do while loop, which tests the condition/expression after the loop has executed.

```html
while (i < 10) {
  text += "The number is " + i;
  i++;
}
```
