# Forms
![form](https://www.sliderrevolution.com/wp-content/uploads/2021/03/form-header1.jpg)


## Form Structure
##### Form controls live inside a \<form> element. This element should always carry the action attribute and will usually have a method and id attribute too.
### Action
##### Every \<form> element requires an action attribute. Its value is the URL for the page on the server that will receive the information in the form when it is submitted.
### Method
##### Forms can be sent using one of two methods: get or post. With the get method, the values from the form are added to the end of the URL specified in the action attribute. The get method is ideal for:
- short forms (such as search boxes).
- when you are just retrieving data from the web server (not sending information that should be added to or deleted from a database).

### Form Structure
##### With the post method the values are sent in what are known as HTTP headers. As a rule of thumb you should use the post method if your form:
- allows users to upload a file.
- is very long.
- contains sensitive data (e.g. passwords).
- adds information to, or deletes information from, a database
##### If the method attribute is not used, the form data will be sent using the get method.
### id: 
##### We look at the id attribute, but the value is used to identify the form distinctly from other elements on the page (and is often used by scripts — such as those that check you have entered information into fields hat require values).


```html
<form action="http://www.example.com/subscribe.php"
method="get">
<p>This is where the form controls will appear.
</p>
</form>
```

## Text Input
##### The \<input> element is used to create several different form controls. The value of the type attribute determines what kind of input they will be creating. When the type attribute has a value of text, it creates a singleline text input.
### Name:
##### When users enter information into a form, the server needs to know which form control each piece of data was entered into. (For example, in a login form, the server needs to know what has been entered as the username and what has been given as the password.) Therefore, each form control requires a name attribute. The value of this attribute identifies the form control and is sent along with the information they enter to the server.
### Maxlength:
##### You can use the maxlength attribute to limit the number of characters a user may enter into the text field. Its value is the number of characters they may enter. For example, if you were asking for a year, the maxlength attribute could have a value of 4.

```html
<form action="http://www.example.com/login.php">
<p>Username:
<input type="text" name="username" size="15"
maxlength="30" />
</p>
</form>
```


## Password Input
##### When the type attribute has a value of password it creates a text box that acts just like a single-line text input, except the characters are blocked out. They are hidden in this way so that if someone is looking over the user's shoulder, they cannot see sensitive data such as passwords.
### Name:
##### The name attribute indicates the name of the password input, which is sent to the server with the password the user enters.
### Size, maxlength:
##### It can also carry the size and maxlength attributes like the the single-line text input.

```html
<form action="http://www.example.com/login.php">
<p>Username:
<input type="text" name="username" size="15"
maxlength="30" />
</p>
<p>Password:
<input type="password" name="password" size="15"
maxlength="30" />
</p>
</form>
```


## Image For Bullets list-style-image
##### You can specify an image to act as a bullet point using the list-style-image property. The value starts with the letters url and is followed by a pair of parentheses. Inside the parentheses, the path to the image is given inside double quotes. This property can be used on rules that apply to the \<ul> and \<li> elements. The example on this page also shows the use of the margin property to increase the vertical gap between each item in the list.

## HTML:
```html
<h1>Index of Translated Poems</h1>
<h2>Arthur Rimbaud</h2>
<ul>
<li>Ophelia</li>
<li>To Music</li>
<li>A Dream for Winter</li>
<li>Vowels</li>
<li>The Drunken Boat</li>
</ul>

```

## CSS
```html
ul {
list-style-image: url("images/star.png");}
li {
margin: 10px 0px 0px 0px;}

```

## Table Properties
##### You have already met several properties that are commonly used with tables. Here we will put them together in a single example using the following: 
- width: to set the width of the table.
- padding: to set the space between the border of each table cell and its content.
-  text-transform to convert the content of the table headers to uppercase
-  letter-spacing, font-size to add additional styling to the content of the table headers.
-  border-top, border-bottom to set borders above and below the table headers.
-  text-align to align the writing to the left of some table cells and to the right of the others.
-  background-color to change the background color of the alternating table rows.
-  hover to highlight a table row when a user's mouse goes over it.

```html
<h1>First Edition Auctions</h1>
<table>
<tr>
<th>Author</th>
<th>Title</th>
<th class="money">Reserve Price</th>
<th class="money">Current Bid</th>
</tr>
<tr>
<td>E.E. Cummings</td>
<td>Tulips & Chimneys</td>
<td class="money">$2,000.00</td>
<td class="money">$2,642.50</td>
</tr>
<tr class="even">
<td>Charles d'Orleans</td>
<td>Poemes</td>
<td class="money"></td>
<td class="money">$5,866.00</td>
</tr>
<tr>
<td>T.S. Eliot</td>
<td>Poems 1909 - 1925</td>
<td class="money">$1,250.00</td>
<td class="money">$8,499.35</td>
</tr>
<tr class="even">
<td>Sylvia Plath</td>
<td>The Colossus</td>
<td class="money"></td>
<td class="money">$1031.72</td>
</tr>
</table>

```



# Events

## USING DOM EVENT HANDLERS
##### the event handler appears on the last line of the JavaScript. Before the DOM event handler, two things are put in place: 
1. If you use a named function when the event fires on your chosen DOM node, write that function first. (You could also use an anonymous function).
2. The DOM element node is stored in a variable. Here the text input (whose id attribute has a va lue of username) is placed into a variable called e 1 Username.
3. On the last line of the code sample above, the event handler e 1 Username. 

##### This is followed by an equal sign, then the name of the function that will run when the event fires on that element. Note that there are no parentheses on the function name. This means you cannot pass arguments to this function. The HTML is the same, but without the onb 1 ur event attribute. This means that. the event handler is in the JavaScript, not the HTML. Browser support: On line 3, the checkUsername() function uses the this keyword in the conditional statement to check the number of characters the user entered. It works in most browsers because they know this refers to the element the event happened on. However, in Internet Explorer 8 or earlier, IE would treat this as the wi ndow object. As a result, it would not know which element the event occurred on and there would be no value bthat it checked the length of, soit would raise an error.

```html
function checkUsername() {
var elMsg = document .get El ementByld('feedback');
if (this .value .l ength< 5) {
elMsg . textContent 'Username mus t be 5 charact ers
else {
elMsg.textContent = '';
@) var elUsername = document. getElementByld('username') ; II Get username input
G) elUsername.onblur = checkUsername; II When it l oses focus call checkuserName()
```


## USING EVENT LISTENERS

##### the event listener appears on the last line of the JavaScript. Before you write an event listener, two things are put in place: 
1. If you use a named function when the event fi res on your chosen DOM node, write that function first. (You could also use an anonymous function.)
2. The DOM element node(s) is stored in a variable. Here the text input (whose id attribute has a value of username) is placed into a variable called el Username.

```html
function chec kUsername( ) {
var elMsg = document .get ElementByld('feedback');
i f (t hi s .value.length< 5) {
elMsg .text Content 'Username must be 5 characters
else {
el Msg .textContent I I, ,
~ var elUsername = document .get El ementByld(' username') ; II Get username i nput
II When i t loses focus call checkUsername()
elUsername.addEventlistener('blur' , checkUsername , false) ;
```

