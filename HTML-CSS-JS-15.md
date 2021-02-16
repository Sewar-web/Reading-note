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







2. Abbreviations & Acronyms
* `<abrr> </abbr>`
* Used for Abbriviations (eg. Doctor - Dr ) and Acronyms (eg. USA - United States of America)
* It shows a description when you mouse over the element.
* Needs “title=” attribute .


3. Citations & Definitions
*`<cite> </cite>`
* Used when mentioning a book name, movie, name of a published paper
* content will appear italic
* <cite>A Brief History of Time</cite> by Stephen Hawking has sold over...
`<dfn> </dfn>`
* Used when defining new term
* A <dfn>black hole</dfn> is a region of space


4. Author Details
contain contact details for the author of the page (his address, email, phone number).

<address> 742 Evergreen Terrace, Springfield.</address>



5. Changes to Content
* `<ins> </ins>`
* used to show content that has been inserted into a document
* appears Underlined
* `<del> </del>`
* to show deleted text
* appears with a line crosssing though it
* `<s> </s>`
* indicates something that is no longer accurate or relevant
* appears with crossed line



## Lists

 * There are three types of HTML lists: 
  1. ordered
  2.  unordered
  3.  definition.

*Ordered Lists*

* Ordered lists use numbers.
  - Each item in the list is numbered.

* created withthe `<ol> `element.

* Each item in the list is placed like this : `<li>` item1 `</li>`

*The li stands for “list item”*

* Unordered Lists
*  Unordered lists use bullets.
*  Items begin with a bullet point (rather than characters that indicate order).
* created withthe `<ul>` element.
* Each item in the list is placed like this : `<li>` item1 `</li>`
  
  *Definition Lists*
  
* Used to define terminology.
* consists of a series of terms and their definitions.
* created with `<dl>` element .
* `<dt>` Term1 `</dt>` used to contain the term being defined
* `<dd>` definition1 `</dd>` used to contain the definition.
  

**Nested Lists**
* Also called “Sub-lists”
* add a list inside <li> element .
* Browsers display nested lists indented further than the parent list.
* browser will change the style of the bullet .
  

**CSS BOXES**

* Boxes Dimentions
 1. use height and width properties.

2. use pixels, percentages, or ems.

3. pixels: allow accurately control size.

4. percentages : size of the box is relative to browser window size or size of the containing box.

5. percentage and ems are flexible with different-sized screens.

**Overflowing Content**
The overflow property tells the browser what to do if the content contained within a box is larger than the box itself. It can have one of two values

1. hidden
2. scroll


 **Border, Margin & Padding**

* Every box has three available properties that can be adjusted to control its appearance:
1. Border
  Every box has a border (even if it is not visible or is specified to be 0 pixels wide). The border separates the edge of one box from another.

2. Margin
  Margins sit outside the edge of the border. You can set the width of a margin to create a gap between the borders of two adjacent boxes.

3. Padding
  Padding is the space between the border of a box and any content contained within it. Adding padding can increase the readability of its contents.



**Border**
1. border-width
2. border-style
3. border-color
4. Shorthand border : The border property allows you to specify the width, style and color of a border in one property (and the values should be coded in that specific order).


**Centering Content :**

1. If you want to center a box on the page (or center it inside the element that it sits in):

2. set the left-margin and right-margin to auto.

3. set a width or the box (otherwise it will take up the full width of the page).

* In order for this to work in older browsers, the element that the box sits inside should have a text-align property set to center.



## CSS

* What Does CSS Do?
  - CSS allows you to create rules that specify how the content of an element should appear .


* How CSS works?
  - The key to understanding how CSS works is to imagine that there is an invisible box around every HTML element .


* BLOCK & INLINE ELEMENTS
  - Every HTML element has a default display value, depending on what type of element it is.


* There are two display values: block and
 - Block level elements :
 - always start on a new line .
- Takes up the full width available .
 - Has default TOP and BOTTOM Margin (16px) .
`<h1>-<h6>`, `<p>` and `<div>` .

* Inline elements:
* Does not start on a new line (flow within the text)
* only takes up as much width as necessary.
* doesn’t have a default margin .

* `<b>, <i>, <img>, <em> and <span>`
  

**Style Rules**

* These rules govern how element’s content should be displayed.
* A CSS rule contains two parts:
1. selector: indicate which element the rule applies to .
2. declaration: how the selected elements should be styled.


* Declarations sit inside curly brackets and each is made up of two parts: a property and a value, separated by a colon







### JavaScript

* What is a script?
 A script is a series of instructions that a computer can follow step-by-step to achieve a goal.

* You could compare scripts to : RECIPES , HANDBOOKS, MANUALS .



* How do I creat a Script?


1. DEFINE THE GOAL
 - To write a script, you need to first state your goal and then list the tasks that need to be completed in order to achieve it.

2. DESIGN THE SCRIPT
 - You can use flowcharts to work out how the tasks fit together. The flowcharts show the paths between each step.


3.  CODE EACH STEP




**EXPRESSIONS**
* An expression results in a single value. There are two types of expressions:

1. EXPRESSIONS THAT JUST ASSIGN A VALUE TO A VARIABLE:
    - var color = 'beige' ;

2. EXPRESSIONS THAT USE TWO OR MORE VALUES TO RETURN A SINGLE VALUE:
    - var area = 3 * 2;

**OPERATORS**
* Expressions rely on operators to calculate a value.



1. ASSIGNMENT OPERATORS
 - color = 'beige';

2. ARITHMETIC OPERATORS
 - area = 3 * 2;

3. STRING OPERATORS
 - greeting= 'Hi 1' + 'Mol ly'

4. COMPARISON OPERATORS
 - buy = 3 > 5;

5. LOGICAL OPERATORS
 - buy= (5 > 3) && (4>2);




**Comparsion Operators**
* Here are the common comparsion operators in programming:
1. Less than (<)
2. Greater than (>)
3. Less than or equal to (<=)
4. Greater than or equal to (>=)
5. Equal to (==)
6. Not equal to (!==)
7. Strict Equal to (===)
8. Strict Not Equal to (!==)



**Logical Operators**
 * Here are the common Logical operators in programming, they usually return True or False


1. || (Logical OR)
  * In classical programming, the logical OR is meant to manipulate boolean values only. If any of its arguments are true, it returns true, otherwise it returns false.

2. && ( Logical AND)
   * In classical programming, AND returns true if both operands are truthy and false otherwise

3.  ! (Logical Not)
   * Converts the operand to boolean type: true/false.
Returns the inverse value.



***Loops***
1. For Loop
 * Used if you need to run a code a specific number of times .
2. While Loop
 * Used if you don’t know how many times the code should run.
3. .Do While
   * Similar to While . It will always run the statement at least once even if the condition is false.


**Loop Counters**
 * For uses counters as a condition, this allows it to run a specified number of times .

* Condition made of 3 statements:
1. Initialization
2. Condition
3. Update
   
   
* SWITCH STATEMENTS
  - A switch statement starts with a variable called the switch value. Each case indicates a possible value for this variable and the code that should run if the variable matches that value.