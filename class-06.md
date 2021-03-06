# **JS Object Literals; The DOM**

# Understanding the problem domain is the hardest part of programming

What can you do about it?
If understanding the problem domain is the hardest part of programming and you want to make programming easier, you can do one of two things:

* Make the problem domain easier
* Get better at understanding the problem domain

> You can often make the problem domain easier by cutting out cases and narrowing your focus to a particular part of the problem.

# Chapter 3: “Object Literals” (pp.100-105)

>An **Object** groups together a set of variables and functions to create a model of something you would recognize from the real world. In a object, variables and functions take on new names.

>A **method** can reference its own object property using **'this'**.

Type| Description| Example
---- | ---- | ----
Property | Tell us about the object. They are the variables
Method | Represents task that are associated with the object. They are the function.
Literal Notations | Easiest and most popular way to create objects.

``` js
var hotel = {
  name: 'Quay',
  rooms: 40,
  booked: 25,
  checkAvailability: function() {
    reut this.rooms - this booked;
  }
};

va elName = document.getElementById('hotelName');
elName.textContent = hotel.name;

var elRooms = document.getElementById('rooms');
elRooms.textContent = hotel.checkAvailability();
```
# Chapter 5: “Document Object Model” (pp.183-242)

>The DOM (Document Object Model) tree is a model of web pages. Consists of 4 main type of nodes.

Type| Description| Example
---- | ---- | ----
Document Node | It represents the top of the page. When you access any element, attribute, or text node you navigate to it via the document node. It is the starting point for all visits to the DOM tree
Element Node | Elements describe the structure of the HTML page. Once you find the element you want then you can access its text. 
Attribute nodes | Are not children of the element that carries them, they are part of that element. 
Text Nodes | Cannot have children. Is always a new branch of the DOM tree. No branches can come off it.

>Methods that find elements in the DOM tree are called DOM queries. When you need to work with an element more than once, you should use a variable to store the result of this query.

>DOM queries may return one element, or they may return a NodeList which is a collection of nodes.

### Methods that return a single element node

Type| Description| Example
---- | ---- | ----
getElementById | Selects an individual element given the value of its id attribute. The HTML mst have an Id attribute.
querySelector  | Uses css selector syntax that would select one or more elements. Returns only the first of the matching elements.

### Methods that return one or more elements

Type| Description| Example
---- | ---- | ----
getElementsByClassName | Select one or more elements given the value of their class attribute.
getElementsByTagName | Selects all element on the page with the specific tag name
querySelectorAll | Uses css selector syntax to select one or more elements and returns all of those that match


**Looping through a node list**

![loop node list](images/loopnodelist.jpg)

### Removing an element via DOM manipulation

1. Store the element to be removed in a variable
2. Store the parent of that element in a variable
3. Remove the element from its containing element

![removing Element](images/removingele.jpg)

### Comparing techniques updating HTML content

Type| Description| Example
---- | ---- | ----
document.write() | Method to add content that was not in the original source code to the page but its use is rarely advised.
element.innerHTML | Property lets you get/ update the entire content of any element as a string.

>Cross-site scripting attacks (or XSS) can happen when you add HTML to a page using innerHTML. Involves attacker placing malicious code in to a site.

[Main Page](https://will-ing.github.io/reading-notes)