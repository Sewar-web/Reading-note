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