# Links

* Links :  are the defining feature of the web
because they allow you to move from
one web page to another — enabling the
very idea of browsing or surfing.

*Links from one website to another
* Links from one page to another on the same website
  
*  Links from one part of a web page to another part of the
same page
*  Links that open in a new browser window
*  Links that start up your email program and address a new
email to someone

*how we write link*

* Links are created using the <a> element. Users can click on anything
between the opening <a> tag and the closing </a> tag. You specify
which page you want to link to using the href attribute.

`<a href="yourlink"> something </a> `

**Linking to Other Sites**
 * When you link to a different
website, the value of the href
attribute will be the full web
address for the site, which is
known as an absolute URL.



**Linking to Other Pages on the Same Site**
 * When you are linking to other
pages within the same site,
you do not need to specify the
domain name in the URL. You
can use a shorthand known as a
relative URL.
If all the pages of the site are in
the same folder, then the value
of the href attribute is just the
name of the file.



**Directory Structure**
* On larger websites it's a good idea to organize your code by placing the
pages for each different section of the site into a new folder. Folders on a
website are sometimes referred to as directories.

**Relationships**
* The relationship between
files and folders on a website
is described using the same
terminology as a family tree.

**Homepages**
* The main homepage of a site
written in HTML (and the
homepages of each section in a
child folder) is called index.html.


**Relative URLs**

* Relative URLs can be used when linking to pages within your own
website. They provide a shorthand way of telling the browser where to
find your files.

  - When you are linking to a page
on your own website, you do
not need to specify the domain
name. You can use relative URLs
which are a shorthand way to tell
the browser where a page is in
relation to the current page.


- This is especially helpful when
creating a new website or
learning about HTML because
you can create links between
pages when they are only on
your personal computer (before
you have got a domain name and
uploaded them to the web)


- If all of the files in your site are
in one folder, you simply use the
file name for that page.


- f your site is organized into
separate folders (or directories),
you need to tell the browser
how to get from the page it is
currently on to the page that you
are linking to.


 - If you link to the same page from
two different pages you might,
therefore, need to write two
different relative URLs.


***Relative Link Type***
1. Same Folder
To link to a file in the same folder, just use the file
name. (Nothing else is needed.)
 
  - example : To link to music reviews from the music homepage:
`<a href="reviews.html">Reviews</a>`

2. Child Folder
For a child folder, use the name of the child folder,
followed by a forward slash, then the file name

 - example : To link to music listings from the homepage:
`<a href="music/listings.html">Listings</a>`


3. Grandchild Folder
Use the name of the child folder, followed by a
forward slash, then the name of the grandchild
folder, followed by another forward slash, then the
file name.

 - example : To link to DVD reviews from the homepage:
`<a href="movies/dvd/reviews.html">
Reviews</a>`

4. Parent Folder
Use ../ to indicate the folder above the current one,
then follow it with the file name.

  - example : To link to the homepage from the music reviews:
`<a href="../index.html">Home</a>`

1. GrandParent Folder
Repeat the ../ to indicate that you want to go up
two folders (rather than one), then follow it with the
file name.

  - example : To link to the homepage from the DVD reviews:
`<a href="../../index.html">Home</a>`



***Email Links***
mailto: 
To create a link that starts up
the user's email program and
addresses an email to a specified
email address, you use the `<a>`
element. However, this time the
value of the href attribute starts
with mailto: and is followed by
the email address you want the
email to be sent to.

  - example `<a href="mailto:jon@example.org">Email Jon</a>`



***Opening Links in a New Window***
*  target
1. If you want a link to open in a
new window, you can use the
target attribute on the opening
`<a>` tag. 

2. The value of this
attribute should be _blank.
One of the most common
reasons a web page author
might want a link to be opened
in a new window is if it points to
another website. In such cases,
they hope the user will return
to the window containing their
site after finishing looking at the
other one.


***Linking to a Specific Part of the Same Page***

 * you need to
identify the points in the page
that the link will go to. You do
this using the id attribute (which
can be used on every HTML
element). You can see that the
`<h1>` and `<h2>` elements in this
example have been given id
attributes that identify those
sections of the page.

***

## Layout

**Building Blocks**
* CSS treats each HTML element as if it is in its
own box. This box will either be a block-level
box or an inline box

1. *Block-level elements*
start on a new line


2. *Inline elements*
flow in between
surrounding text
Examples include:
`<img> <b> <i>`

3. *Containing Elements*
If one block-level element sits inside another
block-level element then the outer box is
known as the containing or parent element.



  1. **Normal flow**
Every block-level element
appears on a new line, causing
each item to appear lower down
the page than the previous one.
Even if you specify the width
of the boxes and there is space
for two elements to sit side-byside, they will not appear next
to each other. This is the default
behavior (unless you tell the
browser to do something else)



2. **Relative Positioning**
This moves an element from the
position it would be in normal
flow, shifting it to the top, right,
bottom, or left of where it
would have been placed. This
does not affect the position of
surrounding elements; they stay
in the position they would be in
in normal flow.


3. **Absolute positioning**
This positions the element
in relation to its containing
element. It is taken out of
normal flow, meaning that it
does not affect the position
of any surrounding elements
(as they simply ignore the
space it would have taken up).
Absolutely positioned elements
move as users scroll up and
down the page.


4. **Fixed Positioning**
This is a form of absolute
positioning that positions
the element in relation to the
browser window, as opposed
to the containing element.
Elements with fixed positioning
do not affect the position of
surrounding elements and they
do not move when the user
scrolls up or down the page.

5. **Floating Elements**
Floating an element allows
you to take that element out
of normal flow and position
it to the far left or right of a
containing box. The floated
element becomes a block-level
element around whic
 
  - A lot of layouts place boxes
next to each other. The float
property is commonly used to
achieve this

- When elements are floated, the
height of the boxes can affect
where the following elements sit.

  
  **Clearing Floats**
   * The clear property allows you
to say that no element (within
the same containing element)
should touch the left or righthand sides of a box. It can take
the following values:
1. left
2. right
3. both
4. none
   
   ***

 **creating Multi-Column Layouts with Floats**
 * Many web pages use multiple
columns in their design. This
is achieved by using a `<div>`
element to represent each
column. The following three CSS
properties are used to position
the columns next to each other:
1. width
This sets the width of the
columns.
2. float
This positions the columns next
to each other.
3. margin
This creates a gap between the
columns.

 **Screen Sizes**
  * When designing for print, you
always know the size of the
piece of paper that your design
will be printed on



- Resolution --> refers to the number of dots a screen shows per inch. Some
devices have a higher resolution than desktop computers and most
operating systems allow users to adjust the resolution of their screens.



**page size**
 - Because screen sizes and display resolutions vary so much, web
designers often try to create pages of around 960-1000 pixels wide
(since most users will be able to see designs this wide on their screens).


*** 
**Fixed width**
fixed width  layout
designs do not
change size as the
user increases
or decreases
the size of their
browser window.
Measurements tend
to be given in pixels


* Advantages
1. Pixel values are accurate
at controlling size and
positioning of elements.
2. The designer has far greater
control over the appearance
and position of items on the
page than with liquid layouts.
3. You can control the lengths
of lines of text regardless of
the size of the user's window.
4. The size of an image will
always remain the same
relative to the rest of the
page.



* Disadvantages
1. You can end up with big gaps
around the edge of a page.
2. If the user's screen is a much
higher resolution than the
designer's screen, the page
can look smaller and text can
be harder to read.
3.  If a user increases font sizes,
text might not fit into the
allotted spaces.
4. The design works best on
devices that have a site or
resolution similar to that of
desktop or laptop computers.
5. The page will often take up
more vertical space than a
liquid layout with the same
content.


**Liquid Layouts**
*Liquid layout designs stretch and contract as the user increases or decreases the size of their browser window. They tend touse percentages.*


***

**Layout Grids**
* it's help to a :
1.  Creates a continuity between
different pages which may
use different designs
2.  Helps users predict where to
find information on various
pages
3.  Makes it easier to add new
content to the site in a
consistent way
4.  Helps people collaborate
on the design of a site in a
consistent way


****

### CSS Frameworks

* CSS frameworks aim to make your life easier by providing the code for
common tasks, such as creating layout grids, styling forms, creating
printer-friendly versions of pages and so on. You can include the CSS
framework code in your projects rather than writing the CSS from scratch.

**ADVANTAGES**
1. They save you from
repeatedly writing code for
the same tasks.
2. They will have been tested
across different browser
versions (which helps avoid
browser bugs).

**DISADVANTAGES**
1. They often require that you
use class names in your
HTML code that only control
the presentation of the page
(rather than describe its
content).
2. In order to satisfy a wide
variety of needs, they often
contain more code than you
need for your particular web
page (commonly referred to
as code “bloat”).


*Multiple Style Sheets*

There are two ways to add
multiple style sheets to a page:

1.  Your HTML page can link
to one style sheet and that
stylesheet can use the @import
rule to import other style sheets.
2.  In the HTML you can use a
separate `<link>` element for
each style sheet.


***

#### JAVASCRIPT

***Functions are one of the fundamental building blocks in JavaScript. A function in JavaScript is similar to a procedure—a set of statements that performs a task or calculates a value, but for a procedure to qualify as a function, it should take some input and return an output where there is some obvious relationship between the input and the output. To use a function, you must define it somewhere in the scope from which you wish to call it.***

*Functions consist of a series of statements padnousuaag together because they perform a specific task. Amethocis the sameUs function excspt metheds re createdinside (andare.*




 * IN OBJECTS The browser comes with a set of objects that act like a toolkit for creating interactive web pages 



* OBJECTS  you saw that programmers use objects to create models of the world using data, 
  


* A script is made up of a series of statements  Each statement is like a step in a recipe.

* Scripts contain very precise instructions before creating a calculation using that value.
  
* Variables are used to temporarily store pieces of  information used in the script.

**objects & methods**
* This one line of JavaScript shows how to use objects and methods. Programmers refer to this as calling a method of an object.
   - document.write("good morning")

 1. objects :The document object represents the entire web page.  All web browsers implement this object, and you can use it just by giving its name.  OBJECT


 2. methods :The write ( ) method of the document object allows new content to be written into the page where the  script  element sits METHOD Good afternoon 
 
 3. MEMBER OPERATOR ( .) :  The document object has several methods and properties . They are known as members of that object . You can access the members of an object using a dot between the object name and the member you want to access . It is called a member operator

 4. PARAMETERS:  Whenever a method requires some information in order to work , the data is given inside the parentheses . Each piece of information is called porter of the method . In this case , the write ( ) method needs to know what to write into the page .





**The HTML script element is used in HTML pages to tell the browser to load the JavaScript file (rather likethe link element can be used to load a CSS file)**


****

***artical***
 
 1. How does pair programming work?
  * two roles: 
   1. the Driver  : is the programmer who is typing and the only one whose hands are on the keyboard. 
   2. the Navigator : The Navigator uses their words to guide the Driver but does not provide any direct input to the computer

2. Why pair program? 

  * Listening: hearing and interpreting the vocabulary
  * Speaking: using the correct words to communicate an idea
  * Reading: understanding what written language intends to convey
  * Writing: producing from scratch a meaningful


* Pair programming touches on all four skills: 
  1. developers explain out loud what the code should do,
  2. listen to others’ guidance, read code that others have written,
  3.  and write code themselves.
   
1. Greater efficiency

* In reality, when two people focus on the same code base, it is easier to catch mistakes in the making.

2. Engaged collaboration
* When two programmers focus on the same code, the experience is more engaging and both programmers are more focused than if they were working alone.

3. Learning from fellow students
* If one developer has a unique approach to a specific problem, pair programming exposes the other developer to a new solution.

4. Social skills
* Pair programming is great for improving social skills. When working with someone who has a different coding style, communication is key.

5. Job interview readiness

* A common step in many interview processes involves pair programming between a current employee and an applicant, either in person or through a shared screen. They will carry out exercises together, such as code challenges, building a project or feature, or debugging an existing code base. By doing so, companies can get a better feel for how an applicant will fit into the team and their collaboration style.


 6. Work environment readiness
Many companies that utilize pair programing expect to train fresh hires from CS-degree programs on how they operate to actually deliver a product. Code Fellows graduates who are already familiar with how pairing works can hit the ground running at a new job, with one less hurdle to overcome.

