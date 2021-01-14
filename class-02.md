# HTML & CSS
     
## chapter 2 Text notes

Tags are otherwise known as markup and their purpose is to create and display a view to the page. Tags help the browser format the page correctly.

### Markup types

1. Structural-- the block level 'containing' elements
2. Semantic-- moreso the 'styling' tags that provides definition to the defined areas

### **Useful to hang onto--**
 **address** tag will probably be used often on account of dual usability with email and physical addresses

 **cite** when you're citing a source of information this tag should be used

 **dfn** another semantic tag that will probably be used semi regularly


**list of tags covered**
1. headers  `<h1> </h1> .. <h2> <h3> <h4> <h5> <h6>`
2. paragraphs   `<p> </p>`
3. bold `<b> </b>` 
4. italics `<i> </i>`
5. superscript `<sup> </sup>`
6. subscript    `<sub> </sub>`
7. line break   `<br/>` 
8. horizontal rules `<hr>`
   
10. strong `<strong> </strong>`
11. emphasis `<em> </em>`
12. blockquote & quote `<blockquote> </blockquote>`, `<q> </q>`
13. abbreviations and acronyms `<abbr>Text</abbr>`
14. citations `<cite> </cite>`
15. definitions `<dfn> </dfn>`
16. address `<addres> </address>`
17. insert  `<ins> </ins>`
18. delete  `<del> </del>`
19. strikethrough `<s> </s>`

## chapter 3 Lists notes

3 types of lists
1. ordered lists
2. unordered lists
3. definition lists-- set of terms along with definitions for each

**browsers indent lists by default**

There can be nested lists with list items



## chapter 10 Introducing CSS notes
CSS is designed to design the styling of html pages.

The two parts of a CSS rule
1. selector `p`
2. _declaration_ `{font-family: Arial;}`
The two parts of a CSS _declaration_
1. property `font-family:`
2. value    `Arial;`
Style multiple selectors by separating them with commas `sel1, sel2`

### linking CSS files in `<head></head>`

`<link href="css/style.css" type="text/css" rel="stylesheet"/> `

breakdown of `<link/>` tag

**href** Attribute designates the path to the css file

**type** Attribute designates the type of file being linked to

**rel** Attribute explains the relationship between the link and the html page

| selector                   | meaning                                                                  | example                                                                                  |
|----------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| Type Selector              | Matches element names                                                    | p, section, img                                                                          |
| Class selector             | Matches element whose class attribute has the same value                 | .hello{} or: section.hello{}                                                             |
| ID Selector                | Matches element whose id attribute has the same value                    | #hello-again{  }                                                                         |
| Child Selector             | matches an element that is a direct  child of the other one              | li > a{} targets the `<a>` elements  that are children of `<li>'s`                       |
| descendant selector        | matches an element that is a  descendant of (inside of another  element) | section p {} targets any <p> tags inside of section tags                                 |
| adjacent sibling  selector | matches an element that is the first  sibling of another                 | h1+p {} targets the first p element that comes after any h1                              |
| general sibling selector   | matches an element that is any  sibling of another                       | h1~p {} if there were multiple p elements that come after h1, they all would be selected |
|                            |                                                                          |                                                                                          |

**Style rules Precedence**

When making a style rule, the last written style will take precedence in absense of a more specific style rule

-refer to a _css selector specificity search_

## Inheritance of rules
rules applied to parent tags of elements will also be applied to that element in the absence of a newer or more specific rule

having a property value of inherit will force an element to **inherit** from its parent 


## chapter 13 _Boxes_ notes

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
.
.

.








# Javascript & Jquery
## Chapter 2 basic javascript
**statement** Each instruction written to a program 

**code blocks** the statements inside of curly braces

## data types
1. Numerical data type
2. String data type
3. Boolean data type

### declare a variable

`var x = 'hello';`

booleans are great to be used as switches when deciding which path the program will take

### Variable naming rules
1. name must start with a letter, $, or _, **specifically not a number**
2. **Do not** use a dash or a period in a variable name
3. Keywords and reserved words are off limits
4. variables are case sensitive
5. use names that are self documenting for ease of readability
6. use proper casing for variable names of more than one word, either **camelCase** or **kebab-case**

## Arrays
` var foods = [ a food, 2 food, me food];`

### array constructor example
different from a standard array declaration
` var foods = new Array('eggs', 'milk', 'cookies');`

arrays are basically lists that for each element in the list it is assigned a value of its place in the list. That value is how you access the actual stored value of that index

### arrays are objects as such they have properties
one of which being the length property

to use the length propert you would type the name of the array then dot operator and the length property **`myArray.length;`**

### expressions
expressions once evaluated returns a single value
there are two types of expressions
1. Expressions that assign a variable a value `var x = 3;`
2. Expressions that use multiple values to return a single value `var xX = 3 + 3;`

### operators
these manipulate values
1. assignment operators
2. arithmetic operators
3. string operators
4. comparison operators
5. logical operators 


## Chapter 10 Decisions & loops
a Decision has two components in a program
1. an expression gets evaluated and returns a value
2. for a given situation the conditional stement how to proceed

When using comparison operators there are usually two parts to the comparison, operands and the operator. Operator would be the way in which the two operands are being compared.
An operand can be a single value or it can be an expression.
### logical operators
1. Logical AND &&

test for more than one condition

2. Logical OR ||

This tests for at least one condition

3. Logical NOT !

This takes a boolean value, and inverts it. True becomes false;

**short circuiting**

this is when there may be a logical && operator, it requires false && another test, if the first test results in true, the test expectation was never met and the second test is never attempted..

## additional reading 1/12

Main purpose of the article is explaining importance of and how to write an individual commit message.

A team's approach to commits should be structured teams should agree on a common convention for commits.
### 3 main points when making a commit
1. style- use proper english and spell things out
2. Content- what should or shouldnt be in the body of a commit message
3. Metadata- How should issue tracking ID's pull requests numbers etc be referenced?

### Seven rules to a great commit message
1. **Separate subject from body with a blank line** can create problems with various tools if not line breaked
2. Limit the subject line to 50 characters
3. Capitalize the subject line
4. Do not end the subject line with a period
5. Use the imperative mood in the subject line
6. Wrap the body at 72 characters.
7. Use the body to explain what and why vs how

## separate subject fomr body with a blank line

Create blank lines in the body to separate the first line commit title, commit body, and further paragraphs. If using bullets or hyphens a somewhat prevalent convention is to use asteriks instead of bullets.


Focus on the **why** you made a commit not the how. 

When a committ message is simple enough for a one line like _"fix typo in the header"_ its okay to use just the one line in the command -m ''

When a commit needs a bit of explaination you need to write a body.

### git commands

**git log** prints out a full log of the entry

**git log --oneline** will print out only the subject line

**git shortlog** prints out commits by the user, only the subject line

## Limit the subject line to 50 characters
not a hard cap, just a useful limit to keep in mind that promotes having concise commit subjects


## capitolize subject line
Start all subject lines with a capitol letter, pretty simple

## Do not end subject line with a period

## Use the imperative mood in subject line
-spoken as if given command or instruction

git will communicate back to users in the imperative so its ideal to tell git stuff in the same manor

_example:_ default message created when using git merge is: '_Merge branch 'myFeat'_

### A properly formed Git commit subject line should always be able to complete the following sentence:
example: "if applied this commit will _refactor subsystem X for readability_

## Wrap the body at 72 characters
Git doesnt automatically wrap lines so you must do it manually, aim for 72 characters per line


## use body to explain what  and why rather than how

