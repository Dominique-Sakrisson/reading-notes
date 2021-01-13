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
