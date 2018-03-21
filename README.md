# Creating a Responsive Web Design Web


## Preparing the HTML Content and Structure - Setting up Your Project

`<meta name="viewport" content="width=device-width, initial-scale=1">`

We have a meta tag with a name of viewport. What this particular tag does by defining width as device-width
and initial-scale, this is tag that will tell individual devices not to scale the web page, but rather to use
the initial scale of 1, meaning if we're on a device that has 700 pixels across, it will render the page as
if there's only 700 pixels, allowing the rest of the HTML to move around. The device will not attempt to show
the entire web page and scale it down. And if we didn't have this particular tag in here, every device would
try to render the entire web page and we would have to zoom up. So again, the idea here is we're going
to make the page respond to the individual devices and adjust the layouts so the users don't have
to zoom in on the content.

See [Viewport meta tag](https://developer.mozilla.org/en-US/docs/Mozilla/Mobile/Viewport_meta_tag)


## Creating the Style and Layout with CSS: Defining the Basic Text Styles

```
h1 { margin: 0 0 1em 0; ... }
H2 { margin: 0 0 .5em 0;... }
```

Inside of here we're going to set a margin. Now for the properties I'm going to use shorthand style, which goes in the order of a clock. So the first one is top, right is second, bottom is third, and left is fourth.

Then for the amount of space after an h1 tag, we're going to use 1em. Now by specifying 1em, we're basically saying 1 times the base font, so this will be approximately 16px. Now I say approximately because by defining em's, we're giving the devices a little bit of leeway so that they can render the type based on their individual screen sizes. So fonts will look better across multiple devices if you use em's versus picking specific point or pixel sizes.

## Creating the Style and Layout with CSS: Style the Heading and Page Container

```
header { height: 430px; background: #cf0004 url(../images/banner_1200.jpg) no-repeat center bottom; position: relative; }
```
Then the last property we're going to set is going to be position. We'll set a position value of relative. What this position property will do is make sure that any items that are positioned inside of the header element will be positioned in relation to the header element itself. 

```
#page { max-width: 1200px; margin: 0 auto; position: relative; }
```

`position: relative`: This means any items positioned inside of the page element will be positioned in relation to this. Now this will become important later one because we're going to reposition the navigation element, and the navigation is not inside of the header, which also has a position relative, so the navigation will position in relation to the page

Take a look at this example [CSS Positioning - Relative Positioning](https://codepen.io/jalanya/pen/pLEzJJ)


## Creating the Style and Layout with CSS: Style the Logo and Hero Item

```
header a.logo {
  position: absolute;
  display: block;
  width: 160px;
  height: 66px;
  background: url(../images/logo.svg) no-repeat 0 0;
  background-size: contain;
  top: 15px;
  left: 20px;
}
```

We're going to set a property called `background-size`. We're going to set this to `contain`. This means the background graphic is going to be sized to fit within the height and width, and since we set the height and width to a proportion based on the size of the logo.svg, which is 160 x 66, this will proportionally scale and fill the entire element with the logo. 

[background-size](https://developer.mozilla.org/en-US/docs/Web/CSS/background-size)

## Creating the Style and Layout with CSS: Creating the Button Style

[transition](https://developer.mozilla.org/en-US/docs/Web/CSS/transition) |
[Using CSS transation](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions)


### **Functional notation**: **rgb(R, G, B[, A])** or **rgba(R, G, B, A)**
R (red), G (green), and B (blue) can be either `<integer>`s or `<percentage>`s, where the number 255 corresponds to 100%. A (alpha) can be a `<number>` between 0 and 1, or a `<percentage>`, where the number 1 corresponds to 100% (full opacity).

```
/* Functional syntax */
rgba(51, 170, 51, .1)    /*  10% opaque green */ 
rgba(51, 170, 51, .4)    /*  40% opaque green */ 
rgba(51, 170, 51, .7)    /*  70% opaque green */ 
rgba(51, 170, 51,  1)    /* full opaque green */ 
```


## Creating a Menu System with CSS: Clearing Floats with CSS Pseudo-elements

The section of main is not going down to extend around all of the items that are floating inside of it, because whenever we float or position an element, the parent container will not extend to the height or width of the items inside.

So what we need to do is have another HTML element in the page with a clear property so that the parent item will clear all of the floating items, but I don't want to add any HTML to our page; I only want the HTML to be as minimal as possible and only relate to the content. So we can use something called a pseudo-element inside of CSS to add a phantom HTML element to our sections

```section::after { content: ''; display: block; clear: both; }```

[Pseudo-elements](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements) | [::after (:after)](https://developer.mozilla.org/en-US/docs/Web/CSS/::after) 
