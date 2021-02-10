## Responsive Web Design

This covered the use of media queries to set css content based off of the width of the current view or screen size.
There are logical statements that can and ideally are used in combination to properly format your site based off screen size

in the css file
`@media all and (min-width: 400px) and (max-width: 600px){}`

The parts of this query are, the call, the type of device or screen, the logical statements and their values

- There are many different types of screen or device selectors not mentioned here. 
- The exact size for the min max is ultimately up to the developer
- Inside the curly braces is where one would put their css identifiers and rule, key value pairs

## All About floats

Floats keep the element floated in the flow of the page unlike certain positioning values
Setting an element css `clear: both;` will not bunch it up with floated elements that are floated left and right. It inside will sit below the lowest point of a floated element

To summarize this article, there 3 pretty simple ways to clearing floats. The empty div method which is making a div, placing it between the float and whatever else and styling it to clear both 
The overflow method- setting the overflow to a parent element to hidden the parent will expand to contain floats. It benefit is its very semantic.
THe easy clearing method- give a parent a class and prefix it with `:after` and rules `content: '.'; visibility: 'hidden'; display: block; height: 0; clear: both;`

## Dont overthink grids
This article went over a basica grid layout involving two divs. One has a width of 2/3 the other a width of 1/3. Float the 2/3 to the left while floating the 1/3 to the right. Their parent div will now collapse due to the childs being both floated. Apply a style to the parent div with the :after to add a rule `clear: both;` And thats about it.

## CSS floats explained
This article put floats into human on an escalator terms regarding how floats work and allow other elements to fill in the gaps between floats until a clear property is set and the elements after the clear will no longer fill in between the floated elements. 
