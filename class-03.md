# chapter 13 _Boxes_ notes

By default a box with no content will have no size
Boxes will be built to fix the content; bigger or smaller if specified

Some CSS properties

 **min width, max-width**
 
 use the property and set the value (%, px, etc)

 **min-height, max-height**
 
 use the property and set the value (%, px, etc)


 
 **overflow**
 
 tells the browser what to do if the contents of a box are more than the box itself
 
 **scroll**

adds a scrollbar to the box to zoom through content

### Different border styles
1. `solid`
2. `dotted`
1. `dashed`
1. `double`
1. `groove` carved into the page
1. `ridge` pops outt of the page
1. `inset` appears embedded
1. `outset`
1. `hidden/none`

## border image!!

**border image takes in values where to make makrs on the image to create slices of the image. the corners of the image are always in the corners of the element, however the edges can be manipulated

**p.one {**

-moz-border-image: url("images/dots.gif")
 11 11 11 11 stretch;

-webkit-border-image: url("images/dots.gif")
 11 11 11 11 stretch;

border-image: url("images/dots.gif")
 11 11 11 11 stretch;}


**p.two {**

-moz-border-image: url("images/dots.gif")
 11 11 11 11 round;

-webkit-border-image: url("images/dots.gif")
 11 11 11 11 round;

border-image: url("images/dots.gif")
 11 11 11 11 round;}`

**these are the different options for border image**

**stretch**

**repeat**
 
**round**

## Box shadows
**`p.one {**

-moz-box-shadow: -5px -5px #777777;

-webkit-box-shadow: -5px -5px #777777;

box-shadow: -5px -5px #777777;}

**.two {**

-moz-box-shadow: 5px 5px 5px #777777;

-webkit-box-shadow: 5px 5px 5px #777777;

box-shadow: 5px 5px 5px #777777;}

**p.three {**

-moz-box-shadow: 5px 5px 5px 5px #777777;

-webkit-box-shadow: 5px 5px 5px 5px #777777;

box-shadow: 5px 5px 5px 5px #777777;}

**p.four {**

-moz-box-shadow: 0 0 10px #777777;

-webkit-box-shadow: 0 0 10px #777777;

box-shadow: 0 0 10px #777777;}

**p.five {**

-moz-box-shadow: inset 0 0 10px #777777;

-webkit-box-shadow: inset 0 0 10px #777777;

box-shadow: inset 0 0 10px #777777;} 


## Elliptical shapes
### border radius

If you supply border radius with a second measurement its like passing a height and a width adjustment

p.one {

border-top-left-radius: 80px 50px;

-moz-border-radius-top-left: 80px 50px;

-webkit-border-radius-top-left: 80px 50px;}

p.two {

border-radius: 1em 4em 1em 4em / 2em 1em 2em 1em;

-moz-border-radius: 1em 4em 1em 4em
 / 2em 1em 2em 1em;

-webkit-border-radius: 1em 4em 1em 4em
 / 2em 1em 2em 1em;}

p.three {

padding: 0px;

border-radius: 100px;

-moz-border-radius: 100px;

-webkit-border-radius: 100px;}


## switch statements
starts with switch then you have parenthesis with a variable or function, for whatever the value, it is tested against each case to determine the next direction the program takes. If no case matches there is a **default** case that must be returned 

each **case** has to have a **break;** keyword at the end.. has to break out of the switch somehow

## type coercion
this is when javascript converts data types automatically in attempts to complete the operation.
This will create unexpected results

**weak** typing is what javascript uses because it does type coercion

other languages that dont use it are referred to ass **strong typing**

This sort of thing is why we use strict comparison operators, it forces the need for types to be the same as well

This also opens the doors for every value in javascript to be either truthy or falsey


## Loops
The counters of a loop
1. initialization x=10;
1. condition    x<0
1. update   x--

A couple loop keywords

1. break 

exits out of the current loop 

2. continue

interpreter to continue with current iteration, check condition if true it runs again.

for loops are ideal for work that you know how many times you will need to perform the task

## while loops

more ideal for iteration when needed to do for an unknown number of times

### do while loop
slightly different than the while loop in that youre saying no matter what, DO this first, then do it until the condition is met.
