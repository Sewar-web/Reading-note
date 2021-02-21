# Table
* What's a Table : A table represents information in a grid format.
* Examples of tables include financial reports, TV schedules, and sports results.

1. Grids allow us to understand
complex data by referencing
information on two axes.

2. Each block in the grid is referred
to as a table cell. In HTML a
table is written out row by row.

**Basic Table Structure**
1. `<table>`
The <table> element is used
to create a table. The contents
of the table are written out row
by row.
2. `<tr>`
You indicate the start of each
row using the opening `<tr>` tag.
(The tr stands for table row.)
It is followed by one or more
`<td>` elements (one for each cell
in that row).
At the end of the row you use a
closing `</tr>` tag.

3. `<td>`
Each cell of a table is represented using a `<td>`
element. (The td stands for table data.)
At the end of each cell you use a
closing `</td>` tag.

**Table Headings**
* `<th>`
The `<th>` element is used just
like the `<td>` element but its
purpose is to represent the
heading for either a column or
a row. (The th stands for table
heading.) 
   - Using `<th>` elements for
headings helps people who
use screen readers, improves
the ability for search engines
to index your pages, and also
enables you to control the
appearance of tables better
when you start to use CSS.

**Spanning Columns**
* The colspan attribute can be
used on a `<th>` or `<td>` element
and indicates how many columns
that cell should run across.


**Spanning Rows**
* The rowspan attribute can be
used on a `<th>` or `<td>` element
to indicate how many rows a cell
should span down the table.

**Long Tables**
These elements help people
who use screen readers and also
allow you to style these sections
in a different manner than the
rest of the table (as you will see
when you learn about CSS).

1. `<thead>`
The headings of the table should
sit inside the `<thead>` element.

2. `<tbody>`
The body should sit inside the
`<tbody>` element.

3. `<tfoot>`
The footer belongs inside the
`<tfoot>` element.

**Width & Spacing**
* The width attribute was used
on the opening `<table>` tag to
indicate how wide that table
should be and on some opening
`<th>` and `<td>` tags to specify
the width of individual cells.
The value of this attribute is
the width of the table or cell in
pixels.

**Border & Background**
* The border attribute was used
on both the <table> and <td>
elements to indicate the width of
the border in pixels.
The bgcolor attribute was used
to indicate background colors
of either the entire table or
individual table cells.

*****

**HOW MEMORY &VARIABLES WORK**
* Global variables use more memory. The browser has to remember them
for as long as the web page using them is loaded. Local variables are only
remembered during the period of time that a function is being executed. 

 1. CREATING THE VARIABLES IN CODE
Each variable that you declare takes up memory.
The more variables a browser has to remember,
the more memory your script requires to run. 

2. NAMING COLLISIONS
You might think you would avoid naming collisions;
after all you know which variables you are using.

**WHAT IS AN OBJECT?**
* Objects group together a set of variables and functions to create a model
of a something you would recognize from the real world. In an object,
variables and functions take on new names

* If a variable is part of an object, it is called a
property

* IN AN OBJECT: FUNCTIONS BECOME
KNOWN AS METHODS
If a function is part of an object, it is called a method. 


1. CREATING· OBJECTS USING
LITERAL NOTATION 

2. CREATING MORE
OBJECT LITERALS 

* creating an object constructor notation :
create blank object.

* to update an object :
we use dot notation or square bracktes

********

**CREATING MANY OBJECTS: CONSTRUCTOR NOTATION**

* Sometimes you will want several objects to represent similar things.
Object constructors can use a function as a template for creating objects.
First, create the template with the object's properties and methods. 


* In JavaScript, data is represented using name/value pairs.
To organize your data, you can use an array or object to group a set of
related values. In arrays and objects the name is also known as a key.  
1. VARIABLES
A variable has just one key (the variable name)
and one value

2. ARRAYS
Arrays can store multiple pieces of information.
Each piece of information is separated by a comma.
The order of the values is important because items
in an array are assigned a number (called an index)


* The first thing you need to do is get to know what tools are available.
You can imagine that your new toolkit has three compartments: 

1. BROWSER OBJECT MODEL
The Browser Object Model contains
objects that represent the current
browser window or tab. It contains
objects that model things like
browser history and the
device's screen. 

2. DOCUMENT OBJECT MODEL
The Document Object Model uses
objects to create a representation of
the current page. It creates a new
object for each element (and each
individual section of text)
within the page.

3. GLOBAL JAVASCRIPT OBJECTS
The global JavaScript objects
represent things that the JavaScript
language needs to create a model
of. For example, there is an
object that deals only with
dates and times. 
*****

**THREE GROUPS OF BUILT-IN OBJECTS**
1. USING BUILT-IN OBJECTS: The three sets of built-in objects each offer a different range of tools that help you write scripts for web pages.

2. BROWSER OBJECT MODEL The Browser Object Model creates a model of the browser tab or window. 

3. DOCUMENT OBJECT MODEL The Document Object Model (DOM) creates model of the current web page.

4. GLOBAL JAVASCRIPT OBJECTS The global objects do not form a single model.



**The window object represents the current browser window or tab. It is the topmost object in the Browser Object Model, and it contains other objects that tell you about the browser.**

window . innerHeight : Height of window (excluding browser chrome/user interface) (in pixels)
window.innerWidth : Width of window (excluding browser chrome/user interface) (in pixels)
window.pageXOffset : Distance document has been scrolled horizontally (in pixels)
window. pageYOffset : Distance document has been scrolled vertically (in pixels)
window.screenX : X-coordinate of pointer, relative to top left corner of screen (in pixels)
window . screenY : Y-coordinate of pointer, relative to top left corner of screen (in pixels)
window.location :Current URL of window object (or local file path)
window.document :Reference to document object, which is used to represent the current page
contained in window
window.history : Reference to history object for browser window or tab, which contains details
DESCRIPTION

window.history.length  : Number of items in hi story object for browser window or tab
window.screen : Reference to screen object
window.screen .width  : Accesses screen object and finds value of its width property (in pixels)
window. screen.height : Accesses screen object and finds value of its height property (in pixels)
 




***

PROPERTY           DESCRIPTION
document.title : Title of current document
document.lastModified : Date on which document was last modified
document .URL : Returns string containing URL of current document
document.domain : Returns domain of current document



**GLOBAL OBJECTS: STRING O BJECT**
Whenever you have a value that is a string, you can use the properties
and methods of the String object on that value. This example stores the
phrase "Home sweet home " in a variable. 


**DATA TYPES REVISITED**
1. String
2. Number
3. Boolean
4. Undefined (a variable that has been declared, but
no value has been assigned to it yet)
5. Null (a variable with no value - it may have had
one at some point, but no longer has a value)
 6. object



**WORKING WITH DECIMAL NUMBERS***

* As with the String object the
properties and methods of the
Number object can be used with
with any value that is a number


* The Math object has properties and methods
for mathematical constants and functions. 






