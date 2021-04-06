# Concepts of Functional Programming in Javascript
**What is functional programming?**
Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data 


* The first fundamental concept we learn when we want to understand functional programming is pure functions. But what does that really mean? What makes a function pure?
So how do we know if a function is pure or not? Here is a very strict definition of purity:
   - It returns the same result if given the same arguments (it is also referred as deterministic)
   - It does not cause any observable side effects
   - It returns the same result if given the same arguments
* Imagine we want to implement a function that calculates the area of a circle. An impure function would receive radius as the parameter, and then calculate radius * radius * PI:


**Random number generation**
- Any function that relies on a random number generator cannot be pure.


**Observation: mutability is discouraged in functional programming.**
We are modifying the global object. But how would we make it pure? Just return the value increased by 1. Simple as that.


**Pure functions benefits**
1. The code’s definitely easier to test. We don’t need to mock anything. So we can unit test pure functions with different contexts:
 - 1. Given a parameter A → expect the function to return value B
 - 2. Given a parameter C → expect the function to return value D




* So here we have the sum function that receives a vector of numerical values. The function calls itself until we get the list empty (our recursion base case). For each "iteration" we will add the value to the total accumulator.


* With recursion, we keep our variables immutable. The list and the accumulator variables are not changed. It keeps the same value.
Observation: Yes! We can use reduce to implement this function. We will cover this in the Higher Order Functions topic.
  
  
* It is also very common to build up the final state of an object. Imagine we have a string, and we want to transform this string into a url slug.
In OOP in Ruby, we would create a class, let’s say, UrlSlugify. And this class will have a slugify! method to transform the string input into a url slug.



*Here we have:*
1. toLowerCase: converts the string to all lower case
2. trim: removes whitespace from both ends of a string
3. split and join: replaces all instances of match with replacement in a given string


**Higher-order functions**
When we talk about higher-order functions, we mean a function that either:
takes one or more functions as arguments, or
returns a function as its result
The doubleOperator function we implemented above is a higher-order function because it takes an operator function as an argument and uses it.
You’ve probably already heard about filter, map, and reduce. Let's take a look at these


**Filter**
Given a collection, we want to filter by an attribute. The filter function expects a true or false value to determine if the element should or should not be included in the result collection. Basically, if the callback expression is true, the filter function will include the element in the result collection. Otherwise, it will not.
A simple example is when we have a collection of integers and we want only the even numbers.
Imperative approach
An imperative way to do it with Javascript is to:
create an empty array evenNumbers
iterate over the numbers array
push the even numbers to the evenNumbers array




**Map**
The idea of map is to transform a collection.
The map method transforms a collection by applying a function to all of its elements and building a new collection from the returned values.
Let’s get the same people collection above. We don't want to filter by “over age” now. We just want a list of strings, something like TK is 26 years old. So the final string might be :name is :age years old where :name and :age are attributes from each element in the people collection.
In a imperative Javascript way, it would be:



In a declarative Javascript way, it would be:

The whole idea is to transform a given array into a new array.
Another interesting Hacker Rank problem was the update list problem. We just want to update the values of a given array with their absolute values.
For example, the input [1, 2, 3, -4, 5]needs the output to be [1, 2, 3, 4, 5]. The absolute value of -4 is 4.
A simple solution would be an in-place update for each collection value.

We use the Math.abs function to transform the value into its absolute value, and do the in-place update.
This is not a functional way to implement this solution.
First, we learned about immutability. We know how immutability is important to make our functions more consistent and predictable. The idea is to build a new collection with all absolute values.



***********
**Reduce**
* The idea of reduce is to receive a function and a collection, and return a value created by combining the items.


* A common example people talk about is to get the total amount of an order. Imagine you were at a shopping website. You’ve added Product 1, Product 2, Product 3, and Product 4 to your shopping cart (order). Now we want to calculate the total amount of the shopping cart.


* In imperative way, we would iterate the order list and sum each product amount to the total amount.








