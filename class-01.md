# HTML Chapter 1: “Structure” (pp.12-39)

name|description| example
---- | ---- | ----
tags | act like containers. They tell you something about the information that lies between their opening and closing tags.| \<p> \</p>
Attributes | Provide additional information about the contents of an element. They appear on the opening tag of an element. They are made up of 2 parts "name' and "value" | \<a href="url"> 
Body | Everything inside this element is shown in the browser | \<body>\</body>
Head | Contains information about the page | \<head>\</head>
Title | Shown in the top of the browser above where you usually type in the URL of the page or on the tab | \<title>\</title>



# HTML Chapter 8: “Extra Markup” (p.176-199)

name|description| example
---- | ---- | ----
Doctypes | Each page should begin with a doctype. | **html 5** =\<DOCTYPE html> **XML declartion**= \<?xml version="1.0" ?>
Comments | It is a good idea to add comments to your code so you always have a reference to go back to | \<!-- your comment -->
ID attribute | it is used to uniquely identify that element form other elements | \<p id="example">
Class Attribute | Identify multiple elements of he page | \<p class="example">
Block | Elements that appear to start on a new line in the browser window | \<h1> \<p> \<ul> \<li>
Inline | Continues on the same line of neighboring elements | \<a> \<b> \<em> \<a>
div | allows you to group a set of elements together | \<div>\</div>
span | Acts like a inline equivalent of div | \<span>\</span>
iframe | A little window that has been cut in to your page. abrevation for inline frame. Uses attributes **src**, **height**, **width**, **frameborder**, **scrolling**, **seamless**| \<iframe width="" height="" src="url">\</iframe>

### Information on the page

name|description| example
---- | ---- | ----
Meta | it contains information about the page. it is an empty element that does not have closing tags. | \<meta>
escape character | used for when you want characters to appear on your page. Put a "\\" before the character | \


# HTML Chapter 17: “HTML5 Layout” (pp.428-451)

> HTML5 uses a new set of elements that allow you to divide up parts of the page.

name|description| example
---- | ---- | ----
header | used for the main header of the page. Usually contains site name. | \<header>\</header>
footer | At the bottom of the page. Contains copyright information or a site map. | \<footer>\</footer>
Navigation | Used to contain the major navigational blocks on the site. Links are used a lot in the nav | \<nav>\</nav>
Articles | Acts as a container for any section of a page that could stand alone. | \<article>\</article>
Asides | Contains information that is related to the article. When outside of an article it acts as container for content as it relates to the entire page. | \<aside>\</aside>
sections | Groups related content together. Each section has its own heading | \<section>\</section>
Heading groups | To group together on or more elements of \<h1> through \<h6>. They are treated as one single heading | \<hgroup>
Figures | Can be used to contain any content that is referenced from the main flow of an article. *Used for graphs, videos, images etc* | \<figure>\</figure>

> Older browsers that do not know the new HTML5 element will automatically treat them as inline elements. For this include a line of CSS that which elements should be rendered as block elements.

# HTML Chapter 18: “Process & Design” (pp.452-475

## Thing to think about
1. who is your site for?

     * Target audience : individuals
        * What is the age range?
        * What gender? Mixed?
        * Which country?
        * Where they live? Urban, rural, etc
        * Average income?
        * Level of education?
        * Marital Status
        * Occupation?
        * How many hours they work?
        * How often they use the web?
        * What device they use when accesiing the web?

     * Target audience : Companies
        * Size of the company?
        * Position of people at the company?
        * Who is this sit for?
        * How large is the budget they control?

### Template for types of visitors

Name| Gorder| Molly| Jasper| Tony| Ivy
--- | --- | --- | --- | --- | --- 
Gender|M |F |M |M |F
Age|
Location|
Occupation|
Income|
Web Use|

## Why people visit your site?

> There are 2 types of categories: Motivation and Goals

**Motivation** - Entertainment? Professional? Luxury?
* enter types
* 

**Goals** - General information? News? Learned about product? Do they need to contack you.
* enter goals
* 

## What are your visitors trying to achieve?

**List of reasons why people would visit site**
* Molly -
* Gorder - 
* Jasper - 
* Tony -
* Ivy -

## What your visitors need?

**List of information they need to achieve goals**
* Enter what they need
* 

## How often people will visit your site?
* Frequency - 
* How often to do updates -

## Site map

1. Create a diagram of what the pages that will be used to structure the site
2. **Card sorting** - Place information on seperate pieces of paper that visitors might need to know.


## Wireframe
> Wireframe - is a simple sketch of the key information that goes on each page. Shows the hierarchy and how much space it needs.

 ~*Don't include color scheme, font choices, backgrounds or images for the website*~

# JS Chapter 1: “The ABC of Programming” (pp.11-52)

>Writing a script

1. Define the goal
2. Design the script
3. Code each step

>Designing a script

1. Tasks
2. Steps

> How HTML, CSS and Javascript fit together

* HTML = Content layer, is where the content of the page lives
* CSS = Presentation layer, enhances the HTML page with rules that state how the HTML content is presented.
* javascript = Behavior layer, how the page behaves, adding interactivity.

Type| Description| Example
---- | ---- | ----
Script| is a series of instructions that a computer can follow one-by-one.
Statement| each step in a script. Should end in a ;. These are instructions and should start on a new line.
Code Blocks| statements that are surrounded by curly braces. They should **not** be followed by a semicolon.
Objects | Each object has its own **properties**, **events** and **methods**
Properties| Characteristics of an object.
Events | The way people interact with objects. Used to trigger a section of code.
Multi line| comments over multiple lines| starts with /* and ends with */
Single line| anything that follows the two forward slash comments| // comment
Variable| Stores data temporarily in a script so it can work. The data changes or varies what each script does.| Var "variable name" = "value";
Booleans| True or false values| true
numbers| handles numbers or integers. These are not written in quotes| 1 2 3
String| consists of letters; values are immutable. Can't be altered.| abc
Assignment operator| Remember that everything to the right of the equals sign is evaluated first
Camel case| upper case that follows the word. js does not use spaces in var
Concatenating| link (things) together in a chain or series
floats| Decimal numbers

[Main Page](https://will-ing.github.io/reading-notes)