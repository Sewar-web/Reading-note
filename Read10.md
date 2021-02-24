# Erorr & handling & Debugging

* To find the source of an error, it helps to know how scripts are processed.
  
*  In order to create that greeting, two functions are used:
1. greetUser () 
2. getName () 



* To complete step one, the interpreter needs the
results of the functions in steps two and three
(because the message contains values returned by
those functions). The order of execution is more like



1. The greeting variable gets its value from the
greetUser() function.
2. greetUser() creates the message by combining
the string 'He 11 o ' with the result of getName ().
3. getName () returns the name to greetUser().
2. greetUser() now knows the name, and combines
it with the string. It then returns the message to the
statement that called it in step 1.
1. The value of the greeting is stored in memory.
4. This greeting variable is written to an alert box.


**EXECUT.ION CONTEXTS**
The JavaScript interpreter uses the concept of execution contexts.
There is one global execution context; plus, each function creates a new
new execution context. 


**THE STACK**
* the JavaScript interpreter processes one line of code at a time. 
 When a statement needs data from another function, it stacks (or piles) the new function on top of the current task. 
 
  * When a statement has to cal some other code in order to do Its job, the new task goes to the top of the pile of things to do. 
  
  *  Once the new task has been performed the interpreter con go back to the look in hend.  Each time awem is added to the stack, Icesa execution content Variables defined in a function for execution contare only available in the function Wafunction is called

**EXECUTION CONTEXT & HOISTING**

Each time a script enters a new execution context, there are two phases
of activity: 
 1.  PREPARE
 - The new scope is created
 -  Variables, functions, and arguments are created
 -  The value of the this keyword is determined

2.  EXECUTE
- Now it can assign values to variables
- Reference functions and run their code
- Execute statements

 * In the interpreter, each execution context has its own va ri ables object.
It holds the variables, functions, and parameters available within it.
Each execution context can also access its parent's v a ri ables object. 


  **UNDERSTANDING ERRORS**
* If a JavaScript statement generates an error, then it throws an exception.
At that point, the interpreter stops and looks for exception-handl ing code.



**erorre**
* name  : Type of execution
* message:  Description 
* file Number : Name of the JavaScript file
* line Number : Line number of error
  
* Syntax Error
 - SYNTAX IS NOT CORRECT
This is caused by incorrect use of the rules of the
language. It is often the result of a simple typo. 


* ReferenceError
  - VARIABLE DOES NOT EXIST
This is caused by a variable that is not declared or is
out of scope. 

* EvalError
INCORRECT USE OF eval() FUNCTION
The eva l () function evaluates text through the
interpreter and runs it as code (it is not discussed
in this book). It is rare that you would see this type
of error, as browsers often throw other errors when
they are supposed to throw an Eva 1 Error.

* URI Error
INCORRECT USE OF URI FUNCTIONS
If these characters are not escaped in URls, they will
cause an error

* Type Error
VALUE IS UNEXPECTED DATA TYPE
This is often caused by trying to use an object or
method that does not exist. 

* RangeError
NUMBER OUTSIDE OF RANGE
If you call a function using numbers outside of its
accepted range.
CANNOT CREATE ARRAY WITH -1 ITEMS
var anArray = new rray( );
RangeError: Array si ze is not a smal l
enough positive integer 


* Error
GENERIC ERROR OBJECT
The generic Error object is the template (or
prototype) from which all other error objects are
created. 

* NaN
NOT AN ERROR
Note: If you perform a mathematical operation using
a value that is not a number, you end up with the
value of NaN, not a type error. 


***

HOW TO DEAL WITH ERRORS
Now that you know what an error is and how the browser treats them,
there are two things you can do with the errors.

1. DEBUG THE SCRIPT TO FIX ERRORS
If you come across an error while writing a script
(or when someone reports a bug), you will need to
debug the code, track down the source of the error,
and fix it.
You will find that the developer tools available in
every major modern browser will help you with
this task. In this chapter, you will learn about the
developer tools in Chrome and Firefox. (The tools in
Chrome are identical to those in Opera.)
IE and Safari also have their own tools (but there is
not space to cover them all).
@ ERROR HANDLING & DEBUGGING

2.  HANDLE ERRORS GRACEFULLY
You can handle errors gracefully using try, catch,
throw, and f i na 1 ly statements.
Sometimes, an error may occur in the script for a
reason beyond your control. For example, you might
request data from a third party, and their server
may not respond. In such cases, it is particularly
important to write error-handling code.
In the latter part of the chapter, you will learn how to
gracefully check whether something will work, and
offer an alternative option if it fails. 


****

**A DEBUGGING WORKFLOW**

Debugging is about deduction: eliminating potential causes of an error.
Here is a workflow for techniques you will meet over the next 20 pages.
Try to narrow down where the problem might be, then look for clues. 


* WHERE IS THE PROBLEM?
First, should try to can narrow down the area where
the problem seems to be. In a long script, this is
especially important.
1. Look at the error message, it tells you:
• The relevant script that caused the problem.
• The line number where it became a problem for
the interpreter. (As you will see, the cause of
the error may be earlier in a script; but this is the
point at which the script could not continue.)
• The type of error (although the underlying cause
of the error may be different).
2. Check how far the script is running.
Use tools to write messages to the console to tell
how far your script has executed.
3. Use breakpoints where things are going wrong.
They let you pause execution and inspect the values
that are stored in variables.


* WHAT EXACTLY IS THE PROBLEM?
Once you think that you might know the rough area
in which your problem is located, you can then try to
find the actual line of code that is causing the error.
1. When you have set breakpoints, you can see if the
variables around them have the values you would
expect them to. If not, look earlier in the script.
2. Break down I break out parts of the code to test
smaller pieces of the functionality.
• Write values of variables into the console.
• Calrfunctions from the console to check if they
are returning what you would expect them to.
• Check if objects exist and have the methods I
properties that you think they do.
3. Check the number of parameters for a function, or
the number of items in an array.
And be prepared to repeat the whole process if the
above solved one error just to uncover another ...

***

* HOW TO LOOK AT ERRORS
IN CHROME
The console will show you when there is an
error in your JavaScript. It also displays the line
where it became a problem for the interpreter.



* WRITING FROM THE
SCRIPT TO THE CONSOLE
Browsers that have a console have a console object, which has several
methods that your script can use to display data in the console.
The object is documented in the Console API.



***

**MORE CONSOLE METHODS**
1. con so 1 e. info() can be used
for general information
2. consol e.warn() can be used
for warnings
3. console .er ror() can be used
to hold errors



* DEBUGGER KEYWORD
You can create a breakpoint
in your code using just the
debugger keyword. When the
developer tools are open, this
will automatically create a
breakpoint


* TRY, CATCH, FINALLY
This example displays JSON data
to the user. But, imagine that the
data is coming from a third party
and there have been occasional
problems with it that could
cause the page to fail.
This script checks if the JSON
can be parsed using a try block
before trying to display the
information to the users. 

