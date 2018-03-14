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

https://developer.mozilla.org/en-US/docs/Mozilla/Mobile/Viewport_meta_tag


## Creating the Style and Layout with CSS: Defining the Basic Text Styles

```
h1 { margin: 0 0 1em 0; ... }
H2 { margin: 0 0 .5em 0;... }
```

Inside of here we're going to set a margin. Now for the properties I'm going to use shorthand style, which goes in the order of a clock. So the first one is top, right is second, bottom is third, and left is fourth.

Then for the amount of space after an h1 tag, we're going to use 1em. Now by specifying 1em, we're basically saying 1 times the base font, so this will be approximately 16px. Now I say approximately because by defining em's, we're giving the devices a little bit of leeway so that they can render the type based on their individual screen sizes. So fonts will look better across multiple devices if you use em's versus picking specific point or pixel sizes.
