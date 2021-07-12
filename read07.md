# Hyber Text Markup Language (HTML)
## Tables
### What's a Table?
##### A table represents information in a grid format. Examples of tables include financial reports, TV schedules, and sports results. 

### Basic Table Structure
1. \<table>: The \<table> element is used to create a table. The contents of the table are written out row by row.
3. \<tr>: You indicate the start of each row using the opening <tr> tag. (The tr stands for table row.) It is followed by one or more \<td> elements (one for each cell in that row). At the end of the row you use a closing \</tr> tag.
4.\<td>: Each cell of a table is represented using a \<td> element. (The td stands for table data.) At the end of each cell you use a closing \</td> tag.

```html
<table>
<tr>
<td>15</td>
<td>15</td>
<td>30</td>
</tr>
<tr>
<td>45</td>
<td>60</td>
<td>45</td>
</tr>
<tr>
<td>60</td>
<td>90</td>
<td>90</td>
</tr>
</table>

```

### Table Headings
#### \<th>
##### The \<th> element is used just like the \<td> element but its purpose is to represent the heading for either a column or a row. (The th stands for table heading.) Even if a cell has no content, you should still use a \<td> or \<th> element to represent the presence of an empty cell otherwise the table will not render correctly. (The first cell in the first row of this example shows an empty cell.) Using \<th> elements for headings helps people who use screen readers, improves the ability for search engines to index your pages, and also enables you to control the appearance of tables better when you start to use CSS. You can use the scope attribute on the \<th> element to indicate whether it is a heading for a column or a row. It can take the values: row to indicate a heading for a row or col to indicate a heading for a column. Browsers usually display the content of a \<th> element in bold and in the middle of the cell.

```html
<table>
<tr>
<th></th>
<th scope="col">Saturday</th>
<th scope="col">Sunday</th>
</tr>
<tr>
<th scope="row">Tickets sold:</th>
<td>120</td>
<td>135</td>
</tr>
<tr>
<th scope="row">Total sales:</th>
<td>$600</td>
<td>$675</td>
</tr>
</table>
```
###  Spanning Columns
##### Sometimes you may need the entries in a table to stretch across more than one column. The colspan attribute can be used on a \<th> or \<td> element and indicates how many columns that cell should run across. In the example on the right you can see a timetable with five columns; the first column contains the heading for that row (the day), the remaining four represent one hour time slots. If you look at the table cell that contains the words 'Geography' you will see that the value of the colspan attribute is 2, which indicates that the cell should run across two columns. In the third row, 'Gym' runs across three columns. You can see that the second and third rows have fewer \<td> elements than there are columns. This is because, when a cell extends across more than one column, the \<td> or \<th> cells that would have been in the place of the wider cells are not included in the code.

```html
<table>
<tr>
<th></th>
<th>9am</th>
<th>10am</th>
<th>11am</th>
<th>12am</th>
</tr>
<tr>
<th>Monday</th>
<td colspan="2">Geography</td>
<td>Math</td>
<td>Art</td>
</tr>
<tr>
<th>Tuesday</th>
<td colspan="3">Gym</td>
<td>Home Ec</td>
</tr>
</table>
```
 ## Spanning Rows
 ##### You may also need entries in a table to stretch down across more than one row. The rowspan attribute can be used on a \<th> or \<td> element to indicate how many rows a cell should span down the table. In the example on the left you can see that ABC is showing a movie from 6pm - 8pm, whereas the BBC and CNN channels are both showing two programs during this time period (each of which lasts one hour). If you look at the last \<tr> element, it only contains three elements even though there are four columns in the result below. This is because the movie in then \<tr> element above it uses the rowspan attribute to stretch down and take over the cell below.


```html

<table>
<tr>
<th></th>
<th>ABC</th>
<th>BBC</th>
<th>CNN</th>
</tr>
<tr>
<th>6pm - 7pm</th>
<td rowspan="2">Movie</td>
<td>Comedy</td>
<td>News</td>
</tr>
<tr>
<th>7pm - 8pm</th>
<td>Sport</td>
<td>Current Affairs</td>
</tr>
</table>

```


# JavaScript (JS)
## Functions, Methods, and Objects
### Functions
##### Functions let you group a series of statements together to perform a specific task. If different parts of a script repeat the same task, you can reuse the function (rather than repeating the same set of st atements). 

### A BASIC FUNCTION

## HTML
```html
<!DOCTYPE html>
<html>
<head>
Before the closing </body>
tag, you can see the link to the
JavaScript file. The JavaScript
file starts with a variable used
to hold a new message, and is
followed by a function ca lled
updateMessage().
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

## JavaScript

```html
var msg = 'Sign up to receive our newsletter for 10% off!';
function updateMessage() {
var el = document.getElementByld('message'};
el .textContent = msg;
}
updateMessage(};
```


### CREATING· OBJECTS USING LITERAL NOTATION
##### This example starts by creating an object using litera l notation. This object is called hotel which represents a hotel called Quay with 40 rooms (25 of which have been booked). Next, the content of the page is updated with data from this object. It shows the name of the hotel by accessing the object's name property and the number of vacant rooms using the checkAvail ability() method. To access a property of this object, the object name is followed by a dot (the period symbol) and the name of the property that you want. Similarly, to use the method, you can use the object name followed by the method name. hotel .checkAvailability() If the method needs parameters, you can supply them in the parentheses (just like you can pass arguments to a function). 

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
##### Here you can see another object. Again it is called hote 1, but this time the model represents a different hotel. For a moment, imagine that this is a different page of the same travel website. The Park hotel is larger. It has 120 rooms and 77 of them are booked. The only things changing in the code are the va lues of the hot e 1 object's properties:
- The name of the hotel
- How many rooms it has
- How many rooms are booked
##### The rest of the page works in exactly the same way. The name is shown using the same code. The checkAvai 1 abi l ity() method has not changed and is called in the same way. If this site had 1,000 hotels, the only thing that would need to change would be the three properties of this object. Because we created a model for the hotel using data, the same code can access and display the details for any hotel that follows the same data model. If you had two objects on the same page, you would create each one using the same notation but store them in variables with different names.

