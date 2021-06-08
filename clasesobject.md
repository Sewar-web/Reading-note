# Classes and Objects

- Objects are an encapsulation of variables and functions into a single entity.

- Classes are essentially a template to create your objects.

- Objects get their variables and functions from classes.

- Example Class
  - > class MyClass: variable = “blah”

def function(self): print(“This is a message inside the class.”)

- Notes:

  - self in Python is equivalent to this in JavaScript
  - class in Python is equivalent to the Constructor(blueprint) in JavaScript
  - variable in Python is equivalent to the property in JavaScript (accessed through dot)
  - function in Python is equivalent to the method in JavaScript (accessed through dot)

# Thinking Recursively in Python

- In order to solve any probelm, the problem should be broken down into smaller elements.
- Iterative Algorithm built on an explicit loop construction

  - Example:

    - houses = [“Eric’s house”, “Kenny’s house”, “Kyle’s house”, “Stan’s house”]

    def deliver_presents_iteratively(): for house in houses: print(“Delivering presents to”, house)

  - Anything that can be defined in terms of smaller entities is recursive

# recursive functions

- Definition:

  - > A recursive function is a function defined in terms of itself via self-referential expressions.

- Structure:
  - base case
  - recursive case

# Maintaining State

- Thread the state through each recursive call so that the current state is part of the current call’s execution context

- Keep the state in global scope

# recursive data structures

- A data structure is recursive if it can be deﬁned in terms of a smaller version of itself.

- list, set, tree, dictionary, e are recursive data structures

# Python Testing | pytest

- pytest : a library for testing Python code

## Fixtures

- In pytest, you define fixtures using a combination of the pytest.fixture decorator, along with a function definition

## Coverage

- Now, 100% code coverage doesn’t mean that your code is perfect or that it lacks bugs. But it does give you a greater degree of confidence in the code and the fact that it has been run at least once.
