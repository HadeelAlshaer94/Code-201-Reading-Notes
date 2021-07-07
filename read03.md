# Hyber Text Markup Language (HTML)
## Lists:
#### Numbered lists

#### Ordered lists 
##### are lists where each item in the list is numbered. For example, the list might be a set of steps for a recipe that must be performed in order, or a legal contract where each point needs to be identified by a section number.

## \<ol>
##### The ordered list is created with the \<ol> element.
  
## \<li>
##### Each item in the list is placed between an opening \<li> tag and a closing \</li> tag. (The li stands for list item.) Browsers indent lists by default. Sometimes you may see a type attribute used with the \<ol> element to specify the type of numbering (numbers, letters, roman numerals and so on). It is better to use the CSS liststyle- type.



```html
<ol>
<li>Chop potatoes into quarters</li>
<li>Simmer in salted water for 15-20
minutes until tender</li>
<li>Heat milk, butter and nutmeg</li>
<li>Drain potatoes and mash</li>
<li>Mix in the milk mixture</li>
</ol>
```
### Results:
<ol>
<li>Chop potatoes into quarters</li>
<li>Simmer in salted water for 15-20
minutes until tender</li>
<li>Heat milk, butter and nutmeg</li>
<li>Drain potatoes and mash</li>
<li>Mix in the milk mixture</li>
</ol>




#### Unordered lists 
##### are lists that begin with a bullet point (rather than characters that indicate order).

### \<ul>
##### The unordered list is created with the \<ul> element.

### \<li>
##### Each item in the list is placed between an opening \<li> tag and a closing \</li> tag. (The li stands for list item.)


```html
<ul>
<li>1kg King Edward potatoes</li>
<li>100ml milk</li>
<li>50g salted butter</li>
<li>Freshly grated nutmeg</li>
<li>Salt and pepper to taste</li>
</ul>
```


### Results:
<ul>
<li>1kg King Edward potatoes</li>
<li>100ml milk</li>
<li>50g salted butter</li>
<li>Freshly grated nutmeg</li>
<li>Salt and pepper to taste</li>
</ul>


#### Definition lists 
##### are made up of a set of terms along with the definitions for each of those terms.

### \<dl>
##### The definition list is created with the \<dl> element and usually consists of a series of terms and their definitions. Inside the \<dl> element you will usually see pairs of \<dt> and \<dd> elements. 

### \<dt> 
##### This is used to contain the term being defined (the definition term).

### \<dd>
##### This is used to contain the definition. 

##### Sometimes you might see a list where there are two terms used for the same definition or two different definitions for the same term.


```html
<dl>
<dt>Sashimi</dt>
<dd>Sliced raw fish that is served with
condiments such as shredded daikon radish or
ginger root, wasabi and soy sauce</dd>
<dt>Scale</dt>
<dd>A device used to accurately measure the
weight of ingredients</dd>
<dd>A technique by which the scales are removed
from the skin of a fish</dd>
<dt>Scamorze</dt>
<dt>Scamorzo</dt>
<dd>An Italian cheese usually made from whole
cow's milk (although it was traditionally made
from buffalo milk)</dd>
</dl>
```

### Results:
<dl>
<dt>Sashimi</dt>
<dd>Sliced raw fish that is served with
condiments such as shredded daikon radish or
ginger root, wasabi and soy sauce</dd>
<dt>Scale</dt>
<dd>A device used to accurately measure the
weight of ingredients</dd>
<dd>A technique by which the scales are removed
from the skin of a fish</dd>
<dt>Scamorze</dt>
<dt>Scamorzo</dt>
<dd>An Italian cheese usually made from whole
cow's milk (although it was traditionally made
from buffalo milk)</dd>
</dl>



#### Nested lists
##### You can put a second list inside an \<li> element to create a sublist or nested list. Browsers display nested lists indented further than the parent list. In nested unordered lists, the browser will usually change the style of the bullet point too.

```html
<ul>
<li>Mousses</li>
<li>Pastries
<ul>
<li>Croissant</li>
<li>Mille-feuille</li>
<li>Palmier</li>
<li>Profiterole</li>
</ul>
</li>
<li>Tarts</li>
</ul>
```

### Results:
<ul>
<li>Mousses</li>
<li>Pastries
<ul>
<li>Croissant</li>
<li>Mille-feuille</li>
<li>Palmier</li>
<li>Profiterole</li>
</ul>
</li>
<li>Tarts</li>
</ul>


## Boxes:

### Box Dimensions: Width, Hieght
##### By default a box is sized just bignenough to hold its contents. To set your own dimensions for a box you can use the height and width properties. The most popular ways to specify the size of a box are to use pixels, percentages, or ems. Traditionally, pixels have been the most popular method because they allow designers to accurately control their size. When you use percentages, the size of the box is relative to the size of the browser window or, if the box is encased within another box, it is a percentage of the size of the containing box. When you use ems, the size of the box is based on the size of text within it. Designers have recently started to use percentages and ems more for measurements as they try to create designs that are flexible across devices which have different-sized screens. In the example on the right, you can see that a containing \<div> element is used which is 300 pixels wide by 300 pixels high. Inside of this is a paragraph that is 75% of the width and height of the containing element. This means that the size of the paragraph is 225 pixels wide by 225 pixels high.

```html
<div>
<p>The Moog company pioneered the commercial
manufacture of modular voltage-controlled
analog synthesizer systems in the early
1950s.</p>
</div>
```

### Limiting Width: min-width, max-width
##### Some page designs expand and shrink to fit the size of the user's screen. In such designs, the min-width property specifies the smallest size a box can be displayed at when the browser window is narrow, and the max-width property indicates the maximum width a box can stretch to when the browser window is wide. These are very helpful properties to ensure that the content of pages are legible (especially on the smaller screens of handheld devices). For example, you can use the max-width property to ensure that lines of text do not appear too wide within a big browser window and you can use the min-width property to make sure that they do not appear too narrow. You may find it helpful to try this example out in your browser so that you can see what happens when you increase or decrease the size of the browser window.

```html
<tr>
<td><img src="images/rhodes.jpg" width="200"
height="100" alt="Fender Rhodes" /></td>
<td class="description">The Rhodes piano is an
electro-mechanical piano, invented by Harold
Rhodes during the fifties and later
manufactured in a number of models ...</td>
<td>$1400</td>
</tr>
```

```html
td.description {
min-width: 450px;
max-width: 650px;
text-align: left;
padding: 5px;
margin: 0px;}
```


# JavaScript (JS)
### Array 
##### An array is a special type of variable. It doesn't just store one value; it stores a list of values.
- You should consider using an array whenever you are working with a list or a set of values that are related to each other.
- Arrays are especially helpful when you do not know how many items a list will contain because, when you create the array, you do not need to specify how many values it will hold.
- If you don't know how many items a list will contain, rather than creating enough variables for a long list (when you might only use a small percentage of them), using an array is considered a better solution.
- For example, an array can be suited to storing the individual items on a shopping list because it is a list of related items.
- Additionally, each time you write a new shopping list, the number of items on it may differ.
- As you will see on the next page, values in an array are separated by commas.



### CREATING AN ARRAY
##### You create an array and give it a name just like you would any other variable (using the var keyword followed by the name of the array). The values are assigned to the array inside a pair of square brackets, and each value is separated by a comma. The values in the array do not need to be the same data type, so you can store a string, a number and a Boolean all in the same array. This technique for creating an array is known as an array literal. It is usually the preferred method for creating an array. You can also write each value.

```html
var colors;
colors ['white', 'black', ' custom '];
var el document.getElementByld('col ors');
el.textContent = col ors[O];
```










### USING IF ... ELSE STATEMENTS
##### Here you can see that an if ... e 1 se statement al lows you to provide two sets of code:
 - one set if the condition evaluates to true
 - another set if the condition is false
 - In this test, there are two possible outcomes: a user can either get a score equal to or greater than the pass mark (which means they pass), or they can score less than the pass mark (which means they fail).
 - One response is required for each eventuality. The response is then written to the page.
 - Note that the statements inside an if statement should be followed by a semicolon, but there is no need to place one after the closing curly brace of the code blocks.

```html
var pass = 50;
var score = 75;
var msg;
II Pass mark
II Current score
II Message
II Select message to write based on score
if (score >= pass) {
msg = 'Congratulations, you passed!';
} else {
msg = 'Have another go!';
var el = document .getElementByld('answer');
el .textContent = msg;
```

### USING SWITCH STATEMENTS
##### In this example, the purpose of the switch statement is to present the user with a different message depending on which level they are at. The message is stored in a variable called msg. The variable called l eve 1 contains a number indicating which level the user is on. This is then used as the switch value. (The switch value could also be an expression.)
##### In the following code block (inside the curly braces), there are three options for what the value of the 1eve1 variable might be: the numbers 1, 2, or 3. If the value of the 1eve1 variable is the number 1, the value of themsg variable is set to 'Good luck on the first test'. If the value is 2, it will read: 'Second of three - keep going!· If the value is 3, the messagem will read: 'Final round, almost it here ' .
```html
var msg;
var level = 2;
II Message
11 Level
/I Determine message based on level
switch (level) {
case 1:
msg = 'Good luck on the first test ' ;
break;
case 2:
msg = 'Second of three - keep going!';
break;
case 3:
msg = ' Final round, almost there!';
break;
default :
msg = 'Good l uck!';
break;
var el = document.getEl ementByld('answer ' );
el .textContent = msg;
```
