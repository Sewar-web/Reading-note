# Pythonisms

**What Are Dunder Methods?**
In Python, special methods are a set of predefined methods you can use to enrich your classes. They are easy to recognize because they start and end with double underscores, for example __init__ or __str__.

As it quickly became tiresome to say under-under-method-under-under Pythonistas adopted the term “dunder methods”, a short form of “double under.”



**Special Methods and the Python Data Model**
This elegant design is known as the Python data model and lets developers tap into rich language features like sequences, iteration, operator overloading, attribute access, etc.

You can see Python’s data model as a powerful API you can interface with by implementing one or more dunder methods. If you want to write more Pythonic code, knowing how and when to use dunder methods is an important step.

For a beginner this might be slightly overwhelming at first though. No worries, in this article I will guide you through the use of dunder methods using a simple Account class as an example.



**Enriching a Simple Account Class**
Throughout this article I will enrich a simple Python class with various dunder methods to unlock the following language features:

1. Initialization of new objects
2. Object representation
3. Enable iteration
4. Operator overloading (comparison)
5. Operator overloading (addition)
6. Method invocation
7. Context manager support (with statement)



**Object Initialization: `__init__`**
Right upon starting my class I already need a special method. To construct account objects from the Account class I need a constructor which in Python is the `__init__` dunder:

```
class Account:
    """A simple account class"""

    def __init__(self, owner, amount=0):
        """
        This is the constructor that lets us create
        objects from this class
        """
        self.owner = owner
        self.amount = amount
        self._transactions = []

```


**Object Representation: `__str__`, `__repr__`**

* It’s common practice in Python to provide a string representation of your object for the consumer of your class (a bit like API documentation.) There are two ways to do this using dunder methods:

1. `__repr__`: The “official” string representation of an object. This is how you would make an object of the class. The goal of `__repr__` is to be unambiguous.

2. `__str__`: The “informal” or nicely printable string representation of an


**Iteration: `__len__, __getitem__, __reversed__`**
In order to iterate over our account object I need to add some transactions. So first, I’ll define a simple method to add transactions. I’ll keep it simple because this is just setup code to explain dunder methods, and not a production-ready accounting system




***********

# Iterators


**Python Iterators That Iterate Forever**

* We’ll begin by writing a class that demonstrates the bare-bones iterator protocol in Python. The example I’m using here might look different from the examples you’ve seen in other iterator tutorials, but bear with me. I think doing it this way gives you a more applicable understanding of how iterators work in Python.


```
    def __init__(self, value):
        self.value = value

    def __iter__(self):
        return RepeaterIterator(self)
```



***RepeaterIterator looks like a straightforward Python class,*** but you might want to take note of the following two things:

In the __init__ method we link each RepeaterIterator instance to the Repeater object that created it. That way we can hold on to the “source” object that’s being iterated over.

In RepeaterIterator.__next__, we reach back into the “source” Repeater instance and return the value associated with it.

In this code example, Repeater and RepeaterIterator are working together to support Python’s iterator protocol. The two dunder methods we defined, __iter__ and __next__, are the key to making a Python object iterable.

We’ll take a closer look at these two methods and how they work together after some hands-on experimentation with the code we’ve got so far.

Let’s confirm that this two-class setup really made Repeater objects compatible with for-in loop iteration. To do that we’ll first create an instance of Repeater that would return the string 'Hello' indefinitely:



**A Simpler Iterator Class**

* Up until now our iterator example consisted of two separate classes, Repeater and RepeaterIterator. They corresponded directly to the two phases used by Python’s iterator protocol:

* First setting up and retrieving the iterator object with an iter() call, and then repeatedly fetching values from it via next().

* Many times both of these responsibilities can be shouldered by a single class. Doing this allows you to reduce the amount of code necessary to write a class-based iterator.

* I chose not to do this with the first example in this tutorial, because it mixes up the cleanliness of the mental model behind the iterator protocol. But now that you’ve seen how to write a class-based iterator the longer and more complicated way, let’s take a minute to simplify what we’ve got so far.

* Remember why we needed the RepeaterIterator class again? We needed it to host the __next__ method for fetching new values from the iterator. But it doesn’t really matter where __next__ is defined. In the iterator protocol, all that matters is that __iter__ returns any object with a __next__ method on it.

* So here’s an idea: RepeaterIterator returns the same value over and over, and it doesn’t have to keep track of any internal state. What if we added the __next__ method directly to the Repeater class instead?

* That way we could get rid of RepeaterIterator altogether and implement an iterable object with a single Python class. Let’s try it out! Our new and simplified iterator example looks as follows:

```
class Repeater:
    def __init__(self, value):
        self.value = value

    def __iter__(self):
        return self

    def __next__(self):
        return self.value
        
```


# Generators

**What Are Python Generators?**

*Python Generators 101 – The Basics*

* Let’s start by looking again at the Repeater example that I previously used to introduce the idea of iterators. It implemented a class-based iterator cycling through an infinite sequence of values.

* This is what the class looked like in its second (simplified) version:

```
class Repeater:
    def __init__(self, value):
        self.value = value

    def __iter__(self):
        return self

    def __next__(self):
        return self.value
```

* If you’re thinking, “that’s quite a lot of code for such a simple iterator,” you’re absolutely right. Parts of this class seem rather formulaic, as if they would be written in exactly the same way from one class-based iterator to the next.

