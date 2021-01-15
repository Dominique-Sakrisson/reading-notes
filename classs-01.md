# chapter 1 structure notes

### hteml pages are text documents rendered to the screen by a web browser
they have different tags to inform the browser how to display the content 

# Chapter 8 extra markup

Over the years as html was improved semantics have changed as well as additional tags and features.

## iFrames

stands for inline frame 

and iFrame can contain any html page such as a rendering of google maps

attributes an iFrame requires

1. src
1. height
1. width

scrolling is no longer supported in html 5 for iFrames

In html5 there is a seamless attribute if you prefer not to have scrollbars

### some more tags
1. meta tag
goes inside the head section of the page, provied the search engines additional information about your page.

meta attributes
1. name
the value of name is the property you are setting
1. content 
the value of the content attribute is the value you want the property you named to have

there are description metas, keywords meta, robots which basically is to tell the search engine to add this page to search results or not

### more on meta 
there is a modifier I'll call it named **http-equiv** used along side with the content attributes 
_<meta http-equiv="author"
 content="Jon Duckett" />_ 
 
 by using pragma keyword the browser is prevented from caching the page. (store locally to save time loading next visits)
 **Expires** option tells the browser how long the page should be cached for. 
 
 
 # chapter 17 html 5 layout
 
 some new tags in html 5
 1. header
 1. nav
 1. article
 1. aside
 1. footer
 1. section
 1. hgroup
 1. figure
 
 ## Old browsers and new code
By default older browsers will display these new tags as inline elements.
To get around this we can simply add in a css rule to make them display content correctly
`header, section, footer, aside, nav, article, figure
{
display: block;}`

### internet explorer sucks so youre going to have to include some javascript for these elements in any version before IE9.

the thing you need to add is **html5 shiv or shim**

google has this hosted so a quick search should do it to explain how this works


# chapter 18 process and design

_keep in mind_

every website should be designed for the target audience, understanding your target audience is vastly important

good questiosn to think about when designing your site towards the audience could be ...

### for individuals

target audience age

more men or women

country the visitors live

average income

### for companies
what is the company size or relevant department size

position of people in the company

will hey be using site for themselves or for someone else

how large is the budget they control

This information is important to be mindful of when designing a site map

### wireframes

A simple sketch up of the key parts of your site with information placed where it makes the most sense to be

Designing a visual heiracrchy help users focus on the key messages of your sight 

### when designing nav make the content **clear, concise, selective**



# javascript Chapter 1

when making a program start from the big picture of what it should do

then break it down to small managable steps

1. define the goal
2. design the script
this is when you break down every small task that might be needed to reach the goal

a flowchart can be a good tool when designing
3. Code each step

## objects

we create opjects with key value pairs meant to model real world objects

those properties could be values the manage the object state or even functionality which when a function belongs to an object its then called an object's method

Web browsers are indeed objects, containing other objects such as the **document and the window**
## how a broswer sees html

1. recieves and reads page of html code
2. creates a model of the page and stores it in memory
3. uses a rendering engine to show the contents to the user

## a popular approach to web design is called Progressive enhancement

