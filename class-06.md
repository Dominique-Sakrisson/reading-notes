## Article reading
_"Understanding the Problem Domain Is the Hardest Part of Programming"_

Understanding the problem is the most critical piece of programming


### What can we do?
Often we want to cut the problem into smaller digestible chunks to which we can narrow our focus
Should also make an effort in undestanding the problem **MORE** the better you understand the problem domain the higher chance you have at solving it



# Chapter 3 Object Literals

Objects purpose is to group together variables and functions that model can real world objects

#### quick tip
In objects variables are known as properties 
They give us information about the object

Functions become known as methods
Desscribe the functionality of they objects 

Defining functions inside objects
1. give the name as a property of the object
1. set the value to the definition of the function `function() {code-inside-here}`

`this` is used to reference to this particular object, if in a method will refer to the object that method belongs

# Chapter 5 Document Object Model

**(API) Application Programmable Interface** 

Api's let humans interact with programs and  programs talk to each other.

### DOM Tree
The model that the browser creates as it loads a webpage. **DOM tree is stored in memory**

#### Has 4 main nodes
1. The Document Node  `document.`
1. Element Nodes  `document.getElementById('');`
1. Attribute Nodes  `element.style.height`
1. Text Nodes   `element.textContent`


## Working with the DOM tree

Accessing and changing the DOM tree involves
1. Locate the node that is for the element you want to change
1. Use the element's text content, child elements, and attributes

===============================================

**Locating the element**
1. use the elements id attribute
1. querySelector() targets an element via its CSS selector (table, .class) 

**Option to select multiple elements**
1. getElementsByClassName()
1. getElementsByTagName()
1. querySelectorAll()

**Traversing between element nodes**
1. parentNode -- Selects the parent of the current element node  
1. previousSibling/ nextSibling -- selects previous or next sibling in the DOM tree
1. firstChild/ lastChild -- select first or last child of current element

**Work with the element**
1. Access/ Update text nodes 

Text inside any element is stored inside a text noded. TO access the element `li` textnode use the `firstChild` property. 
Use the text nodes only porperty (nodeValue) to get the text from the element and update it.

1. Work with the HTML content

`innerHTML` propert allows access to child elements and text content

`textContent` accesses solely the text content
 `createElement(), createTextNode(), appendChild(), removeChild()` allow youcreate new nodes, add or remove them from the node tree 

1. Access or Update Attribute Values  

`className/ id` -- `hasAttribute()` `getAttribute()` `setAttribute()` `removeAttribute()`







