# CSS Transforms, Transitions, and Animations

## Transforms
![transform](https://miro.medium.com/max/900/1*_6MfwckxNfQTca9SiG8MdQ.png)
##### With CSS3 came new ways to position and alter elements. Now general layout techniques can be revisited with alternative ways to size, position, and change elements. All of these new techniques are made possible by the transform property. The transform property comes in two different settings, two-dimensional and three-dimensional. Each of these come with their own individual properties and values. Within this lesson we’ll take a look at both two-dimensional and three-dimensional transforms. Generally speaking, browser support for the transform property isn’t great, but it is getting better every day. For the best support vendor prefixes are encouraged, however you may need to download the nightly version of Chrome to see all of these transforms in action.

## Transform Syntax
##### The actual syntax for the transform property is quite simple, including the transform property followed by the value. The value specifies the transform type followed by a specific amount inside parentheses.

```html
div {
  -webkit-transform: scale(1.5);
     -moz-transform: scale(1.5);
       -o-transform: scale(1.5);
          transform: scale(1.5);
}
```

##### Notice how the transform property includes multiple vendor prefixes to gain the best support across all browsers. The un-prefixed declaration comes last to overwrite the prefixed versions, should a browser fully support the transform property. In the interest of brevity, the remainder of this lesson will not include vendor prefixes. They are, however, strongly encouraged for any code in a production environment. Over time we will be able to remove these prefixes, however keeping them in is the safest approach for the time being.

## 2D Transforms
##### Elements may be distorted, or transformed, on both a two-dimensional plane or a three-dimensional plane. Two-dimensional transforms work on the x and y axes, known as horizontal and vertical axes. Three-dimensional transforms work on both the x and y axes, as well as the z axis. These three-dimensional transforms help define not only the length and width of an element, but also the depth. We’ll start by discussing how to transform elements on a two-dimensional plane, and then work our way into three-dimensional transforms.

## 2D Rotate
##### The transform property accepts a handful of different values. The rotate value provides the ability to rotate an element from 0 to 360 degrees. Using a positive value will rotate an element clockwise, and using a negative value will rotate the element counterclockwise. The default point of rotation is the center of the element, 50% 50%, both horizontally and vertically. Later we will discuss how you can change this default point of rotation.

## HTML
```html
<figure class="box-1">Box 1</figure>
<figure class="box-2">Box 2</figure>
```




## CSS

```html
.box-1 {
  transform: rotate(20deg);
}
.box-2 {
  transform: rotate(-55deg);
}
```


## Transitions & Animations
##### One evolution with CSS3 was the ability to write behaviors for transitions and animations. Front end developers have been asking for the ability to design these interactions within HTML and CSS, without the use of JavaScript or Flash, for years. Now their wish has come true. With CSS3 transitions you have the potential to alter the appearance and behavior of an element whenever a state change occurs, such as when it is hovered over, focused on, active, or targeted. Animations within CSS3 allow the appearance and behavior of an element to be altered in multiple keyframes. Transitions provide a change from one state to another, while animations can set multiple points of transition upon different keyframes.

## Transitions
![tans](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_de9072d0847fc84e38ab1fbc6ee8a5f0.png)
##### As mentioned, for a transition to take place, an element must have a change in state, and different styles must be identified for each state. The easiest way for determining styles for different states is by using the :hover, :focus, :active, and :target pseudo-classes. There are four transition related properties in total, including transition-property, transition-duration, transition-timing-function, and transition-delay. Not all of these are required to build a transition, with the first three are the most popular. In the example below the box will change its background color over the course of 1 second in a linear fashion.


```html
.box {
  background: #2db34a;
  transition-property: background;
  transition-duration: 1s;
  transition-timing-function: linear;
}
.box:hover {
  background: #ff7b29;
}
```

## Vendor Prefixes
##### The code above, as with the rest of the code samples in this lesson, are not vendor prefixed. This is intentionally un-prefixed in the interest of keeping the code snippet small and comprehensible. For the best support across all browsers, use vendor prefixes. For reference, the prefixed version of the code above would look like the following.

```html
.box {
    background: #2db34a;
    -webkit-transition-property: background;
       -moz-transition-property: background;
         -o-transition-property: background;
            transition-property: background;
    -webkit-transition-duration: 1s;
       -moz-transition-duration: 1s;
         -o-transition-duration: 1s;
            transition-duration: 1s;
    -webkit-transition-timing-function: linear;
       -moz-transition-timing-function: linear;
         -o-transition-timing-function: linear;
            transition-timing-function: linear;
}
.box:hover {
  background: #ff7b29;
}
```


## Transitional Property
##### The transition-property property determines exactly what properties will be altered in conjunction with the other transitional properties. By default, all of the properties within an element’s different states will be altered upon change. However, only the properties identified within the transition-property value will be affected by any transitions. In the example above, the background property is identified in the transition-property value. Here the background property is the only property that will change over the duration of 1 second in a linear fashion. Any other properties included when changing an element’s state, but not included within the transition-property value, will not receive the transition behaviors as set by the transition-duration or transition-timing-function properties. If multiple properties need to be transitioned they may be comma separated within the transition-property value. Additionally, the keyword value all may be used to transition all properties of an element.

```html
.box {
    background: #2db34a;
    border-radius: 6px
    transition-property: background, border-radius;
    transition-duration: 1s;
    transition-timing-function: linear;
  }
  .box:hover {
    background: #ff7b29;
    border-radius: 50%;
  }
```


## Transition Duration
##### The duration in which a transition takes place is set using the transition-duration property. The value of this property can be set using general timing values, including seconds (s) and milliseconds (ms). These timing values may also come in fractional measurements, .2s for example. When transitioning multiple properties you can set multiple durations, one for each property. As with the transition-property property value, multiple durations can be declared using comma separated values. The order of these values when identifying individual properties and durations does matter. For example, the first property identified within the transition-property property will match up with the first time identified within the transition-duration property, and so forth. If multiple properties are being transitioned with only one duration value declared, that one value will be the duration of all the transitioned properties.

```html
.box {
  background: #2db34a;
  border-radius: 6px;
  transition-property: background, border-radius;
  transition-duration: .2s, 1s;
  transition-timing-function: linear;
}
.box:hover {
  background: #ff7b29;
  border-radius: 50%;
}
```


## 8 SIMPLE CSS3 TRANSITIONS THAT WILL WOW YOUR USERS

##### CSS3 has introduced countless possibilities for UX designers, and the best thing about them is that the coolest parts are really simple to implement. Just a couple of lines of code will give you an awesome transition effect that will excite your users, increase engagement and ultimately, when used well, increase your conversions. What’s more, these effects are hardware accelerated, and a progressive enhancement that you can use right now. Here are 8 really simple effects that will add life to your UI and smiles to your users’ faces. All of these effects (bar one) are controlled with the transition property. So we can see these effects working, we’ll set up a div in an HTML page:

```html
<!DOCTYPE html>
<html>
<head>
    <style type="text/css">
    </style>
</head>
<body>
    <div></div>
</body>
</html>
```


## 1.Fade in
##### Having things fade in is a fairly common request from clients. It’s a great way to emphasize functionality or draw attention to a call to action. Fade in effects are coded in two steps: first, you set the initial state; next, you set the change, for example on hover:

```html
.fade
{
        opacity:0.5;
}
.fade:hover
{
        opacity:1;
}
```

## 2. Change color
##### Animating a change of color used to be unbelievably complex, with all kinds of math involved in calculating separate RGB values and then recombining them. Now, we just set the div’s class to “color” and specify the color we want in our CSS:

```html
.color:hover
{
        background:#53a7ea;
}
```

## 3. Grow & Shrink
##### To grow an element, you used to have to use its width and height, or its padding. But now we can use CSS3’s transform to enlarge. Set your div’s class to “grow” and then add this code to your style block:

```html
.grow:hover
{
        -webkit-transform: scale(1.3);
        -ms-transform: scale(1.3);
        transform: scale(1.3);
}
```


## 4. Rotate elements
##### CSS transforms have a number of different uses, and one of the best is transforming the rotation of an element. Give your div the class “rotate” and add the following to your CSS:

```html
.rotate:hover
{
        -webkit-transform: rotateZ(-30deg);
        -ms-transform: rotateZ(-30deg);
        transform: rotateZ(-30deg);
}
```


## 5. Square to circle
##### A really popular effect at the moment is transitioning a square element into a round one, and vice versa. With CSS, it’s a simple effect to achieve, we just transition the border-radius property. Give your div the class “circle” and add this CSS to your styles:
```html
.circle:hover
{
        border-radius:50%;
}
```

## 6. 3D shadow
##### 3D shadows were frowned upon for a year or so, because they weren’t seen as compatible with flat design, which is of course nonsense, they work fantastically well to give a user feedback on their interactions and work with flat, or fake 3D interfaces. This effect is achieved by adding a box shadow, and then moving the element on the x axis using the transform and translate properties so that it appears to grow out of the screen. Give your div the class “threed” and then add the following code to your CSS:

```html
.threed:hover
{
        box-shadow:
                1px 1px #53a7ea,
                2px 2px #53a7ea,
                3px 3px #53a7ea;
        -webkit-transform: translateX(-3px);
        transform: translateX(-3px);
}
```

## 7. Swing
##### Not all elements use the transition property. We can also create highly complex animations using @keyframes, animation and animation-iteration.In this case, we’ll first define a CSS animation in your styles. You’ll notice that due to implementation issues, we need to use @-webkit-keyframes as well as @keyframes (yes, Internet Explorer really is better than Chrome, in this respect at least).

```html
@-webkit-keyframes swing
{
    15%
    {
        -webkit-transform: translateX(5px);
        transform: translateX(5px);
    }
    30%
    {
        -webkit-transform: translateX(-5px);
       transform: translateX(-5px);
    } 
    50%
    {
        -webkit-transform: translateX(3px);
        transform: translateX(3px);
    }
    65%
    {
        -webkit-transform: translateX(-3px);
        transform: translateX(-3px);
    }
    80%
    {
        -webkit-transform: translateX(2px);
        transform: translateX(2px);
    }
    100%
    {
        -webkit-transform: translateX(0);
        transform: translateX(0);
    }
}
@keyframes swing
{
    15%
    {
        -webkit-transform: translateX(5px);
        transform: translateX(5px);
    }
    30%
    {
        -webkit-transform: translateX(-5px);
        transform: translateX(-5px);
    }
    50%
    {
        -webkit-transform: translateX(3px);
        transform: translateX(3px);
    }
    65%
    {
        -webkit-transform: translateX(-3px);
        transform: translateX(-3px);
    }
    80%
    {
        -webkit-transform: translateX(2px);
        transform: translateX(2px);
    }
    100%
    {
        -webkit-transform: translateX(0);
        transform: translateX(0);
    }
}
```


## 8. Inset border
##### One of the hottest button styles right now is the ghost button; a button with no background and a heavy border. We can of course add a border to an element simply, but that will change the element’s position. We could fix that problem using box sizing, but a far simpler solution is the transition in a border using an inset box shadow.

```html
.border:hover
{
        box-shadow: inset 0 0 0 25px #53a7ea;
}
```

