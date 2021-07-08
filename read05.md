
# Hyber Text Markup Language (HTML)
## Images
### Adding Images
##### To add an image into the page you need to use an <img> element. This is an empty element (which means there is no closing tag). It must carry the following two attributes:
- src: This tells the browser where it can find the image file. This will usually be a relative URL pointing to an image on your own site. (Here you can see that the images are in a child folder called images.
- alt: This provides a text description of the image which describes the image if you cannot see it. 
- title:  You can also use the title attribute with the \<img> element to provide additional information about the image. Most browsers will display the content of this attribute in a tootip when the user hovers over the image.

```html
<img src="images/quokka.jpg" alt="A family of
quokka" title="The quokka is an Australian
marsupial that is similar in size to the
domestic cat." />
```

### Height & Width of Images
##### You will also often see an \<img> element use two other attributes that specify its size:
- height: This specifies the height of the image in pixels.
- width: This specifies the width of the image in pixels.
##### Images often take longer to load than the HTML code that makes up the rest of the page. It is, therefore, a good idea to specify the size of the image so that the browser can render the rest of the text on the page while leaving the right amount of space for the image that is still loading.

```html
<img src="images/quokka.jpg" alt="A family of
quokka" width="600" height="450" />

```

### Where to Place Images in Your Code
##### Where an image is placed in the code will affect how it is displayed. Here are three examples of image placement that produce different results:
1. before a paragraph The paragraph starts on a new line after the image.
2. inside the start of a paragraph The first row of text aligns with the bottom of the image.
3. in the middle of a paragraph The image is placed between the words of the paragraph that it appears in.

```html
<img src="images/bird.gif" alt="Bird" width="100"
height="100" />
<p>There are around 10,000 living species of birds
that inhabit different ecosystems from the
Arctic to the Antarctic. Many species undertake
long distance annual migrations, and many more
perform shorter irregular journeys.</p>
<hr />
<p><img src="images/bird.gif" alt="Bird" width="100"
height="100" />There are around 10,000 living
species of birds that inhabit different
ecosystems from the Arctic to the Antarctic. Many
species undertake long distance annual
migrations, and many more perform shorter
irregular journeys.</p>
<hr />
<p>There are around 10,000 living species of birds
that inhabit different ecosystems from the
Arctic to the Antarctic.<img
src="images/bird.gif" alt="Bird" width="100"
height="100" />Many species undertake long
distance annual migrations, and many more perform
shorter irregular journeys.</p>
```


## Old Code: Aligning Images Horizontally
###### The align attribute was commonly used to indicate how the other parts of a page should flow around an image. It has been removed from HTML5 and new websites should use CSS to control the alignment of images. I have discussed it here because you are likely to come across it if you look at older code, and because some visual editors still insert this attribute when you indicate how an image should be aligned. The align attribute can take these horizontal values: 
- left: This aligns the image to the left (allowing text to flow around its right-hand side).
- right: This aligns the image to the right (allowing text to flow around its left-hand side).

```html
<p><img src="images/bird.gif" alt="Bird" width="100"
height="100" align="left" />There are around
10,000 living species of birds that inhabit
different ecosystems from the Arctic to the
Antarctic. Many species undertake long distance
annual migrations, and many more perform shorter
irregular journeys.</p>
<hr />
<p><img src="images/bird.gif" alt="Bird" width="100"
height="100" align="right" />There are around
10,000 living species of birds that inhabit
different ecosystems from the Arctic to the
Antarctic. Many species undertake long distance
annual migrations, and many more perform shorter
irregular journeys.</p>

```



## Color
### Foreground Color
##### The color property allows you to specify the color of text inside an element. You can specify any color in CSS in one of three ways:
- rgb values: These express colors in terms of how much red, green and blue are used to make it up. For example: rgb(100,100,90)
- hex codes: These are six-digit codes that represent the amount of red, green and blue in a color, preceded by a pound or hash # sign. For example: #ee3e80
- color names: There are 147 predefined color names that are recognized by browsers. For example: DarkCyan.

```html
/* color name */
h1 {
color: DarkCyan;}
/* hex code */
h2 {
color: #ee3e80;}
/* rgb value */
p {
color: rgb(100,100,90);}

```

### Background Color background-color
##### CSS treats each HTML element as if it appears in a box, and the background-color property sets the color of the background for that box. You can specify your choice of background color in the same three ways you can specify foreground colors: RGB values, hex codes, and color names (covered on the next page). If you do not specify a background color, then the background is transparent. By default, most browser windows have a white background, but browser users can set a background color for their windows, so if you want to be sure that the background is white you can use the background-color property on the \<body> element.

```html
body {
background-color: rgb(200,200,200);}
h1 {
background-color: DarkCyan;}
h2 {
background-color: #ee3e80;}
p {
background-color: white;}
```


## Text
### Specifying Typefaces font-family
##### The font-family property allows you to specify the typeface that should be used for any text inside the element(s) to which a CSS rule applies. The value of this property is the name of the typeface you want to use. The people who are visiting your site need the typeface you have specified installed on their computer in order for it to be displayed. You can specify a list of fonts separated by commas so that, if the user does not have your first choice of typeface installed, the browser can try to use an alternative font from the list. It is also common to end with a generic font name for that type of font.

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
##### The font-size property enables you to specify a size for the font. There are several ways to specify the size of a font. The most common are: 
- Pixels: Pixels are commonly used because they allow web designers very precise control over how much space their text takes up. The number of pixels is followed by the letters px. 
- percentages: The default size of text in browsers is 16px. So a size of 75% would be the equivalent of 12px, and 200% would be 32px. If you create a rule to make all text inside the \<body> element to be 75% of the default size (to make it 12px), and then specify another rule that indicates the content of an element inside the \<body> element should be 75% size, it will be 9px (75% of the 12px font size).
- ems: An em is equivalent to the width of a letter m.

