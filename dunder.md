# Dunder Methods

* What Are Dunder Methods?
 - In Python, special methods are a set of predefined methods you can use to enrich your classes. They are easy to recognize because they start and end with double underscores, for example `__init__ or __str__.`

* As it quickly became tiresome to say under-under-method-under-under Pythonistas adopted the term “dunder methods”, a short form of “double under.”

* These “dunders” or “special methods” in Python are also sometimes called “magic methods.” But using this terminology can make them seem more complicated than they really are—at the end of the day there’s nothing “magical” about them. You should treat these methods like a normal language feature.

```
class NoLenSupport:
    pass

>>> obj = NoLenSupport()
>>> len(obj)
TypeError: "object of type 'NoLenSupport' has no len()"
```


**Special Methods and the Python Data Model**

* This elegant design is known as the Python data model and lets developers tap into rich language features like sequences, iteration, operator overloading, attribute access, etc.

* You can see Python’s data model as a powerful API you can interface with by implementing one or more dunder methods. If you want to write more Pythonic code, knowing how and when to use dunder methods is an important step.


**Enriching a Simple Account Class**
- Throughout this article I will enrich a simple Python class with various dunder methods to unlock the following language features:

1. Initialization of new objects
2. Object representation
3. Enable iteration
4. Operator overloading (comparison)
5. Operator overloading (addition)
6. Method invocation
7. Context manager support (with statement)


**Object Initialization: __init__**
Right upon starting my class I already need a special method. To construct account objects from the Account class I need a constructor which in Python is the __init__ dunder:
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


**Object Representation: __str__, __repr__**
It’s common practice in Python to provide a string representation of your object for the consumer of your class (a bit like API documentation.) There are two ways to do this using dunder methods:

1. `__repr__`: The “official” string representation of an object. This is how you would make an object of the class. The goal of __repr__ is to be unambiguous.

2. `__str__`: The “informal” or nicely printable string representation of an object. This is for the enduser.


**Operator Overloading for Merging Accounts: __add__**
* In Python, everything is an object. We are completely fine adding two integers or two strings with the + (plus) operator, it behaves in expected ways:
```
>>> 1 + 2
3

>>> 'hello' + ' world'
'hello world'
```

**Callable Python Objects: __call__**
* You can make an object callable like a regular function by adding the __call__ dunder method. For our account class we could print a nice report of all the transactions that make up its balance:


**Context Manager Support and the With Statement: __enter__, __exit__**
My final example in this tutorial is about a slightly more advanced concept in Python: Context managers and adding support for the with statement.

Now, what is a “context manager” in Python? Here’s a quick overview:

```
class Account:
    # ... (see above)

    def __enter__(self):
        print('ENTER WITH: Making backup of transactions for rollback')
        self._copy_transactions = list(self._transactions)
        return self

    def __exit__(self, exc_type, exc_val, exc_tb):
        print('EXIT WITH:', end=' ')
        if exc_type:
            self._transactions = self._copy_transactions
            print('Rolling back to previous transactions')
            print('Transaction resulted in {} ({})'.format(
                exc_type.__name__, exc_val))
        else:
            print('Transaction OK')
```


***Conclusion***
* I hope you feel a little less afraid of dunder methods after reading this article. A strategic use of them makes your classes more Pythonic, because they emulate builtin types with Python-like behaviors.

* As with any feature, please don’t overuse it. Operator overloading, for example, can get pretty obscure. Adding “karma” to a person object with +bob or tim << 3 is definitely possible using dunders—but might not be the most obvious or appropriate way to use these special methods. However, for common operations like comparison and additions they can be an elegant approach.






****************


## Statistics - Probability

**What is probability?**
* At the most basic level, probability seeks to answer the question, “What is the chance of an event happening?” An event is some outcome of interest. To calculate the chance of an event happening, we also need to consider all the other events that can occur. The quintessential representation of probability is the humble coin toss. In a coin toss the only events that can happen are:

1. Flipping a heads
2. Flipping a tails


**From statistics to probability**
Our data will be generated by flipping a coin 10 times and counting how many times we get heads. We will call a set of 10 coin tosses a trial. Our data point will be the number of heads we observe. We may not get the “ideal” 5 heads, but we won’t worry too much since one trial is only one data point. If we perform many, many trials, we expect the average number of heads over all of our trials to approach the 50%. The code below simulates 10, 100, 1000, and 1000000 trials, and then calculates the average proportion of heads observed. Our process is summarized in the image below as well.


**The data and the distribution**
* Before we can tackle the question of “which wine is better than average,” we have to mind the nature of our data. Intuitively, we’d like to use the scores of the wines to compare groups, but there comes a problem: the scores usually fall in a range. How do we compare groups of scores between types of wines and know with some degree of certainty that one is better than the other? Enter the normal distribution. The normal distribution refers to a particularly important phenomenon in the realm of probability and statistics. The normal distribution looks like this:


```
non_tokaji = []
for wine in wines:
    if points != '':
        points = wine[4]
    if wine[9] == "Tokaji":
    tokaji.append(float(points))
    else:
        non_tokaji.append(points)
# Extract the Lambrusco scores
lambrusco = []
non_lambrusco = []
for wine in wines:
    if points != '':
        points = wine[4]
    if wine[9] == "Lambrusco":
        lambrusco.append(float(points))
    else:
        non_lambrusco.append(float(points))
```


**Revisiting the normal**
* The normal distribution is significant to probability and statistics thanks to two factors: the Central Limit Theorem and the Three Sigma Rule.

 - **Central Limit Theorem**
In the previous section, we demonstrated that if we repeated our 10-toss trials many, many times, the average heads-count of all of these trials will approach the 50% we expect from an ideal coin. With more trials, the closer the average of these trials approach the true probability, even if the individual trials themselves are imperfect. This idea is a key tenet of the Central Limit Theorem. In our coin-tossing example, a single trial of 10 throws produces a single estimate of what probability suggests should happen (5 heads). We call it an estimate because we know that it won’t be perfect (i.e. we won’t get 5 heads every time).