# JupyterLab

***JupyterLab :*** is a next-generation web-based user interface for Project Jupyter.


**JupyterLab enables you**
1. to work with documents and activities 
2. such as Jupyter notebooks, text editors, terminals
3. and custom components in a flexible, integrated
4. and extensible manner.
5. For a demonstration of JupyterLab and its features



**Code Consoles**
 provide transient scratchpads for running code interactively, with full support for rich output. A code console can be linked to a notebook kernel as a computation log from the notebook, for example.

**Kernel-backed**
 documents enable code in any text file (Markdown, Python, R, LaTeX, etc.) to be run interactively in any Jupyter kernel.

* Notebook cell outputs can be mirrored into their own tab, side by side with the notebook, enabling simple dashboards with interactive controls backed by a kernel.

* Multiple views of documents with different editors or viewers enable live editing of documents reflected in other viewers. For example, it is easy to have live preview of Markdown, Delimiter-separated Values, or Vega/Vega-Lite documents.

* JupyterLab also offers a unified model for viewing and handling data formats. JupyterLab understands many file formats (images, CSV, JSON, Markdown, PDF, Vega, Vega-Lite, etc.) and can also display rich kernel output in these formats. See File and Output Formats for more information.

* To navigate the user interface, JupyterLab offers customizable keyboard shortcuts and the ability to use key maps from vim, emacs, and Sublime Text in the text editor.

* JupyterLab extensions can customize or enhance any part of JupyterLab, including new themes, file editors, and custom components.

* JupyterLab is served from the same server and uses the same notebook document format as the classic Jupyter Notebook.


****************

## NumPy Tutorial: Data Analysis with Python


**NumPy is**
 a commonly used Python data analysis package. By using NumPy, you can speed up your workflow, and interface with other packages in the Python ecosystem, like scikit-learn, that use NumPy under the hood. NumPy was originally developed in the mid 2000s, and arose from an even older package called Numeric. This longevity means that almost every data analysis or machine learning package for Python leverages NumPy in some way.

```
 import csv
with open('winequality-red.csv', 'r') as f:
    wines = list(csv.reader(f, delimiter=';'))
```

***Numpy 2-Dimensional Arrays***

* With NumPy, we work with multidimensional arrays. We’ll dive into all of the possible types of multidimensional arrays later on, but for now, we’ll focus on 2-dimensional arrays. A 2-dimensional array is also known as a matrix, and is something you should be familiar with. In fact, it’s just a different way of thinking about a list of lists. A matrix has rows and columns. By specifying a row number and a column number, we’re able to extract an element from a matrix.



***Creating A NumPy Array***
We can create a NumPy array using the numpy.array function. If we pass in a list of lists, it will automatically create a NumPy array with the same number of rows and columns. Because we want all of the elements in the array to be float elements for easy computation, we’ll leave off the header row, which contains strings. One of the limitations of NumPy is that all the elements in an array have to be of the same type, so if we include the header row, all the elements in the array will be read in as strings. Because we want to be able to do computations like find the average quality of the wines, we need the elements to all be floats.


```
import csv
with open("winequality-red.csv", 'r') as f:
    wines = list(csv.reader(f, delimiter=";"))
import numpy as np
wines = np.array(wines[1:], dtype=np.float)
```


***Alternative NumPy Array Creation Methods***

There are a variety of methods that you can use to create NumPy arrays. To start with, you can create an array where every element is zero


***Using NumPy To Read In Files***
It’s possible to use NumPy to directly read csv or other files into arrays. We can do this using the numpy.genfromtxt function. We can use it to read in our initial data on red wines.

* In the below code, we:

- Use the genfromtxt function to read in the winequality-red.csv file.
- Specify the keyword argument delimiter=";" so that the fields are parsed properly.
- Specify the keyword argument skip_header=1 so that the header row is skipped.


***Indexing NumPy Arrays***
We now know how to create arrays, but unless we can retrieve results from them, there isn’t a lot we can do with NumPy. We can use array indexing to select individual elements, groups of elements, or entire rows and columns. 




***mensional NumPy Arrays***

 * So far, we’ve worked with 2-dimensional arrays, such as wines. However, NumPy is a package for working with multidimensional arrays. One of the most common types of multidimensional arrays is the 1-dimensional array, or vector.


***NumPy Data Types***

As we mentioned earlier, each NumPy array can store elements of a single data type. For example, wines contains only float values. NumPy stores values using its own data types, which are distinct from Python types like float and str. This is because the core of NumPy is written in a programming language called C, which stores data differently than the Python data types. NumPy data types map between Python and C, allowing us to use NumPy arrays without any conversion hitches.


***NumPy Array Operations***

NumPy makes it simple to perform mathematical operations on arrays. This is one of the primary advantages of NumPy, and makes it quite easy to do computations.

**Single Array Math**

If you do any of the basic mathematical operations (/, *, -, +, ^) with an array and a value, it will apply the operation to each of the elements in the array.

**roadcasting**
Unless the arrays that you’re operating on are the exact same size, it’s not possible to do elementwise operations. In cases like this, NumPy performs broadcasting to try to match up elements. Essentially, broadcasting involves a few steps:

The last dimension of each array is compared.
If the dimension lengths are equal, or one of the dimensions is of length 1, then we keep going.
If the dimension lengths aren’t equal, and none of the dimensions have length 1, then there’s an error.
Continue checking dimensions until the shortest array is out of dimensions.



**NumPy Array Comparisons**
NumPy makes it possible to test to see if rows match certain values using mathematical comparison operations like `<, >, >=, <=, and ==`. 


**Subsetting**

One of the powerful things we can do with a Boolean array and a NumPy array is select only certain rows or columns in the NumPy array
