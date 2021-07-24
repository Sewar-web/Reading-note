# A Beginner's Guide to Docker

* This is a beginner’s guide to Docker which is a way to isolate and run entire applications. With Docker it doesn’t matter if you are using a Mac, Windows, or Linux computer anymore. The entire development environment is isolated: programming language, software packages, databases, and more.


* With Docker we now longer have to mess around with virtual environments. We can faithfully reproduce a production environment locally. And Docker can be shared among team members so everyone is working on the same setup. Wins all around.


**Linux Containers**

* Virtualization has its roots at the beginning of computer science when large, expensive mainframe computers were the norm. How could multiple programmers use the same single machine? The answer was virtualization and specifically virtual machines which are complete copies of a computer system from the operating system on up.

If you rent space on a cloud provider like AWS they are typically not providing you with a dedicated piece of hardware. Instead you are probably sharing a physical server with hundreds or even thousands of other clients.

What’s the downside to a virtual machine? Size and speed. A typical guest operating system can easily take up 700MB of size. So if one physical server supports three virtual machines, that’s at least 2.1GB of disk space taken up along with separate needs for CPU and memory resources.



**Containers vs Virtual Environments**

If you are a Python programmer (like me) a common question at this point is, what about virtual environments? How do they differ from containers?

Virtual environments are used to isolate Python software packages locally. We can create an isolated box for individual projects so one can use Python 2.7 and Django 1.5 while another can use Python 3.5 and Django 2.1 on the same computer. Virtual environments are great.

But…virtual environments can only isolate Python packages. They still rely on a global, system-level installation of Python albeit they can refer to the proper version. So when we use Python 2.7 in a project, we’re pointing to an installation of Python 2.7 on the computer itself, not actually within the virtual environment.

Also we can’t run a production database or other services within virtual environments so compared to Docker containers they are far more limited.


## Django for APIs

* Django REST Framework works alongside the Django web framework to create web APIs. We cannot build a web API with only Django Rest Framework; it always must be added to a project after Django itself has been installed and configured.

* In this chapter we will review the similarities and differences between traditional Django and Django REST Framework. The most important takeaway is that Django creates websites containing webpages, while Django REST Framework creates web APIs which are a collection of URL endpoints containing available HTTP verbs that return JSON.

* To illustrate these concepts, we will build out a basic Library website with traditional Django and then extend it into a web API with Django REST Framework.



**Traditional Django**


* First we need a dedicated directory on our computer to store the code. This can live anywhere but for convenience, if you are on a Mac, we can place it in the Desktop folder. The location really does not matter; it just needs to be easily accessible.



*The files have the following roles:*

* `__init__.py` is a Python way to treat a directory as a package; it is empty
* asgi.py stands for Asynchronous Server Gateway Interface and is a new option in Django 3.0+
* settings.py contains all the configuration for our project
* urls.py controls the top-level URL routes
* wsgi.py stands for Web Server Gateway Interface and helps Django serve the eventual web pages
* manage.py executes various Django commands such as running the local web server or creating a new app.


**Browsable API**
* With the local server still running in the first command line console, navigate to our API endpoint in the web browser at `http://127.0.0.1:8000/api/.`


