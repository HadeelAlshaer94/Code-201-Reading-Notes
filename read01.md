# Hyber Text Markup Language (HTML)

### Introduction 
###### When you are looking at a website, it is most likely that your browser will be receiving HTML and CSS from the web server that hosts the site. The web browser interprets the HTML and CSS code to create the page that you see. Most web pages also include extra content such as images, audio, video, or animations and this book will teach you how to prepare them for use on the web and then how to insert them into your web pages. Some sites also send JavaScript or Flash to your browser, and you will see how to add JavaScript and Flash in your web pages. Both of these technologies are advanced topics that you can go on to learn more about once you have mastered HTML and CSS, if you want to. Larger websites — in particular those that are updated regularly and use a content management system (CMS), blogging tools, or e-commerce software — often make use of more complex technologies on the web server, but these technologies are actually used to produce HTML and CSS that is then sent to the browser. So, if your site uses these technologies, you will be able to use your new HTML and CSS knowledge to take more control over how your site looks. Larger, more complex sites like these may use a database to store data, and programming languages such as PHP, ASP.Net, Java, or Ruby on the web server, but you do not need to know these technologies to improve what the user sees. The skills you'll learn in this book should be enough to help you on that road.

### Structure
###### The structure is very similar when a news story is viewed online (although it may also feature audio or video). This is illustrated on the right with a copy of a newspaper alongside the corresponding article on its website. In the browser window you can see a web page that features exactly the same content as the Word document you met on the page 18. To describe the structure of a web page, we add code to the words we want to appear on the page. You can see the HTML code for this page below. Don't worry about what the code means yet. We start to look at it in more detail on the next page. Note that the HTML code is in blue, and the text you see on screen is in black.


```html
<html>
  <body>
     <h1>This is the Main Heading</h1>
     <p>This text might be an introduction to the rest of the page. And if the page is a long one it might be split up into several sub-headings.<p>
     <h2>This is a Sub-Heading</h2>
     <p>Many long articles have sub-headings so to help you follow the structure of what is being written.There may even be sub-sub-headings (or lower-level headings).</p>
     <h2>Another Sub-Heading</h2>
     <p>Here you can see another sub-heading.</p>
  </body>
</html>
```




### Extra Markup
###### There have also been several versions of each browser used to view web pages, each of which implements new code. Not all web users, however, have the latest browsers installed on their computers, which means that not everyone will be able to view all of the latest features and markup. Where you should be particularly aware of browsers not supporting certain features, I have made a note of this (as you have seen with some of the HTML5 elements. One of the key benefits of this change was that XHTML works seamlessly with other programs that are written to create and process XML documents. It could also be used with other data formats such as Scalable Vector Graphics (SVG) — a graphical language written in XML, MathML (used to mark up mathematical formulae), and CML (used to mark up chemical formulae).

#### DOCTYPEs
###### Because there have been several versions of HTML, each web page should begin with a DOCTYPE declaration to tell a browser which version of HTML the page is using (although browsers usually display the page even if it is not included). We will therefore be including one in each example for the rest of the book. As you will see when we come to look at CSS and its box model on page 316, the use of a DOCTYPE can also help the browser to render a page correctly. Because XHTML was written in XML, you will sometimes see pages that use the XHTML strict DOCTYPE start with the optional XML declaration. Where this is used, it should be the first thing in a document. There must be nothing before it, not even a space.

#### HTML5
```html
<!DOCTYPE html>

```
#### HTML4
```html
<!DOCTYPE html PUBLIC
"-//W3C//DTD HTML 4.01 Transitional//EN"
"http://www.w3.org/TR/html4/loose.dtd">
```

#### Transitional XHTML 1.0

```html
<!DOCTYPE html PUBLIC
"-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/
xhtml1-transitional.dtd">

```

#### Strict XHTML 1.0

```html
<!DOCTYPE html PUBLIC
"-//W3C//DTD XHTML 1.0 Strict//EN"
"http://www.w3.org/TR/xhtml1/DTD/
xhtml1-strict.dtd">

```

#### XML Declaration

```html
<?xml version="1.0" ?>

```

### HTML5 Layout
#### Traditional HTML Layouts
###### On the right you can see a layout that is quite common (particularly on blog sites). At the top of the page is the header, containing a logo and the primary navigation. Under this are one or more articles or posts. Sometimes these are summaries that link to individual posts. There is a side bar on the righthand side (perhaps featuring a search option, links to other recent articles, other sections of the site, or even ads). When coding a site like this, developers would usually put these main sections of the page inside div elements and use the class or id attributes to indicate the purpose of that part of the page.

![Traditional](https://csharpcorner-mindcrackerinc.netdna-ssl.com/UploadFile/b5be7f/working-with-new-semantic-elements-in-html5-along-with-html/Images/Html%20Basic%20Structure%20Image.png)


#### New Html 5 Layout Elements
###### This example has exactly the same structure as seen on the previous page. However, many of the div elements have been replaced by new HTML5 layout elements. For example, the header sits inside a new header element, the navigation in a nav element, and the articles are in individual article elements. The point of creating these new elements is so that web page authors can use them to help describe the structure of the page. For example, screen reader software might allow users to ignore headers and footers and get straight to the content. Similarly, search engines might place more weight on the content in an article element than that in the header or  footer elements. I think you will agree that it also makes the code easier to follow.

![New](https://slideplayer.com/slide/12052583/69/images/8/NEW+HTML5+LAYOUT+ELEMENTS.jpg)

### Process & Design
#### Visual Hierarchy
###### Attention is immediately drawnto a picture that shows the service this company offers and a headline to explain it. The size and colored background reinforce that this is the primary message on the page. Should this service appeal to the user, below they can see more detail about what it does, how much it costs, and who uses it.


#### Similarity
###### There are several examples of similarity within this page. The four points (at the bottom left of the screenshot) are all presented in a similar manner with consistent headings and icons. All of the links in the body text are in blue so it is clear what text is clickable.


#### Grouping
###### There are several chunks of information on this page. At the top you can see the logo and navigation. Under this is the information that introduces the company's services. Further down are three distinct groups showing you what the services do, the costs involved and some of the services' users.




# Javascript Language (JS)

### Introduction
###### S, is a programming language that conforms to the ECMAScript specification. JavaScript is high-level, often just-in-time compiled, and multi-paradigm. It has curly-bracket syntax, dynamic typing, prototype-based object-orientation, and first-class functions. Alongside HTML and CSS, JavaScript is one of the core technologies of the World Wide Web. Over 97% of websites use it client-side for web page behavior, often incorporating third-party libraries.[12] All major web browsers have a dedicated JavaScript engine to execute the code on the user's device. As a multi-paradigm language, JavaScript supports event-driven, functional, and imperative programming styles. It has application programming interfaces (APIs) for working with text, dates, regular expressions, standard data structures, and the Document Object Model (DOM). The ECMAScript standard does not include any input/output (I/O), such as networking, storage, or graphics facilities. In practice, the web browser or other runtime system provides JavaScript APIs for I/O.


### The ABC of Programming
###### Before you learn how to read and write the JavaScript language itself, you need to become familiar with some key concepts in computer programming. They will be covered in three sections:
![ABC](https://res.cloudinary.com/practicaldev/image/fetch/s--1LH1zbno--/c_imagga_scale,f_auto,fl_progressive,h_900,q_auto,w_1600/https://dev-to-uploads.s3.amazonaws.com/i/84jmz6dsrpggzfb6ffyr.png)

### A: 
###### What is a script and how do I create one?

### B:
###### How do computers fit in with the world around them?

### C:
###### How do I write a script for a web page?


### Apply().,
```html
const student = {
    name: "Rahul", 
    showName: function(friend1, friend2){
        console.log(this.name); 
        console.log(friend1); 
        console.log(friend2); 
    }
}

student.showName.apply({name: "Rahul" },["John", "Jane"]); 

```



### Bind().,
```html
const student = {
    name: "Rahul", 
    showName: function(){
        console.log(this.name); 
    }
}

const greetStudent = student.showName({
    name: "Rahul from Bind"
}) 

greetStudent(); // Rahul from Bind
```



### Call().,
```html
const student = {
    name: "Rahul", 
    showName: function(friend1, friend2){
        console.log(this.name); 
        console.log(friend1); 
        console.log(friend2); 
    }
}

student.showName.call({name: "Rahul" },"John", "Jane"); 

```
