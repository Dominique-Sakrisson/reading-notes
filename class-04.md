# Chapter 4 LINKS notes

### Relative link
A linkg that is within the same folder as the root folder for the project
To link to other pages on your cite specifiy the files path in the href of your `<a>` 

### Absolute link

A link that uses a URL to navigate to a page outside of the project

_On larger projects_ Its a good idea to organize code by placing each file that has to do with a certain page in one directory

### Email Links
Inside of the `<a>` set the `href="mailto:someonesemail@email.com">email somoene</a>`

**opening links in a new window** is also possible by setting a `target="_blank">`

### Linking to a specifici part of the same page or outside page

In order to **link to a specific part of a page** specify an ID that you're linking to
`<a href="#middle">link text </a>` or to a page on another website and a specific part of that page
simply pass the id of the element at the end of the url 

`<a href="http:/www.
htmlandcssbookcom/
#bottom">
`

# Chapter 15 Layout notes
 Z-index can be used with absolute positioned elements the may be blocking other elements from being visible.
 
 
 ### Float
 
 This allows you to take an element out of the normal flow of the page and position it as far left, or right on the page
 
 Issues can arise with floats, that can be solved with the **Clear property**
 
 This property makes it so that no element within the same containing element, should be able to touch the left or right sides of the box. 
 
 _for example_
 
 if `clear: left;` is used that element will rest at the furthest left side of the page because it cannot have the left side touch any other element within its container. The element will keep getting pushed further down the page until there is space to make that happen. 
 **other clear values**
1. left
2. right
3. both
4. none
 
 **All elements in a cointainer having a float can cause problems**
 Browsers may treat the containing element as if it were 0pixels tall
 
 In the past this was fixed by making an empty element with no float value at the end of the container element and added some styling.
 Since its bad practice to have useless elements on the page there is now a better purely CSS option to fix this. **give the overflow property a value of auto and the width property set to 100%.
 
 
 ### Multi Column layouts
 Each column is contained within a div.
 1. Set the `width` of the columns
 1. `float` the columns next to each other
 1. give them `margins` for some spacing
 
 ### Page Sizes
 
 Its a good idea to design pages with a max width somewhere between **960-1000px** to accomodate for the most amount of screens..
 
 As for the height it seems that you should plan to have given the user the information they need to determine if your site is useful to them within the first **570-600px**
 Tell them what the site is about and give them indication there is more content if they scroll down the page.
 
 
 ### A fixed width layout
 Width usually specified in pixels
 ### A liquid layout
 usually uses percentages for size
 **Composition** is the placement of visual elements, how they are organized..
 
 **The 960px wide grid 12 column layout is BOSS**
 
  `@import` can be used with style sheets to link mulitple of them to your html by only specifying one `<link>` to a single file
  
  Inside that file is where the `@import url("tables.css");` goes to bring in even more styles
  
  
  # Chapter 3 Javscript functions,methods,objects
  
  `Function` a grouping of related statements that work together to perform a specific usually repeated task
  Declared function parameteres act like variables inside the function
  
  
  **argument vs parameter**
  Arguments are the actual values that are passed to the function when it is called
  
  Parameters are the words inside of the parenthesis when a function is declared
  **expressions produce a value and can be used where values are expected 
  
  A function put where the interpreter would expect an expression is known as a **function expression** 
  
  In `function expressions` the name is usally ommitted. And is refered to as an **anonymous function**
  
  **Immediately invoked function expressions (IIFE)**
  `var area = (function() {
  var width =3;
  var height = 2; return width * height;
  }());`
  The final full open and closed parenthesis is what tells this function to be called right after declaring it.
  
  These are used for code that only need to run one time.
  other uses include..
  1. As an argument when a function is called (to calculate a value for tha function)
  1. to assign the value of a property to an object
  1. in event handlers and listeners to perform a task when an event happens
  1. to prevent conflicts between two scrips that might use the same variable name
  
  When a variable is saved in the global scope it takes up space in memory longer than it probably should.
  The browser hangs onto all global scope variables as long as teh page is open
  
  Use locally scoped variable as often as possible. 
  
# Pair Programming reading

Pair programming has shown that it may be a tad slower at pushing out code, it has benefits that outweigh the slower speed. First of which being that the code is often of higher quality. When two people are together working on the same feature it seems that `two heads are better than one` the code is usually cleaner, and much more readable since it was built from a collaborative standpoint than the mind of a sole programmer. The two people have a chance to learn from each other as you work through a problem. It improves communication skills for both parties which leads to other benefits down the road.Examples being job interviews and being more fit for a collabortive working environment in the future. 
