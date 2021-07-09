# JavaScript
## Object Literals
##### Objects group together a set of variables and functions to create a model of a something you would recognize from the real world. In an object, variables and functions take on new names. If a variable is part of an object, it is called a property. Properties te ll us about the object, such as the name of a hotel or the number of rooms it has. Each individual hotel might have a different name and a different number of rooms.

### CREATING OBJECTS USING LITERAL NOTATION
##### This example starts by creating an object using litera l notation. This object is called hotel which represents a hotel called Quay with 40 rooms (25 of which have been booked). Next, the content of the page is updated with data from this object. It shows the name of the hotel by accessing the object's name property and the number of vacant rooms using the checkAvail ability() method. To access a property of thisnobject, the object name is followed by a dot (the period symbol) and the name of the property that you want. Similarly, to use the method, you can use the object name followed by the method name. hotel .checkAvailability() If the method needs parameters, you can supply them in the parentheses (just like you can pass arguments to a funct ion).

```html
var hotel = {
name: 'Quay',
rooms : 40,
booked: 25,
checkAvailability: function() {
return this.rooms - this.booked;
}
} ;
JAVASCRIPT
var elName = document .getElementByld('hotelName');
elName.textContent =hotel .name;
var elRooms = document.getElementByid{'rooms');
elRooms .textContent = hotel .checkAvailability();
```

### CREATING MORE OBJECT LITERALS
##### Here you can see another object.bAgain it is called hote 1, but this time the model represents a different hotel. For a moment, imagine that this is a different page of the same travel website. The Park hotel is larger. It has 120 rooms and 77 of them are booked. The only things changing in the code are the va lues of the hot e 1 object's properties:
- The name of the hotel.
- How many rooms it has.
- How many rooms are booked.

##### The rest of the page works in exactly the same way. The name is shown using the same code. The checkAvai 1 abi l ity() method has not changed and is called in the same way. If this site had 1,000 hotels, the only thing that would need to change would be the three properties of this object. Because we created a model for the hotel using data, the same code can access and display the details for any hotel that follows the same data model. If you had two objects on the same page, you would create each one using the same notation but store them in variables with different names.

```html
var hotel = {
name: 'Park',
rooms : 120,
booked : 77,
checkAvailabi lity: function() {
return this . rooms - th i s.booked;
}
} ;
var elName = document .getElementByid('hotelName') ;
elName .textContent =hotel .name ;
var el Rooms = document .getElementByid( ' rooms') ;
e 1 Rooms . text Content = hote 1 . checkAvai l abi lity();

```



## Document Object Model
##### As a browser loads a web page, it creates a model of that page. The model is called a DOM tree, and it is stored in the browsers' memory. It consists of four main types of nodes.

```html
<html>
<body>
<di v id="page">
<hl id="header">List</hl>
<h2>Buy groceries</h2>
<ul>
<li id="one" class="hot"><em>fresh</em> figs</li>
<li id="two" class="hot">pine nuts</l i>
<l i id="three" class="hot">honey</l i>
<l i id="four">balsamic vinegar</l i>
</ ul>
<script src="js/l i st. js "></scri pt>
</ div>
</ body>
</ html>
```

### SELECTING ELEMENTS USING ID ATTRIBUTES
##### get El ementByid () al lows you to select a single element node by specifying the value of its id attribute. This method has one parameter: the value of the id attribute on the element you want to select. This value is placed inside quote marks because it is a string. The quotes can be single or double quotes, but they must match. In the example on the left, the first line of JavaScript code finds the element whose id attribute has a value of one, and stores a reference to that node in a variable ca lled e 1. The code then uses a property called cl assName (which you meet on p232) to update the value of the cl ass attribute of the element stored in this variable. Its value is coo 1, and this triggers a new rule in the CSS that sets the background color of the element to aqua. Note how the c 1 assName property is used on the variable that stores the reference to the element. Browser Support: This is one of the oldest and best supported methods for accessing elements.


## HTML:

```html
<hl id="header">List King<lhl>
<h2>Buy groceries<lh2>
<ul>
<li id="one" class="hot"><em>fresh<lem>
figs<lli>
<li id="two" class="hot">pine nut s<lli>
<li id="three" class="hot">honey<lli>
<li id="four">balsamic vi negar<ll i>
</ul>
```

## JavaScript
```html
II Select the element and store it in a variable.
var el = document.getElementByid('one');
II Change the value of the class attribute.
el.className ='cool ' ;
```

### SELECTING ELEMENTS USING CLASS ATTRIBUTES
##### The get El ementsByCl ass Name() method allows you to select elements whose c 1 ass attribute contains a specific va lue. The method has one parameter: the class name which is given in quotes within the parentheses after the method name. Because several elements can have the same value for their cl ass attribute, this method always returns a Nodelist.

```html
var elements = document .getEl ementsByClassName('hot'); II Find hot items
if (e lements .l ength> 2) {
var el = elements[2];
el.className = 'cool';}
```


### SELECTING ELEMENTS BY TAG NAME
##### The get El ementsByTagName () method allows you to select elements using their tag name. The element name is specified as a parameter, so it is placed inside the parentheses and is contained by quote marks. Note that you do not include the angled brackets that surround the tag name in the HTML (just the letters inside the brackets).


```html
var elements = document.getElementsByTagName('li '); /I Find <li> elements
if (elements.length> O) {
l;IJiliii
var el = elements[O];
el.className = 'cool';}
```


### SELECTING ELEMENTS USING CSS SELECTORS
##### querySe 1 ector() returns the first element node that matches the CSS-style selector. querySe 1ectorA11 () returns a Nodelist of all of the matches. Both methods take a CSS selector as their only parameter. The CSS selector syntax offers more flexibility and accuracy when selecting an element than just specifying a class name or a tag name, and should also be familiar to front-end web developers who are used to targeting elements using CSS.

```html
II querySel ector() only retur ns the fi rst match
var el = document .querySel ector('li .hot ' };
el .cl assName = ' cool' ;
II querySel ectorAll returns a Nodeli st
just specifying a class name
or a tag name, and should also
be familiar to front-end web
developers who are used to
targeting elements using CSS.
JAVASCRIPT
II The second matching element (the t hird list item) is selected and changed
var el s = document .querySelectorAll('li .hot') ;
els[l] .className = ' cool' ;
```


## 1. WHEN THE PAGE FIRST LOADS

```htmk
<ul>
<li id="one" class="hot">
<em>fresh</em> figs</li>
<li id="two" class="hot">pine nuts</li>
<li id="three" cl ass="hot">honey</li>
<li id="four">balsamic vinegar</li>
</ul>
```


## 2. AFTER THE FIRST SET OF STATEMENTS

```html
<ul>
<li id="one" class=" cool ">
<em>fresh</em> figs</li>
<li id="two" class="hot">pine nuts</li>
<li id="three" class="hot">honey</l i>
<li id="four">balsamic vinegar</li>
</ul>
```


## 3. AFTER THE SECOND SET OF STATEMENTS

```html
<ul>
<li id="one" cl ass=" cool ">
<em>fresh</em> figs</li>
<li id="two" class="hot">pine nuts~/li>
<l i id="three" cl ass=" cool ">honey</l i>
<l i id="four">bal samic vi negar</l i>
</ul>
```
