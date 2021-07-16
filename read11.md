# Images
![image](https://lh3.googleusercontent.com/proxy/pGGdeWAA2PcKhEIoextUUBK2VjCkR5d9wmV9JCzWLAmsmCkx8GixI5EqdjcH-agDCIy9g_4lbWUiWD4fnufADP_tx-PTbrHgR3WW7kF3F8U4BZHdV3w)
## Controlling Sizes of images in CSS
##### You can control the size of an image using the width and height properties in CSS, just like you can for any other box. Specifying image sizes helps pages to load more smoothly because the HTML and CSS code will often load before the images, and telling the browser how much space to leave for an image allows it to render the rest of the page without waiting for the image to download. You might think that your site is likely to have images of all different sizes, but a lot of sites use the same sized image across many of their pages. For example, an e-commerce site tends to show product photos at the same size. Or, if your site is designed on a grid, then you might have a selection of image sizes that are commonly used on all pages, such as:
- Small portrait: 220 x 360
- Small landscape: 330 x 210
- Feature photo: 620 x 400
##### Whenever you use consistently sized images across a site, you can use CSS to control the dimensions of the images, instead of putting the dimensions in the HTML.

## HTML
```html
<img src="images/magnolia-large.jpg"
class="large" alt="Magnolia" />
<img src="images/magnolia-medium.jpg"
class="medium" alt="Magnolia" />
<img src="images/magnolia-small.jpg"
class="small" alt="Magnolia" />
```

## CSS
```html
img.large {
width: 500px;
height: 500px;}
img.medium {
width: 250px;
height: 250px;}
img.small {
width: 100px;
height: 100px;}
```


## Aligning images Using CSS
##### float property can be used to move an element to the left or the right of its containing block, allowing text to flow around it. Rather than using the /<img> element's align attribute, web page authors are increasingly using the float property to align images. There are two ways that this is commonly achieved:
1. The float property is added to the class that was created to represent the size of the image (such as the small class in our example).
2. New classes are created with names such as align-left or align-right to align the images to the left or right of the page.

##### These class names are used in addition to classes that indicate the size of the image. In this example you can see the align-left and align-right classes used to align the image. It is also common to add a margin to the image to ensure that the text does not touch their edges.

## HTML
```html
<p><img src="images/magnolia-medium.jpg"
alt="Magnolia" class="align-left medium" />
<b><i>Magnolia</i></b> is a large genus that
contains over 200 flowering plant species...</p>
<p><img src="images/magnolia-medium.jpg"
alt="Magnolia" class="align-right medium" />
Some magnolias, such as <i>Magnolia stellata</i>
and <i>Magnolia soulangeana</i>, flower quite
early in the spring before the leaves open...</p>
```

## CSS 
```html
img.align-left {
float: left;
margin-right: 10px;}
img.align-right {
float: right;
margin-left: 10px;}
img.medium {
width: 250px;
height: 250px;}
```


## Centering images Using CSS
##### By default, images are inline elements. This means that they flow within the surrounding text. In order to center an image, it should be turned into a blocklevel element using the display property with a value of block. Once it has been made into a block-level element, there are two common ways in which you can horizontally center an image:
1. On the containing element, you can use the text-align property with a value of center.
2. On the image itself, you can use the use the margin property and set the values of the left and right margins to auto.
##### You can specify class names that allow any element to be centered, in the same way that you can for the dimensions or alignment of images. The techniques for specifying image size and alignment of images can also be used with the HTML5 \<figure> element.

## HTML
```html
<p><img src="images/magnolia-medium.jpg"
alt="Magnolia" class="align-center medium" />
<b><i>Magnolia</i></b> is a large genus that
contains over 200 flowering plant species. It
is named after French botanist Pierre Magnol and,
having evolved before bees appeared, the
flowers were developed to encourage pollination
by beetle.</p>

```

## CSS 
```html
img.align-center {
display: block;
margin: 0px auto;}
img.medium {
width: 250px;
height: 250px;}
```

# Practical Information
## Where Are Your Visitors Coming From?
##### The traffic sources link on the left hand side allows you to learn where your visitors are coming from.

1. Referrers: This shows the sites that have linked to you and the number of people who have come via those sites. If a site sends a lot of traffic to you, get in touch and try to work together to ensure that traffic keeps flowing. You could also try to find similar sites and ask them to link to you.
2. Direct: This shows which page a user arrived on if they did not come via a link on another site. They might have typed the URL into their browser, used a browser bookmark, or clicked a link in an email, PDF, or Word document.
3. Search Terms: This shows the terms users entered into a search engine to find your site. This can help you learn how visitors describe what they're looking for (which is often different to how someone might describe their own site). This can help you fine-tune your content and your SEO keywords.
4. Advanced Features We have only scratched the surface of what you can find out about your visitors from Google Analytics. Their help files tell you many more of the advanced features. If you run an online shop, it is well worth looking at their e-commerce tracking, which adds information about products sold, average basket size and much more. You can also set up goals where you specify the paths you want people to take, and then see how far they get through those paths, which is especially useful when gathering data from users.

## FTP & Third Party Tools
![FTp](https://cdn.educba.com/academy/wp-content/uploads/2019/12/what-is-ftp-server-1.png)
##### To transfer your code and images from your computer to your hosting company, you use something known as File Transfer Protocol. As the name suggests, File Transfer Protocol (or FTP) allows you to transfer files across the Internet from your computer to the web server hosting your site. There are many FTP programs that offer a simple interface that shows you the files on your computer alongside the files that are on your web server. These allow you to drag and drop files from your computer to the server or vice versa.
