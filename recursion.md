# In Tests We Trust - TDD with Python

**Unit tests and TDD?**

* Probably there are million of blog posts about this subject. But let’s talk just a bit about it on my point of view! 😅
Unit tests are some pieces of code to exercise the input, the output and the behaviour of your code. You can write them anytime you want.
But Test-Driven Development is a strategy to think (and write!) tests first.


**The freela**

* Imagine that a client has a website and through it he receives a lot of contacts from potential customers. After a while he realized that it is important for the business to identify the profile of consumer: age, gender, job and so on. But the website just receive the name and the email.

- Important aspects about the unit test


```def test_should_return_female_when_the_name_is_from_female_gender():
    detector = GenderDetector()
    expected_gender = detector.run(‘Ana’)
    assert expected_gender == ‘female’
```

******



# Recursion


***What is Recursion?***

* The process in which a function calls itself directly or indirectly is called recursion and the corresponding function is called as recursive function. Using recursive algorithm, certain problems can be solved quite easily. Examples of such problems are Towers of Hanoi (TOH), Inorder/Preorder/Postorder Tree Traversals, DFS of Graph, etc.

***A Mathematical Interpretation***

Let us consider a problem that a programmer have to determine the sum of first n natural numbers, there are several ways of doing that but the simplest approach is simply add the numbers starting from 1 to n. So the function simply looks like,

 - approach(1) – Simply adding one by one

```f(n) = 1 + 2 + 3 +……..+ ns```