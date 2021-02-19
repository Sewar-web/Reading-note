# Images
* A picture can say a thousand words, and great
images help make the difference between an
average-looking site and a really engaging one.

* Images can be used to set the
tone for a site in less time than
it takes to read a description

 *Storing Images on Your Site*
 * If you are building a site from scratch, it is good
practice to create a folder for all of the images
the site uses.
 

 **Adding Images**


* `<img>` 
* To add an image into the page
you need to use an `<img>`
element. This is an empty
element (which means there is
no closing tag). It must carry the
following two attributes:

1. src
This tells the browser where
it can find the image file. This
will usually be a relative URL
pointing to an image on your
own site.

2. alt
This provides a text description
of the image which describes the
image if you cannot see it.


3. title
You can also use the title
attribute with the `<img>` element
to provide additional information
about the image. Most browsers
will display the content of this
attribute in a tootip when the
user hovers over the image.


**Height & Width of Images**
 1. height
This specifies the height of the
image in pixels.

2. width
This specifies the width of the
image in pixels.


**Where to Place Images in Your Code**
1.  before a paragraph
2.  
The paragraph starts on a new
line after the image.

2. inside the start of a paragraph
   
The first row of text aligns with
the bottom of the image.

3. in the middle of a paragraph

The image is placed between the
words of the paragraph that it
appears in

 **Aligning Images Horizontally**
 * align : 
The align attribute was
commonly used to indicate how
the other parts of a page should
flow around an image.


* The align attribute can take
these horizontal values:
1. left
This aligns the image to the left
(allowing text to flow around its
right-hand side).

2. right
This aligns the image to the right
(allowing text to flow around its
left-hand side).
 


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


**Three Rules for Creating Images**
1. Save images in the right format

2. Save images at the right size
   
3. Use the correct resolution


**Image Dimensions**
The images you use on your website should be
saved at the same width and height that you
want them to appear on the page


* When <strong>cropping images <strong>it is important not to
lose valuable information. It is best to source
images that are the correct shape if possible.


* bitmap : JPGs, GIFs, and PNGs belong to
a type of image format 

* The resolution of an image is the
number of squares that fit within
a 1 inch x 1 inch square area.


* pixels : Images appearing on computer
screens are made of tiny squares


* Vector images differ from bitmap images and
are resolution-independent. Vector images are
commonly created in programs such as Adobe
Illustrator.

1. Vector images are created by
placing points on a grid, and
drawing lines between those
points.  

* Animated GIFs show several frames of an
image in sequence and therefore can be used to
create simple animations.


***

## color 
* The color property allows you
to specify the color of text inside
an element. You can specify any
color in CSS in one of three ways:**

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
We look at these three different
ways of specifying colors on the
next double-page spread.

 **background-color**

* You can specify your choice of
background color in the same
three ways 
1. background-color: rgb(200,200,200);

2. background-color: DarkCyan
   
3. background-color: #ee3e80
   
*  defulat color :background-color: white 

*Every color on a computer screen is created by mixing amounts of red,
green, and blue. To find the color you want, you can use a color picker.*


 * pixels : Computer monitors are made
up of thousands of tiny squares

* The color of every pixel on the
screen is expressed in terms of
a mix of red, green, and blue —
just like on a television screen.

* Color picking tools are available
in image editing programs like
Photoshop and GIMP. You can
see the RGB values specified
next to the radio buttons that
say R, G, B.

* The hex value is provided
next to the pound or hash
 symbol. There is also a
good color picking tool at:

[colorschemedesigner](https://paletton.com/#uid=1000u0kllllaFw0g0qFqFg0w0aF)


1. RGB Values
Values for red, green, and blue
are expressed as numbers
between 0 and 255. 
rgb(102,205,170)
This color is made up of the
following values:
102 red
205 green
170 blue

2. Hex Codes
Hex values represent values
for red, green, and blue in
hexadecimal code.
#66cdaa
The value of the red, 102, is
expressed as 66 in hexadecimal
code. The 205 of the green is
expressed as cd and the 170 of
the blue equates to aa.


3. Color Names
Colors are represented by
predefined names. However,
they are very limited in number.
MediumAquaMarine
There are 147 color names
supported by browsers (this
color is MediumAquaMarine).
Most consider this to be a
limited color palette, and it is
hard to remember the name for
each of the colors so (apart from
white and black) they are not
commonly used.


4. Hue
Hue is near to the colloquial idea
of color. Technically speaking
however, a color can also have
saturation and brightness as
well as hue.

5. Saturation
Saturation refers to the amount
of gray in a color. At maximum
saturation, there would be no
gray in the color. At minimum
saturation, the color would be
mostly gray.

6. Brightness
Brightness (or "value") refers
to how much black is in a color.
At maximum brightness, there
would be no black in the color.
At minimum brightness, the
color would be very dark.


  **When picking foreground and background colors, it is important to ensure that there is enough contrast for the text to be legible.**


* CSS3 introduces an entirely new and intuitive
way to specify colors using hue, saturation,
and lightness values.

1. hue
Hue is the colloquial idea of
color. In HSL colors, hue is often
represented as a color circle
where the angle represents the
color, although it may also be
shown as a slider with values
from 0 to 360

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
luminosity.


**example of color :**

 1. background-color: rgb(84,182,237)

 2. background-color: rgb(48,170,233)

 3. background-color: #ffffff;

 4. background-color: hsla(0,100%,100%,0.5);

 

 * Color not only brings your site to life, but also helps
convey the mood and evokes reactions.

* There are three ways to specify colors in CSS:
RGB values, hex codes, and color names.
* Color pickers can help you find the color you want.
  
* It is important to ensure that there is enough contrast
between any text and the background color (otherwise
people will not be able to read your content).

* CSS3 has introduced an extra value for RGB colors to
indicate opacity. It is known as RGBA.

* X CSS3 also allows you to specify colors as HSL values,
with an optional opacity value. It is known as HSLA.


*** 

### TEXT

* When creating a web page, you add TAGS
Tags known as: MARKUPS
This chapter will cover Text Markups

  **Typeface Terminology**
 1. Serif
Serif fonts have extra details on
the ends of the main strokes of
the letters. These details are
known as serifs.


2. Sans-Serif
Sans-serif fonts have straight
ends to letters, and therefore
have a much cleaner design.


3. Monospace
Every letter in a monospace (or
fixed-width) font is the same
width. (Non-monospace fonts
have different widths.)


 *There are several ways to use fonts other than those listed on the previous page. However, typefaces are subject to copyright, so the techniques you can choose from are limited by their respective licenses.: *

 1. font-family :
   The user's computer needs the
typeface installed. CSS is used to
specify the typeface.

* The font-family property
allows you to specify the
typeface that should be used for
any text inside the element(s) to
which a CSS rule applies.

  - src
This specifies the path to the
font. In order for this technique
to work in all browsers, you will
probably need to specify paths
to a few different versions of the
font, as shown on the next page.
  - format
This specifies the format that the
font is supplied in. (It's discussed
in detail on the next page.)

 2. font-face :
CSS specifies where a font can
be downloaded from if it is not
installed on the computer.

* The font-size property enables
you to specify a size for the
font. There are several ways to
specify the size of a font. The
most common are:

1. pixels
Pixels are commonly used
because they allow web
designers very precise control
over how much space their text
takes up. The number of pixels is
followed by the letters px.

2. percentages
The default size of text in
browsers is 16px. So a size of
75% would be the equivalent of
12px, and 200% would be 32px.

3. ems
An em is equivalent to the width
of a letter m.



*  3. Service-based Font-Face:

Commercial services give users
access to a wider range of fonts
using @font-face.


**Understanding Font Format**

* Different browsers support
different formats for fonts
(in the same way that they
support different audio and
video formats), so you will need
to supply the font in several
variations to reach all browsers


**Bold**
The font-weight property
allows you to create bold text.
There are two values that this
property commonly takes:

1. normal
This causes text to appear at a
normal weight.
2. bold
This causes text to appear bold.
In this example, you can see
that the element whose class
attribute has a value of credits
has been bolded.


**Italic**

If you want to create italic text,
you can use the font-style
property. There are three values
this property can take:

1. normal
This causes text to appear in a
normal style (as opposed to italic
or oblique).

2. italic
This causes text to appear italic.

3. oblique
This causes text to appear
oblique.

**UpperCase & LowerCase**
1. uppercase
This causes the text to appear
uppercase.

2. lowercase
This causes the text to appear
lowercase.

*text-decoration property*
* The text-decoration property
allows you to specify the
following values:
1. none
This removes any decoration
already applied to the text.

2. underline
This adds a line underneath the
text.

3. overline
This adds a line over the top of
the text.

4. line-through
This adds a line through words.

5. blink
This animates the text to make it
flash on and off (however this is
generally frowned upon, as it is
considered rather annoying).


**letter-spacing, word-spacing**

1. It is particularly helpful to
increase the kerning when
your heading or sentence is
all in uppercase. If your text is
in sentence (or normal) case,
increasing or decreasing the
kerning can make it harder to
read.

2. You can also control the gap
between words using the
word-spacing property

**text-align**

* The text-align property allows
you to control the alignment of
text. The property can take one
of four values:
1. left
This indicates that the text
should be left-aligned.

2. right
This indicates that the text
should be right-aligned.

3. center
This allows you to center text.

4. justify
This indicates that every line in
a paragraph, except the last line,
should be set to take up the full
width of the containing box


***vertical-align***

* The vertical-align property is
a common source of confusion.
It is not intended to allow you to
vertically align text in the middle
of block level elements



**The text-indent**
 * property allows you to indent the first
line of text within an element.
The amount you want the line
indented by can be specified in
a number of ways but is usually
given in pixels or ems.

* It can take a negative value,
which means it can be used
to push text off the browser
window



**The text-shadow**
* property has become commonly used despite lacking support in all browsers.It is used to create a drop shadow, which is a dark version of the word just behind it andslightly offset. It can also be used to create an embossed effect byadding a shadow that is slightlylighter than the text.


* :hover
This is applied when a user
hovers over an element with a
pointing device such as a mouse.
This has commonly been used
to change the appearance of
links and buttons when a user
places their cursor over them


* :active
This is applied when an element
is being activated by a user; for
example, when a button is being
pressed or a link being clicked.


* :focus
This is applied when an element
has focus. Any element that
you can interact with, such as a
link you can click on or any form
control can have focus

**JPEG** is a lossy compression specification that takes advantage of human perception. It can achieve compression ratios of 1:10 without any perceivable difference in quality. Beyond this, the compression artefacts become more prominent. Because JPEG compression works by averaging out colours of nearby pixels (read Discrete Cosine Transform), JPEG images are best suited for photographs and paintings of natural scenes where the variations in colour and intensity are smooth. However, if an image contains text or lines, where a sharp contrast between adjacent pixels is desired to highlight the proper shape, this lossy compression technique does not yield good results.



**PNG** is a lossless image format using DEFLATE compression. No data is lost during compression and no compression artefacts are introduced in the image. For this reason, a PNG image would retain higher quality than an image than JPEG and would look a lot sharper, it would also occupy more space on the disk. This makes it unsuitable for storing or transferring high-resolution digital photographs but a great choice for images with text, logos and shapes with sharp edges.



**GIF** is also a lossless image format that uses LZW compression algorithm. It was favoured over PNG for simple graphics in websites in its early days because the support of PNG was still growing. Given that PNG is now supported across all major devices and that PNG compression is about 5–25% better than GIF compression, GIF images are now mainly used only if the image contains animations.





















