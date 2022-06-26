# JupyterLab

## JupyterLab 

JupyterLab is a next-generation web-based user interface for Project Jupyter.

JupyterLab enables you to work with documents and activities such as Jupyter notebooks, text editors, terminals, and custom components in a flexible, integrated, and extensible manner. For a demonstration of JupyterLab and its features, you can view [this video](https://www.youtube.com/watch?v=A5YyoCKxEOU&t=43s) [1]

JupyterLab also offers a unified model for viewing and handling data formats. JupyterLab understands many file formats (images, CSV, JSON, Markdown, PDF, Vega, Vega-Lite, etc.) and can also display rich kernel output in these formats. See File and Output Formats for more information. [1]

# **NumPy**: Data Analysis with Python

**NumPy** is a commonly used _Python data analysis package_. By using **NumPy**, you can _speed up_ your workflow, and _interface_ with other packages in the Python ecosystem, like **scikit-learn**, that use **NumPy** under the hood. **NumPy** was originally developed in the mid 2000s, and arose from an even older package called **Numeric**. This longevity means that almost every _data analysis_ or _machine learning_ package for Python leverages **NumPy** in some way. 

- Note the **ssv** _(semicolon separated values)_ format, where each record is separated by a semicolon `(;)`, and rows are separated by a new line.

## Numpy 2-Dimensional Arrays

With NumPy, we work with multidimensional arrays. A _2-dimensional_ array is also known as a _matrix_. In fact, it’s just a different way of thinking about a _list of lists_. A _matrix_ has `rows` and `columns`. By specifying a row number and a column number, we’re able to extract an `element` from a _matrix_.

> In a NumPy array, the number of dimensions is called the rank, and each dimension is called an axis. So the rows are the first axis, and the columns are the second axis.  <sup>[2]</sup>

## Creating A NumPy Array
We can create a NumPy array using the [numpy.array](https://docs.scipy.org/doc/numpy/reference/generated/numpy.array.html) function. If we pass in a list of lists, it will automatically create a NumPy array with the same number of rows and columns. Because we want all of the elements in the array to be _**float** elements for easy computation_, we’ll leave off the header row, which contains strings. **One of the limitations of NumPy is that all the elements in an array have to be of the same type**, so if we include the header row, all the elements in the array will be read in as strings. Because we want to be able to do computations like find the average quality of the data, we need the elements to all be floats.

We can check the number of rows and columns in our data using the [.shape](https://docs.scipy.org/doc/numpy/reference/generated/numpy.ndarray.shape.html) property of NumPy arrays.

## NumPy Data Types

Each NumPy array can store elements of a single data type.
NumPy stores values using its own data types, which are distinct from Python types like float and str. This is because the core of NumPy is written in a programming language called C, which stores data differently than the Python data types. NumPy data types map between Python and C, allowing us to use NumPy arrays without any conversion hitches.

You can find the data type of a NumPy array by accessing the [.dtype](https://docs.scipy.org/doc/numpy/reference/arrays.dtypes.html) property. [2]

NumPy has several different data types, which mostly map to Python data types, like float, and str. You can find a full listing of NumPy data types here, but here are a few important ones:

- float — numeric floating point data.
- int — integer data.
- string — character data.
- object — Python objects.
Data types additionally end with a suffix that indicates how many bits of memory they take up. So int32 is a 32 bit integer data type, and float64 is a 64 bit float data type.






## **Pseudocodes**

### Here is the pseudocode for the `enqueue` method:


### Here is the pseudocode for the `dequeue` method:






<!-- _For more on the subject of **-----**, check this [**GREAT** Article](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/stacks_and_queues.html)  on codefellows_ -->


## Things I want to know more about:
1. NumPy different data types.
2. Python's Data Model.
3. NumPy different data types.
4. Multidimentional Arrays.



[1]: https://jupyterlab.readthedocs.io/en/stable/getting_started/overview.html
[2]: https://www.dataquest.io/blog/numpy-tutorial-python/