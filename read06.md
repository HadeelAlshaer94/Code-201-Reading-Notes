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
