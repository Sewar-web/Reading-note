# CALLING FUNCTIONS THAT NEED INFORMATION

* When you call a function that has parameters, you specify the values it should use in the parentheses that follow its name. The values are called arguments, and they can be provided as values or as variables.

1. ARGUMENTS AS VALUES : 

When the function below is called, the number 3 will be used for the width of the wall, and 5 will be used for its height.

2. ARGUMENTS AS VARIABLES :

 calling a function you can use variables in thein You do not have to specify actual values when place. So the following does the same thing.

  **GETTING A SINGLE VALUE OUT OF A FUNCTION**
   * Some functions return information to the code that called them. 


**GETTING MULTIPLE VALUES OUT OF A FUNCTION**
* Functions can return more than one value using an array. 

**ANONYMOUS FUNCTIONS & FUNCTION EXPRESSIONS**
* Expressions produce a value. They can be used where values are expected.
If a function is placed where a browser expects to see an expression,
 then it gets treated as an expression. 


 1. FUNCTION DECLARATION :
A function declaration creates a function that you
can call later in your code. It is the type of function
you have seen so far in this book.
In order to call the function later in your code, you
must give it a name, so these are known as named
functions. Below, a function called area() is
declared, which can then be called using its name. 

2. FUNCTION EXPRESSION
If you put a function where the interpreter would
expect to see an expression, then it is treated as an
expression, and it is known as a function expression.
In function expressions, the name is usually omitted.
A function with no name is called an anonymous
function. Below, the function is stored in a variable
called area. It can be called like any function created
with a function declaration.


**IMMEDIATELY INVOKED FUNCTION EXPRESSIONS**

1. IMMEDIATELY INVOKED FUNCTION
EXPRESSIONS (llFE)
Pronounced "iffy," these functions are not given
a name. Instead, they are executed once as the
interpreter comes across them.
Below, the variable called area will hold the value
returned from the function (rather than storing the
function itself so that it can be called later). 

  - The final parentheses (shown on green) after
the closing curly brace of the code block tell the
interpreter to call the function immediately.

  - The grouping operators (shown on pink) are
parentheses there to ensure the intrepreter treats
this as an expression.


**VARIABLE SCOPE**

* SCOPE : The location where you declare a variable will affect where it can be used
within your code. If you declare it within a function, it can only be used
within that function.

1. LOCAL VARIABLES
When a variable is created inside a function using the
var keyword, it can only be used in that function.
It is called a local variable or function-level variable.
It is said to have local scope or function-level scope.
It cannot be accessed outside of the function in
which it was declared. Below, area is a local variable. 

2. If you create a variable outside of a function, then it
can be used anywhere within the script. It is called a
global variable and has global scope 
* Global variables are stored in memory for as long
as the web page is loaded into the web browser.
This means they take up more memory than local
variables, and it also increases the risk of naming
conflicts.

***

## The Document Object Model 

* As a browser loads a web page, it creates a model of that page.
The model is called a DOM tree, and it is stored in the browsers' memory.
It consists of four main types of nodes. 

* Each node is an object with methods and properties.
Scripts access and update this DOM tree (not the source HTML file).
Any changes made to the DOM tree are reflected in the browser. 

 1. THE DOCUMENT NODE (html , head , body ,...)
 2. ELEMENT NODES (h1 , p, ..)
 3. ATTRIBUTE NODES (div , script , li)
 4. TEXT NODES


**Accessing and updating the DOM tree involves two steps:**
1. Locate the node that represents the element you want to work with.
2. Use its text content, child elements, and attributes. 


1. **STEP 1: ACCESS THE ELEMENTS**
   * SELECT AN INDIVIDUAL ELEMENT NODE
   * SELECT MULTIPLE ELEMENTS (NODELISTS)
   * TRAVERSING BETWEEN ELEMENT NODES

2. **STEP 2: WORK W ITH THOSE ELEMENTS**
   * ACCESS/ UPDATE TEXT NODES
   * WORK W ITH HTML CONTENT
   * ACCESS OR UPDATE ATTRIBUTE VALUES 


**CACHING DOM QUERIES**
* Methods that find elements in the DOM tree are called DOM queries. When you need to work with an element more than once, you should use a variable to store the result of this query.

* When a script selects an element to access or update, the Interpreter must find the elementca) in the DOM tree.


**ACCESSING ELEMENTS**
* DOM queries may return one element, or they may return a Nodelist,
which is a collection of nodes. 


* GROUPS OF ELEMENT NODES
If a method can return more than one node, it will
always return a Nodelist, which is a collection of
nodes

* FASTEST ROUTE
Finding the quickest way to access an element
within your web page will make the page seem
faster and/or more responsive. 


* METHODS THAT RETURN A SINGLE ELEMENT NODE:

1. getElementByld :
Selects an individual element given the value of its i d attribute .
The HTML must have an id attribute in order for it to be selectable.

2. querySel ector
Uses CSS selector syntax that would select one or more elements .
This method returns only the first of the matching elements

  **METHODS THAT RETURN ONE OR MORE ELEMENTS (AS A NODELIST):**
  1. getEl ementsByClassName( 1
class 1 )
Selects one or more elements given the value of their cl ass attribute.
The HTML must have a cl ass attribute for it to be selectable.
This method is faster than querySe 1ectorA11 () .


2. getEl ementsByTagName
Selects all elements on the page with the specified tag name.
This method is faster than querySe 1ectorA11 (). 

3. querySelectorAll 
Uses CSS selector syntax to select one or more elements and returns all
of those that match.


**TRAVERSING THE DOM**
* When you have an element node, you can select
another element in relation to it using these five
properties. This is known as traversing the DOM. 


1. parentNode
This property finds the element
node for the containing (or
parent) element in the HTML


2. previousSibling
nextSibling
These properties find the
previous or next sibling of a node
if there are siblings. 

3. first Child-lastChild
These properties find the first or
last child of the current element.


**WHITESPACE NODES**
Traversing the DOM can be difficult because
some browsers add a text node whenever they
come across whitespace between elements



**HOW TO GET/UPDATE ELEMENT CONTENT**
* When you select a text node, you can retrieve or amend the content of it
using the node Va 1 ue property. 
ex : 
document.getElementByid( 1 one 1 ).firstChild.nextSibling. nodeValue;





* get El ementByi d () allows you
to select a single element node
by specifying the value of its
id attribute.
This method has one parameter:
the value of the id attribute on
the element you want to select.


**When a DOM query returns a Nodelist, you may want to:**
1. Select one element from the NodeList.
2. Loop through each item in the Nodelist and
perform the same statements on each of the
element nodes. 




* In a **live Nodelist**, when your script updates the
page, the Nodelist is updated at the same time.
The methods beginning getEl ementsBy_ return live
Node lists. They are also typically faster to generate
than static Nodelists. 

* In a **static Nodelist** when your script updates the
page, the NodeList is not updated to reflect the
changes made by the script.



*ACCESSING TEXT ONLY*
* The script starts off by getting
the content of the first list item
using both the textContent 

**ADDING OR REMOVING HTML CONTENT**
  * There are two very different approaches to adding and removing content from a DOM tree: the innerHTML property and DOM manipulation.

1. APPROACH : 
   Inner can be used on any element node. It is used both to retrieve and replace content. To update an element, new content is provided as a string It can contain markup for descendant elements.

2. ADDING : 
   CONTENT To add new content 1. Store new content (including markup) asa string in a variable. 2. Select the element whose content you want to replace. 3. Set the element's InnerHTHL property to be the new string

3. REMOVING : 
  CONTENT To remove all content from an element, you set innerNTML to an empty string To remove one element from a DOM fragment, eg, one <11> from a ul, you need to provide the entire fragment minus that element.



* document.write()
* The document object's write () method is a simple
way to add content that was not in the original
source code to the page, but its use is rarely advised.
**ADVANTAGES**
1. It is a quick and easy way to show beginners how content can be added to a page.

**DISADVANTAGES**
1. It only works when the page initially loads.
2. If you use it after the page has loaded it can:
3. Overwrite the whole page
4. Not add the content to the page
5. Create a new page
6. It can cause problems with XHTML pages that
are strictly validated.
7. This method is very rarely used by programmers
these days and is generally frowned upon.


**CREATING ATTRIBUTES & CHANGING THEIR VALUES**
* The className property allows
you to change the value of the
class attribute. If the attribute
does not exist, it will be created
and given the specified value.
cOS/js/set-attribute.js
You have seen this property
used throughout the chapter
to update the status of the
list items. Below, you can see
another way to achieve the task.
The setAttri bute() method
allows you to update the value
of any attribute. It takes two
parameters: the attribute name,
and the value for the attribute. 



**REMOVING ATTRI BUTES**
To remove an attribute from an
element, first select the element,
then call removeAtt r i bute () .
It has one parameter: the name
of the attribute to remove. 





