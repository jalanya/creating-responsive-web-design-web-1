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
