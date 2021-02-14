# HTML & CSS

**When the web was first taking
off, one of the most common
ways to learn about HTML and
discover new tips and techniques
was to look at the source code
that made up web pages.
These days there are many
more books and online tutorials
that teach HTML, but you can
still look at the code that a web
server sends to you**


* HTML pages are text documents.
  
*  HTML uses tags (characters that sit inside angled
brackets) to give the information they surround special
meaning.

*  Tags are often referred to as elements.
  
*  Tags usually come in pairs. The opening tag denotes
the start of a piece of content; the closing tag denotes
the end.

*  Opening tags can carry attributes, which tell us more
about the content of that element.

*  Attributes require a name and a value.
  
*  To learn HTML you need to know what tags are
available for you to use, what they do, and where they
can go.

 *****

## TEXT

* When creating a web page, you add tags
(known as markup) to the contents of the
page. These tags provide extra meaning
and allow browsers to show users the
appropriate structure for the page.


1. Structural markup: the elements that you can use to
describe both headings and paragraphs

2.  Semantic markup: which provides extra information; such
as where emphasis is placed in a sentence, that something
you have written is a quotation (and who said it), the
meaning of acronyms, and so on

  **Headings**

 * HTML has six "levels" of
headings:
  - h1 is used for main headings
  - h2 is used for subheadings
  - and so on
  
* Browsers display the contents of
headings at different sizes. The
contents of an <h1> element is
the largest, and the contents of
an <h6> element is the smallest.

****
**Paragraphs**

* To create a paragraph, surround
the words that make up the
paragraph with an opening <p>
tag and closing </p> tag.

***Bold & Italic***
 
* b :<b>
By enclosing words in the tags
<b> and </b> we can make
characters appear bold.
The <b> element also represents
a section of text that would be
presented in a visually different
way (for example key words in a
paragraph) although the use of
the <b> element does not imply
any additional meaning 


* i : By enclosing words in the tags
<i> and </i> we can make
characters appear italic.
The <i> element also represents
a section of text that would be
said in a different way from
surrounding content — such as
technical terms, names of ships,
foreign words, thoughts, or other
terms that would usually be
italicized.


**Superscript & Subscrip**

1. sup :The <sup> element is used
to contain characters that
should be superscript such
as the suffixes of dates or
mathematical concepts like
raising a number to a power such
as 22
.
2. sub :The <sub> element is used to
contain characters that should
be subscript. It is commonly
used with foot notes or chemical
formulas such as H2o


**White Space**
In order to make code easier to
read, web page authors often
add extra spaces or start some
elements on new lines.
When the browser comes across
two or more spaces next to each
other, it only displays one space



**Line Breaks & Horizontal Rules**

1. line breaks :
   <br />
As you have already seen, the
browser will automatically show
each new paragraph or heading
on a new line. But if you wanted
to add a line break inside the
middle of a paragraph you can
use the line break tag <br />.


2. horizontal rules :
   <hr />
To create a break between
themes — such as a change of
topic in a book or a new scene
in a play — you can add a
horizontal rule between sections
using the <hr /> tag.



**Visual Editors & Their Code views**
1. Visual editors often resemble
word processors. Although
each editor will differ slightly,
there are some features that
are common to most editors
that allow you to control the
presentation of text.
  - example  :
  - Headings are created by
highlighting text then using
a drop-down box to select a
heading.
 - Bold and italic text are
created by highlighting some
text and pressing a b or i
button.
- New paragraphs are created
using the return or the enter
key.
- Line breaks are created by
pressing the shift key and the
return key at the same time.
- Horizontal rules are created
using a button with a straight
line on it.


2. Code views show you the code
created by the visual editor so
you can manually edit it, or so
you can just enter new code
yourself. It is often activated
using a button with an icon
that says HTML or has angled
brackets. White space may be
added to the code by the editor
to make the code easier to read.


**Semantic Markup**
 semantic markup : There are some text elements that are not intended to affect the
structure of your web pages, but they do add extra information to the
pages 

* <em>
element is shown in italics

* a <blockquote> is usually
indented.


**Strong & Emphasis**
1. strong:
The use of the strong
element indicates that its
content has strong importance.
For example, the words
contained in this element might
be said with strong emphasis.
By default, browsers will show
the contents of a strong
element in bold

2. em :
The em element indicates
emphasis that subtly changes
the meaning of a sentence.
By default browsers will show
the contents of an em element
in italic




**Quotations**
There are two elements
commonly used for marking up
quotations:
  
  1. blockquote :
The blockquote element is
used for longer quotes that take
up an entire paragraph. Note
how the <p> element is still
used inside the blockquote
element.
Browsers tend to indent the
contents of the blockquote
element, however you should not
use this element just to indent a
piece of text — rather you should
achieve this effect using CSS. 


2. q :
The q element is used for
shorter quotes that sit within
a paragraph. Browsers are
supposed to put quotes around
the q element, however
Internet Explorer does not —
therefore many people avoid
using the q element.



**Abbreviations & Acronyms**

1. abbr 
If you use an abbreviation or
an acronym, then the abbr
element can be used. A title
attribute on the opening tag is
used to specify the full term

2.  acronym  :
 element for
acronyms. To spell out the full
form of the acronym, the title
attribute was used (as with the
abbr element above). HTML5
just uses the abbr element
for both abbreviations and
acronyms. 


**Citations & Definitions**
1. cite:
When you are referencing a
piece of work such as a book,
film or research paper, the
cite element can be used
to indicate where the citation is
from.
In HTML5, cite should not
really be used for a person's
name — but it was allowed in
HTML 4, so most people are
likely to continue to use it. 

2. dfn
The first time you explain some
new terminology (perhaps an
academic concept or some
jargon) in a document, it is
known as the defining instance
of it.
The dfn element is used to
indicate the defining instance of
a new term.
Some browsers show the
content of the dfn element in
italics. Safari and Chrome do not
change its appearance.

****

# javascript

**objects & methods**
* This one line of JavaScript shows how to use objects and methods. Programmers refer to this as calling a method of an object.
   - document.write("good morning")

 1. objects :The document object represents the entire web page.  All web browsers implement this object, and you can use it just by giving its name.  OBJECT


 2. methods :The write ( ) method of the document object allows new content to be written into the page where the  script  element sits METHOD Good afternoon 
 
 3. MEMBER OPERATOR ( .) :  The document object has several methods and properties . They are known as members of that object . You can access the members of an object using a dot between the object name and the member you want to access . It is called a member operator

 4. PARAMETERS:  Whenever a method requires some information in order to work , the data is given inside the parentheses . Each piece of information is called porter of the method . In this case , the write ( ) method needs to know what to write into the page .





**The HTML script element is used in HTML pages to tell the browser to load the JavaScript file (rather likethe link element can be used to load a CSS file)**

**script : A script is a series of instructions that a computer can follow one-by-one. Each individual instruction or step is known as a statement. Statements should end with a semicolon.**


*comments*
it's help to :
1. You should write comments to explain what your code does.
2. They help make your code easier to read and understand.
3. This can help you and others who read your code.

there tow way to write comments
1. // single statement
2. /* */ multi statement
   

**VARIABLE**

A script will have to temporarily
store the bits of information it
needs to do its job. It can store this
data in variables.

* how to declare varibale :
  var varibale name = the varibale value


  **data types**
  1. string : letters and other characters. 
  2. number : 1,15..
  3. boolean : true ,false


* CHANGING THE VALUE OF A VARIABLE
Once you have assigned a value to a variable, you can then change what is stored in the variable later in the same script.
Once the variable has been
created, you do not need to
use the var keyword to assign
it a new value. You just use the
variable name, the equals sign
(also known as the assignment
operator), and the new value for
that attribute.



**RULES FOR NAMING VARIABLES**
1. The name must begin with
a letter, dollar sign ($),or an
underscore (_). It must not start
with a number.
2. The name can contain letters,
numbers, dollar sign ($), or an
underscore (_). Note that you
must not use a dash(-) or a
period (.) in a variable name. 
 
3. You cannot use keywords or
reserved words. Keywords
are special words that tell the
interpreter to do something. For
example, var is a keyword used
to declare a variable. Reserved
words are ones that may be used
in a future version of JavaScript. 

4. All variables are case sensitive,
so score and Score would be
different variable names, but
it is bad practice to create two
variables that have the same
name using different cases. 

5. Use a name that describes the
kind of information that the
variable stores. For example,
fi rstName might be used to
store a person's first name,
l astNarne for their last name,
and age for their age

6. If your variable name is made
up of more than one word, use a
capital letter for the first letter of
every word after the first word.
For example, f i rstName rather
than fi rstnarne (this is referred
to as camel case). You can also
use an underscore between each
word (you cannot use a dash)


**arrays**

An array  : is a special type of variable. It doesn't
just store one value; it stores a list of values. 


*Arrays are especially helpful when you do not know how many items a list will contain because, when you create the array, you do not need to specify how many values it will hold.*

 how creat array:

 var colors;
colors ['white', 'black', ' custom'];
var el document.getElementByld('col ors');
el . textContent = col ors[O];


**EXPRESSIONS**
An expression evaluates into (results in) a single value. Broadly speaking
there are two types of expressions. 

1. EXPRESSIONS THAT JUST ASSIGN A
VALUE TO A VARIABLE

2. EXPRESSIONS THAT USE TWO OR
MORE VALUES TO RETURN A
SINGLE VALUE


* ASSIGNMENT OPERATORS : Assign a value to a variable 
  color = 'beige';

* ARITHMETIC OPERATORS : Perform basic math 
 area = 3 * 2;


* COMPARISON OPERATORS : Compare two values and return true or false 
 buy = 3 > 5; 

* LOGICAL OPERATORS : Combine expressions and return true or false
  buy= (5 > 3) && (2 < 4); 

  * STRING OPERATORS : Combine two strings
greeting= 'Hi 1 + 'Mol ly'; 



ARITHMETI C OPERATORS :
1. +
2. -
3. /
4. *
5. ++
6. --
7. %
   


   ***SWITCH STATEMENTS***

**A switch statement starts with a variable called the switch value. Each case indicates a possible value for this variable and the code that should run if the variable matches that value.**


**CREATING A DATE OBJECT**
 1.  a new Date
object is created using the
Date {) object constructor
It is called today
2. If you do not specify a date
when creating a Date object, it
will contain the date and time
when the JavaScript interpreter
encounters that line of code
3. Once you have an instance of the
Date object (holding the current
date and time), you can use any
of its properties or methods



#### Functions 

***Functions are one of the fundamental building blocks in JavaScript. A function in JavaScript is similar to a procedure—a set of statements that performs a task or calculates a value, but for a procedure to qualify as a function, it should take some input and return an output where there is some obvious relationship between the input and the output. To use a function, you must define it somewhere in the scope from which you wish to call it.***

*Functions consist of a series of statements padnousuaag together because they perform a specific task. Amethocis the sameUs function excspt metheds re createdinside (andare.*




 * IN OBJECTS The browser comes with a set of objects that act like a toolkit for creating interactive web pages 



* OBJECTS  you saw that programmers use objects to create models of the world using data, 
  


* A script is made up of a series of statements  Each statement is like a step in a recipe.

* Scripts contain very precise instructions before creating a calculation using that value.
  
* Variables are used to temporarily store pieces of  information used in the script.
  



**DECISION MAKING**
 There are often several places in a script where decisions are made that determine which lines of code should be run next. Flowcharts can help you plan for these occasions.


 There are two components to a decision: 
 1. An expression is evaluated, which returns a value 
 2.  A conditional statement says what to do in a given situa


***You can evaluate a situation by comparing one value in the script to what you expect it might be. The result will be a Boolean: true or false***

1. == : This operator compares two values (numbers, strings, or Booleans) to see if they are the same

2. != : This operator compares two values (numbers, strings, or Booleans) to see if they are not the same

3. === : This operator compares two values to check that both the data type and value are the same.

4. !== : This operator compares two values to check that both the data type and value are not the same.

5. > : greater than This operater checks if the number on the let is greater than the number  on the right

6. < : less than This operater checks if the number on the let is less than the number  on the right

7.  >= : greater than or aqual to  This operator checks if the number on the left is greater than or aqual to the number on the right.

8.  <= : less than  or aqual to This operator checks if the number on the left is less than or aqual to the number on the right.




**IF ,ELSE STATMENT**

*if ,eLse statement allows you to provide two sets of code:

* one set if the condition evaluates to true

* another set if the condition is false*

* note all the statment inside the if should be followed by ;



  **SWITCH STATEMENTS**
* A switch statement starts with a variable called the switch value. Each case indicates a possible value for this variable and the code that should run if the variable matches that value.

* the struct of switch : switch () { case ' ': break; case '': break; default : break; } 















 