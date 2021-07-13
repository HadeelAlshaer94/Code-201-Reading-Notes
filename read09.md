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









# Lists, Tables & Forms













# Events
