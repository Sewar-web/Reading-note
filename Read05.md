*# Images
* A picture can say a thousand words, and great
images help make the difference between an
average-looking site and a really engaging one.

* Images can be used to set the
tone for a site in less time than
it takes to read a description.

**Images should**
 1. Be relevant
 2. Convey information
 3. Convey the right mood
 4. Be instantly recognisable
 5. Fit the color palette


* If you are using a content
management system or blogging
platform, there are usually tools
built into the admin site that
allow you to upload images,
and the program will probably
already have a separate folder
for image files and any
other uploads.

**Adding Images**

1. `<img>`
* To add an image into the page
you need to use an `<img>`
element


*  It must carry the
following two attributes:

1. src : This tells the browser where
it can find the image file. This
will usually be a relative URL
pointing to an image on your
own site


2. alt : This provides a text description
of the image which describes the
image if you cannot see it.


3. title : You can also use the title
attribute with the `<img>` element
to provide additional information
about the image


**Height & Width of Images**
1. height
This specifies the height of the
image in pixels.

2. width
This specifies the width of the
image in pixels.

* Images often take longer to
load than the HTML code that
makes up the rest of the page.
It is, therefore, a good idea to
specify the size of the image
so that the browser can render
the rest of the text on the page
while leaving the right amount of
space for the image that is still
loading.


**align** 
- The align attribute was
commonly used to indicate how
the other parts of a page should
flow around an image.

1. left
This aligns the image to the left
(allowing text to flow around its
right-hand side).

2. right
This aligns the image to the right
(allowing text to flow around its
left-hand side)

* There are three values that the
align attribute can take that
control how the image should
align vertically with the text that
surrounds it:

1. top
This aligns the first line of the
surrounding text with the top of
the image.

2. middle
This aligns the first line of the
surrounding text with the middle
of the image.

3. bottom
This aligns the first line of the
surrounding text with the bottom
of the image.


*Three Rules for Creating Images*

 1. Save images inthe right format
 2. Save images at the right size
 3. Use the correct resolution

**Cropping Images**
 When cropping images it is important not to
lose valuable information. It is best to source
images that are the correct shape if possible


* JPGs, GIFs, and PNGs belong to
a type of image format known
as *bitmap*


*  pixels : Images appearing on computer
screens are made of tiny squares


**Vector**
 images differ from bitmap images and
are resolution-independent. Vector images are
commonly created in programs such as Adobe
Illustrator.

* Vector images are created by
placing points on a grid, and
drawing lines between those
points. A color can then be
added to "fill in" the lines that
have been created.

* The advantage of creating line
drawings in vector format is that
you can increase the dimensions
of the image without affecting
the quality of it.

**Animated GIFs**
Animated GIFs show several frames of an
image in sequence and therefore can be used to
create simple animations.


 * Transparent GIF :

If the transparent part of the
image has straight edges and
it is 100% transparent (that is,
not semi-opaque), you can save
the image as a GIF (with the
transparency option selected).

* PNG :
If the transparent part of the
image has diagonal or rounded
edges or if you want a semiopaque transparency or a dropshadow, then you will need to
save it as a PNG.


## Color

* The color property allows you
to specify the color of text inside
an element. You can specify any
color in CSS in one of three ways:

1. rgb values
These express colors in terms
of how much red, green and
blue are used to make it up. For
example: rgb(100,100,90)

2. hex codes
These are six-digit codes that
represent the amount of red,
green and blue in a color,
preceded by a pound or hash #
sign. For example: #ee3e80 

3. color names
There are 147 predefined color
names that are recognized
by browsers. For example:
DarkCyan


***background-color***

* You can specify your choice of
background color in the same
three ways you can specify
foreground colors: RGB values,
hex codes, and color names
(covered on the next page).

* By default, most browser
windows have a white
background, but browser users
can set a background color for
their windows

**Every color on a computer screen is created by mixing amounts of red, green, and blue. To find the color you want, you can use a color picker.**


*HSL Colors*
1. hue
Hue is the colloquial idea of
color. In HSL colors, hue is often
represented as a color circle
where the angle represents the
color, although it may also be
shown as a slider with values
from 0 to 360.

2. saturation
Saturation is the amount of
gray in a color. Saturation is
represented as a percentage.
100% is full saturation and 0%
is a shade of gray.

3. lightness
Lightness is the amount of
white (lightness) or black
(darkness) in a color. Lightness
is represented as a percentage.
0% lightness is black, 100%
lightness is white, and 50%
lightness is normal. Lightness
is sometimes referred to as
luminosity



# TEXT

* When creating a web page, you add TAGS
Tags known as: MARKUPS
This chapter will cover Text Markups


***

1. Structural markup:
Allow browsers to show users the appropriate structure for the page. It describes the structure of page .


2. Semantic markup:
* Doesn’t affect the structure of web pages 
*  Provides extra information and meaning and description of content .

**Structural markups**
1. Headings
HTML has six “levels” of headings
<h1> <h2> .....<h6>
<h1> : main headings
<h2> : subheadings


2. Paragraphs
`<p>` your paragraph ..... `</p>`

* browser will show each paragraph on a new line with some space between it and any following paragraphs.




3. Bold
* text `<b>` bold texts... `</b>` text
* Make characters appear bold.
* Used for Keywords
* Does not imply any additional meaning.



3. Italic
* text `<b>` bold texts... `</b>` text
* Make characters appear bold.
Used for
   - Technical terms
   - Names of ships,
   - Foreign words




4. Super-script and Sub-script
* Superscript
  - The 4<sup>th</sup> of October
  - Contain characters slightly above the normal line
  - suffixes of dates or mathematical concepts like (power)

* Subscript
  - The H<sub>2</sub>O
  - Contain characters slightly below the normal line
  - Chemical formulas such as H20






**White Space**
* What’s White Space?
  a Text composed only of spaces, tabs or line breaks




*What’s White space collapsing?*
* browser completely ignore white spaces .

* Two or more spaces next to each other —-> only one space displayed

* linevbreak —-> only one space displayed

* Makes code easier to read







5.Line Breaks and Horizontal Rules
* `<br>` Add a line break inside the middle of a paragraph
* `<hr>` add a ruler . Used as a break .



**Empty elements**
* elements that do not have words between an opening and closing tag.
Like `<img>` , `<br>` , `<hr>`
* GOOD PRACTICE : add space and a forward slash like :
`<br>` same as `<br />`




2. Semantic markup:
  * Purpose : Describe the content of your web pages


  * Shouldn’t use them to change the way that your text looks .


  * WHY? : Used for programs like screen readers or search engines .


* HOW? They use the extra information. For example:
voice of a screen reader may add emphasis to the words inside the
search engine might register that the page has a quote if you use the `<blockquote>`







1. Strong & Emphasis
`<strong> </strong>`
* indicates that content has strong importance
* will show the contents in bold
* `<em> </em>`
* Changes the meaning of a sentence (depending on what word in the sentence is Italic).









1. Qoutations
* used for marking up quotations:
`<blockquote> </blockquote>`
used for longer quotes that take up an entire paragraph.

* `<p>` tag still used inside .
it indent the paragraph (push it away . adds a margin)




* `<q> </q>`

  - used for shorter quotes

  - most browsers put quotes around the content














