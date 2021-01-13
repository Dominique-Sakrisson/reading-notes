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


