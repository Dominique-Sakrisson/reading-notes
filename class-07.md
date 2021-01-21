# Domain Modeling 
Has to deal with properly 'sketching out' the problem domain. Having a structured approach will help make the problem domain clear. 

We're modelling with objects, in order to do so they must be made a constructor and at somepoint instantiated with the `new` keyword 
Object prototype are basically outlaying the structure the objects takes, onces it instantiated it actually makes an object with values for those prototype methods, properties


# Chapter 6 HTML tables
  tables have some basic structure including `<table> <tr> <th> <td>`
  
  
 `colspan='2'` will make a <td> span multiple columns across the table
 `rowSpan='2'` similarly work the same way but with rows
 
 #### Some more tags for tables `<thead> <tbody> <tfoot>`
 
 
 # Chapter 3 JS Objects (part 2)
  Objects can be created blank with properties and methods added later
  `var hot = new Object();`
  
  `hotel.name = 'Quay';`
  
  
  dot notations `.name` or square brackets `['name']` can be used to access and update object properties 
  or deleting `delete hotel.name`
  
  Maybe you want to keep a property but clear its value:  `hotel.name = '';`
  
  ### constructor notation
  `function Hotel(name,rooms,booked){this.name= name; this.rooms=rooms; this.booked = booked; this.checkAvailability = function() {return this.rooms - this.booked}`
  
 creating instances is of the object is simple as calling the constructor function and passing it arguments which will be injected to the property values.
 
  ### constructor and literal notation
  
  constructor : `var hotel = new object();`   literal: ` var hotel = {}`
  
  ### creating an object with props. and methods
  
  literal notation: `var hotel= {bame: "quay"}`  object constructor notation ` function hotel(name, rooms, booked){this.name = name;} 
  
  ### THe `this` keyword
  whatever 'this' is will change depending on the scope 
  
  
  When it comes to the browser it is modeled as an object. To access the properties we will use the `window.` anything after the dot would be a property name. 
  `refer to page 124 for some of those properties`
  The top most object in the DOM is the document object. This represents the webpage loaded into the current browser window. 
  `refer to page 126 for some document properties`
  
  
  
  `MATH` is an object just like arrays
  
  On page 137 there is a reference to some methods of the `Date` object
  example ` var today = new Date();`
  
  
  Review:
  Objects are series of variables and functions that represent soemthing from real life
  
  Web browsers implement objects that represent both the browser and window and the document loaded into the browser window
  
  The javascript language has its own built in objects suchs as ` String, Number Math, Date`
  
  
  
  
  
  
  
